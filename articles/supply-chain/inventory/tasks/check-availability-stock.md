---
title: Stok uygunluğu denetleme
description: Bu prosedürde size belirli bir madde numarası için eldeki ve fiziksel stoğun nasıl kontrol edileceği gösterilmektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0c00b2a79ab588ff47c249f73570544d884b79e
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995269"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="75105-103">Stok uygunluğu denetleme</span><span class="sxs-lookup"><span data-stu-id="75105-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75105-104">Bu prosedürde size belirli bir madde numarası için eldeki ve fiziksel stoğun nasıl kontrol edileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="75105-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="75105-105">Ayrıca, bir maddeyle ilgili tedarik bilgilerinin nasıl alınacağı da gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="75105-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="75105-106">Eldeki fiziksel stok, eldeki mevcut, yani satın alınmış, teslim alınmış ve kaydedilmiş stoktur.</span><span class="sxs-lookup"><span data-stu-id="75105-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="75105-107">Eldeki stok, eldeki mevcut stoğun yanı sıra, sipariş edilip beklenen ve henüz teslim alınıp kaydedilmemiş stoğu da içerir.</span><span class="sxs-lookup"><span data-stu-id="75105-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="75105-108">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75105-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="75105-109">USMF kullanıyorsanız, gösterilen örnek değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75105-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="75105-110">Bu görevler genellikle bir ambar çalışanı tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="75105-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="75105-111">Eldeki stokta bir maddeyi kontrol edin</span><span class="sxs-lookup"><span data-stu-id="75105-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="75105-112">**Gezinti bölmesi > Modüller > Stok yönetimi > Sorgular ve raporlar > Eldeki stok** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="75105-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="75105-113">**Madde numarası** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="75105-113">Select the **Item number** row.</span></span> <span data-ttu-id="75105-114">Eldeki stoğu madde numarasına göre sorgulamak için, Tablo ayarının **Eldeki stok** ve Alan ayarının **Madde** numarası olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="75105-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="75105-115">**Ölçütler**  alanında, sorgulamak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="75105-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="75105-116">USMF demo verileri şirketini kullanıyorsanız "M9201" seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75105-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="75105-117">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-117">Click **OK**.</span></span>
5. <span data-ttu-id="75105-118">**Eylem bölmesinde** **Boyutlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-118">On the **Action pane**, click **Dimensions**.</span></span> <span data-ttu-id="75105-119">**Boyutlar** sekmesi, eldeki stoğunuz hakkında ne kadar ayrıntı görmek istediğinizi seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="75105-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="75105-120">Rezervasyonla ilgili verilere gereksiniminiz varsa, gelişmiş ambar (WHS) işlemlerini kullanan maddeler için tüm stok boyutlarını görüntülemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="75105-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>
6. <span data-ttu-id="75105-121">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-121">Click **OK**.</span></span>
7. <span data-ttu-id="75105-122">**Eylem Bölmesinde**, **İlgili bilgiler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="75105-123">Bu seçeneği görmüyorsanız, ek eylem bölmesi seçeneklerini görmek için üç nokta düğmesine (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="75105-123">If you don’t see this option, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>
8. <span data-ttu-id="75105-124">**Tedarik özeti**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-124">Click **Supply overview**.</span></span> <span data-ttu-id="75105-125">**Tedarik özeti** sekmesinde, belirli bir maddenin eldeki miktar, sağlama süresi ve satıcı bilgileri gibi tedarik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="75105-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="75105-126">**Eldeki** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="75105-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="75105-127">**Satıcılar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="75105-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="75105-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="75105-128">Close the page.</span></span>
12. <span data-ttu-id="75105-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="75105-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="75105-130">Eldeki fiziksel stoğu kontrol edin</span><span class="sxs-lookup"><span data-stu-id="75105-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="75105-131">**Gezinti bölmesi > Modüller > Ambar yönetimi > Sorgular ve raporlar > Fiziksel eldeki stok** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="75105-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="75105-132">**Madde numarası** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="75105-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="75105-133">Maddeler listesini filtre etmek için Tesis ve Ambar alanlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75105-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="75105-134">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="75105-134">Refresh the page.</span></span>
4. <span data-ttu-id="75105-135">**Eylem bölmesinde** **Boyutları Görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-135">On the **Action pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="75105-136">Boyutların Görünümü sekmesi, eldeki stoğunuz hakkında ne kadar ayrıntı görmek istediğinizi seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="75105-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="75105-137">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-137">Click **OK**.</span></span>
6. <span data-ttu-id="75105-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="75105-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="75105-139">Eldeki stoğu yerleşime göre kontrol edin</span><span class="sxs-lookup"><span data-stu-id="75105-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="75105-140">**Gezinti bölmesi > Modüller > Ambar yönetimi > Sorgular ve raporlar > Yerleşime göre eldeki** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="75105-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="75105-141">**Ambar** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="75105-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="75105-142">USMF demo veri şirketini kullanıyorsanız, "51" kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75105-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="75105-143">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="75105-143">Refresh the page.</span></span>
4. <span data-ttu-id="75105-144">**Boyutları Görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="75105-145">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="75105-145">Click **OK**.</span></span>
6. <span data-ttu-id="75105-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="75105-146">Close the page.</span></span>

