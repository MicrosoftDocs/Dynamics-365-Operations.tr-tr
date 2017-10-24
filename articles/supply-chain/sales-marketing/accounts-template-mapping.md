---
title: "Finans işlemlerini ve müşterilere satış hesaplarını eşitle"
description: "Bu konu, hesapları Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="1576b-103">Finans işlemlerini ve müşterilere satış hesaplarını eşitle</span><span class="sxs-lookup"><span data-stu-id="1576b-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1576b-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun.</span><span class="sxs-lookup"><span data-stu-id="1576b-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="1576b-105">Bu konu, hesapları Microsoft Dynamics 365 for Sales'tan (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a (Finance and Operations) eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="1576b-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="1576b-106">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="1576b-106">Template and task</span></span>

<span data-ttu-id="1576b-107">Aşağıdaki şablonlar ve altta yatan görevler, hesapları Sales'tan Finance to Operations'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="1576b-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="1576b-108">**Şablonun adı:** Hesaplar (Sales'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="1576b-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="1576b-109">**Projedeki görevin adı:** Hesaplar - Hesap - Müşteriler</span><span class="sxs-lookup"><span data-stu-id="1576b-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="1576b-110">Hesap / Müşteri eşitlemesinden önce gerekli görevler: Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="1576b-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="1576b-111">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="1576b-111">Entity set</span></span>

| <span data-ttu-id="1576b-112">Satış</span><span class="sxs-lookup"><span data-stu-id="1576b-112">Sales</span></span>    | <span data-ttu-id="1576b-113">CDS</span><span class="sxs-lookup"><span data-stu-id="1576b-113">CDS</span></span>     | <span data-ttu-id="1576b-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1576b-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="1576b-115">Hesaplar</span><span class="sxs-lookup"><span data-stu-id="1576b-115">Accounts</span></span> | <span data-ttu-id="1576b-116">Hesap</span><span class="sxs-lookup"><span data-stu-id="1576b-116">Account</span></span> | <span data-ttu-id="1576b-117">Müşteriler</span><span class="sxs-lookup"><span data-stu-id="1576b-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="1576b-118">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="1576b-118">Entity flow</span></span>

<span data-ttu-id="1576b-119">Hesaplar Sales'ta yönetilir ve Finance and Operations'a Müşteriler olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="1576b-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="1576b-120">Bu Müşterilerdeki **Harici Olarak Tutulur** özelliği Sales'tan gelen Müşterileri izlemek için **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1576b-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="1576b-121">Faturalama sırasında, bu bilgi Sales'a eşitlenen faturaları filtrelemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1576b-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1576b-122">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="1576b-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1576b-123">**Hesap numarası** alanı, **Hesap** sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1576b-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="1576b-124">Tümleştirmeyi desteklemek için doğal ve benzersiz anahtar yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="1576b-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="1576b-125">Müşteri İlişkileri Yönetimi'nin (CRM) doğal anahtar özelliği, halihazırda **Hesap Numarası** alanını kullanan ancak hesap başına benzersiz **Hesap Numarası** kullanmayan müşterileri etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="1576b-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="1576b-126">Şu anda, tümleştirme çözümü bu durumu desteklemez.</span><span class="sxs-lookup"><span data-stu-id="1576b-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="1576b-127">Yeni bir hesap oluşturulduğunda, bir **Hesap Numarası** değeri zaten mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1576b-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="1576b-128">Değer **ACC**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir.</span><span class="sxs-lookup"><span data-stu-id="1576b-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="1576b-129">Aşağıda bir örnek verilmiştir: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="1576b-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="1576b-130">Sales için tümleştirme çözümü uygulandığında, bir güncelleştirme kodu **Hesap Numarası** alanını Sales içindeki mevcut hesaplarda ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1576b-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="1576b-131">**Hesap Numarası** değeri yoksa, daha önce açıklanan numara serisi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1576b-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1576b-132">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="1576b-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="1576b-133">**CustomerGroupId** içinden **CDS &gt; Hedef** eşleşmesi, Finance and Operations içinde geçerli bir değer bulmak için güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1576b-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="1576b-134">Bir varsayılan değer belirtebilir veya değeri, bir değer haritası kullanarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1576b-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="1576b-135">Varsayılan şablon değeri **10**'dur.</span><span class="sxs-lookup"><span data-stu-id="1576b-135">The default template value is **10**.</span></span>
- <span data-ttu-id="1576b-136">**Adres ülke bölge kodu** alanı Finance and Operations'ta gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1576b-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="1576b-137">Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; Hedef** eşlemesinden belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1576b-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="1576b-138">Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1576b-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="1576b-139">**AddressCountryRegionISOCode** için varsayılan şablon değeri **ABD**'dir.</span><span class="sxs-lookup"><span data-stu-id="1576b-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="1576b-140">**DeliveryAddressCountryRegionISOCode** için varsayılan bir şablon değeri **ABD**'dir.</span><span class="sxs-lookup"><span data-stu-id="1576b-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="1576b-141">Aşağıdaki eşleşmeleri **CDS &gt; Hedef**'ten ekleyerek, Finance and Operations'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1576b-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="1576b-142">Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1576b-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="1576b-143">**SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1576b-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="1576b-144">Bir varsayılan site, sipariş başlığında üründen veya müşteriden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="1576b-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="1576b-145">**SiteId** için varsayılan bir şablon değeri **1**'dur.</span><span class="sxs-lookup"><span data-stu-id="1576b-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="1576b-146">**WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1576b-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="1576b-147">Bir varsayılan ambar, Finance and Operations'ta sipariş başlığında üründen veya müşteriden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="1576b-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="1576b-148">**WarehouseId** için varsayılan bir şablon değeri **13**'dur.</span><span class="sxs-lookup"><span data-stu-id="1576b-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="1576b-149">**LanguageId** – Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1576b-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1576b-150">Varsayılan olarak, müşterinin sipariş başlığındaki dil kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1576b-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="1576b-151">**LanguageId** için varsayılan şablon değeri **en-us** olur.</span><span class="sxs-lookup"><span data-stu-id="1576b-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="1576b-152">CDS kuruluş kodunu (**Organization_OrganizationId**) **Kaynak &gt; CDS** eşlemesinde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1576b-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="1576b-153">Varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="1576b-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="1576b-154">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="1576b-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="1576b-155">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="1576b-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="1576b-156">Bu alanları eşleştirmek için bir değer eşleşmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1576b-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="1576b-157">Değer eşlemeleri, varlığın aralarında eşitlendiği kuruluşlardaki veriye özgüdür.</span><span class="sxs-lookup"><span data-stu-id="1576b-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="1576b-158">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="1576b-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/accounts-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki Hesaplar için şablon eşleme](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="1576b-161">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="1576b-161">Related topics</span></span>

[<span data-ttu-id="1576b-162">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="1576b-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="1576b-163">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="1576b-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="1576b-164">Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="1576b-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="1576b-165">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="1576b-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="1576b-166">Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="1576b-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




