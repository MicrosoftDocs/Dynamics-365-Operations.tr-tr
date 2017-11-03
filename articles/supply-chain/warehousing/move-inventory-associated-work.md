---
title: "Ambar yönetiminde stoğu ilişkili işle birlikte taşıma"
description: "Bu konu bir mobil cihazdan parça çekme onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b330d6aa8e972d3c35bb7783ec0a39f09775011
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="55c26-103">Ambar yönetiminde stoğu ilişkili işle birlikte taşıma</span><span class="sxs-lookup"><span data-stu-id="55c26-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="55c26-104">Stok hareketini kullanarak, hangi ambar çalışanlarının rezerve edilmiş stoku taşımaya izni olduklarına karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55c26-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="55c26-105">Bu, bir çalışanın halihazırda oluşturulmuş olan bir çekme işi için yeni bir çekme konumu seçmesine izin vermemeyi seçtiğiniz, düzenlenmiş ambarlarda esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="55c26-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="55c26-106">Ayrıca, ambar yöneticilerinin, daha az deneyimli çalışanların hangi yeterliklere sahip olması gerektiğini kontrol etmesine yardım eder.</span><span class="sxs-lookup"><span data-stu-id="55c26-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="55c26-107">Ambar çalışanlarının günlük faaliyetlerini yönetme esnekliği, şu gibi senaryolarda yararlı olabilir:</span><span class="sxs-lookup"><span data-stu-id="55c26-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="55c26-108">Senaryo 1</span><span class="sxs-lookup"><span data-stu-id="55c26-108">Scenario 1</span></span>
<span data-ttu-id="55c26-109">Bir şirket, nispeten küçük bir alma bölgesine sahiptir ve bu alan, yerine koyulmayı bekleyen kutular ve paletlerle doludur.</span><span class="sxs-lookup"><span data-stu-id="55c26-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="55c26-110">Geçerli gün içerisinde büyük bir sevkiyat beklenmektedir, bu yüzden de alma işinden sorumlu çalışanın, alma alanını bazı paletleri ikincil giriş hazırlama alanına taşıyarak yer açması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="55c26-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="55c26-111">Senaryo 2</span><span class="sxs-lookup"><span data-stu-id="55c26-111">Scenario 2</span></span>
<span data-ttu-id="55c26-112">Deneyimli bir ambar çalışanı, maddeleri az miktarda yakında bulunan 3 farklı alana bölmektense, tek bir konumda birleştirme fırsatını fark eder.</span><span class="sxs-lookup"><span data-stu-id="55c26-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="55c26-113">Çalışan, miktarı bu konumların her birinden aynı konuma ve aynı plakaya taşıyarak birleştirmek istemektedir.</span><span class="sxs-lookup"><span data-stu-id="55c26-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="55c26-114">Senaryo 3</span><span class="sxs-lookup"><span data-stu-id="55c26-114">Scenario 3</span></span>
<span data-ttu-id="55c26-115">Palet, hazırlama konumunda sevkiyatı beklemektedir; BAYDOOR01 yakınında bulunan STAGE01 gibi.</span><span class="sxs-lookup"><span data-stu-id="55c26-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="55c26-116">Ancak, plandaki değişiklik sebebiyle, kamyonun BAYDOOR04'e varması planlanır.</span><span class="sxs-lookup"><span data-stu-id="55c26-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="55c26-117">Sevk memuru bunun farkındadır ve kamyonun STAGE01 üzerinden yüklenmek için beklemesinden emin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="55c26-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="55c26-118">Sevk memuru, sevkiyattaki maddeleri, STAGE01'den yeni hedefe daha yakın olan STAGE04'e taşımaya karar verir.</span><span class="sxs-lookup"><span data-stu-id="55c26-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="55c26-119">Geçerli sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="55c26-119">Current limitations</span></span>

<span data-ttu-id="55c26-120">Taşıyabileceğiniz iş rezervasyonları, satış siparişiyle, Transfer emri çıkışı, Transfer emri alış irsaliyesi, Satınalma siparişi ve Stok yenileme işi ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="55c26-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="55c26-121">İş satırlarının bölünmesini önlemek için maddelerin taşınması kısıtlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55c26-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="55c26-122">Bu, Loc1 konumundaki A maddesinin 100 adetini içeren bir iş satırına sahipseniz, yalnızca 30 maddeyi A konumundan başka bir konuma taşıyamayacağınız anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="55c26-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="55c26-123">Bu, konumların farklı olmasından dolayı mevcut iş satırının 30 ve 70 şeklinde parçalanmasına yol açar.</span><span class="sxs-lookup"><span data-stu-id="55c26-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="55c26-124">Maddeleri aldığınız plakanın, maddeleri taşıdığınız plakadan farklı olduğu, bir iş siparişi için Hedef LP olarak ayarlandığı hazırlama senaryoları için, Hedef LP'nin bölünmemesi için yalnızca tüm LP'nin taşınmasına izin verilir.</span><span class="sxs-lookup"><span data-stu-id="55c26-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="55c26-125">Şu anda yalnızca geçici hareket desteklenir.</span><span class="sxs-lookup"><span data-stu-id="55c26-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="55c26-126">Bu da, rezerve edilmiş stoku, şablona göre taşıma mobil cihaz menü öğeleri aracılığıyla taşıyamayacağınız anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="55c26-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="55c26-127">Tek tek çalışanlar için rezerve stoku taşıma izni ayarlayın</span><span class="sxs-lookup"><span data-stu-id="55c26-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="55c26-128">Rezerve edilmiş stoku taşımasına izin verilecek çalışan için **İlişkilendirilen iş ile stok taşınmasına izin ver** onay kutusunu **Ambar yönetimi** > **Kurulum** > **Çalışan** içerisinden seçin.</span><span class="sxs-lookup"><span data-stu-id="55c26-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="55c26-129">Backported</span><span class="sxs-lookup"><span data-stu-id="55c26-129">Backported</span></span>

<span data-ttu-id="55c26-130">Bu özellik Microsoft Dynamics AX 2012 R3'e geri aktarılmıştır ve CU12'nin parçası olarak kullanılabilecektir.</span><span class="sxs-lookup"><span data-stu-id="55c26-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="55c26-131">KB numarası 3192548 ile tek olarak da indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="55c26-131">It can also be downloaded individually through KB number 3192548.</span></span> 

