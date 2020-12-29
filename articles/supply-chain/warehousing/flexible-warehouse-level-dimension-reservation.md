---
title: Esnek ambar düzeyi boyut rezervasyon ilkesi
description: Bu konu, toplu işle izlenen ürünler satan ve lojistiklerini WMS-etkin operasyonlar olarak çalıştıran işletmelerin, ürünlerle ilişkili rezervasyon hiyerarşisi belirli toplu işlerin rezervasyonuna izin vermese bile, belirli toplu işleri rezerve etmelerine izin veren stok rezervasyon ilkesini açıklar.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b9bd4e67ed64218f9c4ac87bd143f73680af9ac4
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439626"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="3b57b-103">Esnek ambar düzeyi boyut rezervasyon ilkesi</span><span class="sxs-lookup"><span data-stu-id="3b57b-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b57b-104">"Toplu iş-\[yerleşim\] altı" türünde stok rezervasyon hiyerarşisi ürünlerle ilişkiliyse, toplu işle izlenen ürünler satan ve lojistiklerini Microsoft Dynamics 365 Warehouse Management System (WMS) için etkinleştirilmiş operasyonlar olarak yürüten işletmeler, müşteri satış siparişleri için bu ürünlerin belirli toplu işlerini rezerve edemez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="3b57b-105">Benzer şekilde, satış siparişlerindeki ürünler varsayılan rezervasyon hiyerarşisiyle ilişkilendirildiğinde bu ürünler için belirli plakalar rezerve edilemez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="3b57b-106">Bu konu, ürünler bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkili olsa bile, bu işletmelerin belirli toplu işleri veya plakaları rezerve etmelerine izin veren stok rezervasyon ilkesini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="3b57b-107">Stok rezervasyonu hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="3b57b-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="3b57b-108">Bu bölüm, varolan stok rezervasyon hiyerarşisini özetlemektedir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="3b57b-109">Ambar mantığı, istenen miktarlara yerleşim atamaktan ve yerleşimi rezerve etmekten sorumluyken, stok rezervasyon hiyerarşisi, depolama boyutlarıyla ilgili olarak, talep emrinin tesis, ambar ve stok durumu zorunlu boyutlarını taşımasını zorunlu kılar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="3b57b-110">Başka bir deyişle, talep emri ve ambar operasyonları arasındaki etkileşimlerde, talep emrinde siparişin sevk çıkışının yapılacağı yerin (yani tesis ve ambar) belirtilmesi beklenir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="3b57b-111">Ambar, bunun üzerine, ambar tesislerindeki gerekli miktarı bulmak için kendi mantığını temel alır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="3b57b-112">Bununla birlikte, işletmenin operasyon modelini yansıtmak için, izleme boyutları (toplu iş ve seri numaraları) daha fazla esneklik gerektirir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="3b57b-113">Bir stok rezervasyonu hiyerarşisi aşağıdaki koşulların geçerli olduğu senaryolar barındırabilir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="3b57b-114">İşletme, ambar depolama alanında miktarlar bulunduktan sonra, toplu iş veya seri numaraları olan miktarların çekilmesini yönetmek için kendi ambar operasyonlarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="3b57b-115">Bu modele genellikle *Toplu iş-\[yerleşim\] altı* adı verilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="3b57b-116">Genellikle, satıcı şirketle talebi oluşturan müşteriler için bir ürünün toplu iş veya seri numarası tanımlaması önemli olmadığı zaman kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="3b57b-117">Toplu iş veya seri numaraları bir müşterinin sipariş belirtiminin parçasıysa ve bunlar talep emrinde kaydedilirse, ambardaki miktarları bulan ambar operasyonları istenen belirli sayılarla sınırlandırılır ve bunları değiştirmelerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="3b57b-118">Bu modele *Toplu iş-\[yerleşim\] üstü* adı verilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="3b57b-119">Bu senaryolarda sorun, serbest bırakılan her ürüne yalnızca bir stok rezervasyonu hiyerarşisinin atanabilmesidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="3b57b-120">Bu nedenle, WMS'nin izlenen kalemleri işlemesi için, hiyerarşi ataması toplu iş veya seri numarasının ne zaman rezerve edilmesi gerektiğini (talep emri alındığı zaman veya ambar çekme işi sırasında) belirledikten sonra bu zamanlama geçici olarak değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="3b57b-121">Toplu işle izlenen kalemler için esnek rezervasyon</span><span class="sxs-lookup"><span data-stu-id="3b57b-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="3b57b-122">İş senaryosu</span><span class="sxs-lookup"><span data-stu-id="3b57b-122">Business scenario</span></span>

<span data-ttu-id="3b57b-123">Bu senaryoda, bir şirket, mamul malların toplu iş numaralarına göre izlendiği bir stok stratejisi kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="3b57b-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="3b57b-124">Bu şirket aynı zamanda WMS iş yükünü de kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="3b57b-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="3b57b-125">Bu iş yükünün toplu iş etkin kalemler için ambar çekme ve sevkiyat operasyonları planlamak ve çalıştırmak için iyi donatılmış bir mantığı olduğundan, mamul kalemlerin çoğu bir "Toplu iş\[yerleşim\] altı" stok rezervasyon hiyerarşisiyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="3b57b-126">Bu tür operasyon kurulumunun avantajı, hangi toplu işlerin çekileceği ve bu maddelerin ambarda nereye koyulacağı ile ilgili kararların (yürürlükteki rezervasyon kararları), ambar çekme operasyonları başlayana kadar ertelenmesidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="3b57b-127">Bunlar müşterinin siparişi verilirken yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="3b57b-128">"Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi şirketin işletme hedeflerine uygun olmakla birlikte, şirketin mevcut müşterilerinin birçoğu, ürünleri yeniden sipariş ettikleri zaman, daha önce satın aldıkları aynı toplu işi istemektedir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="3b57b-129">Bu nedenle, şirket, müşterinin aynı kalem için talebine bağlı olarak toplu iş rezervasyonu kurallarının işleniş biçiminde esneklik istiyor ve böylece aşağıdaki davranışlar ortaya çıkıyor:</span><span class="sxs-lookup"><span data-stu-id="3b57b-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="3b57b-130">Bir toplu iş numarası, satış işlemcisi tarafından sipariş alınırken kaydedilip rezerve edilebilir ve ambar operasyonları sırasında değiştirilemez ve/veya başka taleplerle alınamaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="3b57b-131">Bu davranış, sipariş edilen toplu iş numarasının müşteriye sevk edilmesini garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="3b57b-132">Toplu iş numarası müşteri için önemli değilse, ambar operasyonları, satış siparişi kaydı ve rezervasyon yapıldıktan sonra malzeme çekme işi sırasında bir toplu iş numarası belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="3b57b-133">Satış siparişinde belirli bir toplu işin rezervasyonuna izin verme</span><span class="sxs-lookup"><span data-stu-id="3b57b-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="3b57b-134">Bir "Toplu iş-\[yerleşim\] altı" stok rezervasyon hiyerarşisi ile ilişkilendirilmiş kalemler için toplu iş rezervasyon davranışında istenen esnekliği sağlamak için, stok yöneticilerinin, **Stok rezervasyonu hiyerarşileri** sayfasındaki **Toplu iş numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu işaretlemeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Stok rezervasyonu hiyerarşisini esnek hale getirme](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="3b57b-136">Hiyerarşide **Toplu iş numarası** düzeyi seçildiği zaman, o düzeyin üzerindeki ve **Yerleşim** düzeyine kadar olan tüm boyutlar otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="3b57b-137">(Varsayılan olarak **Yerleşim** düzeyinin üzerindeki tüm boyutlar önceden seçilmiştir.) Bu davranış, siz sipariş satırında belirli bir toplu iş numarasını rezerve ettikten sonra, toplu iş numarası ve yerleşim arasındaki aralıkta yer alan tüm boyutların da otomatik olarak rezerve edildiği mantığı yansıtır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="3b57b-138">**Talep emrinde rezervasyona izin ver** onay kutusu yalnızca ambar yerleşim boyutunun altındaki rezervasyon hiyerarşisi düzeylerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="3b57b-139">**Toplu iş numarası** ve **Plaka**, hiyerarşide esnek rezervasyon ilkesi için açık olan tek düzeydir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="3b57b-140">Başka bir deyişle, **Konum** veya **Seri numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="3b57b-141">Rezervasyon hiyerarşiniz her zaman **Toplu iş numarası** düzeyinin altında olması gereken seri numarası boyutunu içeriyorsa ve toplu iş numarası için toplu işe özel rezervasyonu etkinleştirdiyseniz, "Seri-\[yerleşim\] altı" rezervasyon ilkesi için geçerli olan kurallara dayalı olarak, sistem seri numarası rezervasyonu ve malzeme çekme operasyonlarını işlemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="3b57b-142">Herhangi bir noktada, dağıtımınızda varolan bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi için toplu işe özel rezervasyona izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="3b57b-143">Bu değişiklik, değişiklik yapılmadan önce oluşturulan rezervasyonları ve açık ambar işini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="3b57b-144">Ancak, bu rezervasyon hiyerarşisiyle ilişkili bir veya daha fazla kalem için **Siparişli rezerve miktar**, **Fiziksel rezerve miktar** veya **Sipariş edilen** çıkış türünde stok hareketleri mevcutsa **Talep emrinde rezervasyona izin ver** onay kutusunun işareti kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="3b57b-145">Bir kalemin varolan rezervasyon hiyerarşisi siparişte toplu iş belirtimine izin vermiyorsa, hiyerarşi düzeyi yapısının her iki hiyerarşide de aynı olması koşuluyla, o kalemi toplu iş belirtimine izin veren bir rezervasyon hiyerarşisine yeniden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="3b57b-146">Yeniden atamak için **Maddeler için rezervasyon hiyerarşisini değiştir** işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="3b57b-147">Bu değişiklik, esnek toplu iş rezervasyonunu toplu iş izlemeli kalemlerin bir alt kümesi için önlemek ama ürün portföyünün geri kalanı için izin vermek istediğinizde uygun olabilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="3b57b-148">**Talep emrinde rezervasyona izin ver** onay kutusunu seçip seçmemenizden bağımsız olarak, bir sipariş satırındaki kalem için belirli bir toplu iş numarasını rezerve etmek istemiyorsanız, "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi için geçerli olan varsayılan ambar operasyonları mantığı uygulanmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="3b57b-149">Müşteri siparişi için belirli bir toplu iş numarasını rezerve etme</span><span class="sxs-lookup"><span data-stu-id="3b57b-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="3b57b-150">Toplu iş izlemeli bir maddenin "Toplu iş-\[yerleşim\] altı" stok rezervasyonu hiyerarşisi satış siparişlerinde belirli toplu iş numaralarının rezervasyonuna izin verecek şekilde ayarlandıktan sonra, satış siparişi işlemcileri, müşterinin talebine bağlı olarak, aynı kalem için müşteri siparişlerini aşağıdaki yollardan biriyle alabilir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="3b57b-151">**Sipariş ayrıntılarını bir toplu iş numarası belirtmeden girmek** – Ürünün toplu iş belirtimi müşteri için önemli değilse bu yaklaşım kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="3b57b-152">Sistemde bu tür bir siparişin işlenmesiyle ilişkili tüm varolan işlemler değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="3b57b-153">Kullanıcılar tarafında ek bir değerlendirme gerekmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="3b57b-154">**Sipariş ayrıntılarını girmek ve belirli bir toplu iş numarasını rezerve etmek** – Müşteri belirli bir toplu işi istediğinde bu yaklaşım kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="3b57b-155">Genellikle, müşteriler daha önce satın aldıkları bir ürünü yeniden sipariş ederken belirli bir toplu işi isteyecektir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="3b57b-156">Bu tür toplu iş rezervasyonuna *sipariş taahhütlü rezervasyon* adı verilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="3b57b-157">Miktarlar işlendiği ve belirli bir sipariş için bir toplu iş numarası taahhüt edildiği zaman aşağıdaki kural kümesi geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="3b57b-158">"Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altındaki bir kalem için belirli bir toplu iş numarasının rezervasyonuna izin vermek amacıyla, sistem yerleşim ve üzerindeki tüm boyutları rezerve etmelidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="3b57b-159">Bu aralık genellikle plaka boyutunu içerir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="3b57b-160">Sipariş taahhütlü toplu iş rezervasyonu kullanan bir satış satırı için malzeme çekme işi oluşturulduğunda yerleşim yönergeleri kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="3b57b-161">Sipariş taahhütlü toplu işler için işin ambara işlenmesi sırasında, kullanıcının ve sistemin toplu iş numarasını değiştirmesine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="3b57b-162">(Bu işlem özel durum işlemeyi kapsar.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="3b57b-163">Aşağıdaki örnekte uçtan uca akış gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="3b57b-164">Örnek senaryo: Toplu iş numarası tahsisatı</span><span class="sxs-lookup"><span data-stu-id="3b57b-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="3b57b-165">Bu örnek için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="3b57b-166">Toplu işe özel rezervasyona izin vermek için bir stok rezervasyonu hiyerarşisi ayarlama</span><span class="sxs-lookup"><span data-stu-id="3b57b-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="3b57b-167">**Ambar yönetimi** \> **Kurulum** \> **Stok \> Rezervasyon hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="3b57b-168">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-168">Select **New**.</span></span>
3. <span data-ttu-id="3b57b-169">**Ad** alanına bir ad girin (örneğin **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="3b57b-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="3b57b-170">**Açıklama** alanına bir açıklama girin (örneğin **Toplu iş alt esnek**).</span><span class="sxs-lookup"><span data-stu-id="3b57b-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="3b57b-171">**Seçili** alanda, **Seri numarası** ve **Sahip**'i seçin ve ardından sol ok düğmesini seçerek bunları **Kullanılabilir** alanına taşıyın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="3b57b-172">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-172">Select **OK**.</span></span>
7. <span data-ttu-id="3b57b-173">**Toplu iş numarası** boyut düzeyinin satırında, **Talep emrinde rezervasyona izin ver** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="3b57b-174">**Plaka** ve **Yerleşim** düzeyleri otomatik olarak seçilir ve bunların onay kutularını temizleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="3b57b-175">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="3b57b-176">Yeni bir serbest bırakılan ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="3b57b-176">Create a new released product</span></span>

1. <span data-ttu-id="3b57b-177">Bu değerleri kullanarak ürünün üç ana veri parametresini ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="3b57b-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="3b57b-178">**Depolama boyutu grubu** alanında **Ambar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="3b57b-179">**İzleme boyutu grubu** alanında **Batch-Phy**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="3b57b-180">**Rezervasyon hiyerarşisi** alanında **BatchFlex**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="3b57b-181">**B11** ve **B22** gibi iki toplu iş numarası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b57b-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="3b57b-182">Aşağıdaki değerleri kullanarak eldeki stoka kalem miktarları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="3b57b-183">Ambar</span><span class="sxs-lookup"><span data-stu-id="3b57b-183">Warehouse</span></span> | <span data-ttu-id="3b57b-184">Parti numarası</span><span class="sxs-lookup"><span data-stu-id="3b57b-184">Batch number</span></span> | <span data-ttu-id="3b57b-185">Konum</span><span class="sxs-lookup"><span data-stu-id="3b57b-185">Location</span></span> | <span data-ttu-id="3b57b-186">Plaka</span><span class="sxs-lookup"><span data-stu-id="3b57b-186">License plate</span></span> | <span data-ttu-id="3b57b-187">Miktar</span><span class="sxs-lookup"><span data-stu-id="3b57b-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="3b57b-188">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-188">24</span></span>        | <span data-ttu-id="3b57b-189">B11</span><span class="sxs-lookup"><span data-stu-id="3b57b-189">B11</span></span>          | <span data-ttu-id="3b57b-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="3b57b-190">BULK-001</span></span> | <span data-ttu-id="3b57b-191">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="3b57b-191">None</span></span>          | <span data-ttu-id="3b57b-192">10</span><span class="sxs-lookup"><span data-stu-id="3b57b-192">10</span></span>       |
    | <span data-ttu-id="3b57b-193">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-193">24</span></span>        | <span data-ttu-id="3b57b-194">B11</span><span class="sxs-lookup"><span data-stu-id="3b57b-194">B11</span></span>          | <span data-ttu-id="3b57b-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="3b57b-195">FL-001</span></span>   | <span data-ttu-id="3b57b-196">LP11</span><span class="sxs-lookup"><span data-stu-id="3b57b-196">LP11</span></span>          | <span data-ttu-id="3b57b-197">10</span><span class="sxs-lookup"><span data-stu-id="3b57b-197">10</span></span>       |
    | <span data-ttu-id="3b57b-198">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-198">24</span></span>        | <span data-ttu-id="3b57b-199">B22</span><span class="sxs-lookup"><span data-stu-id="3b57b-199">B22</span></span>          | <span data-ttu-id="3b57b-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="3b57b-200">FL-002</span></span>   | <span data-ttu-id="3b57b-201">LP22</span><span class="sxs-lookup"><span data-stu-id="3b57b-201">LP22</span></span>          | <span data-ttu-id="3b57b-202">10</span><span class="sxs-lookup"><span data-stu-id="3b57b-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="3b57b-203">Satış siparişi ayrıntılarını girin</span><span class="sxs-lookup"><span data-stu-id="3b57b-203">Enter sales order details</span></span>

1. <span data-ttu-id="3b57b-204">**Satış ve pazarlama** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="3b57b-205">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-205">Select **New**.</span></span>
3. <span data-ttu-id="3b57b-206">Satış siparişi başlığındaki **Müşteri hesabı** alanına **US-003** girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="3b57b-207">Yeni kalem için bir satır ekleyin ve miktar olarak **10** girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="3b57b-208">**Ambar** alanının **24**'e ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="3b57b-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="3b57b-209">**Satış siparişi satırları** hızlı sekmesinde, **Stok**'u ve ardından **Bakım** grubunu seçin ve **Toplu iş rezervasyonu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="3b57b-210">**Toplu iş rezervasyonu** sayfası, sipariş satırı rezervasyonu için kullanılabilecek toplu işlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="3b57b-211">Bu örnekte, **B11** numaralı toplu iş için miktarı **20** ve **B22** numaralı toplu iş için miktarı **10** gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="3b57b-212">Bir satırdaki kalem "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkiliyse, toplu işe özel rezervasyona izin vermek üzere ayarlanmadığı sürece, **Toplu iş rezervasyonu** sayfasına o satırdan erişilemeyeceğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b57b-213">Bir satış siparişi için belirli bir toplu iş rezerve etmek isterseniz **Toplu iş rezervasyonu** sayfasını kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="3b57b-214">Toplu iş numarasını doğrudan satış siparişi satırına girerseniz, sistem "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesine tabi olan bir kalem için belirli bir toplu iş değeri girmişsiniz gibi davranır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="3b57b-215">Satırı kaydettiğinizde bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="3b57b-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="3b57b-216">Toplu iş numarasının doğrudan sipariş satırında belirtilmesi gerektiğini onaylarsanız, satır normal ambar yönetimi mantığı tarafından işlenmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="3b57b-217">Miktarı **Rezervasyon** sayfasından rezerve ederseniz, belirli bir toplu iş rezerve edilmez ve satır için ambar operasyonları, "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altında uygulanabilecek kurallara uygun biçimde yürütülür.</span><span class="sxs-lookup"><span data-stu-id="3b57b-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="3b57b-218">Genel olarak bu sayfa, ilişkili "Toplu iş-\[yerleşim\] altı" türünde rezervasyon hiyerarşisi olan kalemler için çalıştığı ve etkileşime girdiği şekilde çalışıp etkileşime girer.</span><span class="sxs-lookup"><span data-stu-id="3b57b-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="3b57b-219">Ancak, aşağıdaki özel durumlar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="3b57b-220">**Kaynak satıra taahhütlü toplu iş numaraları** hızlı sekmesi, sipariş satırı için rezerve edilen toplu iş numaralarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="3b57b-221">Kılavuzdaki toplu iş değerleri, ambar işleme aşamaları da dahil olmak üzere, sipariş satırının karşılanma döngüsü boyunca gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="3b57b-222">Bunun aksine, **Genel bakış** hızlı sekmesinde, normal sipariş satırı rezervasyonu (yani **Yerleşim** düzeyinin üzerindeki boyutlar için yapılan rezervasyon), ambar işinin oluşturulduğu noktaya kadar kılavuzda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="3b57b-223">Bunun üzerine, iş varlığı satır rezervasyonunu üstlenir ve satır rezervasyonu artık sayfada görünmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="3b57b-224">**Kaynak satıra taahhütlü toplu iş numaraları** hızlı sekmesi, satış siparişi işlemcisinin, faturalamaya kadar yaşam döngüsünün her noktasında, müşterinin siparişine taahhüt edilmiş toplu iş numaralarını görüntüleyebilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="3b57b-225">Belirli bir toplu işi rezerve etmeye ek olarak, bir kullanıcı sistemin otomatik olarak seçmesine izin vermek yerine toplu işin özel yerleşimini ve plakasını kendisi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="3b57b-226">Bu yetenek, sipariş taahhütlü toplu iş rezervasyon mekanizmasının tasarımıyla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="3b57b-227">Daha önce belirtildiği gibi, bir toplu iş numarası "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altındaki bir kalem için rezerve edildiği zaman, sistem yerleşime kadar olan tüm boyutları rezerve etmelidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="3b57b-228">Bu nedenle, ambar işi, siparişlerle çalışan kullanıcılar tarafından rezerve edilmiş olan aynı depolama boyutlarını taşır ve malzeme çekme operasyonları için uygun ve hatta olası olan kalem depolama yerleşimini temsil edemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="3b57b-229">Sipariş işlemciler ambar kısıtlamalarını biliyorsa, toplu iş rezerve ederken belirli yerleşimleri ve plakaları kendileri seçmek isteyebilirler.</span><span class="sxs-lookup"><span data-stu-id="3b57b-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="3b57b-230">Bu durumda , kullanıcının sayfa üst bilgisindeki **Boyutları görüntüle** işlevini kullanması, **Genel bakış** hızlı sekmesindeki kılavuza yerleşimi ve plakayı eklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="3b57b-231">**Toplu iş rezervasyonu** sayfasında toplu iş **B11** numaralı toplu işe ait satırı ve ardından **Satırı rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="3b57b-232">Otomatik rezervasyon sırasında yerleşimleri ve plakaları atamak için belirlenmiş bir mantık yoktur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="3b57b-233">Miktarı **Rezervasyon** alanına el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="3b57b-234">**Kaynak satırına taahhütlü toplu iş numaraları** hızlı sekmesinde, **B11** numaralı toplu işin **Taahhüt edilen** olarak gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Toplu iş rezervasyonu sayfasındaki bir satış siparişi satırı için belirli bir toplu iş numarasını taahhüt etme](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="3b57b-236">Bir satış siparişi satırındaki miktarın rezervasyonu çoklu toplu işler arasında yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="3b57b-237">Benzer şekilde, aynı toplu işin rezervasyonu birden çok yerleşime ve plakaya karşı yapılabilir (yerleşimler için plakalar etkinleştirilirse).</span><span class="sxs-lookup"><span data-stu-id="3b57b-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="3b57b-238">Bir satış siparişi satırındaki miktar için belirli bir toplu işin rezervasyonu kısmi de olabilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="3b57b-239">Örneğin, 100 birimlik toplam miktar, belirli bir toplu işe 20 birim taahhüt edilirken, uygun herhangi bir toplu işe tesis ve ambar düzeylerinde 80 birim rezerve edilecek şekilde rezerve edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="3b57b-240">Bu durumda, WMS malzeme çekme işlemlerini iki ayrı iş satırı kullanarak işler.</span><span class="sxs-lookup"><span data-stu-id="3b57b-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="3b57b-241">**Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="3b57b-242">Kaleminizi ve ardından **Stok yönetimi** \> **Görüntüle** \> **Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Bir stok hareketi türü olarak sipariş taahhütlü rezervasyon](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="3b57b-244">Kalemin, satış siparişi satırı rezervasyonuna ilişkin stok hareketlerini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="3b57b-245">**Referans** alanının **Satış siparişi** olarak ve **Çıkış** alanının **Fiziksel rezerve miktar** olarak ayarlandığı bir hareket, **Yerleşim** düzeyinin üzerindeki stok boyutları için sipariş satırı rezervasyonunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="3b57b-246">Kalemin stok rezervasyonu hiyerarşisine göre bu boyutlar tesis, ambar ve stok durumudur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="3b57b-247">**Referans** alanının **Sipariş taahhütlü rezervasyon** olarak ve **Çıkış** alanının **Fiziksel rezerve miktar** olarak ayarlandığı bir hareket, belirli toplu iş ve onun üzerindeki tüm stok boyutları için sipariş satırı rezervasyonunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="3b57b-248">Kalemin stok rezervasyonu hiyerarşisine göre bu boyutlar toplu iş numarası ve yerleşimidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="3b57b-249">Bu örnekte yerleşim **Bulk-001**'dir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="3b57b-250">Satış siparişi üst bilgisinde **Ambar** \> **Eylemler** \> **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="3b57b-251">Sipariş satırı artık dalgalıdır ve bir yük ve iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="3b57b-252">Sipariş taahhütlü toplu iş numaraları olan ambar işini inceleyin ve işleyin</span><span class="sxs-lookup"><span data-stu-id="3b57b-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="3b57b-253">**Satış siparişi satırları** hızlı sekmesinde **Ambar** \> **İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="3b57b-254">Satış siparişi satırına taahhüt edilen toplu iş miktarları için malzeme çekme işlemini işleyen iş aşağıdaki özelliklere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="3b57b-255">Sistem iş oluşturmak için, yerleşim yönergelerini değil sistem çalışma şablonlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="3b57b-256">Yeni işin oluşturulacağı zamanı belirlemek için, en fazla malzeme çekme satırı veya özel bir ölçü birimi gibi iş şablonları için tanımlanan tüm standart ayarlar uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="3b57b-257">Bununla birlikte, sipariş taahhütlü rezervasyon tüm stok boyutlarını zaten belirttiğinden, çekme yerleşimlerinin belirlenmesi ile ilgili yerleşim yönergeleriyle ilişkili kurallar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="3b57b-258">Bu stok boyutları, ambar depolama düzeyindeki boyutları içerir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="3b57b-259">Bu nedenle, iş, yerleşim yönergelerine danışmak zorunda kalmadan bu boyutları devralır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="3b57b-260">Toplu iş numarası, çekme satırında gösterilmez (ilişkili bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi olan bir kalem için oluşturulan iş satırında olduğu gibi). Bunun yerine, "ilk" toplu iş numarası ve tüm diğer depolama boyutları, ilişkili stok hareketlerinden referansta bulunulan iş satırı iş stok hareketinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Sipariş taahhütlü rezervasyondan kaynaklanan iş için ambar stok hareketi](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="3b57b-262">İş oluşturulduktan sonra, **Referans** alanının **Sipariş taahhütlü rezervasyon** olarak ayarlandığı kalem stok hareketi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="3b57b-263">**Referans** alanının **İş** olarak ayarlandığı stok hareketi, miktarın tüm stok boyutlarında fiziksel rezervasyonu tutar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="3b57b-264">Ambar operasyonları her zaman olduğu gibi işin yürütülmesini işlemeye devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="3b57b-265">Ancak, mobil cihazdaki yönergelerde çalışandan belirli bir toplu iş numarası seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="3b57b-266">Yerleşimlerin plaka denetimli olduğu ambar ortamlarında, bir çalışan birden fazla plakada aynı toplu işi depolayan bir yerleşime ulaştığında, henüz rezerve edilmemiş olan (örneğin başka bir sipariş taahhütlü rezervasyon veya o türde bir rezervasyondan kaynaklanan iş tarafından) herhangi bir plakayı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="3b57b-267">İş satırında belirtilen yerleşimden seçim yapılması pratik değilse, ambar operatörleri, belirli toplu işin çekilmesini daha uygun bir yerleşimden yeniden yönlendirmek için aşağıdaki eylemlerden birini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="3b57b-268">Bir mobil cihazdaki standart **Konumu geçersiz kıl** eylemi (ambar çalışanının **Çekme yerleşimini geçersiz kılmaya izin ver** ayarını etkinleştirmesi koşuluyla)</span><span class="sxs-lookup"><span data-stu-id="3b57b-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="3b57b-269">**Çalışma listesi ayrıntıları** sayfasında **Yerleşimi değiştir** eylemi.</span><span class="sxs-lookup"><span data-stu-id="3b57b-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="3b57b-270">Mobil cihazda, işi çekme ve yerleştirme işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="3b57b-271">Artık **B11** numaralı toplu iş için **10** miktarı artık satış siparişi satırı için çekilmiş ve **Baydoor** yerleşimine yerleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="3b57b-272">Bu noktada, miktar kamyona yüklenmeye ve müşterinin adresine gönderilmeye hazırdır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="3b57b-273">Esnek plaka rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="3b57b-274">İş senaryosu</span><span class="sxs-lookup"><span data-stu-id="3b57b-274">Business scenario</span></span>

<span data-ttu-id="3b57b-275">Bu senaryoda, bir şirket ambar yönetimi ve iş işlemeyi kullanır ve iş oluşturulmadan önce, yük planlamayı Supply Chain Management dışındaki bağımsız paletler/kapsayıcılar düzeyinde işler.</span><span class="sxs-lookup"><span data-stu-id="3b57b-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="3b57b-276">Bu kapsayıcılar, stok boyutlarında plakalarla temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="3b57b-277">Bu nedenle, bu yaklaşım için malzeme çekme işi yapılmadan önce belirli plakaların önceden satış siparişi satırlarına atanması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="3b57b-278">Şirket, plaka kuralları rezervasyonu kurallarının işlenme biçimi ile aşağıdaki davranışlar oluşmasını sağlayacak şekilde esneklik aramaktadır:</span><span class="sxs-lookup"><span data-stu-id="3b57b-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="3b57b-279">Bir plaka, satış işlemcisi tarafından sipariş alınırken kaydedilip rezerve edilebilir ve başka taleplerle alınamaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="3b57b-280">Bu davranış, planlanan plakanın müşteriye sevk edilmesini garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="3b57b-281">Plaka henüz bir satış siparişi satırına atanmamışsa, satış siparişi kaydı ve rezervasyon tamamlandıktan sonra, ambar personeli malzeme çekme işi sırasında bir plaka seçebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="3b57b-282">Esnek plaka rezervasyonunu etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3b57b-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="3b57b-283">Esnek plaka rezervasyonunu kullanabilmeniz için sisteminizde iki özelliğin etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="3b57b-284">Yöneticiler bu özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="3b57b-285">Özellikleri aşağıdaki sırada açmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="3b57b-286">**Özellik adı:** *Esnek ambar düzeyi boyut rezervasyonu*</span><span class="sxs-lookup"><span data-stu-id="3b57b-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="3b57b-287">**Özellik adı:** *Esnek sipariş taahhütlü plaka rezervasyonu*</span><span class="sxs-lookup"><span data-stu-id="3b57b-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="3b57b-288">Satış siparişi üzerinde belirli bir plakayı rezerve etme</span><span class="sxs-lookup"><span data-stu-id="3b57b-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="3b57b-289">Bir siparişte plaka rezervasyonunu etkinleştirmek için ilgili öğeyle ilişkilendirilmiş olan hiyerarşi için **Stok rezervasyonu hiyerarşileri** sayfasındaki **Plaka** düzeyi için **Talep üzerine rezervasyona izin ver** onay kutusunu işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Esnek plaka rezervasyon hiyerarşisi için stok rezervasyonu hiyerarşileri sayfası](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="3b57b-291">Plaka rezervasyonunu dağıtımınızdaki herhangi bir noktada, sipariş üzerinde etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="3b57b-292">Bu değişiklik, değişiklik yapılmadan önce oluşturulan rezervasyonları veya açık ambar işini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="3b57b-293">Ancak, bu rezervasyon hiyerarşisiyle ilişkili bir veya daha fazla kalem için *Siparişte*, *Siparişli rezerve miktar* veya *Fiziksel rezerve miktar* sorun durumuna sahip giden açık stok hareketleri varsa **Talep emrinde rezervasyona izin ver** onay kutusunun işareti kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="3b57b-294">**Plaka** düzeyinde **Talep emrinde rezervasyon izni ver** onay kutusu seçili olsa bile siparişte belirli bir plakanın rezerve edilmesi mümkün *değildir*.</span><span class="sxs-lookup"><span data-stu-id="3b57b-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="3b57b-295">Bu durumda, rezervasyon hiyerarşisi için geçerli olan varsayılan ambar operasyonları mantığı geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="3b57b-296">Belirli bir plakayı rezerve etmek için bir [Açık Veri Protokolü (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) işlemi kullanmanız gerekir. Uygulamada bu rezervasyonu doğrudan bir satış siparişinden, **Excel'de aç** komutunun **Lisans levhası başına sipariş taahhütlü rezervasyon sayısı** seçeneğini kullanarak yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="3b57b-297">Excel eklentilerinde açılan varlık verilerinde, aşağıdaki rezervasyon ile ilgili verileri girmeniz ve sonra verileri Supply Chain Management'a geri göndermek için **Yayımla**'yı seçmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="3b57b-298">Referans (Yalnızca *Satış siparişi* değeri desteklenir.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="3b57b-299">Sipariş numarası (Değer lotun içinden türetilebilir.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="3b57b-300">Lot kodu</span><span class="sxs-lookup"><span data-stu-id="3b57b-300">Lot ID</span></span>
- <span data-ttu-id="3b57b-301">Plaka</span><span class="sxs-lookup"><span data-stu-id="3b57b-301">License plate</span></span>
- <span data-ttu-id="3b57b-302">Miktar</span><span class="sxs-lookup"><span data-stu-id="3b57b-302">Quantity</span></span>

<span data-ttu-id="3b57b-303">Toplu olarak izlenen bir kalem için belirli bir plakayı rezerve etmeniz gerekiyorsa, [Satış siparişi ayrıntılarını girme](#sales-order-details) bölümünde açıklandığı şekilde **Toplu rezervasyon** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="3b57b-304">Sipariş taahhütlü bir plaka rezervasyonu kullanan satış siparişi satırı ambar operasyonları tarafından işlendiğinde, konum yönergeleri kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="3b57b-305">Ambar iş maddesi tam palete eşit ve plaka taahhütlü miktarlara sahip satırlardan oluşuyorsa, **Plakaya göre işle** seçeneği *Evet* olarak ayarlanmış bir mobil cihaz menü öğesini kullanarak malzeme çekme işlemini optimize edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="3b57b-306">Böylece bir ambar çalışanı, bir işe ait kalemleri tek tek taramak yerine, bir malzeme çekme işlemini tamamlamak için bir plakayı tarayabilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Plakaya göre işle seçeneğinin Evet olarak ayarlandığı mobil cihaz menü öğesi](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="3b57b-308">**Plakaya göre işle** işlevi, çoklu paletleri kapsayan işleri desteklemediğinden, farklı plakalar için ayrı bir iş maddesi olması daha iyidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="3b57b-309">Bu yaklaşımı kullanmak için **Sipariş taahhüttlü plaka kimliği** alanını **İş şablonu** sayfasında ,iş üst bilgisi sonu olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="3b57b-310">Siparişle taahhüt edilen iş oluşturma işlemi için, malzeme çekme işi satırlarına bir "siparişle taahhüt edilen stok boyutu" değeri atanacaktır ve plaka değerini doğrudan görüntülemek mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-310">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="3b57b-311">Mobil cihaz menü öğesi ayarlanırken yalnızca *Kullanıcı tarafından yönlendirilen* işlem desteklenir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-311">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="3b57b-312">Örnek senaryo: Sipariş taahhütlü plaka rezervasyonunu ayarlama ve işleme</span><span class="sxs-lookup"><span data-stu-id="3b57b-312">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="3b57b-313">Bu senaryoda sipariş taahhütlü plaka rezervasyonunun ayarlanması ve işlenmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-313">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="3b57b-314">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="3b57b-314">Make demo data available</span></span>

<span data-ttu-id="3b57b-315">Bu senaryo, Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerler ve kayıtlarla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-315">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="3b57b-316">Burada sunulan değerleri kullanarak bu senaryoyla çalışmak istiyorsanız demo verilerinin yüklenmiş olduğu bir ortamda çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-316">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="3b57b-317">Ek olarak, başlamadan önce tüzek kişiliği **USMF** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-317">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="3b57b-318">Plaka rezervasyonuna izin veren bir stok rezervasyonu hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3b57b-318">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="3b57b-319">**Ambar yönetimi \> Kurulum \> Stok \> Rezervasyon hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-319">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="3b57b-320">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-320">Select **New**.</span></span>
1. <span data-ttu-id="3b57b-321">**Ad** alanına bir değer girin (örneğin *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="3b57b-321">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="3b57b-322">**Açıklama** alanına bir değer girin (örneğin *Esnek LP rezervasyonu*).</span><span class="sxs-lookup"><span data-stu-id="3b57b-322">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="3b57b-323">**Seçili** listede **Toplu iş numarası**, **Seri numarası** ve **Sahip** seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-323">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="3b57b-324">Seçili kayıtları **Kullanılabilir** listesine taşımak için **Kaldır** düğmesini ![geri ok](media/backward-button.png) seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-324">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="3b57b-325">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-325">Select **OK**.</span></span>
1. <span data-ttu-id="3b57b-326">**Plaka** boyut düzeyinin satırında, **Talep emrinde rezervasyona izin ver** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-326">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="3b57b-327">**Konum** düzeyi otomatik olarak seçilir ve onay kutusunun işaretini kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="3b57b-327">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="3b57b-328">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-328">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="3b57b-329">Yayımlanan iki ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="3b57b-329">Create two released products</span></span>

1. <span data-ttu-id="3b57b-330">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-330">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="3b57b-331">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-331">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3b57b-332">**Yeni yayımlanan ürün** iletişim kutusunda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="3b57b-332">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3b57b-333">**Ürün numarası:** *Kalem1*</span><span class="sxs-lookup"><span data-stu-id="3b57b-333">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="3b57b-334">**Kalem numarası:** *Kalem1*</span><span class="sxs-lookup"><span data-stu-id="3b57b-334">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="3b57b-335">**Kalem modeli grubu:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="3b57b-335">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="3b57b-336">**Kalem grubu:** *Ses*</span><span class="sxs-lookup"><span data-stu-id="3b57b-336">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="3b57b-337">**Depolama boyutu grubu:** *Ambar*</span><span class="sxs-lookup"><span data-stu-id="3b57b-337">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="3b57b-338">**İzleme boyutu grubu:** *Yok*</span><span class="sxs-lookup"><span data-stu-id="3b57b-338">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="3b57b-339">**Rezervasyon hiyerarşisi:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="3b57b-339">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="3b57b-340">Ürün oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-340">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="3b57b-341">Yeni ürün açılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-341">The new product is opened.</span></span> <span data-ttu-id="3b57b-342">**Ambar** hızlı sekmesinde, **Birim sıra grubu kodu** alanını *beher* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-342">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="3b57b-343">Aynı ayarlara sahip ikinci bir ürün oluşturmak için önceki adımları yineleyin ancak **ürün numarası** ve **kalem numarası** alanlarını *Kalem2* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-343">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="3b57b-344">Eylem Bölmesinde, **Stoku yönet** sekmesindeki **Görünüm** grubunda, **Eldeki stoku**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-344">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="3b57b-345">Ardından **Miktar düzeltmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-345">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="3b57b-346">Yeni kalemlerin eldeki stokunu aşağıdaki tabloda belirtildiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-346">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="3b57b-347">Madde</span><span class="sxs-lookup"><span data-stu-id="3b57b-347">Item</span></span>  | <span data-ttu-id="3b57b-348">Ambar</span><span class="sxs-lookup"><span data-stu-id="3b57b-348">Warehouse</span></span> | <span data-ttu-id="3b57b-349">Yer</span><span class="sxs-lookup"><span data-stu-id="3b57b-349">Location</span></span> | <span data-ttu-id="3b57b-350">Plaka</span><span class="sxs-lookup"><span data-stu-id="3b57b-350">License plate</span></span> | <span data-ttu-id="3b57b-351">Miktar</span><span class="sxs-lookup"><span data-stu-id="3b57b-351">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="3b57b-352">Kalem1</span><span class="sxs-lookup"><span data-stu-id="3b57b-352">Item1</span></span> | <span data-ttu-id="3b57b-353">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-353">24</span></span>        | <span data-ttu-id="3b57b-354">FL-010</span><span class="sxs-lookup"><span data-stu-id="3b57b-354">FL-010</span></span>   | <span data-ttu-id="3b57b-355">LP01</span><span class="sxs-lookup"><span data-stu-id="3b57b-355">LP01</span></span>          | <span data-ttu-id="3b57b-356">10</span><span class="sxs-lookup"><span data-stu-id="3b57b-356">10</span></span>       |
    | <span data-ttu-id="3b57b-357">Kalem1</span><span class="sxs-lookup"><span data-stu-id="3b57b-357">Item1</span></span> | <span data-ttu-id="3b57b-358">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-358">24</span></span>        | <span data-ttu-id="3b57b-359">FL-011</span><span class="sxs-lookup"><span data-stu-id="3b57b-359">FL-011</span></span>   | <span data-ttu-id="3b57b-360">LP02</span><span class="sxs-lookup"><span data-stu-id="3b57b-360">LP02</span></span>          | <span data-ttu-id="3b57b-361">10</span><span class="sxs-lookup"><span data-stu-id="3b57b-361">10</span></span>       |
    | <span data-ttu-id="3b57b-362">Kalem2</span><span class="sxs-lookup"><span data-stu-id="3b57b-362">Item2</span></span> | <span data-ttu-id="3b57b-363">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-363">24</span></span>        | <span data-ttu-id="3b57b-364">FL-010</span><span class="sxs-lookup"><span data-stu-id="3b57b-364">FL-010</span></span>   | <span data-ttu-id="3b57b-365">LP01</span><span class="sxs-lookup"><span data-stu-id="3b57b-365">LP01</span></span>          | <span data-ttu-id="3b57b-366">5</span><span class="sxs-lookup"><span data-stu-id="3b57b-366">5</span></span>        |
    | <span data-ttu-id="3b57b-367">Kalem2</span><span class="sxs-lookup"><span data-stu-id="3b57b-367">Item2</span></span> | <span data-ttu-id="3b57b-368">24</span><span class="sxs-lookup"><span data-stu-id="3b57b-368">24</span></span>        | <span data-ttu-id="3b57b-369">FL-011</span><span class="sxs-lookup"><span data-stu-id="3b57b-369">FL-011</span></span>   | <span data-ttu-id="3b57b-370">LP02</span><span class="sxs-lookup"><span data-stu-id="3b57b-370">LP02</span></span>          | <span data-ttu-id="3b57b-371">5</span><span class="sxs-lookup"><span data-stu-id="3b57b-371">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="3b57b-372">İki plaka oluşturmanız ve *FL-010* ile *FL-011* gibi karışık kalemlere izin veren konumları kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-372">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="3b57b-373">Satış siparişi oluşturma ve belirli bir plakayı rezerve etme</span><span class="sxs-lookup"><span data-stu-id="3b57b-373">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="3b57b-374">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-374">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3b57b-375">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-375">Select **New**.</span></span>
1. <span data-ttu-id="3b57b-376">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="3b57b-376">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3b57b-377">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3b57b-377">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3b57b-378">**Ambar:** *24*</span><span class="sxs-lookup"><span data-stu-id="3b57b-378">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="3b57b-379">**Satış siparişi oluştur** iletişim kutusunu kapatmak ve yeni satış siparişini açmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-379">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="3b57b-380">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="3b57b-380">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="3b57b-381">**Kalem numarası:** *Kalem1*</span><span class="sxs-lookup"><span data-stu-id="3b57b-381">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="3b57b-382">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="3b57b-382">**Quantity:** *10*</span></span>

1. <span data-ttu-id="3b57b-383">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="3b57b-383">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="3b57b-384">**Kalem numarası:** *Kalem2*</span><span class="sxs-lookup"><span data-stu-id="3b57b-384">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="3b57b-385">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="3b57b-385">**Quantity:** *5*</span></span>

1. <span data-ttu-id="3b57b-386">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-386">Select **Save**.</span></span>
1. <span data-ttu-id="3b57b-387">**Satır ayrıntıları** hızlı sekmesinde, **Kurulum** sekmesinde her satırın **Lot kodu** değerini not edin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-387">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="3b57b-388">Bu değerler, belirli plakaların rezervasyonu sırasında gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-388">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b57b-389">Belirli bir plakayı rezerve etmek için **Plaka başına sipariş taahhütlü rezervasyon sayısı** veri varlığını kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-389">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="3b57b-390">Belirli bir plakada toplu olarak izlenen bir kalemi izlemek için [Satış siparişi ayrıntılarını girme](#sales-order-details) bölümünde açıklandığı şekilde **Toplu rezervasyon** sayfasını da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-390">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="3b57b-391">Plakayı doğrudan satış siparişi satırına girip sistemde onayladıysanız, ambar yönetimi işlemi satır için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-391">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="3b57b-392">**Microsoft Office'te Aç**'ı ve ardından **Plaka başına sipariş taahhütlü rezervasyon sayısı**'nı seçip dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-392">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="3b57b-393">İndirilen dosyayı Excel'de açın ve **Düzenlemeyi etkinleştir**'i seçerek Excel eklentisini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-393">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="3b57b-394">Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-394">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="3b57b-395">Oturum açmanız istendiğinde **Oturum aç**'ı seçin ve ardından Supply Chain Management'ta oturum açmak için kullandığınız kimlik bilgilerini kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-395">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="3b57b-396">Belirli bir plakada bir kalemi rezerve etmek için Excel eklentisinde **Yeni**'yi seçerek rezervasyon satırı ekleyin ve sonra aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="3b57b-396">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="3b57b-397">**Lot Kodu:** *Kalem1* için satış siparişi satırına yönelik bulduğunuz **Lot Kodu** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-397">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="3b57b-398">**Plaka:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="3b57b-398">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="3b57b-399">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="3b57b-399">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="3b57b-400">**Yeni**'yi seçerek başka bir rezervasyon satırı daha ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="3b57b-400">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="3b57b-401">**Lot Kodu:** *Kalem2* için satış siparişi satırına yönelik bulduğunuz **Lot Kodu** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-401">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="3b57b-402">**Plaka:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="3b57b-402">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="3b57b-403">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="3b57b-403">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="3b57b-404">Verileri Supply Chain Management'a geri göndermek için Excel eklentisinde **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-404">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b57b-405">Rezervasyon satırı yalnızca, yayımlanma hatasız olarak tamamlanırsa sistemde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-405">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="3b57b-406">Supply Chain Management'a geri dönün.</span><span class="sxs-lookup"><span data-stu-id="3b57b-406">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="3b57b-407">Kalemin rezervasyonunu gözden geçirmek için **Satış siparişi satırları** hızlı sekmesinde, **Stok** menüsünde **Koru \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-407">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="3b57b-408">*Kalem1* satış siparişi satırı için *10* stok rezerve edildiğine ve *Kalem2* satış siparişi satırı için ise *5* stok rezerve edildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-408">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="3b57b-409">Satış siparişi satırı rezervasyonuna ilişkin stok hareketlerini gözden geçirmek için **Satış siparişi satırları** hızlı sekmesinde, **Stok** menüsünde **Görüntüle \> Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-409">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="3b57b-410">Rezervasyonla ilgili iki hareket olduğuna dikkat edin: **Referans** alanının *Satış Siparişi* olarak ayarlandığı yer ve **Referans** alanının *Sipariş taahhütlü rezervasyon* olarak ayarlandığı yer.</span><span class="sxs-lookup"><span data-stu-id="3b57b-410">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b57b-411">**Referans** alanının *Satış siparişi* olarak ayarlandığı bir hareket, **Konum** düzeyinin üzerindeki stok boyutları (tesis, ambar ve stok durumu) için sipariş satırı rezervasyonunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-411">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="3b57b-412">**Referans** alanının *Sipariş taahhütlü rezervasyon* olarak ayarlandığı bir hareket, belirli bir plaka ve konum için sipariş satırı rezervasyonunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-412">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="3b57b-413">Satış siparişini serbest bırakmak için Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-413">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="3b57b-414">Sipariş taahhütlü plaka atanmış ambar işini gözden geçirme ve işleme</span><span class="sxs-lookup"><span data-stu-id="3b57b-414">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="3b57b-415">**Satış siparişi satırları** hızlı sekmesinde, **Ambar** menüsünde **İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-415">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="3b57b-416">Belirli bir toplu iş için rezervasyon yapıldığında, sistem, plaka rezervasyonunu kullanan satış siparişi için işi oluşturduğunda konum yönergelerini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-416">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="3b57b-417">Sipariş taahhütlü rezervasyon, konum da dahil olmak üzere tüm stok boyutlarını belirttiğinden, bu stok boyutları işe girilmiş olduğu için konum yönergelerinin kullanılması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-417">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="3b57b-418">Bunlar **İş stok hareketleri** sayfasındaki **Stok boyutlarından** bölümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-418">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b57b-419">İş oluşturulduktan sonra, **Referans** alanının *Sipariş taahhütlü rezervasyon* olarak ayarlandığı kalem stok hareketi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-419">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="3b57b-420">**Referans** alanının *İş* olarak ayarlandığı stok hareketi, miktarın tüm stok boyutlarında fiziksel rezervasyonu tutar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-420">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="3b57b-421">Mobil cihazda, **Plakaya göre işle** onay kutusunun seçili olduğu bir menü öğesi kullanarak işi çekmeyi ve yerleştirmeyi tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-421">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b57b-422">**Plakaya göre işle** işlevi, tüm plakayı işlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-422">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="3b57b-423">Plakanın bir kısmını işlemeniz gerekiyorsa bu işlevi kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3b57b-423">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="3b57b-424">Her plaka için oluşturulmuş ayrı işinizin olmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-424">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="3b57b-425">Bu sonuca ulaşmak için **İş şablonu** sayfasındaki **İş üst bilgisi sonları** özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-425">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="3b57b-426">*LP02* plakası, satış siparişi satırları için alınır ve *Baydoor* konumuna yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-426">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="3b57b-427">Bu noktada, yüklenmeye ve müşteriye gönderilmeye hazırdır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-427">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="3b57b-428">Sipariş taahhütlü toplu iş numaraları olan ambar işinin özel durumunu işleme</span><span class="sxs-lookup"><span data-stu-id="3b57b-428">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="3b57b-429">Sipariş taahhütlü toplu iş numaralarını toplama için yapılan ambar işi, normal işle aynı standart ambar özel durum işlemeye tabidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-429">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="3b57b-430">Genel olarak, açık iş veya iş satırı iptal edilebilir, bir kullanıcı yerleşimi dolu olduğu için durdurulabilir ve bir hareket nedeniyle güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-430">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="3b57b-431">Benzer şekilde, zaten tamamlanmış olan çekilmiş iş miktarı azaltılabilir veya işe ters işlem uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-431">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="3b57b-432">Tüm bu özel durum işleme eylemlerine şu temel kural uygulanır: Müşteri için rezerve edilen parti numarası başka bir toplu iş numarasıyla değiştirilemez ancak depolama boyutları (yerleşim ve plaka) bir kullanıcının el ile yapacağı güncelleştirmeyle ya da sistemin otomatik güncelleştirmesiyle değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-432">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="3b57b-433">Otomatik güncelleştirme, belirli bir toplu iş otomatik olarak rezerve edildiği ama depolama boyutları belirlenmediği zaman uygulanan aynı rastgele depolama boyutları atamasına dayanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-433">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="3b57b-434">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="3b57b-434">Example scenario</span></span>

<span data-ttu-id="3b57b-435">Bu senaryoya bir örnek, önceden tamamlanan işin seçiminin **Çekilen miktarı düş** işleviyle iptal edildiği durumdur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-435">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="3b57b-436">Bu örnekte, [Örnek senaryo: Toplu iş numarası tahsisatı](#Example-batch-allocation) konusunda açıklanan adımları zaten tamamladığınız varsayılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-436">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="3b57b-437">Bu örnekten devam edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-437">It continues from that example.</span></span>

1. <span data-ttu-id="3b57b-438">**Ambar yönetimi** \> **Yükler** \> **Etkin yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-438">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="3b57b-439">Satış siparişinin sevkiyatı ile bağlantılı olarak oluşturulan yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-439">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="3b57b-440">**Yük emri satırları** hızlı sekmesinden, **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-440">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="3b57b-441">**Çekilen miktarı düş** sayfasındaki **Yerleşime taşı** alanında **FL-001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-441">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="3b57b-442">**Plakaya taşı** alanında **LP33**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-442">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="3b57b-443">Kılavuzdaki **Çekme işlemi geri alınacak stok miktarı** alanına **10** girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-443">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="3b57b-444">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-444">Select **OK**.</span></span>

<span data-ttu-id="3b57b-445">Çekme işlemini geri alma eyleminin sonuçları:</span><span class="sxs-lookup"><span data-stu-id="3b57b-445">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="3b57b-446">Daha önce kapatılan işin durumu **İptal edildi** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-446">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="3b57b-447">**B11** numaralı toplu işte çekme işlemi iptal edilen **10** miktarı için **Stok hareketi** türünde yeni iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-447">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="3b57b-448">Bu iş, **Baydoor** yerleşiminden **FL-001** yerleşimindeki **LP33** numaralı plakaya hareketi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3b57b-448">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="3b57b-449">Durum ayarı **Kapalı** yapılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-449">The status is set to **Closed**.</span></span>
- <span data-ttu-id="3b57b-450">Sistem, başlangıçta sipariş edilen toplu iş numarasını yeniden rezerve edip yerleşim ve plaka kodlarının atamasını yapar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-450">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="3b57b-451">(Bu işlem, belirli bir toplu iş numarasına yönelik olarak sipariş satırı için **Satırı rezerve et** işlevini çalıştırmaya eşdeğerdir.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-451">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="3b57b-452">Sonuç olarak **B11** numaralı toplu iş, **Toplu iş rezervasyonu** sayfasının **Kaynak satırına taahhütlü toplu iş numaraları** hızlı sekmesinde Taahhüt edildi olarak gösterilir ve **Rezervasyon** alanında **B11** numaralı toplu iş için **10** miktarı yer alır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-452">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="3b57b-453">Ek olarak, **Yerleşim** alanı ayarı **FL-001**, **Plaka** alanı ayarı **LP11** olur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-453">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="3b57b-454">(Bu alanlar görünmüyorsa, kılavuza ekleyebilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-454">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="3b57b-455">Aşağıdaki tablolarda, sistemin belirli ambar eylemleri için sipariş taahhütlü toplu iş rezervasyonunu nasıl işleyeceğine ilişkin genel bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-455">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="3b57b-456">Tablolardaki içeriği yorumlamak için, her ambar eyleminin, sipariş taahhütlü bir toplu iş rezervasyonundan kaynaklanan mevcut ambar işi bağlamında çalıştırıldığını veya her ambar eyleminin bu türdeki işi etkilediğini varsayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-456">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="3b57b-457">Bu tablolarda "Toplu iş miktarı kullanılabilir" sütunu, mevcut sipariş taahhütlü rezervasyonlar için zaten rezerve edilmiş veya o türdeki rezervasyonlardan kaynaklanan ambar işi tarafından önceden rezerve edilmiş miktara ek olarak bir toplu iş miktarının kullanılabilir olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-457">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="3b57b-458">Açık işte çekme yerleşimini geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="3b57b-458">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-459">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-459">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-460">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-460">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-461">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-461">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-462">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-462">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-463">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-463">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-464"><strong>Çekme yerleşimini geçersiz kılmaya izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-464">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="3b57b-465">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-465">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-466">Malzeme çekme işini başlatırken ambarlama uygulamasında <strong>Konumu geçersiz kıl</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-466">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="3b57b-467"><strong>Öner</strong>'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-467">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="3b57b-468">Toplu iş miktarı kullanılabilirliğine dayalı olarak önerilen yeni yerleşimi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-468">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-469">Geçerli işte aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-469">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="3b57b-470">Çekme satırındaki yerleşim yeni yerleşime güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-470">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="3b57b-471">(Yerleşim plaka denetimliyse, iş stok hareketine rastgele bir plaka atanır ve çalışan, kullanılabilir miktarlı herhangi bir plakadan çekme işlemi yapabilir.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-471">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="3b57b-472">Miktar yeni yerleşimde birden fazla plakada bulunursa, orijinal çekme satırı her bir plakayla eşleştirilmek üzere birden çok satıra bölünür.</span><span class="sxs-lookup"><span data-stu-id="3b57b-472">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-473">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="3b57b-473">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-474">No</span><span class="sxs-lookup"><span data-stu-id="3b57b-474">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-475">Malzeme çekme işini başlatırken ambarlama uygulamasında <strong>Konumu geçersiz kıl</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-475">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="3b57b-476">El ile bir yerleşim girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-476">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-477"><strong>Konumu geçersiz kıl</strong> eylemi mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-477">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="3b57b-478">Başarısız olur ve bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-478">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="3b57b-479">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-479">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="3b57b-480">Tam düğme – Kullanıcı yerleşimindeki taşma nedeniyle bir iş satırını bölün</span><span class="sxs-lookup"><span data-stu-id="3b57b-480">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-481">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-481">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-482">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-482">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-483">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-483">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-484">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-484">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-485">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-485">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3b57b-486">Mobil cihaz menü öğesinde <strong>İşin bölünmesine izin ver</strong> seçeneği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-486">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="3b57b-487">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="3b57b-487">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-488">Malzeme çekme işini işlerken ambarlama uygulamasındaki <strong>Tam</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-488">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="3b57b-489"><strong>Çekme Miktarı</strong> alanında, tam kapasiteyi belirtmek için gereken kısmi bir çekme miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-489">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="3b57b-490">Geçerli işte, miktar, çekilmesi gereken kalan miktara güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-490">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="3b57b-491">Çekilen miktar için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-491">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="3b57b-492">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-492">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="3b57b-493">Tamamlanan işin çekilen miktarını bir yükten düşme</span><span class="sxs-lookup"><span data-stu-id="3b57b-493">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-494">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-494">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-495">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-495">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-496">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-496">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-497">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-497">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-498">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-498">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-499">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-499">Not applicable</span></span></td>
<td><span data-ttu-id="3b57b-500">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-500">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-501">Yük satırından <strong>Çekilen miktarı düş</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-501">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="3b57b-502">Çekme işlemi iptal edilecek tam miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-502">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="3b57b-503">Bir "taşıma" yerleşimi/plakası seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-503">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="3b57b-504">Yük satırıyla ilişkili iş iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-504">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="3b57b-505">Stok hareketi için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-505">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-506">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-506">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-507">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-507">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-508">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-508">No</span></span></td>
<td><span data-ttu-id="3b57b-509">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-509">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-510">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-510">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-511">Miktar; aynı toplu iş için ve çekme işlemi iptal sırasında girilen aynı yerleşim ve plaka (yerleşim plaka denetimliyse) için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-511">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="3b57b-512">Ambar içinde bir kalemi taşıma</span><span class="sxs-lookup"><span data-stu-id="3b57b-512">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="3b57b-513">Bu ambar eylemi şablonla hareket için değil, yalnızca **İş oluşturma işlemi** türündeki hareket için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-513">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-514">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-514">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-515">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-515">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-516">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-516">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-517">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-517">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-518">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-518">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-519"><strong>Stoğun ilişkili işle birlikte taşınmasına izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-519">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="3b57b-520">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-520">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-521">Ambarlama uygulamasında bir hareket başlatın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-521">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="3b57b-522">"Çıkış" ve "hedef" yerleşimlerini girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-522">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="3b57b-523">Taşımadan etkilenen mevcut tüm işte çekme yerleşimi yeni "hedef" yerleşime güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-523">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="3b57b-524">Stok hareketi için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-524">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-525">Belirtilen yerleşimden miktar hareketinden etkilenen mevcut tüm rezervasyonlar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-525">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-526">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-526">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-527">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-527">No</span></span></td>
<td><span data-ttu-id="3b57b-528">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-528">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-529">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-529">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-530">Belirtilen yerleşimden miktar hareketinden etkilenen tüm mevcut rezervasyonlar aynı toplu iş için ve yeni "hedef" yerleşim ve plaka (yerleşim plaka denetimliyse) için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="3b57b-531">Tamamlanan işin çekilen miktarını bir yükten veya dalgadan geri alma</span><span class="sxs-lookup"><span data-stu-id="3b57b-531">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-532">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-532">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-533">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-533">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-534">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-534">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-535">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-535">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-536">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-536">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="3b57b-537">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-537">Not applicable</span></span></td>
<td><span data-ttu-id="3b57b-538">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-538">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-539"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-539">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="3b57b-540">İstek sayfasında <strong>Maddeleri geçerli konumda bırak</strong>seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-540">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-541">Yükle ilişkili tüm iş iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-541">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="3b57b-542">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-542">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-543">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-543">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-544">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-544">No</span></span></td>
<td><span data-ttu-id="3b57b-545">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-545">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-546">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-546">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-547">Miktar, aynı toplu iş için ve miktarın geri almaya bırakıldığı yerleşim ve plaka için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-547">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-548">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-548">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-549"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-549">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="3b57b-550">İstek sayfasında <strong>Maddeleri bu konuma ata</strong>seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-550">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="3b57b-551">Geçerli iş iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-551">The current work is canceled.</span></span></li>
<li><span data-ttu-id="3b57b-552">Stok hareketi için yeni iş oluşturulur ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-552">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-553">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-553">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-554">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-554">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-555">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-555">No</span></span></td>
<td><span data-ttu-id="3b57b-556">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-556">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-557">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-557">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-558">Miktar, aynı toplu iş için ve miktarın geri alma işlemine atandığı yerleşim ve plaka için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-558">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-559">Evet/Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-559">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-560"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-560">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="3b57b-561">İstek sayfasında <strong>Maddeleri bu konuma taşı</strong>seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-561">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-562">Ters işlem desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-562">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="3b57b-563">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-563">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-564">Evet/Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-565"><strong>İşi geri al</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="3b57b-566">İstek sayfasında <strong>Maddeleri konum yönergelerine göre taşı</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-566">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-567">Ters işlem desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-567">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="3b57b-568">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-568">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="3b57b-569">Miktarı eksik seçme – Siz malzeme çekme işini gerçekleştirirken, miktarın kaydını yerleşimde/plakada fiziksel olarak bulunamadı şeklinde yapın</span><span class="sxs-lookup"><span data-stu-id="3b57b-569">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-570">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-570">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-571">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-571">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-572">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-572">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-573">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-573">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-574">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-574">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-575"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Yok</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b57b-575">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="3b57b-576">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-576">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-577">Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-577">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="3b57b-578"><strong>Malzeme çekme miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-578">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="3b57b-579"><strong>Neden</strong> alanına <strong>Yeniden tahsis yok</strong> girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-579">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="3b57b-580">Geçerli iş kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="3b57b-580">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="3b57b-581">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-581">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-582">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-582">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-583">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-583">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-584">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-584">No</span></span></td>
<td><span data-ttu-id="3b57b-585">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-585">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3b57b-586">Eksik malzeme çekme eylemi başarısız olur ve bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-586">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="3b57b-587">Geçerli iş açık kalır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-587">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-588">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-588">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-589"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Yok</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b57b-589">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="3b57b-590">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-590">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-591">Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-591">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="3b57b-592"><strong>Malzeme çekme miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-592">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="3b57b-593"><strong>Neden</strong> alanına <strong>Yeniden tahsis yok</strong> girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-593">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="3b57b-594">Geçerli iş kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="3b57b-594">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="3b57b-595">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-595">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-596">Eksik çekilen yerleşimde miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-596">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-597">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-597">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-598">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-598">No</span></span></td>
<td><span data-ttu-id="3b57b-599">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-599">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-600">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-600">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-601">Eksik çekilen yerleşimde miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-602"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır/Evet</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b57b-602">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="3b57b-603">Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-603">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="3b57b-604">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-604">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-605">Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-605">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="3b57b-606"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-606">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="3b57b-607"><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-607">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="3b57b-608">Listede yerleşimi/plakayı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-608">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="3b57b-609">Geçerli işte aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-609">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="3b57b-610">Çekme satırı kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="3b57b-610">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="3b57b-611">Yerine koyma satırı iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-611">The put line is canceled.</span></span></li>
<li><span data-ttu-id="3b57b-612">Yeni bir çekme satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-612">A new pick line is created.</span></span> <span data-ttu-id="3b57b-613">Satır, kullanıcının seçtiği yerleşimi/plakayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-613">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="3b57b-614">Yeni bir yerine koyma satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-614">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3b57b-615">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-615">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-616">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-616">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-617"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b57b-617">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="3b57b-618">Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-618">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="3b57b-619">No</span><span class="sxs-lookup"><span data-stu-id="3b57b-619">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-620">Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-620">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="3b57b-621"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-621">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="3b57b-622"><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-622">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-623">Eksik malzeme çekme eylemi başarısız olur ve bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-623">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="3b57b-624">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3b57b-624">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-625"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b57b-625">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="3b57b-626">Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-626">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="3b57b-627">No</span><span class="sxs-lookup"><span data-stu-id="3b57b-627">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-628">Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-628">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="3b57b-629"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-629">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="3b57b-630"><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-630">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="3b57b-631">Listede yerleşimi/plakayı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-631">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="3b57b-632">Geçerli işte aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="3b57b-632">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="3b57b-633">Çekme satırı kapalı ve çekilen miktar 0 (sıfır).</span><span class="sxs-lookup"><span data-stu-id="3b57b-633">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="3b57b-634">Yerine koyma satırı iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-634">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3b57b-635">Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-635">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="3b57b-636">Eksik çekilen yerleşimde/plakada miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-636">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-637"><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Otomatik</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet/Hayır</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet/Hayır</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b57b-637">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="3b57b-638">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="3b57b-638">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-639">Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-639">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="3b57b-640"><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-640">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="3b57b-641"><strong>Neden</strong> alanında <strong>Otomatik tahsisatla kısa malzeme çekme</strong>'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-641">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-642">Otomatik yeniden tahsisat içeren eksik çekme desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-642">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="3b57b-643">Otomatik yeniden tahsisat içeren eksik çekme desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-643">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="3b57b-644">Stok durumunu değiştir</span><span class="sxs-lookup"><span data-stu-id="3b57b-644">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="3b57b-645">Bu ambar eylemi birden fazla giriş noktasından gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-645">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="3b57b-646">Burada gösterilen örnek, **Konuma göre eldeki** sayfasında **Stok durumu değişikliği** eylemini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-646">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3b57b-647">Temel kurulum parametresi</span><span class="sxs-lookup"><span data-stu-id="3b57b-647">Key setup parameter</span></span></th>
<th><span data-ttu-id="3b57b-648">Toplu iş miktarı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="3b57b-648">Batch quantity is available</span></span></th>
<th><span data-ttu-id="3b57b-649">Temel kullanıcı adımları</span><span class="sxs-lookup"><span data-stu-id="3b57b-649">Key user steps</span></span></th>
<th><span data-ttu-id="3b57b-650">Ambar işi</span><span class="sxs-lookup"><span data-stu-id="3b57b-650">Warehouse work</span></span></th>
<th><span data-ttu-id="3b57b-651">Sipariş taahhütlü toplu iş rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="3b57b-651">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-652"><strong>Ambar</strong> sekmesindeki <strong>Ambar</strong> kaydında, <strong>Rezervasyonları ve işaretleri kaldır</strong> alanının ayarı <strong>Rezervasyonlar</strong> veya <strong>İşaretler ve rezervasyonlar</strong> yapılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-652">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="3b57b-653">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-653">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-654">Belirli bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-654">Select a specific location.</span></span></li>
<li><span data-ttu-id="3b57b-655">Belirli bir kalem, yerleşim ve plakası (yerleşim plaka denetimliyse) olan bir satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-655">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="3b57b-656"><strong>Stok durumu değişikliği</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-656">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="3b57b-657"><strong>Stok durumu</strong> alanının ayarını <strong>Durdurma</strong> yapın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-657">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-658">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-658">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3b57b-659">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-659">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-660">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-660">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="3b57b-661">Stok durumu boyutundaki değişikliği temsil için <strong>Stok durumu değişikliği</strong> türünde iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-661">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="3b57b-662">Durdurulan miktarın rezervasyonunu temsil için <strong>Stok durdurma</strong> türünde ve <strong>Fiziksel rezerve miktar</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-662">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-663">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-663">No</span></span></td>
<td><span data-ttu-id="3b57b-664">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-664">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-665">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-665">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="3b57b-666">Rezervasyon kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-666">The reservation is removed.</span></span></li>
<li><span data-ttu-id="3b57b-667">Stok durumu boyutundaki değişikliği temsil için <strong>Stok durumu değişikliği</strong> türünde iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-667">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="3b57b-668">Durdurulan miktarın rezervasyonunu temsil için <strong>Stok durdurma</strong> türünde ve <strong>Fiziksel rezerve miktar</strong> çıkış türünde bir stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3b57b-668">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="3b57b-669"><strong>Ambar</strong> sekmesindeki <strong>Ambar</strong> kaydında, <strong>Rezervasyonları ve işaretleri kaldır</strong> alanının ayarı <strong>Yok</strong> yapılır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-669">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="3b57b-670">Evet</span><span class="sxs-lookup"><span data-stu-id="3b57b-670">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="3b57b-671">Belirli bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-671">Select a specific location.</span></span></li>
<li><span data-ttu-id="3b57b-672">Belirli bir kalem, yerleşim ve plakası (yerleşim plaka denetimliyse) olan bir satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-672">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="3b57b-673"><strong>Stok durumu değişikliği</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-673">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="3b57b-674"><strong>Stok durumu</strong> alanının ayarını <strong>Durdurma</strong> yapın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-674">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="3b57b-675">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-675">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="3b57b-676">Miktar aynı toplu iş için yeniden rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-676">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="3b57b-677">Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</span><span class="sxs-lookup"><span data-stu-id="3b57b-677">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b57b-678">Hayır</span><span class="sxs-lookup"><span data-stu-id="3b57b-678">No</span></span></td>
<td><span data-ttu-id="3b57b-679">Önceki satıra bakın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-679">See the previous row.</span></span></td>
<td><span data-ttu-id="3b57b-680">İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="3b57b-681">Stok durumu değişikliklerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="3b57b-681">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="3b57b-682">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="3b57b-682">Limitations</span></span>

- <span data-ttu-id="3b57b-683">Esnek ambar düzeyinde boyut rezervasyonu işlevi aşağıdaki özellikleri desteklemez:</span><span class="sxs-lookup"><span data-stu-id="3b57b-683">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="3b57b-684">Fiili ağırlık yönetimi</span><span class="sxs-lookup"><span data-stu-id="3b57b-684">Catch weight management</span></span>
    - <span data-ttu-id="3b57b-685">Fiziksel negatif stok</span><span class="sxs-lookup"><span data-stu-id="3b57b-685">Physical negative inventory</span></span>
    - <span data-ttu-id="3b57b-686">Sipariş edilen tedarikte rezervasyon</span><span class="sxs-lookup"><span data-stu-id="3b57b-686">Reservation against ordered supply</span></span>
    - <span data-ttu-id="3b57b-687">Transfer emirleri ve hammadde çekme</span><span class="sxs-lookup"><span data-stu-id="3b57b-687">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="3b57b-688">Yönerge birimine göre ambalajlama için konteyner konsolidasyon kuralında sınırlamalar vardır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-688">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="3b57b-689">Sipariş taahhütlü rezervasyonlar için, **Yönerge birimine gör ambalajla** alanının etkinleştirildiği konteyner yapı şablonlarını kullanmamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-689">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="3b57b-690">Geçerli tasarımda, ambar işi oluşturulurken yerleşim yönergeleri kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-690">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="3b57b-691">Bu nedenle, konteyner kullanımı dalga adımı sırasında yalnızca birim sıra grubundaki en küçük birim uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-691">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
