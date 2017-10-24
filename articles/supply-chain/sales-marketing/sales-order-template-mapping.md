---
title: "Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme"
description: "Bu konu, satış siparişi başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 707efc97afc0679ed1fc22539789e98cbabcb581
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="7d2e5-103">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7d2e5-104">Bu konu, satış siparişi başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="7d2e5-105">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="7d2e5-105">Template and tasks</span></span>

<span data-ttu-id="7d2e5-106">Aşağıdaki şablonlar ve altta yatan görevler, satış siparişi başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="7d2e5-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="7d2e5-107">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="7d2e5-108">Satış Siparişleri (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="7d2e5-109">**Veri tümleştirme projesindeki görevlerin adları**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="7d2e5-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="7d2e5-110">OrderHeader</span></span>
    - <span data-ttu-id="7d2e5-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="7d2e5-111">OrderLine</span></span>

<span data-ttu-id="7d2e5-112">Satış faturası başlığı ve satırları eşitlemesinden önce gerekli eşitleme görevleri:</span><span class="sxs-lookup"><span data-stu-id="7d2e5-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="7d2e5-113">Ürünler (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="7d2e5-114">Hesaplar (Sales'tan Fin and Ops'a) (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="7d2e5-115">İlgili kişiden Müşterilere (Sales'tan Fin and Ops'a) (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="7d2e5-116">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-116">Entity set</span></span>

| <span data-ttu-id="7d2e5-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d2e5-117">Finance and Operations</span></span> |    <span data-ttu-id="7d2e5-118">Ortak Veri Servisi (CDS)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="7d2e5-119">Satış</span><span class="sxs-lookup"><span data-stu-id="7d2e5-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="7d2e5-120">CDS satışları sipariş başlıkları</span><span class="sxs-lookup"><span data-stu-id="7d2e5-120">CDS sales order headers</span></span>| <span data-ttu-id="7d2e5-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="7d2e5-121">SalesOrder</span></span>     | <span data-ttu-id="7d2e5-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="7d2e5-122">SalesOrders</span></span> |
| <span data-ttu-id="7d2e5-123">CDS satış siparişi satırları</span><span class="sxs-lookup"><span data-stu-id="7d2e5-123">CDS sales order lines</span></span>  | <span data-ttu-id="7d2e5-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="7d2e5-124">SalesOrderLine</span></span> | <span data-ttu-id="7d2e5-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="7d2e5-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="7d2e5-126">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="7d2e5-126">Entity flow</span></span>

<span data-ttu-id="7d2e5-127">Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış siparişleri.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="7d2e5-128">Şablondaki filtreler yalnızca ilgili satış siparişlerinin eşitlemeye dahil edilmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="7d2e5-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="7d2e5-129">Satış siparişinde, Sales'tan gelen hem sipariş hem de faturalama müşterisi eşitlemeye dahil edilecektir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="7d2e5-130">Finance and Operations içerisinde **OrderingCustomerIsExternallyMaintained** ve **InvoiceCustomerIsExternallyMaintained** alanları veri varlıkları içindeki eşitlemeyi izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="7d2e5-131">Finance and Operations içindeki **Satış siparişi**'nin onaylanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="7d2e5-132">Yalnızca onaylanmış satış siparişleri veya daha yüksek işleme durumuna sahip satış siparişler, örneğin Sevk edilen veya Faturalanan durumlar, Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="7d2e5-133">Bir satış siparişi oluşturduktan veya değiştirdikten sonra, Finance and Operations'daki **Satış toplamlarını hesapla** toplu işinin yürütülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="7d2e5-134">Yalnızca satış toplamları hesaplanmış satış siparişleri CDS ve Sales'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="7d2e5-135">**Satış siparişi başlığı** üzerindeki masraflarla ilişkili vergiler, şu anda Finance and Operations'tan Sales'a eşitlemeye dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="7d2e5-136">Bu, Sales vergi bilgisini başlık düzeyinde desteklemediği içindir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="7d2e5-137">Satır düzeyi giderleri ile ilgili vergiler dahildir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7d2e5-138">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="7d2e5-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="7d2e5-139">Yeni alanlar **Sipariş** varlığına eklenir ve sayfada görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="7d2e5-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="7d2e5-140">**Harici olarak tutuluyor** - Sipariş Finance and Operations'tan geliyorsa **Evet** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="7d2e5-141">**İşleme durumu** - Siparişin Finance and Operations içerisinde işleme durumunu göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="7d2e5-142">Değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7d2e5-142">Values are:</span></span>

    - <span data-ttu-id="7d2e5-143">Etkin</span><span class="sxs-lookup"><span data-stu-id="7d2e5-143">Active</span></span>
    - <span data-ttu-id="7d2e5-144">Onaylandı</span><span class="sxs-lookup"><span data-stu-id="7d2e5-144">Confirmed</span></span>
    - <span data-ttu-id="7d2e5-145">Sevk İrsaliyesi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-145">Packing Slip</span></span>
    - <span data-ttu-id="7d2e5-146">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="7d2e5-146">Invoiced</span></span>
    - <span data-ttu-id="7d2e5-147">Malzeme çekildi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-147">Picked</span></span>
    - <span data-ttu-id="7d2e5-148">Kısmen Çekildi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-148">Partially Picked</span></span>
    - <span data-ttu-id="7d2e5-149">Kısmen Paketlendi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-149">Partially Packed</span></span>
    - <span data-ttu-id="7d2e5-150">Sevk Edildi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-150">Shipped</span></span>
    - <span data-ttu-id="7d2e5-151">Kısmen Sevk Edildi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-151">Partially Shipped</span></span>
    - <span data-ttu-id="7d2e5-152">Kısmen Faturalandı</span><span class="sxs-lookup"><span data-stu-id="7d2e5-152">Partially Invoiced</span></span>
    - <span data-ttu-id="7d2e5-153">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-153">Cancelled</span></span>

<span data-ttu-id="7d2e5-154">**Yalnızca Dışarıda Tutulan Ürünlere Sahip** ayarı, diğer satış siparişi senaryolarında (Sales'tan Finance and Operations'a eşitleme), satış siparişinin tümüyle **Dışarıda Tutulan Ürünler**'den mi oluştuğunu izlemek için kullanılır; bu durumda ürünler Finance and Operations'ta tutulur.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="7d2e5-155">Bu Finance and Operations tarafından bilenmeyen ürünlerin satış siparişi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="7d2e5-156">**Satış siparişi** sayfasındaki **Fatura Oluştur**, **Siparişi İptal Et**, **Yeniden hesapla**, **Ürünleri Al** ve **Arama Adresi** düğmeleri, dışarıda tutulan siparişler için gizlenmiştir çünkü faturalar Finance and Operations içerisinde oluşturulacak ve Sales'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="7d2e5-157">Sipariş sayfası düzenlenemez çünkü satış siparişi bilgisi Finance and Operations'tan eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="7d2e5-158">**Satış siparişi durumu**, Finance and Operations'tan gelen değişikliklerin Sales içerisinde **Satış siparişi** içine aktığından emin olunması için etkin kalacaktır.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="7d2e5-159">Bu, varsayılan **Statecode [Durum]**'u Veri tümleştirme projesinde **Etkin** olarak ayarlayarak denetlenir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7d2e5-160">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="7d2e5-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="7d2e5-161">Satış siparişlerini eşitlemeden önce, sistemleri aşağıdaki ayarla güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="7d2e5-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="7d2e5-162">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="7d2e5-162">Setup in Sales</span></span>

- <span data-ttu-id="7d2e5-163">Kullanıcının atanmış olduğu (Sales **Bağlantı kümesi**'nizden) ekip için izinlerden emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="7d2e5-164">Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım değil.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="7d2e5-165">Bu olmadan, projeyi Veri tümleştiriciden çalıştırırken Asıl ekibin eksik olduğu hatası alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="7d2e5-166">**Ayarlar** > **Güvenlik** > **Ekipler** altında, ilgili ekibi seçin **Rolleri Yönet**'e tıklayın ve istenilen izinlere sahip bir rolü seçin; örn. Sistem Yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="7d2e5-167">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **Sistem fiyatlama hesaplama sistemini kullan**'ın **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="7d2e5-168">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **İndirim hesaplama yöntemi**'nin **Satır maddesi** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="7d2e5-169">Finance and Operations'ta kurulum</span><span class="sxs-lookup"><span data-stu-id="7d2e5-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="7d2e5-170">**Satış ve pazarlama** > **Periyodik görevler** > **Satış toplamlarını hesapla**'yı bir toplu iş olarak çalışmak üzere, **Satış siparişleri için toplamları hesapla**'yı **Evet** olarak ayarlamış şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="7d2e5-171">Bu, yalnızca satış toplamları hesaplanmış satış siparişleri CDS ve Sales'a eşitleneceği için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="7d2e5-172">Toplu işin sıklığı, satış siparişi eşitlemesinin sıklığı ile hizalanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-172">The frequence of the batch job should be alligned with the frequence of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="7d2e5-173">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="7d2e5-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="7d2e5-174">SalesHeader görevi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-174">SalesHeader task</span></span>

- <span data-ttu-id="7d2e5-175">**Kaynakta CDS Kuruluş Kodu** > **CDS** için eşleşmeyi güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="7d2e5-176">**Account_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="7d2e5-177">**InvoiceAccount_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="7d2e5-178">**Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="7d2e5-179">İhtiyaç duyulan eşleşmenin **Kaynak** > **InvoiceCountryRegionId üzerinden BillingAddress_Country üzerine için CDS** ve **DeliveryCountryRegionId üzerinden DeliveryAddress_Country üzerine** için mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="7d2e5-180">Şablon değeri, eşlenmiş ülkelerin sayısı ile **ValueMap**'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="7d2e5-181">**Fiyat listesi** Sales içerisinde siparişleri oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="7d2e5-182">**ValueMap**'i **CDS** > **Hedef**'i **pricelevelid.name [Fiyat Listesi Adı]** için **Fiyat listesi**'ne, Sales'ta para birimi başına kullanılmak üzere güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="7d2e5-183">İster varsayılan **Fiyat listesi**'ni tek bir para birimi için kullanabilir veya birden fazla para biriminde **Fiyat listeleri** mevcutsa **ValueMap** kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="7d2e5-184">**pricelevelid.name [Fiyat Listesi Adı]** için varsayılan şablon CRM Service USA (örnek)'tir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="7d2e5-185">SalesLine görevi</span><span class="sxs-lookup"><span data-stu-id="7d2e5-185">SalesLine task</span></span>

- <span data-ttu-id="7d2e5-186">**Kaynakta CDS Kuruluş Kodu** > **CDS** için eşleşmeyi güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="7d2e5-187">**SalesOrder_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="7d2e5-188">**Product_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="7d2e5-189">Gerekli eşleşmenin **Kaynak** > **CDS** içerisinde, **DeliveryCountryRegionId** üzerinden **DeliveryAddress_Country** üzerine için mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="7d2e5-190">Şablon değeri, eşlenmiş ülkelerin sayısı ile **ValueMap**'dir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="7d2e5-191">Finance and Operations içerisinde **SalesUnitSymbol** için gereken **ValueMap**'in **Kaynak** > **CDS eşleme** içinde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="7d2e5-192">**ValueMap** ile şablon değeri **SalesUnitSymbol to Quantity_UOM** için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="7d2e5-193">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="7d2e5-194">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="7d2e5-195">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="7d2e5-196">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="7d2e5-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="7d2e5-197">OrderHeader</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="7d2e5-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="7d2e5-200">OrderLine</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="7d2e5-203">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="7d2e5-203">Related topics</span></span>

[<span data-ttu-id="7d2e5-204">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="7d2e5-205">Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="7d2e5-206">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="7d2e5-207">Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="7d2e5-208">Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="7d2e5-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


