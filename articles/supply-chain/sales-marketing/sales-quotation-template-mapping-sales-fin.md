---
title: Satış teklifi başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitleme
description: Bu konu, satış teklifi başlıklarını ve satırlarını Dynamics 365 Sales'ten Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 19c7de1436b2fe4a859ac20d3db1fefa445a115f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991877"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="4c004-103">Satış teklifi başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="4c004-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4c004-104">Bu konu, satış teklifi başlıklarını ve satırlarını Dynamics 365 Sales'ten Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4c004-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="4c004-105">Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4c004-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4c004-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="4c004-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4c004-107">Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4c004-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="4c004-108">Veri Tümleştirme özelliğiyle kullanılabilecek Aday müşteriden nakde şablonları; hesaplar, ilgili kişiler, ürünler, satış teklifleri, satış siparişleri ve satış faturaları için Supply Chain Management ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="4c004-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="4c004-109">Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4c004-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="4c004-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4c004-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="4c004-111">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="4c004-111">Template and tasks</span></span>

<span data-ttu-id="4c004-112">Aşağıdaki şablon ve temel görevler, teklif başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitlemede kullanılır:</span><span class="sxs-lookup"><span data-stu-id="4c004-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="4c004-113">**Veri tümleştirmedeki şablonun adı:** Satış Teklifleri (Sales'ten Supply Chain Management'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="4c004-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="4c004-114">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="4c004-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="4c004-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4c004-115">QuoteHeader</span></span>
    - <span data-ttu-id="4c004-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4c004-116">QuoteLine</span></span>

<span data-ttu-id="4c004-117">Aşağıdaki eşitleme görevleri, satış teklifi başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4c004-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="4c004-118">Ürünler (Supply Chain Management'tan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="4c004-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="4c004-119">Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="4c004-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="4c004-120">İlgili kişilerden Müşterilere (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="4c004-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="4c004-121">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="4c004-121">Entity set</span></span>

| <span data-ttu-id="4c004-122">Satışlar</span><span class="sxs-lookup"><span data-stu-id="4c004-122">Sales</span></span>        | <span data-ttu-id="4c004-123">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4c004-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="4c004-124">Alıntılar</span><span class="sxs-lookup"><span data-stu-id="4c004-124">Quotes</span></span>       | <span data-ttu-id="4c004-125">Dataverse satış teklifi başlığı</span><span class="sxs-lookup"><span data-stu-id="4c004-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="4c004-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="4c004-126">QuoteDetails</span></span> | <span data-ttu-id="4c004-127">Dataverse satış teklifi satırları</span><span class="sxs-lookup"><span data-stu-id="4c004-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="4c004-128">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="4c004-128">Entity flow</span></span>

<span data-ttu-id="4c004-129">Satış teklifleri Sales'te oluşturulur ve Supply Chain Management'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="4c004-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="4c004-130">Sales'taki satış teklifleri, yalnızca aşağıdaki koşullar gerçekleşirse eşitlenir:</span><span class="sxs-lookup"><span data-stu-id="4c004-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="4c004-131">Satış teklifindeki tüm teklif ürünleri harici olarak tutuluyor.</span><span class="sxs-lookup"><span data-stu-id="4c004-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="4c004-132">**Teklifi etkinleştir**'i tıkladıktan sonra, satış teklifi etkindir.</span><span class="sxs-lookup"><span data-stu-id="4c004-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4c004-133">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="4c004-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4c004-134">Yalnızca **Dışarıda Tutulan Ürünleri Var** alanı, satış teklifinin tümüyle harici tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için **Teklif** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4c004-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="4c004-135">Bir satış teklifinde yalnızca harici tutulan ürünler varsa ürünler Supply Chain Management'ta tutulur.</span><span class="sxs-lookup"><span data-stu-id="4c004-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="4c004-136">Bu davranış, Supply Chain Management tarafından bilenmeyen ürünlerin satış teklifi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="4c004-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="4c004-137">Satış teklifindeki tüm teklif ürünleri, satış teklifi başlığından **Yalnızca Dışarıda Tutulan Ürünlere Sahip** bilgisi ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4c004-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="4c004-138">Bu bilgi, **QuoteDetails** varlığındaki **Teklif Yalnızca Dışarıda Tutulan Ürünlere Sahip** alanında bulunur.</span><span class="sxs-lookup"><span data-stu-id="4c004-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="4c004-139">Teklif ürününe bir iskonto eklenebilir ve Supply Chain Management'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="4c004-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="4c004-140">Başlıktaki **İskonto**, **Masraflar** ve **Vergi** alanları Supply Chain Management'taki bir ayar tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="4c004-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="4c004-141">Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="4c004-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="4c004-142">Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları korunur ve Supply Chain Management'ta işlenir.</span><span class="sxs-lookup"><span data-stu-id="4c004-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="4c004-143">Sales'te, çözüm aşağıdaki alanları salt okunur yapar çünkü değerler Supply Chain Management'a eşitlenmez:</span><span class="sxs-lookup"><span data-stu-id="4c004-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="4c004-144">Satış teklifi başlığındaki salt okunur alanlar: **İskonto %**, **İskonto** ve **Navlun Tutarı**</span><span class="sxs-lookup"><span data-stu-id="4c004-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="4c004-145">Teklif ürünlerindeki salt okunur alanlar: **Vergi**</span><span class="sxs-lookup"><span data-stu-id="4c004-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4c004-146">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="4c004-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="4c004-147">Satış tekliflerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="4c004-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="4c004-148">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="4c004-148">Setup in Sales</span></span>

- <span data-ttu-id="4c004-149">Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="4c004-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="4c004-150">Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="4c004-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="4c004-151">Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4c004-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="4c004-152">Ekip için izinleri ayarlamak üzere **Ayarlar** &gt; **Güvenlik** &gt; **Ekipler**'e gidin ve ilgili ekibi seçin.</span><span class="sxs-lookup"><span data-stu-id="4c004-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="4c004-153">**Rolleri Yönet**'i seçin ve ardından **Sistem Yöneticisi** gibi istenen izinlere sahip bir rol seçin.</span><span class="sxs-lookup"><span data-stu-id="4c004-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="4c004-154">**Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="4c004-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="4c004-155">**Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4c004-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="4c004-156">**İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4c004-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="4c004-157">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="4c004-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="4c004-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4c004-158">QuoteHeader</span></span>

- <span data-ttu-id="4c004-159">**Shipto\_country** ile **DeliveryAddressCountryRegionISOCode** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4c004-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="4c004-160">Değer eşlemesinde, değer boş bırakılırsa kullanılacak olan bir varsayılan değer tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c004-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="4c004-161">Sol tarafı boş bırakmanız ve sağ tarafı istenen ülkeye veya bölgeye ayarlamanız yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="4c004-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="4c004-162">Bu şekilde, ulusal siparişler için ülke veya bölge yazmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="4c004-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="4c004-163">Şablon değeri çeşitli ülkelerin veya bölgelerin eşleştirildiği bir değer eşlemesidir ve boş değer **ABD** değerine eşittir.</span><span class="sxs-lookup"><span data-stu-id="4c004-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="4c004-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4c004-164">QuoteLine</span></span>

- <span data-ttu-id="4c004-165">Supply Chain Management'ta **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4c004-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="4c004-166">Gerekli birimlerin Sales'ta tanımlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="4c004-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="4c004-167">Bir değer eşlemesi bulunan şablon değeri **oumid.name** için **SalesUnitSymbol** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="4c004-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="4c004-168">İsteğe bağlı: Aşağıdaki eşleşmeleri satış teklifi satırlarının müşteriden veya üründen gelen varsayılan bilgi yoksa Supply Chain Management'a aktarılmasını garanti etmeye yardımcı olmak amacıyla ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4c004-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="4c004-169">**SiteId** - Supply Chain Management'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4c004-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="4c004-170">**SiteId** için varsayılan şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="4c004-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="4c004-171">**WarehouseId** - Supply Chain Management'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4c004-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="4c004-172">**WarehouseId** için varsayılan şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="4c004-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="4c004-173">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="4c004-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="4c004-174">**İskonto**, **Masraflar** ve **Vergi** alanları Supply Chain Management'taki karmaşık bir ayar tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="4c004-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="4c004-175">Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="4c004-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="4c004-176">Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Supply Chain Management tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="4c004-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="4c004-177">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="4c004-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="4c004-178">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4c004-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="4c004-179">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c004-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="4c004-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4c004-180">QuoteHeader</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="4c004-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4c004-182">QuoteLine</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="4c004-184">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="4c004-184">Related topics</span></span>

[<span data-ttu-id="4c004-185">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="4c004-185">Prospect to cash</span></span>](prospect-to-cash.md)

