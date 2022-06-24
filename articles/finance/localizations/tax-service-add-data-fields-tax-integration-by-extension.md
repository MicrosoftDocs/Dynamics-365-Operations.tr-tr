---
title: Uzantıları kullanarak vergi tümleştirmesine veri alanları ekleme
description: Bu makale, vergi tümleştirmesinde veri alanları eklemek için X++ uzantılarının nasıl kullanılacağını açıklar.
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 184012dcc0b68e017bb28d8d73caa9e8415bdbfa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871063"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Uzantı kullanarak vergi tümleştirmesine veri alanları ekleme

[!include [banner](../includes/banner.md)]


Bu makale, vergi tümleştirmesinde veri alanları eklemek için X++ uzantılarının nasıl kullanılacağını açıklar. Bu alanlar vergi hizmetinin vergi veri modeline genişletilebilir ve vergi kodlarını belirlemek için kullanılabilir. Daha fazla bilgi için, bkz. [Vergi yapılandırmalarında veri alanları ekleme](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Veri modeli

Veri modelindeki veriler nesneler tarafından taşınır ve sınıflar tarafından uygulanır.

Önemli nesnelerin listesi aşağıdadır:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Aşağıdaki resim bu nesnelerin nasıl ilişkili olduğunu gösterir.

[![Veri modeli nesne ilişkisi.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

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
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

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

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

Bu kodda, `_destination` isteğini oluşturmak için kullanılan sarmalayıcı nesnedir ve `_source` `TaxIntegrationLineObject` nesnesidir.

> [!NOTE]
> Talepte kullanılan alan adını **private const str** olarak tanımlayın. Dize tam olarak [Vergi yapılandırmalarına veri alanları ekleme](tax-service-add-data-fields-tax-configurations.md) makalesinde eklenen düğüm adı (etiket değil) ile aynı olmalıdır.
> 
> **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** yönetimdeki alanı **SetField** yöntemi kullanarak ayarlayın. İkinci parametrenin veri türü **string** olmalıdır. Veri türü **string** değilse dizeye dönüştürün.
> Veri türü X++ **sabit liste türünde** ise, sabit liste değerini bir dizeye dönüştürmek için **enum2Symbol** yöntemini kullanmanızı öneririz. Vergi yapılandırmasına eklenen sabit liste değeri tam olarak numaralandırma adı ile aynı olmalıdır. Aşağıda, sabit liste değeri, etiketi ve adı arasındaki farklılıkların bir listesi verilmiştir.
> 
>   - Sabit liste adı kod içindeki bir simgesel addır. **enum2Symbol()** numaralandırma değerini dönüştürmek için kullanılabilir.
>   - Numaralandırma değeri tamsayıdır.
>   - Enum etiketi, tercih edilen diller arasında farklı olabilir. **enum2Strl()** numaralandırma değerini etikete dönüştürmek için kullanılabilir.

## <a name="model-dependency"></a>Model bağımlılığı

Projeyi başarılı bir şekilde oluşturmak için model bağımlılıklarına aşağıdaki referans modellerini ekleyin:

- ApplicationPlatform
- ApplicationSuite
- Vergi Altyapısı
- Boyutlar, mali boyut kullanılıyorsa
- Kodda başvurulan diğer gerekli modeller

## <a name="validation"></a>Doğrulama

Önceki adımları tamamladıktan sonra değişikliklerinizi doğrulayabilirsiniz.

1. Finance'ta **Borç hesapları**'na gidin ve URL'ye **&debug=vs%2CconfirmExit&** ekleyin. Örneğin, `https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&`. Son **&** gereklidir.
2. Satınalma siparişi oluşturmak için **Satınalma siparişi** sayfasını açın ve **Yeni**'yi seçin.
3. Özelleştirilmiş alanın değerini ayarlayın ve **Satış vergisi**'ni seçin. Öneki **TaxServiceTroubleshootingLog** olan bir sorun gidermek dosyası otomatik olarak indirilir. Bu dosya, Vergi Hesaplama Hizmeti'ne gönderilen hareket bilgilerini içerir. 
4. **Vergi hizmeti hesaplaması girişi JSON** bölümünde eklenen özelleştirilmiş alanın bulunduğunu ve değerinin doğru olduğunu kontrol edin. Değer doğru değilse, bu belgedeki adımları tekrar denetleyin.

Dosya örneği:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Ek

Bu ekte, satır düzeyinde mali boyutların (**Maliyet merkezi** ve **Proje**) tümleştirilmesi için örnek kodun tamamı gösterilir.

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
    // Define the field name in the request
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
