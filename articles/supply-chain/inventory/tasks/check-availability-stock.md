---
title: "Stok uygunluğu denetleme"
description: "Bu prosedürde size belirli bir madde numarası için eldeki ve fiziksel stoğun nasıl kontrol edileceği gösterilmektedir."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 74eaa59db44e21b3ddfae38d28f84712959cc40e
ms.contentlocale: tr-tr
ms.lasthandoff: 01/17/2018

---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="099d1-103">Stok uygunluğu denetleme</span><span class="sxs-lookup"><span data-stu-id="099d1-103">Check the availability of stock</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="099d1-104">Bu prosedürde size belirli bir madde numarası için eldeki ve fiziksel stoğun nasıl kontrol edileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="099d1-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="099d1-105">Ayrıca, bir maddeyle ilgili tedarik bilgilerinin nasıl alınacağı da gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="099d1-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="099d1-106">Eldeki fiziksel stok, eldeki mevcut, yani satın alınmış, teslim alınmış ve kaydedilmiş stoktur.</span><span class="sxs-lookup"><span data-stu-id="099d1-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="099d1-107">Eldeki stok, eldeki mevcut stoğun yanı sıra, sipariş edilip beklenen ve henüz teslim alınıp kaydedilmemiş stoğu da içerir.</span><span class="sxs-lookup"><span data-stu-id="099d1-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="099d1-108">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="099d1-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="099d1-109">USMF kullanıyorsanız, gösterilen örnek değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="099d1-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="099d1-110">Bu görevler genellikle bir ambar çalışanı tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="099d1-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="099d1-111">Eldeki stokta bir maddeyi kontrol edin</span><span class="sxs-lookup"><span data-stu-id="099d1-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="099d1-112">Stok yönetimi > Sorgular ve raporlar > Eldeki stok öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="099d1-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="099d1-113">Madde numarası satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="099d1-113">Select the Item number row.</span></span>
    * <span data-ttu-id="099d1-114">Eldeki stoğu madde numarasına göre sorgulamak için, Tablo ayarının Eldeki stok ve Alan ayarının Madde numarası olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="099d1-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="099d1-115">Ölçütler alanında, sorgulamak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="099d1-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="099d1-116">USMF demo verileri şirketini kullanıyorsanız "M9201" seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="099d1-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="099d1-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-117">Click OK.</span></span>
5. <span data-ttu-id="099d1-118">Boyutlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-118">Click Dimensions.</span></span>
    * <span data-ttu-id="099d1-119">Boyutlar sekmesi, eldeki stoğunuz hakkında ne kadar ayrıntı görmek istediğinizi seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="099d1-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="099d1-120">Rezervasyonla ilgili verilere gereksiniminiz varsa, gelişmiş ambar (WHS) işlemlerini kullanan maddeler için tüm stok boyutlarını görüntülemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="099d1-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="099d1-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-121">Click OK.</span></span>
7. <span data-ttu-id="099d1-122">Eylem Bölmesinde, İlgili bilgiler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="099d1-123">Bunu görmüyorsanız, ek eylem bölmesi seçeneklerini görmek için üç nokta düğmesine (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="099d1-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="099d1-124">Tedarik özeti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-124">Click Supply overview.</span></span>
    * <span data-ttu-id="099d1-125">Tedarik özeti sekmesinde, belirli bir maddenin eldeki miktar, sağlama süresi ve satıcı bilgileri gibi tedarik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="099d1-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="099d1-126">Eldeki bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="099d1-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="099d1-127">Satıcılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="099d1-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="099d1-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="099d1-128">Close the page.</span></span>
12. <span data-ttu-id="099d1-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="099d1-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="099d1-130">Eldeki fiziksel stoğu kontrol edin</span><span class="sxs-lookup"><span data-stu-id="099d1-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="099d1-131">Ambar yönetimi > Sorgular ve raporlar > Eldeki fiziksel stok öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="099d1-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="099d1-132">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="099d1-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="099d1-133">Maddeler listesini filtre etmek için Tesis ve Ambar alanlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="099d1-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="099d1-134">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="099d1-134">Refresh the page.</span></span>
4. <span data-ttu-id="099d1-135">Boyutları Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="099d1-136">Boyutların Görünümü sekmesi, eldeki stoğunuz hakkında ne kadar ayrıntı görmek istediğinizi seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="099d1-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="099d1-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-137">Click OK.</span></span>
6. <span data-ttu-id="099d1-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="099d1-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="099d1-139">Eldeki stoğu yerleşime göre kontrol edin</span><span class="sxs-lookup"><span data-stu-id="099d1-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="099d1-140">Ambar yönetimi > Sorgular ve raporlar > Yerleşime göre eldeki öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="099d1-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="099d1-141">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="099d1-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="099d1-142">USMF demo veri şirketini kullanıyorsanız, "51" kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="099d1-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="099d1-143">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="099d1-143">Refresh the page.</span></span>
4. <span data-ttu-id="099d1-144">Boyutları Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="099d1-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="099d1-145">Click OK.</span></span>
6. <span data-ttu-id="099d1-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="099d1-146">Close the page.</span></span>

