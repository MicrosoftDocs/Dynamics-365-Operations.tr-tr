---
title: "Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme"
description: "Bu konu, satış siparişi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="16d1b-103">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="16d1b-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="16d1b-104">Bu konu, satış siparişi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="16d1b-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="16d1b-105">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="16d1b-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="16d1b-106">Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="16d1b-107">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="16d1b-108">Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="16d1b-109">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="16d1b-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="16d1b-110">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="16d1b-110">Templates and tasks</span></span>

<span data-ttu-id="16d1b-111">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="16d1b-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="16d1b-112">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="16d1b-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="16d1b-113">Aşağıdaki şablon ve altta yatan görevler, satış siparişi başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="16d1b-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="16d1b-114">**Veri tümleştirmedeki şablonun adı:** Satış Siparişleri (Fin and Ops'dan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="16d1b-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="16d1b-115">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="16d1b-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="16d1b-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="16d1b-116">OrderHeader</span></span>
    - <span data-ttu-id="16d1b-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="16d1b-117">OrderLine</span></span>

<span data-ttu-id="16d1b-118">Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="16d1b-119">Ürünler (Fin and Ops'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="16d1b-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="16d1b-120">Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="16d1b-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="16d1b-121">İlgili kişilerden Müşterilere (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="16d1b-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="16d1b-122">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="16d1b-122">Entity set</span></span>

| <span data-ttu-id="16d1b-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="16d1b-123">Finance and Operations</span></span>  | <span data-ttu-id="16d1b-124">Satış</span><span class="sxs-lookup"><span data-stu-id="16d1b-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="16d1b-125">CDS satışları sipariş başlıkları</span><span class="sxs-lookup"><span data-stu-id="16d1b-125">CDS sales order headers</span></span> | <span data-ttu-id="16d1b-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="16d1b-126">SalesOrders</span></span>       |
| <span data-ttu-id="16d1b-127">CDS satış siparişi satırları</span><span class="sxs-lookup"><span data-stu-id="16d1b-127">CDS sales order lines</span></span>   | <span data-ttu-id="16d1b-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="16d1b-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="16d1b-129">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="16d1b-129">Entity flow</span></span>

<span data-ttu-id="16d1b-130">Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış siparişleri.</span><span class="sxs-lookup"><span data-stu-id="16d1b-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="16d1b-131">Şablondaki filtreler yalnızca ilgili satış siparişlerinin eşitlemeye dahil edilmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="16d1b-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="16d1b-132">Satış siparişinde, siparişi veren müşteri ile faturalanan müşteri Sales'tan geliyorsa, eşitlemeye dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="16d1b-133">Finance and Operations'da **OrderingCustomerIsExternallyMaintained** ve **InvoiceCustomerIsExternallyMaintained** alanları, veri varlıkları içindeki eşitlemeyi izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="16d1b-134">Finance and Operations içindeki satış siparişinin onaylanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="16d1b-135">Yalnızca onaylanmış satış siparişleri veya daha yüksek işleme durumuna sahip satış siparişler (örneğin **Sevk edildi** veya **Faturalandı** durumları) Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="16d1b-136">Bir satış siparişi oluşturulduktan veya değiştirildikten sonra, Finance and Operations'da **Satış toplamlarını hesapla** toplu işinin çalıştırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="16d1b-137">Yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="16d1b-138">Şu anda, satış faturası siparişi üzerindeki masraflarla ilişkili vergiler, Finance and Operations'tan Sales'a eşitlemeye dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="16d1b-139">Sales vergi bilgisini başlık düzeyinde desteklemez.</span><span class="sxs-lookup"><span data-stu-id="16d1b-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="16d1b-140">Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="16d1b-141">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="16d1b-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="16d1b-142">Yeni alanlar **Sipariş** varlığına eklenir ve sayfada görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="16d1b-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="16d1b-143">**Dışarıda Tutulan** – Sipariş Finance and Operations'tan geliyorsa bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="16d1b-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="16d1b-144">**İşleme durumu** – Bu alan siparişin Finance and Operations'taki işleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="16d1b-145">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="16d1b-145">The following values are available:</span></span>

    - <span data-ttu-id="16d1b-146">Etkin</span><span class="sxs-lookup"><span data-stu-id="16d1b-146">Active</span></span>
    - <span data-ttu-id="16d1b-147">Onaylandı</span><span class="sxs-lookup"><span data-stu-id="16d1b-147">Confirmed</span></span>
    - <span data-ttu-id="16d1b-148">Sevk İrsaliyesi</span><span class="sxs-lookup"><span data-stu-id="16d1b-148">Packing Slip</span></span>
    - <span data-ttu-id="16d1b-149">Faturalanan</span><span class="sxs-lookup"><span data-stu-id="16d1b-149">Invoiced</span></span>
    - <span data-ttu-id="16d1b-150">Malzeme çekildi</span><span class="sxs-lookup"><span data-stu-id="16d1b-150">Picked</span></span>
    - <span data-ttu-id="16d1b-151">Kısmen Çekildi</span><span class="sxs-lookup"><span data-stu-id="16d1b-151">Partially Picked</span></span>
    - <span data-ttu-id="16d1b-152">Kısmen Paketlendi</span><span class="sxs-lookup"><span data-stu-id="16d1b-152">Partially Packed</span></span>
    - <span data-ttu-id="16d1b-153">Sevk Edildi</span><span class="sxs-lookup"><span data-stu-id="16d1b-153">Shipped</span></span>
    - <span data-ttu-id="16d1b-154">Kısmen Sevk Edildi</span><span class="sxs-lookup"><span data-stu-id="16d1b-154">Partially Shipped</span></span>
    - <span data-ttu-id="16d1b-155">Kısmen Faturalandı</span><span class="sxs-lookup"><span data-stu-id="16d1b-155">Partially Invoiced</span></span>
    - <span data-ttu-id="16d1b-156">İptal edildi</span><span class="sxs-lookup"><span data-stu-id="16d1b-156">Cancelled</span></span>

<span data-ttu-id="16d1b-157">Yalnızca **Dışarıda Tutulan Ürünlere Sahip** ayarı, diğer satış siparişi senaryolarında (örneğin Sales'tan Finance and Operations'a eşitleme), satış siparişinin tümüyle dışarıda tutulan ürünlerden mi oluştuğunu izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="16d1b-158">Bir satış siparişi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta korunur.</span><span class="sxs-lookup"><span data-stu-id="16d1b-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="16d1b-159">Bu ayar, Finance and Operations tarafından bilenmeyen ürünlere sahip satış siparişi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="16d1b-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="16d1b-160">Dışarıda tutulan siparişler için **Satış siparişi** sayfasındaki **Fatura Oluştur**, **Siparişi İptal Et**, **Yeniden hesapla**, **Ürünleri Al** ve **Arama Adresi** düğmeleri gizlenmiştir çünkü faturalar Finance and Operations içerisinde oluşturulacak ve Sales'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="16d1b-161">Sipariş sayfası düzenlenemez çünkü satış siparişi bilgisi Finance and Operations'tan eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="16d1b-162">Satış siparişi durumu, Finance and Operations'tan gelen değişikliklerin Sales içerisinde satış siparişi içine aktığından emin olunması için **Etkin** kalacaktır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="16d1b-163">Bu davranışı kontrol etmek için, varsayılan **Statecode\[Durum\]** değerini Veri tümleştirme projesinde **Etkin** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="16d1b-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="16d1b-164">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="16d1b-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="16d1b-165">Satış siparişlerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="16d1b-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="16d1b-166">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="16d1b-166">Setup in Sales</span></span>

- <span data-ttu-id="16d1b-167">Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="16d1b-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="16d1b-168">Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="16d1b-169">Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine de sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="16d1b-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="16d1b-170">**Ayarlar** > **Güvenlik** > **Ekipler**'e gidin, ilgili ekibi seçin, **Rolleri Yönet**'i ve istenilen izinlere sahip bir rolü seçin; örn. **Sistem Yöneticisi**.</span><span class="sxs-lookup"><span data-stu-id="16d1b-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="16d1b-171">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="16d1b-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="16d1b-172">**Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="16d1b-173">**İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="16d1b-174">Finance and Operations'ta kurulum</span><span class="sxs-lookup"><span data-stu-id="16d1b-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="16d1b-175">**Satış ve pazarlama** > **Periyodik görevler** > **Satış toplamlarını hesapla**'ya gidin ve işi bir toplu iş olarak çalışacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="16d1b-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="16d1b-176">**Satış siparişleri için toplamları hesapla** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="16d1b-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="16d1b-177">Bu adım önemlidir çünkü yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="16d1b-178">Toplu işin sıklığı, satış siparişi eşitlemesinin sıklığı ile uyumlu olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="16d1b-179">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="16d1b-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="16d1b-180">SalesHeader görevi</span><span class="sxs-lookup"><span data-stu-id="16d1b-180">SalesHeader task</span></span>

- <span data-ttu-id="16d1b-181">Gerekli eşleşmenin **InvoiceCountryRegionId** ile **BillingAddress\_Country** arasında ve **DeliveryCountryRegionId** ile **DeliveryAddress\_Country** arasında mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="16d1b-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="16d1b-182">Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="16d1b-183">Sales'ta siparişler oluşturmak için bir fiyat listesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="16d1b-184">**pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin. </span><span class="sxs-lookup"><span data-stu-id="16d1b-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="16d1b-185">Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16d1b-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="16d1b-186">Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16d1b-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="16d1b-187">**pricelevelid.name \[Fiyat listesi adı\]** için varsayılan şablon değeri **CRM Hizmeti ABD (örnek)**'dir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="16d1b-188">SalesLine görevi</span><span class="sxs-lookup"><span data-stu-id="16d1b-188">SalesLine task</span></span>

- <span data-ttu-id="16d1b-189">**DeliveryCountryRegionId** ile **DeliveryAddress\_Country** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="16d1b-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="16d1b-190">Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="16d1b-191">Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="16d1b-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="16d1b-192">Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="16d1b-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="16d1b-193">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="16d1b-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="16d1b-194">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="16d1b-195">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="16d1b-196">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="16d1b-197">Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="16d1b-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="16d1b-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="16d1b-198">OrderHeader</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="16d1b-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="16d1b-200">OrderLine</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="16d1b-202">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="16d1b-202">Related topics</span></span>

[<span data-ttu-id="16d1b-203">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="16d1b-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="16d1b-204">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="16d1b-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="16d1b-205">Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="16d1b-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="16d1b-206">Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="16d1b-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="16d1b-207">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="16d1b-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




