---
title: "Sales'deki satış teklifi başlıklarını ve satırlarını doğrudan Finance and Operations'la eşitleme"
description: "Bu konu, satış teklif başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3d546dc180ec53ad0fac40fe134ed811af68658f
ms.contentlocale: tr-tr
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="71d8e-103">Sales'deki satış teklifi başlıklarını ve satırlarını doğrudan Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="71d8e-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="71d8e-104">Bu konu, satış teklif başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="71d8e-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="71d8e-105">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="71d8e-106">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="71d8e-106">Template and tasks</span></span>

<span data-ttu-id="71d8e-107">Aşağıdaki şablon ve altta yatan görevler, teklif başlıklarını ve satırlarını doğrudan Sales'tan Finance and Operations'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="71d8e-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="71d8e-108">**Veri tümleştirmedeki şablonun adı:** Satış Teklifleri (Sales'ten Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="71d8e-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="71d8e-109">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="71d8e-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="71d8e-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="71d8e-110">QuoteHeader</span></span>
    - <span data-ttu-id="71d8e-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="71d8e-111">QuoteLine</span></span>

<span data-ttu-id="71d8e-112">Aşağıdaki eşitleme görevleri, satış teklifi başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="71d8e-113">Ürünler (Fin and Ops'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="71d8e-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="71d8e-114">Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="71d8e-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="71d8e-115">İlgili kişilerden Müşterilere (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="71d8e-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="71d8e-116">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="71d8e-116">Entity set</span></span>

| <span data-ttu-id="71d8e-117">Satış</span><span class="sxs-lookup"><span data-stu-id="71d8e-117">Sales</span></span>        | <span data-ttu-id="71d8e-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="71d8e-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="71d8e-119">Alıntılar</span><span class="sxs-lookup"><span data-stu-id="71d8e-119">Quotes</span></span>       | <span data-ttu-id="71d8e-120">CDS satış teklifi başlığı</span><span class="sxs-lookup"><span data-stu-id="71d8e-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="71d8e-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="71d8e-121">QuoteDetails</span></span> | <span data-ttu-id="71d8e-122">CDS satış teklifi satırları</span><span class="sxs-lookup"><span data-stu-id="71d8e-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="71d8e-123">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="71d8e-123">Entity flow</span></span>

<span data-ttu-id="71d8e-124">Sales'ta oluşturulmuş ve Finance and Operations'a eşitlenmiş satış teklifleri.</span><span class="sxs-lookup"><span data-stu-id="71d8e-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="71d8e-125">Sales'taki satış teklifleri, yalnızca aşağıdaki koşullar gerçekleşirse eşitlenir:</span><span class="sxs-lookup"><span data-stu-id="71d8e-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="71d8e-126">Satış teklifindeki tüm teklif ürünleri harici olarak tutuluyor.</span><span class="sxs-lookup"><span data-stu-id="71d8e-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="71d8e-127">**Teklifi etkinleştir**'i tıkladıktan sonra, satış teklifi etkindir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="71d8e-128">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="71d8e-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="71d8e-129">Yalnızca **Dışarıda Tutulan Ürünleri Var** alanı, satış teklifinin tümüyle harici tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için **Teklif** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="71d8e-130">Bir satış teklifi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta tutulur.</span><span class="sxs-lookup"><span data-stu-id="71d8e-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="71d8e-131">Bu davranış, Finance and Operations tarafından bilenmeyen ürünlerin satış teklifi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="71d8e-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="71d8e-132">Satış teklifindeki tüm teklif ürünleri, satış teklifi başlığından **Yalnızca Dışarıda Tutulan Ürünlere Sahip** bilgisi ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="71d8e-133">Bu bilgi, **QuoteDetails** varlığındaki **Teklif Yalnızca Dışarıda Tutulan Ürünlere Sahip** alanında bulunur.</span><span class="sxs-lookup"><span data-stu-id="71d8e-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="71d8e-134">Teklif ürününe bir iskonto eklenebilir ve Finance and Operations'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="71d8e-135">Başlıktaki **İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'taki bir ayar tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="71d8e-136">Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="71d8e-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="71d8e-137">Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları korunur ve Finance and Operations tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="71d8e-138">Sales'ta, çözüm aşağıdaki alanları salt okunur yapar çünkü değerler Finance and Operations'a eşitlenmez:</span><span class="sxs-lookup"><span data-stu-id="71d8e-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="71d8e-139">Satış teklifi başlığındaki salt okunur alanlar: **İskonto %**, **İskonto** ve **Navlun Tutarı**</span><span class="sxs-lookup"><span data-stu-id="71d8e-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="71d8e-140">Teklif ürünlerindeki salt okunur alanlar: **Vergi**</span><span class="sxs-lookup"><span data-stu-id="71d8e-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="71d8e-141">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="71d8e-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="71d8e-142">Satış tekliflerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="71d8e-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="71d8e-143">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="71d8e-143">Setup in Sales</span></span>

- <span data-ttu-id="71d8e-144">Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="71d8e-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="71d8e-145">Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="71d8e-146">Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="71d8e-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="71d8e-147">Ekip için izinleri ayarlamak üzere **Ayarlar** &gt; **Güvenlik** &gt; **Ekipler**'e gidin ve ilgili ekibi seçin.</span><span class="sxs-lookup"><span data-stu-id="71d8e-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="71d8e-148">**Rolleri Yönet**'i seçin ve ardından **Sistem Yöneticisi** gibi istenen izinlere sahip bir rol seçin.</span><span class="sxs-lookup"><span data-stu-id="71d8e-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="71d8e-149">**Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="71d8e-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="71d8e-150">**Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="71d8e-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="71d8e-151">**İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="71d8e-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="71d8e-152">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="71d8e-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="71d8e-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="71d8e-153">QuoteHeader</span></span>

- <span data-ttu-id="71d8e-154">**Shipto\_country** ile **DeliveryAddressCountryRegionISOCode** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="71d8e-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="71d8e-155">Değer eşlemesinde, değer boş bırakılırsa kullanılacak olan bir varsayılan değer tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="71d8e-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="71d8e-156">Sol tarafı boş bırakmanız ve sağ tarafı istenen ülkeye veya bölgeye ayarlamanız yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="71d8e-157">Bu şekilde, ulusal siparişler için ülke veya bölge yazmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="71d8e-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="71d8e-158">Şablon değeri çeşitli ülkelerin veya bölgelerin eşleştirildiği bir değer eşlemesidir ve boş değer **ABD** değerine eşittir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="71d8e-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="71d8e-159">QuoteLine</span></span>

- <span data-ttu-id="71d8e-160">Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="71d8e-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="71d8e-161">Gerekli birimlerin Sales'ta tanımlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="71d8e-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="71d8e-162">Bir değer eşlemesi bulunan şablon değeri **oumid.name** için **SalesUnitSymbol** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="71d8e-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="71d8e-163">İsteğe bağlı: Aşağıdaki eşleşmeleri satış teklifi satırlarının müşteriden veya üründen gelen varsayılan bilgi yoksa Finance and Operations'a aktarılmasını garanti etmeye yardımcı olmak amacıyla ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="71d8e-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="71d8e-164">**SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="71d8e-165">**SiteId** için varsayılan şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="71d8e-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="71d8e-166">**WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="71d8e-167">**WarehouseId** için varsayılan şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="71d8e-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="71d8e-168">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="71d8e-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="71d8e-169">**İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'ta karmaşık bir kurulumda denetlenir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="71d8e-170">Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="71d8e-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="71d8e-171">Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Finance and Operations tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="71d8e-172">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="71d8e-173">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="71d8e-174">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="71d8e-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="71d8e-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="71d8e-175">QuoteHeader</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="71d8e-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="71d8e-177">QuoteLine</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="71d8e-179">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="71d8e-179">Related topics</span></span>

[<span data-ttu-id="71d8e-180">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="71d8e-180">Prospect to cash</span></span>](prospect-to-cash.md)


