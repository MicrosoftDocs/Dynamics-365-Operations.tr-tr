---
title: Uzantıları kullanarak vergi tümleştirmesine veri alanları ekleme
description: Bu konu, vergi tümleştirmesinde veri alanları eklemek için X++ uzantılarının nasıl kullanılacağını açıklar.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a3da8e1b8176eb25fe4e0a320aa3e907c06e09c5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021404"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="ec5d6-103">Uzantı kullanarak vergi tümleştirmesine veri alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="ec5d6-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ec5d6-104">Bu konu, vergi tümleştirmesinde veri alanları eklemek için X++ uzantılarının nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="ec5d6-105">Bu alanlar vergi hizmetinin vergi veri modeline genişletilebilir ve vergi kodlarını belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="ec5d6-106">Daha fazla bilgi için, bkz. [Vergi yapılandırmalarında veri alanları ekleme](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="ec5d6-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="ec5d6-107">Veri modeli</span><span class="sxs-lookup"><span data-stu-id="ec5d6-107">Data model</span></span>

<span data-ttu-id="ec5d6-108">Veri modelindeki veriler nesneler tarafından taşınır ve sınıflar tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="ec5d6-109">Önemli nesnelerin listesi aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="ec5d6-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="ec5d6-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="ec5d6-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="ec5d6-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="ec5d6-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="ec5d6-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="ec5d6-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="ec5d6-113">Aşağıdaki resim bu nesnelerin nasıl ilişkili olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="ec5d6-114">[![Veri modeli nesne ilişkisi](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="ec5d6-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="ec5d6-115">Bir **Belge** nesnesi birçok **satır** nesnesi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="ec5d6-116">Her nesne vergi hizmeti için meta verilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="ec5d6-117">`TaxIntegrationDocumentObject`, kaynak adres hakkında bilgiler içeren `originAddress` meta verileri ve satır tutarının satış vergisini içerip içermediğini gösteren `includingTax` meta veriler içerir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="ec5d6-118">`TaxIntegrationLineObject` `itemId`, `quantity` ve `categoryId` meta verilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="ec5d6-119">`TaxIntegrationLineObject` **gider** nesnelerini de uygular.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="ec5d6-120">Tümleştirme akışı</span><span class="sxs-lookup"><span data-stu-id="ec5d6-120">Integration flow</span></span>

<span data-ttu-id="ec5d6-121">Akıştaki veriler etkinlikler tarafından değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="ec5d6-122">Önemli etkinlikler</span><span class="sxs-lookup"><span data-stu-id="ec5d6-122">Key activities</span></span>

* <span data-ttu-id="ec5d6-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ec5d6-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="ec5d6-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ec5d6-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="ec5d6-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ec5d6-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="ec5d6-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ec5d6-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="ec5d6-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ec5d6-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="ec5d6-128">Etkinlikler aşağıdaki sıraya göre çalıştırılır:</span><span class="sxs-lookup"><span data-stu-id="ec5d6-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="ec5d6-129">Alma işlemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="ec5d6-129">Setting Retrieval</span></span>
2. <span data-ttu-id="ec5d6-130">Veri Alma</span><span class="sxs-lookup"><span data-stu-id="ec5d6-130">Data Retrieval</span></span>
3. <span data-ttu-id="ec5d6-131">Hesaplama servisi</span><span class="sxs-lookup"><span data-stu-id="ec5d6-131">Calculation Service</span></span>
4. <span data-ttu-id="ec5d6-132">Döviz kuru</span><span class="sxs-lookup"><span data-stu-id="ec5d6-132">Currency Exchange</span></span>
5. <span data-ttu-id="ec5d6-133">Veri kalıcılığı</span><span class="sxs-lookup"><span data-stu-id="ec5d6-133">Data Persistence</span></span>

<span data-ttu-id="ec5d6-134">Örneğin, **Hesaplama hizmetinden** önce **veri alma**'yı genişletin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="ec5d6-135">Veri alma faaliyetleri</span><span class="sxs-lookup"><span data-stu-id="ec5d6-135">Data Retrieval activities</span></span>

<span data-ttu-id="ec5d6-136">**Veri alma** eylemleri veritabanından veri alır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="ec5d6-137">Farklı işlem tablolarından veri almak için farklı işlemler için bağdaştırıcılar kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="ec5d6-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="ec5d6-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="ec5d6-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="ec5d6-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="ec5d6-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="ec5d6-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="ec5d6-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="ec5d6-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ec5d6-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="ec5d6-145">Bu **veri alma** faaliyetlerinde, veriler veritabanından `TaxIntegrationDocumentObject` ve `TaxIntegrationLineObject`'e kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="ec5d6-146">Tüm bu faaliyetler aynı soyut şablon sınıfını genişlettiğinden, ortak yöntemleri vardır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="ec5d6-147">Hesaplama Hizmeti faaliyetleri</span><span class="sxs-lookup"><span data-stu-id="ec5d6-147">Calculation Service activities</span></span>

<span data-ttu-id="ec5d6-148">**Hesaplama Hizmeti** faaliyeti, Vergi hizmeti ile vergi tümleştirmesi arasındaki bağlantıdır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="ec5d6-149">Bu faaliyet aşağıdaki işlevlerden sorumludur:</span><span class="sxs-lookup"><span data-stu-id="ec5d6-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="ec5d6-150">İsteği oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-150">Construct the request.</span></span>
2. <span data-ttu-id="ec5d6-151">Talebi vergi hizmetine nakledin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="ec5d6-152">Yanıtı vergi hizmetinden alın.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="ec5d6-153">Yanıtı ayrıştırın.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-153">Parse the response.</span></span>

<span data-ttu-id="ec5d6-154">İsteğe eklediğiniz bir veri alanı diğer meta verilerle birlikte deftere nakledilecektir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="ec5d6-155">Uzantıyı uygulama</span><span class="sxs-lookup"><span data-stu-id="ec5d6-155">Extension implementation</span></span>

<span data-ttu-id="ec5d6-156">Bu bölüm, uzantının nasıl uygulanacağını açıklayan ayrıntılı adımlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="ec5d6-157">Bu, **Maliyet merkezini** ve **Proje** Mali boyutlarını örnek olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="ec5d6-158">1. Adım</span><span class="sxs-lookup"><span data-stu-id="ec5d6-158">Step 1.</span></span> <span data-ttu-id="ec5d6-159">Nesne sınıfına veri değişkeni ekleme</span><span class="sxs-lookup"><span data-stu-id="ec5d6-159">Add the data variable in the object class</span></span>

<span data-ttu-id="ec5d6-160">Nesne sınıfı, veriler için veri değişkeni ve alıcı/kurucu yöntemlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="ec5d6-161">Alan düzeyine bağlı olarak veri alanını `TaxIntegrationDocumentObject` ya da `TaxIntegrationLineObject`'e ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="ec5d6-162">Aşağıdaki örnekte satır düzeyi kullanılır ve `TaxIntegrationLineObject_Extension.xpp` dosya adı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="ec5d6-163">Eklediğiniz veri alanı belge düzeyindeyse dosya adını `TaxIntegrationDocumentObject_Extension.xpp` olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

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

<span data-ttu-id="ec5d6-164">**Maliyet merkezi** ve **Proje** özel değişkenler olarak eklendi.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="ec5d6-165">Verileri değiştirmek üzere bu veri alanları için alıcı ve ayarlayıcı yöntemleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="ec5d6-166">2. Adım</span><span class="sxs-lookup"><span data-stu-id="ec5d6-166">Step 2.</span></span> <span data-ttu-id="ec5d6-167">Veritabanından veri alma</span><span class="sxs-lookup"><span data-stu-id="ec5d6-167">Retrieve data from the database</span></span>

<span data-ttu-id="ec5d6-168">İşlemi belirtin ve verileri almak için uygun bağdaştırıcı sınıflarını genişletin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="ec5d6-169">Örneğin, bir **Satın alma siparişi** işlemikullanırsanız, `TaxIntegrationPurchTableDataRetrieval` ve `TaxIntegrationVendInvoiceInfoTableDataRetrieval` öğesini genişletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="ec5d6-170">`TaxIntegrationPurchParmTableDataRetrieval`, `TaxIntegrationPurchTableDataRetrieval`'dan devralınmıştır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="ec5d6-171">`purchTable` ve `purchParmTable` tablolarının mantığı farklı olmadıkça değiştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="ec5d6-172">Veri alanının tüm işlemler için eklenmesi gerekiyorsa tüm `DataRetrieval` sınıflarını genişletin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="ec5d6-173">Tüm **veri alma** etkinlikleri aynı şablon sınıfını genişlettiği için sınıf yapıları, değişkenler ve Yöntemler benzerdir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

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

<span data-ttu-id="ec5d6-174">Aşağıdaki örnek, `PurchTable` tablosu kullanıldığında temel yapıyı gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

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

<span data-ttu-id="ec5d6-175">`CopyToDocument` yöntemi çağrıldığında, `this.purchTable` arabelleği zaten vardır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="ec5d6-176">Bu yöntemin amacı, `DocumentObject` sınıfında oluşturulmuş olan ayarlayıcı yöntemini kullanarak `this.purchTable`'daki gerekli tüm verilerin `document` nesnesine kopyalanmasını sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="ec5d6-177">Benzer şekilde, `this.purchLine` arabelleği `CopyToLine` yönteminde zaten mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="ec5d6-178">Bu yöntemin amacı, `LineObject` sınıfında oluşturulmuş olan ayarlayıcı yöntemini kullanarak `this.purchLine`'daki gerekli tüm verilerin `_line` nesnesine kopyalanmasını sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="ec5d6-179">En doğrudan yaklaşım, `CopyToDocument` ve `CopyToLine` yöntemlerini uzatmaktır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="ec5d6-180">Ancak, önce `copyToDocumentFromHeaderTable` ve `copyToLineFromLineTable` yöntemlerini denemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="ec5d6-181">Bunlar gerektiği gibi çalışmıyorsa, kendi yönteminizi uygulayın ve `CopyToDocument` ve `CopyToLine`'de çağırın.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="ec5d6-182">Bu yaklaşımı kullanabileceğiniz üç yaygın durum vardır:</span><span class="sxs-lookup"><span data-stu-id="ec5d6-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="ec5d6-183">Gerekli alan `PurchTable` veya `PurchLine`'dadır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="ec5d6-184">Bu durumda, `copyToDocumentFromHeaderTable` ve `copyToLineFromLineTable` öğesini genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="ec5d6-185">Örnek kod aşağıdadır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-185">Here is the sample code.</span></span>

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

- <span data-ttu-id="ec5d6-186">Gerekli veriler, işlemin varsayılan tablosunda yoktur.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="ec5d6-187">Ancak, varsayılan tabloyla birlikte bazı birleştirme ilişkileri vardır ve alan çoğu satırda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="ec5d6-188">Bu durumda, tabloyu birleştirme ilişkisiyle sorgulamak için `getDocumentQueryObject` veya `getLineObject`'i değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="ec5d6-189">Aşağıdaki örnekte, **Şimdi teslim et** alanı satır düzeyinde satış siparişiyle tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

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

    <span data-ttu-id="ec5d6-190">Bu örnekte, bir `mcrSalesLineDropShipment` arabelleği bildirilir ve sorgu `getLineQueryObject`'te tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="ec5d6-191">Sorgu `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId` ilişkisini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="ec5d6-192">Bu durumu uzatırken, `getLineQueryObject` nesnesini kendi oluşturduğunuz sorgu nesnenizle değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="ec5d6-193">Ancak, aşağıdaki noktaları unutmayın:</span><span class="sxs-lookup"><span data-stu-id="ec5d6-193">However, note the following points:</span></span>

    * <span data-ttu-id="ec5d6-194">`getLineQueryObject` Yönteminin dönüş değeri `SysDaQueryObject` olduğundan, bu nesneyi SysDa yaklaşımını kullanarak oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="ec5d6-195">Var olan tablo kaldırılamıyor.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-195">Can't remove existed table.</span></span>

- <span data-ttu-id="ec5d6-196">Gerekli veriler, karmaşık birleştirme ilişkisi aracılığıyla işlem tablosuyla ilişkilendirilir veya ilişki bire bire bir (1:1) değildir bire çoktur (1: N).</span><span class="sxs-lookup"><span data-stu-id="ec5d6-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="ec5d6-197">Bu durumda, işler biraz karmaşık olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="ec5d6-198">Bu durum mali boyut örnekleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="ec5d6-199">Bu durumda, verileri almak için kendi yönteminizi uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="ec5d6-200">`TaxIntegrationPurchTableDataRetrieval_Extension.xpp` dosyasındaki örnek kod aşağıdadır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

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

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="ec5d6-201">3. Adım</span><span class="sxs-lookup"><span data-stu-id="ec5d6-201">Step 3.</span></span> <span data-ttu-id="ec5d6-202">İsteğe veri ekleme</span><span class="sxs-lookup"><span data-stu-id="ec5d6-202">Add data to the request</span></span>

<span data-ttu-id="ec5d6-203">İstek için veri eklemek için `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` ya da `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` yöntemini genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="ec5d6-204">`TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` dosyasındaki örnek kod aşağıdadır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

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

<span data-ttu-id="ec5d6-205">Bu kodda, `_destination` gönderi isteğini oluşturmak için kullanılan sarmalayıcı nesnedir ve `_source` `TaxIntegrationLineObject` nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="ec5d6-206">Talep formunda kullanılan anahtarı olduğu `private const str` olarak tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="ec5d6-207">`copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` yönteminde `SetField` yöntemini kullanarak alanı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="ec5d6-208">İkinci parametrenin veri türü `string` olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="ec5d6-209">Veri türü `string` değilse, `string`'e dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="ec5d6-210">Ek</span><span class="sxs-lookup"><span data-stu-id="ec5d6-210">Appendix</span></span>

<span data-ttu-id="ec5d6-211">Bu ekte, satır düzeyinde mali boyutların (**maliyet merkezi** ve **Proje**) tümleştirilmesi için örnek kodun tamamı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="ec5d6-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ec5d6-212">TaxIntegrationLineObject_Extension.xpp</span></span>

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="ec5d6-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ec5d6-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="ec5d6-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ec5d6-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

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
