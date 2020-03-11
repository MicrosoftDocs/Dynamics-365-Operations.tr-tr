---
title: Esnek ambar düzeyi boyut rezervasyon ilkesi
description: Bu konu, toplu işle izlenen ürünler satan ve lojistiklerini WMS-etkin operasyonlar olarak çalıştıran işletmelerin, ürünlerle ilişkili rezervasyon hiyerarşisi belirli toplu işlerin rezervasyonuna izin vermese bile, belirli toplu işleri rezerve etmelerine izin veren stok rezervasyon ilkesini açıklar.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cd6ec1013de757214db99ada02170bb6e2af96c0
ms.sourcegitcommit: f52ddcad105aac4ad2caef709751ff80caf363c0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036941"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="c7217-103">Esnek ambar düzeyi boyut rezervasyon ilkesi</span><span class="sxs-lookup"><span data-stu-id="c7217-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7217-104">"Toplu iş-\[yerleşim\] altı" türünde stok rezervasyon hiyerarşisi ürünlerle ilişkiliyse, toplu işle izlenen ürünler satan ve lojistiklerini Microsoft Dynamics 365 Warehouse Management System (WMS) için etkinleştirilmiş operasyonlar olarak yürüten işletmeler, müşteri satış siparişleri için bu ürünlerin belirli toplu işlerini rezerve edemez.</span><span class="sxs-lookup"><span data-stu-id="c7217-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="c7217-105">Bu konu, ürünler bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkili olsa bile, bu işletmelerin belirli toplu işleri rezerve etmelerine izin veren stok rezervasyon ilkesini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7217-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="c7217-106">Stok rezervasyonu hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="c7217-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="c7217-107">Bu bölüm, varolan stok rezervasyon hiyerarşisini özetlemektedir.</span><span class="sxs-lookup"><span data-stu-id="c7217-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="c7217-108">Toplu işle izlenen ve seri izlenen kalemlerin işlenme şekline odaklanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="c7217-109">Ambar mantığı, istenen miktarlara yerleşim atamaktan ve yerleşimi rezerve etmekten sorumluyken, stok rezervasyon hiyerarşisi, depolama boyutlarıyla ilgili olarak, talep emrinin tesis, ambar ve stok durumu zorunlu boyutlarını taşımasını zorunlu kılar.</span><span class="sxs-lookup"><span data-stu-id="c7217-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="c7217-110">Başka bir deyişle, talep emri ve ambar operasyonları arasındaki etkileşimlerde, talep emrinde siparişin sevk çıkışının yapılacağı yerin (yani tesis ve ambar) belirtilmesi beklenir.</span><span class="sxs-lookup"><span data-stu-id="c7217-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="c7217-111">Ambar, bunun üzerine, ambar tesislerindeki gerekli miktarı bulmak için kendi mantığını temel alır.</span><span class="sxs-lookup"><span data-stu-id="c7217-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="c7217-112">Bununla birlikte, işletmenin operasyon modelini yansıtmak için, izleme boyutları (toplu iş ve seri numaraları) daha fazla esneklik gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c7217-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="c7217-113">Bir stok rezervasyonu hiyerarşisi aşağıdaki koşulların geçerli olduğu senaryolar barındırabilir:</span><span class="sxs-lookup"><span data-stu-id="c7217-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="c7217-114">İşletme, ambar depolama alanında miktarlar bulunduktan sonra, toplu iş veya seri numaraları olan miktarların çekilmesini yönetmek için kendi ambar operasyonlarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="c7217-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="c7217-115">Bu modele genellikle *Toplu iş-\[yerleşim\] altı* adı verilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="c7217-116">Genellikle, satıcı şirketle talebi oluşturan müşteriler için bir ürünün toplu iş veya seri numarası tanımlaması önemli olmadığı zaman kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="c7217-117">Toplu iş veya seri numaraları bir müşterinin sipariş belirtiminin parçasıysa ve bunlar talep emrinde kaydedilirse, ambardaki miktarları bulan ambar operasyonları istenen belirli sayılarla sınırlandırılır ve bunları değiştirmelerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="c7217-118">Bu modele *Toplu iş-\[yerleşim\] üstü* adı verilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="c7217-119">Bu senaryolarda sorun, serbest bırakılan her ürüne yalnızca bir stok rezervasyonu hiyerarşisinin atanabilmesidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="c7217-120">Bu nedenle, WMS'nin izlenen kalemleri işlemesi için, hiyerarşi ataması toplu iş veya seri numarasının ne zaman rezerve edilmesi gerektiğini (talep emri alındığı zaman veya ambar çekme işi sırasında) belirledikten sonra bu zamanlama geçici olarak değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="c7217-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="c7217-121">Toplu işle izlenen kalemler için esnek rezervasyon</span><span class="sxs-lookup"><span data-stu-id="c7217-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="c7217-122">İş senaryosu</span><span class="sxs-lookup"><span data-stu-id="c7217-122">Business scenario</span></span>

<span data-ttu-id="c7217-123">Bu senaryoda, bir şirket, mamul malların toplu iş numaralarına göre izlendiği bir stok stratejisi kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="c7217-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="c7217-124">Bu şirket aynı zamanda WMS iş yükünü de kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="c7217-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="c7217-125">Bu iş yükünün toplu iş etkin kalemler için ambar çekme ve sevkiyat operasyonları planlamak ve çalıştırmak için iyi donatılmış bir mantığı olduğundan, mamul kalemlerin çoğu bir "Toplu iş\[yerleşim\] altı" stok rezervasyon hiyerarşisiyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="c7217-126">Bu tür operasyon kurulumunun avantajı, hangi toplu işlerin çekileceği ve bu maddelerin ambarda nereye koyulacağı ile ilgili kararların (yürürlükteki rezervasyon kararları), ambar çekme operasyonları başlayana kadar ertelenmesidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="c7217-127">Bunlar müşterinin siparişi verilirken yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="c7217-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="c7217-128">"Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi şirketin işletme hedeflerine uygun olmakla birlikte, şirketin mevcut müşterilerinin birçoğu, ürünleri yeniden sipariş ettikleri zaman, daha önce satın aldıkları aynı toplu işi istemektedir.</span><span class="sxs-lookup"><span data-stu-id="c7217-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="c7217-129">Bu nedenle, şirket, müşterinin aynı kalem için talebine bağlı olarak toplu iş rezervasyonu kurallarının işleniş biçiminde esneklik istiyor ve böylece aşağıdaki davranışlar ortaya çıkıyor:</span><span class="sxs-lookup"><span data-stu-id="c7217-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="c7217-130">Bir toplu iş numarası, satış işlemcisi tarafından sipariş alınırken kaydedilip rezerve edilebilir ve ambar operasyonları sırasında değiştirilemez ve/veya başka taleplerle alınamaz.</span><span class="sxs-lookup"><span data-stu-id="c7217-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="c7217-131">Bu davranış, sipariş edilen toplu iş numarasının müşteriye sevk edilmesini garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c7217-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="c7217-132">Toplu iş numarası müşteri için önemli değilse, ambar operasyonları, satış siparişi kaydı ve rezervasyon yapıldıktan sonra malzeme çekme işi sırasında bir toplu iş numarası belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="c7217-133">Satış siparişinde belirli bir toplu işin rezervasyonuna izin verme</span><span class="sxs-lookup"><span data-stu-id="c7217-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="c7217-134">Bir "Toplu iş-\[yerleşim\] altı" stok rezervasyon hiyerarşisi ile ilişkilendirilmiş kalemler için toplu iş rezervasyon davranışında istenen esnekliği sağlamak için, stok yöneticilerinin, **Stok rezervasyonu hiyerarşileri** sayfasındaki **Toplu iş numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu işaretlemeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7217-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Stok rezervasyonu hiyerarşisini esnek hale getirme](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="c7217-136">Hiyerarşide **Toplu iş numarası** düzeyi seçildiği zaman, o düzeyin üzerindeki ve **Yerleşim** düzeyine kadar olan tüm boyutlar otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="c7217-137">(Varsayılan olarak **Yerleşim** düzeyinin üzerindeki tüm boyutlar önceden seçilmiştir.) Bu davranış, siz sipariş satırında belirli bir toplu iş numarasını rezerve ettikten sonra, toplu iş numarası ve yerleşim arasındaki aralıkta yer alan tüm boyutların da otomatik olarak rezerve edildiği mantığı yansıtır.</span><span class="sxs-lookup"><span data-stu-id="c7217-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="c7217-138">**Talep emrinde rezervasyona izin ver** onay kutusu yalnızca ambar yerleşim boyutunun altındaki rezervasyon hiyerarşisi düzeylerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="c7217-139">**Toplu iş numarası**, hiyerarşide esnek rezervasyon ilkesi için açık olan tek düzeydir.</span><span class="sxs-lookup"><span data-stu-id="c7217-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="c7217-140">Başka bir deyişle, **Yerleşim**, **Plaka** veya **Seri numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7217-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="c7217-141">Rezervasyon hiyerarşiniz her zaman **Toplu iş numarası** düzeyinin altında olması gereken seri numarası boyutunu içeriyorsa ve toplu iş numarası için toplu işe özel rezervasyonu etkinleştirdiyseniz, "Seri-\[yerleşim\] altı" rezervasyon ilkesi için geçerli olan kurallara dayalı olarak, sistem seri numarası rezervasyonu ve malzeme çekme operasyonlarını işlemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="c7217-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="c7217-142">Herhangi bir noktada, dağıtımınızda varolan bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi için toplu işe özel rezervasyona izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7217-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="c7217-143">Bu değişiklik, değişiklik yapılmadan önce oluşturulan rezervasyonları ve açık ambar işini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="c7217-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="c7217-144">Ancak, bu rezervasyon hiyerarşisiyle ilişkili bir veya daha fazla kalem için **Siparişli rezerve miktar**, **Fiziksel rezerve miktar** veya **Sipariş edilen** çıkış türünde stok hareketleri mevcutsa **Talep emrinde rezervasyona izin ver** onay kutusunun işareti kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="c7217-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="c7217-145">Bir kalemin varolan rezervasyon hiyerarşisi siparişte toplu iş belirtimine izin vermiyorsa, hiyerarşi düzeyi yapısının her iki hiyerarşide de aynı olması koşuluyla, o kalemi toplu iş belirtimine izin veren bir rezervasyon hiyerarşisine yeniden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7217-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="c7217-146">Yeniden atamak için **Maddeler için rezervasyon hiyerarşisini değiştir** işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7217-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="c7217-147">Bu değişiklik, esnek toplu iş rezervasyonunu toplu iş izlemeli kalemlerin bir alt kümesi için önlemek ama ürün portföyünün geri kalanı için izin vermek istediğinizde uygun olabilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="c7217-148">**Talep emrinde rezervasyona izin ver** onay kutusunu seçip seçmemenizden bağımsız olarak, bir sipariş satırındaki kalem için belirli bir toplu iş numarasını rezerve etmek istemiyorsanız, "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi için geçerli olan varsayılan ambar operasyonları mantığı uygulanmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="c7217-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="c7217-149">Müşteri siparişi için belirli bir toplu iş numarasını rezerve etme</span><span class="sxs-lookup"><span data-stu-id="c7217-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="c7217-150">Toplu iş izlemeli bir maddenin "Toplu iş-\[yerleşim\] altı" stok rezervasyonu hiyerarşisi satış siparişlerinde belirli toplu iş numaralarının rezervasyonuna izin verecek şekilde ayarlandıktan sonra, satış siparişi işlemcileri, müşterinin talebine bağlı olarak, aynı kalem için müşteri siparişlerini aşağıdaki yollardan biriyle alabilir:</span><span class="sxs-lookup"><span data-stu-id="c7217-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="c7217-151">**Sipariş ayrıntılarını bir toplu iş numarası belirtmeden girmek** – Ürünün toplu iş belirtimi müşteri için önemli değilse bu yaklaşım kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7217-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="c7217-152">Sistemde bu tür bir siparişin işlenmesiyle ilişkili tüm varolan işlemler değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="c7217-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="c7217-153">Kullanıcılar tarafında ek bir değerlendirme gerekmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="c7217-154">**Sipariş ayrıntılarını girmek ve belirli bir toplu iş numarasını rezerve etmek** – Müşteri belirli bir toplu işi istediğinde bu yaklaşım kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7217-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="c7217-155">Genellikle, müşteriler daha önce satın aldıkları bir ürünü yeniden sipariş ederken belirli bir toplu işi isteyecektir.</span><span class="sxs-lookup"><span data-stu-id="c7217-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="c7217-156">Bu tür toplu iş rezervasyonuna *sipariş taahhütlü rezervasyon* adı verilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="c7217-157">Miktarlar işlendiği ve belirli bir sipariş için bir toplu iş numarası taahhüt edildiği zaman aşağıdaki kural kümesi geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="c7217-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="c7217-158">"Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altındaki bir kalem için belirli bir toplu iş numarasının rezervasyonuna izin vermek amacıyla, sistem yerleşim ve üzerindeki tüm boyutları rezerve etmelidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="c7217-159">Bu aralık genellikle plaka boyutunu içerir.</span><span class="sxs-lookup"><span data-stu-id="c7217-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="c7217-160">Sipariş taahhütlü toplu iş rezervasyonu kullanan bir satış satırı için malzeme çekme işi oluşturulduğunda yerleşim yönergeleri kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="c7217-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="c7217-161">Sipariş taahhütlü toplu işler için işin ambara işlenmesi sırasında, kullanıcının ve sistemin toplu iş numarasını değiştirmesine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="c7217-162">(Bu işlem özel durum işlemeyi kapsar.)</span><span class="sxs-lookup"><span data-stu-id="c7217-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="c7217-163">Aşağıdaki örnekte uçtan uca akış gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c7217-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c7217-164">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="c7217-164">Example scenario</span></span>

<span data-ttu-id="c7217-165">Bu örnek için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7217-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="c7217-166">Toplu işe özel rezervasyona izin vermek için bir stok rezervasyonu hiyerarşisi ayarlama</span><span class="sxs-lookup"><span data-stu-id="c7217-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="c7217-167">**Ambar yönetimi** \> **Kurulum** \> **Stok \> Rezervasyon hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c7217-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="c7217-168">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-168">Select **New**.</span></span>
3. <span data-ttu-id="c7217-169">**Ad** alanına bir ad girin (örneğin **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="c7217-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="c7217-170">**Açıklama** alanına bir açıklama girin (örneğin **Toplu iş alt esnek**).</span><span class="sxs-lookup"><span data-stu-id="c7217-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="c7217-171">**Seçili** alanda, **Seri numarası** ve **Sahip**'i seçin ve ardından sol ok düğmesini seçerek bunları **Kullanılabilir** alanına taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c7217-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="c7217-172">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-172">Select **OK**.</span></span>
7. <span data-ttu-id="c7217-173">**Toplu iş numarası** boyut düzeyinin satırında, **Talep emrinde rezervasyona izin ver** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="c7217-174">**Plaka** ve **Yerleşim** düzeyleri otomatik olarak seçilir ve bunların onay kutularını temizleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7217-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="c7217-175">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="c7217-176">Yeni bir serbest bırakılan ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7217-176">Create a new released product</span></span>

1. <span data-ttu-id="c7217-177">Bu değerleri kullanarak ürünün üç ana veri parametresini ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c7217-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="c7217-178">**Depolama boyutu grubu** alanında **Ambar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="c7217-179">**İzleme boyutu grubu** alanında **Batch-Phy**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="c7217-180">**Rezervasyon hiyerarşisi** alanında **BatchFlex**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="c7217-181">**B11** ve **B22** gibi iki toplu iş numarası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c7217-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="c7217-182">Aşağıdaki değerleri kullanarak eldeki stoka kalem miktarları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c7217-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="c7217-183">Ambar</span><span class="sxs-lookup"><span data-stu-id="c7217-183">Warehouse</span></span> | <span data-ttu-id="c7217-184">Parti numarası</span><span class="sxs-lookup"><span data-stu-id="c7217-184">Batch number</span></span> | <span data-ttu-id="c7217-185">Konum</span><span class="sxs-lookup"><span data-stu-id="c7217-185">Location</span></span> | <span data-ttu-id="c7217-186">Plaka</span><span class="sxs-lookup"><span data-stu-id="c7217-186">License plate</span></span> | <span data-ttu-id="c7217-187">Miktar</span><span class="sxs-lookup"><span data-stu-id="c7217-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="c7217-188">24</span><span class="sxs-lookup"><span data-stu-id="c7217-188">24</span></span>        | <span data-ttu-id="c7217-189">B11</span><span class="sxs-lookup"><span data-stu-id="c7217-189">B11</span></span>          | <span data-ttu-id="c7217-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="c7217-190">BULK-001</span></span> | <span data-ttu-id="c7217-191">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="c7217-191">None</span></span>          | <span data-ttu-id="c7217-192">10</span><span class="sxs-lookup"><span data-stu-id="c7217-192">10</span></span>       |
    | <span data-ttu-id="c7217-193">24</span><span class="sxs-lookup"><span data-stu-id="c7217-193">24</span></span>        | <span data-ttu-id="c7217-194">B11</span><span class="sxs-lookup"><span data-stu-id="c7217-194">B11</span></span>          | <span data-ttu-id="c7217-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="c7217-195">FL-001</span></span>   | <span data-ttu-id="c7217-196">LP11</span><span class="sxs-lookup"><span data-stu-id="c7217-196">LP11</span></span>          | <span data-ttu-id="c7217-197">10</span><span class="sxs-lookup"><span data-stu-id="c7217-197">10</span></span>       |
    | <span data-ttu-id="c7217-198">24</span><span class="sxs-lookup"><span data-stu-id="c7217-198">24</span></span>        | <span data-ttu-id="c7217-199">B22</span><span class="sxs-lookup"><span data-stu-id="c7217-199">B22</span></span>          | <span data-ttu-id="c7217-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="c7217-200">FL-002</span></span>   | <span data-ttu-id="c7217-201">LP22</span><span class="sxs-lookup"><span data-stu-id="c7217-201">LP22</span></span>          | <span data-ttu-id="c7217-202">10</span><span class="sxs-lookup"><span data-stu-id="c7217-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="c7217-203">Satış siparişi ayrıntılarını girin</span><span class="sxs-lookup"><span data-stu-id="c7217-203">Enter sales order details</span></span>

1. <span data-ttu-id="c7217-204">**Satış ve pazarlama** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c7217-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="c7217-205">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-205">Select **New**.</span></span>
3. <span data-ttu-id="c7217-206">Satış siparişi başlığındaki **Müşteri hesabı** alanına **US-003** girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="c7217-207">Yeni kalem için bir satır ekleyin ve miktar olarak **10** girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="c7217-208">**Ambar** alanının **24**'e ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="c7217-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="c7217-209">**Satış siparişi satırları** hızlı sekmesinde, **Stok**'u ve ardından **Bakım** grubunu seçin ve **Toplu iş rezervasyonu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="c7217-210">**Toplu iş rezervasyonu** sayfası, sipariş satırı rezervasyonu için kullanılabilecek toplu işlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7217-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="c7217-211">Bu örnekte, **B11** numaralı toplu iş için miktarı **20** ve **B22** numaralı toplu iş için miktarı **10** gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7217-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="c7217-212">Bir satırdaki kalem "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkiliyse, toplu işe özel rezervasyona izin vermek üzere ayarlanmadığı sürece, **Toplu iş rezervasyonu** sayfasına o satırdan erişilemeyeceğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="c7217-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7217-213">Bir satış siparişi için belirli bir toplu iş rezerve etmek isterseniz **Toplu iş rezervasyonu** sayfasını kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7217-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="c7217-214">Toplu iş numarasını doğrudan satış siparişi satırına girerseniz, sistem "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesine tabi olan bir kalem için belirli bir toplu iş değeri girmişsiniz gibi davranır.</span><span class="sxs-lookup"><span data-stu-id="c7217-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="c7217-215">Satırı kaydettiğinizde bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="c7217-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="c7217-216">Toplu iş numarasının doğrudan sipariş satırında belirtilmesi gerektiğini onaylarsanız, satır normal ambar yönetimi mantığı tarafından işlenmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="c7217-217">Miktarı **Rezervasyon** sayfasından rezerve ederseniz, belirli bir toplu iş rezerve edilmez ve satır için ambar operasyonları, "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altında uygulanabilecek kurallara uygun biçimde yürütülür.</span><span class="sxs-lookup"><span data-stu-id="c7217-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="c7217-218">Genel olarak bu sayfa, ilişkili "Toplu iş-\[yerleşim\] altı" türünde rezervasyon hiyerarşisi olan kalemler için çalıştığı ve etkileşime girdiği şekilde çalışıp etkileşime girer.</span><span class="sxs-lookup"><span data-stu-id="c7217-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="c7217-219">Ancak, aşağıdaki özel durumlar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="c7217-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="c7217-220">**Kaynak satıra taahhütlü toplu iş numaraları** hızlı sekmesi, sipariş satırı için rezerve edilen toplu iş numaralarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7217-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="c7217-221">Kılavuzdaki toplu iş değerleri, ambar işleme aşamaları da dahil olmak üzere, sipariş satırının karşılanma döngüsü boyunca gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="c7217-222">Bunun aksine, **Genel bakış** hızlı sekmesinde, normal sipariş satırı rezervasyonu (yani **Yerleşim** düzeyinin üzerindeki boyutlar için yapılan rezervasyon), ambar işinin oluşturulduğu noktaya kadar kılavuzda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="c7217-223">Bunun üzerine, iş varlığı satır rezervasyonunu üstlenir ve satır rezervasyonu artık sayfada görünmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="c7217-224">**Kaynak satıra taahhütlü toplu iş numaraları** hızlı sekmesi, satış siparişi işlemcisinin, faturalamaya kadar yaşam döngüsünün her noktasında, müşterinin siparişine taahhüt edilmiş toplu iş numaralarını görüntüleyebilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c7217-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="c7217-225">Belirli bir toplu işi rezerve etmeye ek olarak, bir kullanıcı sistemin otomatik olarak seçmesine izin vermek yerine toplu işin özel yerleşimini ve plakasını kendisi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="c7217-226">Bu yetenek, sipariş taahhütlü toplu iş rezervasyon mekanizmasının tasarımıyla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="c7217-227">Daha önce belirtildiği gibi, bir toplu iş numarası "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altındaki bir kalem için rezerve edildiği zaman, sistem yerleşime kadar olan tüm boyutları rezerve etmelidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="c7217-228">Bu nedenle, ambar işi, siparişlerle çalışan kullanıcılar tarafından rezerve edilmiş olan aynı depolama boyutlarını taşır ve malzeme çekme operasyonları için uygun ve hatta olası olan kalem depolama yerleşimini temsil edemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="c7217-229">Sipariş işlemciler ambar kısıtlamalarını biliyorsa, toplu iş rezerve ederken belirli yerleşimleri ve plakaları kendileri seçmek isteyebilirler.</span><span class="sxs-lookup"><span data-stu-id="c7217-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="c7217-230">Bu durumda , kullanıcının sayfa üst bilgisindeki **Boyutları görüntüle** işlevini kullanması, **Genel bakış** hızlı sekmesindeki kılavuza yerleşimi ve plakayı eklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7217-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="c7217-231">**Toplu iş rezervasyonu** sayfasında toplu iş **B11** numaralı toplu işe ait satırı ve ardından **Satırı rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="c7217-232">Otomatik rezervasyon sırasında yerleşimleri ve plakaları atamak için belirlenmiş bir mantık yoktur.</span><span class="sxs-lookup"><span data-stu-id="c7217-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="c7217-233">Miktarı **Rezervasyon** alanına el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7217-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="c7217-234">**Kaynak satırına taahhütlü toplu iş numaraları** hızlı sekmesinde, **B11** numaralı toplu işin **Taahhüt edilen** olarak gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="c7217-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Toplu iş rezervasyonu sayfasındaki bir satış siparişi satırı için belirli bir toplu iş numarasını taahhüt etme](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="c7217-236">Bir satış siparişi satırındaki miktarın rezervasyonu çoklu toplu işler arasında yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="c7217-237">Benzer şekilde, aynı toplu işin rezervasyonu birden çok yerleşime ve plakaya karşı yapılabilir (yerleşimler için plakalar etkinleştirilirse).</span><span class="sxs-lookup"><span data-stu-id="c7217-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="c7217-238">Bir satış siparişi satırındaki miktar için belirli bir toplu işin rezervasyonu kısmi de olabilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="c7217-239">Örneğin, 100 birimlik toplam miktar, belirli bir toplu işe 20 birim taahhüt edilirken, uygun herhangi bir toplu işe tesis ve ambar düzeylerinde 80 birim rezerve edilecek şekilde rezerve edilebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="c7217-240">Bu durumda, WMS malzeme çekme işlemlerini iki ayrı iş satırı kullanarak işler.</span><span class="sxs-lookup"><span data-stu-id="c7217-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="c7217-241">**Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c7217-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="c7217-242">Kaleminizi ve ardından **Stok yönetimi** \> **Görüntüle** \> **Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Bir stok hareketi türü olarak sipariş taahhütlü rezervasyon](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="c7217-244">Kalemin, satış siparişi satırı rezervasyonuna ilişkin stok hareketlerini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="c7217-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="c7217-245">**Referans** alanının **Satış siparişi** olarak ve **Çıkış** alanının **Fiziksel rezerve miktar** olarak ayarlandığı bir hareket, **Yerleşim** düzeyinin üzerindeki stok boyutları için sipariş satırı rezervasyonunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c7217-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="c7217-246">Kalemin stok rezervasyonu hiyerarşisine göre bu boyutlar tesis, ambar ve stok durumudur.</span><span class="sxs-lookup"><span data-stu-id="c7217-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="c7217-247">**Referans** alanının **Sipariş taahhütlü rezervasyon** olarak ve **Çıkış** alanının **Fiziksel rezerve miktar** olarak ayarlandığı bir hareket, belirli toplu iş ve onun üzerindeki tüm stok boyutları için sipariş satırı rezervasyonunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c7217-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="c7217-248">Kalemin stok rezervasyonu hiyerarşisine göre bu boyutlar toplu iş numarası ve yerleşimidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="c7217-249">Bu örnekte yerleşim **Bulk-001**'dir.</span><span class="sxs-lookup"><span data-stu-id="c7217-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="c7217-250">Satış siparişi üst bilgisinde **Ambar** \> **Eylemler** \> **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="c7217-251">Sipariş satırı artık dalgalıdır ve bir yük ve iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="c7217-252">Sipariş taahhütlü toplu iş numaraları olan ambar işini inceleyin ve işleyin</span><span class="sxs-lookup"><span data-stu-id="c7217-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="c7217-253">**Satış siparişi satırları** hızlı sekmesinde **Ambar** \> **İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="c7217-254">Satış siparişi satırına taahhüt edilen toplu iş miktarları için malzeme çekme işlemini işleyen iş aşağıdaki özelliklere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="c7217-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="c7217-255">Sistem iş oluşturmak için, yerleşim yönergelerini değil sistem çalışma şablonlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="c7217-256">Yeni işin oluşturulacağı zamanı belirlemek için, en fazla malzeme çekme satırı veya özel bir ölçü birimi gibi iş şablonları için tanımlanan tüm standart ayarlar uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="c7217-257">Bununla birlikte, sipariş taahhütlü rezervasyon tüm stok boyutlarını zaten belirttiğinden, çekme yerleşimlerinin belirlenmesi ile ilgili yerleşim yönergeleriyle ilişkili kurallar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="c7217-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="c7217-258">Bu stok boyutları, ambar depolama düzeyindeki boyutları içerir.</span><span class="sxs-lookup"><span data-stu-id="c7217-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="c7217-259">Bu nedenle, iş, yerleşim yönergelerine danışmak zorunda kalmadan bu boyutları devralır.</span><span class="sxs-lookup"><span data-stu-id="c7217-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="c7217-260">Toplu iş numarası, çekme satırında gösterilmez (ilişkili bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi olan bir kalem için oluşturulan iş satırında olduğu gibi). Bunun yerine, "ilk" toplu iş numarası ve tüm diğer depolama boyutları, ilişkili stok hareketlerinden referansta bulunulan iş satırı iş stok hareketinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Sipariş taahhütlü rezervasyondan kaynaklanan iş için ambar stok hareketi](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="c7217-262">İş oluşturulduktan sonra, **Referans** alanının **Sipariş taahhütlü rezervasyon** olarak ayarlandığı kalem stok hareketi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="c7217-263">**Referans** alanının **İş** olarak ayarlandığı stok hareketi, miktarın tüm stok boyutlarında fiziksel rezervasyonu tutar.</span><span class="sxs-lookup"><span data-stu-id="c7217-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="c7217-264">Ambar operasyonları her zaman olduğu gibi işin yürütülmesini işlemeye devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="c7217-265">Ancak, mobil cihazdaki yönergelerde çalışandan belirli bir toplu iş numarası seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="c7217-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="c7217-266">Yerleşimlerin plaka denetimli olduğu ambar ortamlarında, bir çalışan birden fazla plakada aynı toplu işi depolayan bir yerleşime ulaştığında, henüz rezerve edilmemiş olan (örneğin başka bir sipariş taahhütlü rezervasyon veya o türde bir rezervasyondan kaynaklanan iş tarafından) herhangi bir plakayı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="c7217-267">İş satırında belirtilen yerleşimden seçim yapılması pratik değilse, ambar operatörleri, belirli toplu işin çekilmesini daha uygun bir yerleşimden yeniden yönlendirmek için aşağıdaki eylemlerden birini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="c7217-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="c7217-268">Bir mobil cihazdaki standart **Konumu geçersiz kıl** eylemi (ambar çalışanının **Çekme yerleşimini geçersiz kılmaya izin ver** ayarını etkinleştirmesi koşuluyla)</span><span class="sxs-lookup"><span data-stu-id="c7217-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="c7217-269">**Çalışma listesi ayrıntıları** sayfasında **Yerleşimi değiştir** eylemi.</span><span class="sxs-lookup"><span data-stu-id="c7217-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="c7217-270">Mobil cihazda, işi çekme ve yerleştirme işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="c7217-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="c7217-271">Artık **B11** numaralı toplu iş için **10** miktarı artık satış siparişi satırı için çekilmiş ve **Baydoor** yerleşimine yerleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7217-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="c7217-272">Bu noktada, miktar kamyona yüklenmeye ve müşterinin adresine gönderilmeye hazırdır.</span><span class="sxs-lookup"><span data-stu-id="c7217-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="c7217-273">Sipariş taahhütlü toplu iş numaraları olan ambar işinin özel durumunu işleme</span><span class="sxs-lookup"><span data-stu-id="c7217-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="c7217-274">Sipariş taahhütlü toplu iş numaralarını toplama için yapılan ambar işi, normal işle aynı standart ambar özel durum işlemeye tabidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="c7217-275">Genel olarak, açık iş veya iş satırı iptal edilebilir, bir kullanıcı yerleşimi dolu olduğu için durdurulabilir ve bir hareket nedeniyle güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="c7217-276">Benzer şekilde, zaten tamamlanmış olan çekilmiş iş miktarı azaltılabilir veya işe ters işlem uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="c7217-277">Tüm bu özel durum işleme eylemlerine şu temel kural uygulanır: Müşteri için rezerve edilen parti numarası başka bir toplu iş numarasıyla değiştirilemez ancak depolama boyutları (yerleşim ve plaka) bir kullanıcının el ile yapacağı güncelleştirmeyle ya da sistemin otomatik güncelleştirmesiyle değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="c7217-278">Otomatik güncelleştirme, belirli bir toplu iş otomatik olarak rezerve edildiği ama depolama boyutları belirlenmediği zaman uygulanan aynı rastgele depolama boyutları atamasına dayanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="c7217-279">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="c7217-279">Example scenario</span></span>

<span data-ttu-id="c7217-280">Bu senaryoya bir örnek, önceden tamamlanan işin seçiminin **Çekilen miktarı düş** işleviyle iptal edildiği durumdur.</span><span class="sxs-lookup"><span data-stu-id="c7217-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="c7217-281">Bu örnek, bu konudaki önceki örneğin devamıdır.</span><span class="sxs-lookup"><span data-stu-id="c7217-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="c7217-282">**Ambar yönetimi** \> **Yükler** \> **Etkin yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c7217-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="c7217-283">Satış siparişinin sevkiyatı ile bağlantılı olarak oluşturulan yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="c7217-284">**Yük emri satırları** hızlı sekmesinden, **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="c7217-285">**Çekilen miktarı düş** sayfasındaki **Yerleşime taşı** alanında **FL-001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="c7217-286">**Plakaya taşı** alanında **LP33**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="c7217-287">Kılavuzdaki **Çekme işlemi geri alınacak stok miktarı** alanına **10** girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="c7217-288">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-288">Select **OK**.</span></span>

<span data-ttu-id="c7217-289">Çekme işlemini geri alma eyleminin sonuçları:</span><span class="sxs-lookup"><span data-stu-id="c7217-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="c7217-290">Daha önce kapatılan işin durumu **İptal edildi** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="c7217-291">**B11** numaralı toplu işte çekme işlemi iptal edilen **10** miktarı için **Stok hareketi** türünde yeni iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="c7217-292">Bu iş, **Baydoor** yerleşiminden **FL-001** yerleşimindeki **LP33** numaralı plakaya hareketi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c7217-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="c7217-293">Durum ayarı **Kapalı** yapılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="c7217-294">Sistem, başlangıçta sipariş edilen toplu iş numarasını yeniden rezerve edip yerleşim ve plaka kodlarının atamasını yapar.</span><span class="sxs-lookup"><span data-stu-id="c7217-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="c7217-295">(Bu işlem, belirli bir toplu iş numarasına yönelik olarak sipariş satırı için **Satırı rezerve et** işlevini çalıştırmaya eşdeğerdir.)</span><span class="sxs-lookup"><span data-stu-id="c7217-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="c7217-296">Sonuç olarak **B11** numaralı toplu iş, **Toplu iş rezervasyonu** sayfasının **Kaynak satırına taahhütlü toplu iş numaraları** hızlı sekmesinde Taahhüt edildi olarak gösterilir ve **Rezervasyon** alanında **B11** numaralı toplu iş için **10** miktarı yer alır.</span><span class="sxs-lookup"><span data-stu-id="c7217-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="c7217-297">Ek olarak, **Yerleşim** alanı ayarı **FL-001**, **Plaka** alanı ayarı **LP11** olur.</span><span class="sxs-lookup"><span data-stu-id="c7217-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="c7217-298">(Bu alanlar görünmüyorsa, kılavuza ekleyebilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="c7217-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="c7217-299">Aşağıdaki tablolarda, sistemin belirli ambar eylemleri için sipariş taahhütlü toplu iş rezervasyonunu nasıl işleyeceğine ilişkin genel bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c7217-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="c7217-300">Tablolardaki içeriği yorumlamak için, her ambar eyleminin, sipariş taahhütlü bir toplu iş rezervasyonundan kaynaklanan mevcut ambar işi bağlamında çalıştırıldığını veya her ambar eyleminin bu türdeki işi etkilediğini varsayın.</span><span class="sxs-lookup"><span data-stu-id="c7217-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="c7217-301">Bu tablolarda "Toplu iş miktarı kullanılabilir" sütunu, mevcut sipariş taahhütlü rezervasyonlar için zaten rezerve edilmiş veya o türdeki rezervasyonlardan kaynaklanan ambar işi tarafından önceden rezerve edilmiş miktara ek olarak bir toplu iş miktarının kullanılabilir olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7217-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="c7217-302">Açık işte çekme yerleşimini geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="c7217-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-303">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-304">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-305">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-305">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-306">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-306">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-307">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-308"><strong>Çekme yerleşimini geçersiz kılmaya izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7217-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="c7217-309">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-310">Malzeme çekme işini başlatırken Ambar Mobil Uygulaması'nda (WMA) <strong>Konumu geçersiz kıl</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="c7217-311"><strong>Öner</strong>'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="c7217-312">Toplu iş miktarı kullanılabilirliğine dayalı olarak önerilen yeni yerleşimi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c7217-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-313">Geçerli işte aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="c7217-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="c7217-314">Çekme satırındaki yerleşim yeni yerleşime güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="c7217-315">(Yerleşim plaka denetimliyse, iş stok hareketine rastgele bir plaka atanır ve çalışan, kullanılabilir miktarlı herhangi bir plakadan çekme işlemi yapabilir.)</span><span class="sxs-lookup"><span data-stu-id="c7217-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="c7217-316">Miktar yeni yerleşimde birden fazla plakada bulunursa, orijinal çekme satırı her bir plakayla eşleştirilmek üzere birden çok satıra bölünür.</span><span class="sxs-lookup"><span data-stu-id="c7217-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-317">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-318">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-319">Malzeme çekme işini başlatırken WMA'daki <strong>Konumu geçersiz kıl</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="c7217-320">El ile bir yerleşim girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-321"><strong>Konumu geçersiz kıl</strong> eylemi mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="c7217-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="c7217-322">Başarısız olur ve bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="c7217-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="c7217-323">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="c7217-324">Tam düğme – Kullanıcı yerleşimindeki taşma nedeniyle bir iş satırını bölün</span><span class="sxs-lookup"><span data-stu-id="c7217-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-325">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-326">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-327">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-327">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-328">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-328">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-329">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c7217-330">Mobil cihaz menü öğesinde <strong>İşin bölünmesine izin ver</strong> seçeneği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="c7217-331">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-332">Malzeme çekme işini işlerken WMA'daki <strong>Tam</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="c7217-333"><strong>Çekme Miktarı</strong> alanında, tam kapasiteyi belirtmek için gereken kısmi bir çekme miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="c7217-334">Geçerli işte, miktar, çekilmesi gereken kalan miktara güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="c7217-335">Çekilen miktar için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="c7217-336">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="c7217-337">Tamamlanan işin çekilen miktarını bir yükten düşme</span><span class="sxs-lookup"><span data-stu-id="c7217-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-338">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-339">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-340">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-340">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-341">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-341">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-342">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-343">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-343">Not applicable</span></span></td>
<td><span data-ttu-id="c7217-344">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-345">Yük satırından <strong>Çekilen miktarı düş</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c7217-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="c7217-346">Çekme işlemi iptal edilecek tam miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="c7217-347">Bir "taşıma" yerleşimi/plakası seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="c7217-348">Yük satırıyla ilişkili iş iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="c7217-349">Stok hareketi için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-350">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-351">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-352">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-352">No</span></span></td>
<td><span data-ttu-id="c7217-353">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-353">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-354">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-354">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-355">Miktar; aynı toplu iş için ve çekme işlemi iptal sırasında girilen aynı yerleşim ve plaka (yerleşim plaka denetimliyse) için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="c7217-356">Ambar içinde bir kalemi taşıma</span><span class="sxs-lookup"><span data-stu-id="c7217-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="c7217-357">Bu ambar eylemi şablonla hareket için değil, yalnızca **İş oluşturma işlemi** türündeki hareket için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c7217-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-358">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-359">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-360">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-360">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-361">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-361">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-362">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-363"><strong>Stoğun ilişkili işle birlikte taşınmasına izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7217-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="c7217-364">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-365">WMA 'da bir hareket başlatın.</span><span class="sxs-lookup"><span data-stu-id="c7217-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="c7217-366">"Çıkış" ve "hedef" yerleşimlerini girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="c7217-367">Taşımadan etkilenen mevcut tüm işte çekme yerleşimi yeni "hedef" yerleşime güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="c7217-368">Stok hareketi için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-369">Belirtilen yerleşimden miktar hareketinden etkilenen mevcut tüm rezervasyonlar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-370">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-371">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-371">No</span></span></td>
<td><span data-ttu-id="c7217-372">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-372">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-373">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-373">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-374">Belirtilen yerleşimden miktar hareketinden etkilenen tüm mevcut rezervasyonlar aynı toplu iş için ve yeni "hedef" yerleşim ve plaka (yerleşim plaka denetimliyse) için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="c7217-375">Tamamlanan işin çekilen miktarını bir yükten veya dalgadan geri alma</span><span class="sxs-lookup"><span data-stu-id="c7217-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-376">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-377">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-378">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-378">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-379">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-379">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-380">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="c7217-381">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-381">Not applicable</span></span></td>
<td><span data-ttu-id="c7217-382">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-383"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c7217-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="c7217-384">İstek sayfasında <strong>Maddeleri geçerli konumda bırak</strong>seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c7217-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-385">Yükle ilişkili tüm iş iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="c7217-386">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-387">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-388">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-388">No</span></span></td>
<td><span data-ttu-id="c7217-389">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-389">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-390">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-390">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-391">Miktar, aynı toplu iş için ve miktarın geri almaya bırakıldığı yerleşim ve plaka için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-392">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-393"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c7217-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="c7217-394">İstek sayfasında <strong>Maddeleri bu konuma ata</strong>seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c7217-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="c7217-395">Geçerli iş iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="c7217-396">Stok hareketi için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-397">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-398">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-399">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-399">No</span></span></td>
<td><span data-ttu-id="c7217-400">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-400">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-401">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-401">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-402">Miktar, aynı toplu iş için ve miktarın geri alma işlemine atandığı yerleşim ve plaka için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-403">Evet/Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-404"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c7217-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="c7217-405">İstek sayfasında <strong>Maddeleri bu konuma taşı</strong>seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c7217-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-406">Ters işlem desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="c7217-407">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-408">Evet/Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-409"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c7217-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="c7217-410">İstek sayfasında <strong>Maddeleri konum yönergelerine göre taşı</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c7217-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-411">Ters işlem desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="c7217-412">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="c7217-413">Miktarı eksik seçme – Siz malzeme çekme işini gerçekleştirirken, miktarın kaydını yerleşimde/plakada fiziksel olarak bulunamadı şeklinde yapın</span><span class="sxs-lookup"><span data-stu-id="c7217-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-414">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-415">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-416">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-416">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-417">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-417">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-418">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-419"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Yok</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7217-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="c7217-420">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-421">Siz malzeme çekme işini işlerken WMA'da <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="c7217-422"><strong>Malzeme çekme miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="c7217-423"><strong>Neden</strong> alanına <strong>Yeniden tahsis yok</strong> girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="c7217-424">Geçerli iş kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="c7217-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="c7217-425">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-426">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-427">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-428">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-428">No</span></span></td>
<td><span data-ttu-id="c7217-429">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="c7217-430">Eksik malzeme çekme eylemi başarısız olur ve bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="c7217-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="c7217-431">Geçerli iş açık kalır.</span><span class="sxs-lookup"><span data-stu-id="c7217-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-432">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-433"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Yok</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7217-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="c7217-434">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-435">Siz malzeme çekme işini işlerken WMA'da <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="c7217-436"><strong>Malzeme çekme miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="c7217-437"><strong>Neden</strong> alanına <strong>Yeniden tahsis yok</strong> girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="c7217-438">Geçerli iş kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="c7217-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="c7217-439">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-440">Eksik çekilen yerleşimde miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-441">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-442">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-442">No</span></span></td>
<td><span data-ttu-id="c7217-443">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-443">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-444">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-444">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-445">Eksik çekilen yerleşimde miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-446"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır/Evet</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7217-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="c7217-447">Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7217-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="c7217-448">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-449">Siz malzeme çekme işini işlerken WMA'da <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="c7217-450"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="c7217-451"><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="c7217-452">Listede yerleşimi/plakayı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="c7217-453">Geçerli işte aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="c7217-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="c7217-454">Çekme satırı kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="c7217-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="c7217-455">Yerine koyma satırı iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="c7217-456">Yeni bir çekme satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-456">A new pick line is created.</span></span> <span data-ttu-id="c7217-457">Satır, kullanıcının seçtiği yerleşimi/plakayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="c7217-458">Yeni bir yerine koyma satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c7217-459">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-460">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-461"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7217-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="c7217-462">Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7217-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="c7217-463">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-464">Siz malzeme çekme işini işlerken WMA'da <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="c7217-465"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="c7217-466"><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-467">Eksik malzeme çekme eylemi başarısız olur ve bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="c7217-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="c7217-468">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-469"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7217-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="c7217-470">Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7217-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="c7217-471">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-472">Siz malzeme çekme işini işlerken WMA'da <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="c7217-473"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="c7217-474"><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="c7217-475">Listede yerleşimi/plakayı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="c7217-476">Geçerli işte aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="c7217-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="c7217-477">Çekme satırı kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="c7217-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="c7217-478">Yerine koyma satırı iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c7217-479">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c7217-480">Eksik çekilen yerleşimde/plakada miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-481"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Otomatik</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet/Hayır</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet/Hayır</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7217-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="c7217-482">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="c7217-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-483">Siz malzeme çekme işini işlerken WMA'da <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="c7217-484"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="c7217-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="c7217-485"><strong>Neden</strong> alanında <strong>Otomatik tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-486">Otomatik yeniden tahsisat içeren eksik çekme desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="c7217-487">Otomatik yeniden tahsisat içeren eksik çekme desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="c7217-488">Stok durumunu değiştir</span><span class="sxs-lookup"><span data-stu-id="c7217-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="c7217-489">Bu ambar eylemi birden fazla giriş noktasından gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="c7217-490">Burada gösterilen örnek, **Konuma göre eldeki** sayfasında **Stok durumu değişikliği** eylemini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c7217-491">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="c7217-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="c7217-492">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c7217-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="c7217-493">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="c7217-493">Key user steps</span></span></th>
<th><span data-ttu-id="c7217-494">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="c7217-494">Warehouse work</span></span></th>
<th><span data-ttu-id="c7217-495">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="c7217-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-496"><strong>Ambar</strong> sekmesindeki <strong>Ambar</strong> kaydında, <strong>Rezervasyonları ve işaretleri kaldır</strong> alanının ayarı <strong>Rezervasyonlar</strong> veya <strong>İşaretler ve rezervasyonlar</strong> yapılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="c7217-497">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-498">Belirli bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="c7217-499">Belirli bir kalem, yerleşim ve plakası (yerleşim plaka denetimliyse) olan bir satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="c7217-500"><strong>Stok durumu değişikliği</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="c7217-501"><strong>Stok durumu</strong> alanının ayarını <strong>Durdurma</strong> yapın.</span><span class="sxs-lookup"><span data-stu-id="c7217-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-502">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="c7217-503">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-504">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="c7217-505">Stok durumu boyutundaki değişikliği temsil için <strong>Stok durumu değişikliği</strong> türünde iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="c7217-506">Durdurulan miktarın rezervasyonunu temsil için <strong>Stok durdurma</strong> türünde ve <strong>Fiziksel rezerve miktar</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="c7217-507">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-507">No</span></span></td>
<td><span data-ttu-id="c7217-508">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-508">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-509">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="c7217-510">Rezervasyon kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="c7217-511">Stok durumu boyutundaki değişikliği temsil için <strong>Stok durumu değişikliği</strong> türünde iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="c7217-512">Durdurulan miktarın rezervasyonunu temsil için <strong>Stok durdurma</strong> türünde ve <strong>Fiziksel rezerve miktar</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7217-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="c7217-513"><strong>Ambar</strong> sekmesindeki <strong>Ambar</strong> kaydında, <strong>Rezervasyonları ve işaretleri kaldır</strong> alanının ayarı <strong>Yok</strong> yapılır.</span><span class="sxs-lookup"><span data-stu-id="c7217-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="c7217-514">Evet</span><span class="sxs-lookup"><span data-stu-id="c7217-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="c7217-515">Belirli bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="c7217-516">Belirli bir kalem, yerleşim ve plakası (yerleşim plaka denetimliyse) olan bir satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="c7217-517"><strong>Stok durumu değişikliği</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c7217-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="c7217-518"><strong>Stok durumu</strong> alanının ayarını <strong>Durdurma</strong> yapın.</span><span class="sxs-lookup"><span data-stu-id="c7217-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="c7217-519">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="c7217-520">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="c7217-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="c7217-521">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="c7217-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c7217-522">Hayır</span><span class="sxs-lookup"><span data-stu-id="c7217-522">No</span></span></td>
<td><span data-ttu-id="c7217-523">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="c7217-523">See the previous row.</span></span></td>
<td><span data-ttu-id="c7217-524">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="c7217-525">Stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="c7217-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="c7217-526">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="c7217-526">Limitations</span></span>

- <span data-ttu-id="c7217-527">Esnek ambar düzeyinde boyut rezervasyonu işlevi aşağıdaki özellikleri desteklemez:</span><span class="sxs-lookup"><span data-stu-id="c7217-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="c7217-528">Fiili ağırlık yönetimi</span><span class="sxs-lookup"><span data-stu-id="c7217-528">Catch weight management</span></span>
    - <span data-ttu-id="c7217-529">Fiziksel negatif stok</span><span class="sxs-lookup"><span data-stu-id="c7217-529">Physical negative inventory</span></span>
    - <span data-ttu-id="c7217-530">Sipariş edilen tedarikte rezervasyon</span><span class="sxs-lookup"><span data-stu-id="c7217-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="c7217-531">Transfer emirleri ve hammadde çekme</span><span class="sxs-lookup"><span data-stu-id="c7217-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="c7217-532">Yönerge birimine göre ambalajlama için konteyner konsolidasyon kuralında sınırlamalar vardır.</span><span class="sxs-lookup"><span data-stu-id="c7217-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="c7217-533">Sipariş taahhütlü rezervasyonlar için, **Yönerge birimine gör ambalajla**alanının etkinleştirildiği konteyner yapı şablonlarını kullanmamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="c7217-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="c7217-534">Geçerli tasarımda, ambar işi oluşturulurken yerleşim yönergeleri kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="c7217-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="c7217-535">Bu nedenle, konteyner kullanımı dalga adımı sırasında yalnızca birim sıra grubundaki en küçük birim uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c7217-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
