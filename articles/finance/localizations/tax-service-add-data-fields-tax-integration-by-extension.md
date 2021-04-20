---
title: Uzantıları kullanarak vergi tümleştirmesine veri alanları ekleme
description: Bu konu, vergi tümleştirmesinde veri alanları eklemek için X++ uzantılarının nasıl kullanılacağını açıklar.
author: qire
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830352"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Uzantı kullanarak vergi tümleştirmesine veri alanları ekleme

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, vergi tümleştirmesinde veri alanları eklemek için X++ uzantılarının nasıl kullanılacağını açıklar. Bu alanlar vergi hizmetinin vergi veri modeline genişletilebilir ve vergi kodlarını belirlemek için kullanılabilir. Daha fazla bilgi için, bkz. [Vergi yapılandırmalarında veri alanları ekleme](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Veri modeli

Veri modelindeki veriler nesneler tarafından taşınır ve sınıflar tarafından uygulanır.

Önemli nesnelerin listesi aşağıdadır:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Aşağıdaki resim bu nesnelerin nasıl ilişkili olduğunu gösterir.

[![Veri modeli nesne ilişkisi](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Bir **Belge** nesnesi birçok **satır** nesnesi içerebilir. Her nesne vergi hizmeti için meta verilerini içerir.

- `TaxIntegrationDocumentObject`, kaynak adres hakkında bilgiler içeren `originAddress` meta verileri ve satır tutarının satış vergisini içerip içermediğini gösteren `includingTax` meta veriler içerir.
- `TaxIntegrationLineObject` `itemId`, `quantity` ve `categoryId` meta verilerini içerir.

> [!NOTE]
> `TaxIntegrationLineObject` **gider** nesnelerini de uygular.

## <a name="integration-flow"></a>Tümleştirme akışı

Akıştaki veriler etkinlikler tarafından değiştirilir.

### <a name="key-activities"></a>Önemli etkinlikler

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Etkinlikler aşağıdaki sıraya göre çalıştırılır:

1. Alma işlemini ayarlama
2. Veri Alma
3. Hesaplama servisi
4. Döviz kuru
5. Veri kalıcılığı

Örneğin, **Hesaplama hizmetinden** önce **veri alma**'yı genişletin.

#### <a name="data-retrieval-activities"></a>Veri alma faaliyetleri

**Veri alma** eylemleri veritabanından veri alır. Farklı işlem tablolarından veri almak için farklı işlemler için bağdaştırıcılar kullanılabilir:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

Bu **veri alma** faaliyetlerinde, veriler veritabanından `TaxIntegrationDocumentObject` ve `TaxIntegrationLineObject`'e kopyalanır. Tüm bu faaliyetler aynı soyut şablon sınıfını genişlettiğinden, ortak yöntemleri vardır.

#### <a name="calculation-service-activities"></a>Hesaplama Hizmeti faaliyetleri

**Hesaplama Hizmeti** faaliyeti, Vergi hizmeti ile vergi tümleştirmesi arasındaki bağlantıdır. Bu faaliyet aşağıdaki işlevlerden sorumludur:

1. İsteği oluşturun.
2. Talebi vergi hizmetine nakledin.
3. Yanıtı vergi hizmetinden alın.
4. Yanıtı ayrıştırın.

İsteğe eklediğiniz bir veri alanı diğer meta verilerle birlikte deftere nakledilecektir. 

## <a name="extension-implementation"></a>Uzantıyı uygulama

Bu bölüm, uzantının nasıl uygulanacağını açıklayan ayrıntılı adımlar sağlar. Bu, **Maliyet merkezini** ve **Proje** Mali boyutlarını örnek olarak kullanır.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>1. Adım Nesne sınıfına veri değişkeni ekleme

Nesne sınıfı, veriler için veri değişkeni ve alıcı/kurucu yöntemlerini içerir. Alan düzeyine bağlı olarak veri alanını `TaxIntegrationDocumentObject` ya da `TaxIntegrationLineObject`'e ekleyin. Aşağıdaki örnekte satır düzeyi kullanılır ve `TaxIntegrationLineObject_Extension.xpp` dosya adı kullanılır.

> [!NOTE]
> Eklediğiniz veri alanı belge düzeyindeyse dosya adını `TaxIntegrationDocumentObject_Extension.xpp` olarak değiştirin.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Maliyet merkezi** ve **Proje** özel değişkenler olarak eklendi. Verileri değiştirmek üzere bu veri alanları için alıcı ve ayarlayıcı yöntemleri oluşturun.

### <a name="step-2-retrieve-data-from-the-database"></a>2. Adım Veritabanından veri alma

İşlemi belirtin ve verileri almak için uygun bağdaştırıcı sınıflarını genişletin. Örneğin, bir **Satın alma siparişi** işlemikullanırsanız, `TaxIntegrationPurchTableDataRetrieval` ve `TaxIntegrationVendInvoiceInfoTableDataRetrieval` öğesini genişletmeniz gerekir. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval`, `TaxIntegrationPurchTableDataRetrieval`'dan devralınmıştır. `purchTable` ve `purchParmTable` tablolarının mantığı farklı olmadıkça değiştirilmemelidir.

Veri alanının tüm işlemler için eklenmesi gerekiyorsa tüm `DataRetrieval` sınıflarını genişletin.

Tüm **veri alma** etkinlikleri aynı şablon sınıfını genişlettiği için sınıf yapıları, değişkenler ve Yöntemler benzerdir.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

Aşağıdaki örnek, `PurchTable` tablosu kullanıldığında temel yapıyı gösterir.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

`CopyToDocument` yöntemi çağrıldığında, `this.purchTable` arabelleği zaten vardır. Bu yöntemin amacı, `DocumentObject` sınıfında oluşturulmuş olan ayarlayıcı yöntemini kullanarak `this.purchTable`'daki gerekli tüm verilerin `document` nesnesine kopyalanmasını sağlamaktır.

Benzer şekilde, `this.purchLine` arabelleği `CopyToLine` yönteminde zaten mevcuttur. Bu yöntemin amacı, `LineObject` sınıfında oluşturulmuş olan ayarlayıcı yöntemini kullanarak `this.purchLine`'daki gerekli tüm verilerin `_line` nesnesine kopyalanmasını sağlamaktır.

En doğrudan yaklaşım, `CopyToDocument` ve `CopyToLine` yöntemlerini uzatmaktır. Ancak, önce `copyToDocumentFromHeaderTable` ve `copyToLineFromLineTable` yöntemlerini denemenizi öneririz. Bunlar gerektiği gibi çalışmıyorsa, kendi yönteminizi uygulayın ve `CopyToDocument` ve `CopyToLine`'de çağırın. Bu yaklaşımı kullanabileceğiniz üç yaygın durum vardır:

- Gerekli alan `PurchTable` veya `PurchLine`'dadır. Bu durumda, `copyToDocumentFromHeaderTable` ve `copyToLineFromLineTable` öğesini genişletebilirsiniz. Örnek kod aşağıdadır.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- Gerekli veriler, işlemin varsayılan tablosunda yoktur. Ancak, varsayılan tabloyla birlikte bazı birleştirme ilişkileri vardır ve alan çoğu satırda gereklidir. Bu durumda, tabloyu birleştirme ilişkisiyle sorgulamak için `getDocumentQueryObject` veya `getLineObject`'i değiştirin. Aşağıdaki örnekte, **Şimdi teslim et** alanı satır düzeyinde satış siparişiyle tümleşiktir.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    Bu örnekte, bir `mcrSalesLineDropShipment` arabelleği bildirilir ve sorgu `getLineQueryObject`'te tanımlanmıştır. Sorgu `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId` ilişkisini kullanır. Bu durumu uzatırken, `getLineQueryObject` nesnesini kendi oluşturduğunuz sorgu nesnenizle değiştirebilirsiniz. Ancak, aşağıdaki noktaları unutmayın:

    * `getLineQueryObject` Yönteminin dönüş değeri `SysDaQueryObject` olduğundan, bu nesneyi SysDa yaklaşımını kullanarak oluşturmalısınız.
    * Var olan tablo kaldırılamıyor.

- Gerekli veriler, karmaşık birleştirme ilişkisi aracılığıyla işlem tablosuyla ilişkilendirilir veya ilişki bire bire bir (1:1) değildir bire çoktur (1: N). Bu durumda, işler biraz karmaşık olacaktır. Bu durum mali boyut örnekleri için geçerlidir. 

    Bu durumda, verileri almak için kendi yönteminizi uygulayabilirsiniz. `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` dosyasındaki örnek kod aşağıdadır.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>3. Adım İsteğe veri ekleme

İstek için veri eklemek için `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` ya da `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` yöntemini genişletebilirsiniz. `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` dosyasındaki örnek kod aşağıdadır.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

Bu kodda, `_destination` gönderi isteğini oluşturmak için kullanılan sarmalayıcı nesnedir ve `_source` `TaxIntegrationLineObject` nesnesidir. 

> [!NOTE]
> * Talep formunda kullanılan anahtarı olduğu `private const str` olarak tanımlayın.
> * `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` yönteminde `SetField` yöntemini kullanarak alanı ayarlayın. İkinci parametrenin veri türü `string` olmalıdır. Veri türü `string` değilse, `string`'e dönüştürün.

## <a name="appendix"></a>Ek

Bu ekte, satır düzeyinde mali boyutların (**maliyet merkezi** ve **Proje**) tümleştirilmesi için örnek kodun tamamı gösterilir.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
