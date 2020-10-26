---
title: Maddeler için kapsam kurallarını tanımlama
description: Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3974992"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="4edb8-103">Maddeler için kapsam kurallarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="4edb8-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4edb8-104">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="4edb8-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4edb8-105">Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="4edb8-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="4edb8-106">Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.</span><span class="sxs-lookup"><span data-stu-id="4edb8-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="4edb8-107">Bir kapsam grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="4edb8-107">Create a coverage group</span></span>
1. <span data-ttu-id="4edb8-108">**Gezinti bölmesi > Modüller > Master planlama > Kurulum > Kapsam grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="4edb8-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-109">Click **New**.</span></span>
3. <span data-ttu-id="4edb8-110">**Kapsam grubu** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="4edb8-111">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="4edb8-112">**Takvim** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="4edb8-113">Nazım planlamanın bu gruptaki maddelerin stok yenilemesi önerilerini oluşturmak için kullandığı takvimi seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="4edb8-114">**Kapsam kodu** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="4edb8-115">Bu yordam için 'Gereksinim'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="4edb8-116">**Kapsam zaman dilimi (gün) alanı**'na '90' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="4edb8-117">Bu gruptaki maddeler için, master planlama gelecek en fazla 90 gün için stok yenileme önerileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4edb8-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="4edb8-118">**Negatif günler** alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="4edb8-119">**Pozitif günler** alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="4edb8-120">**Diğer** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="4edb8-121">**Gün sayısı olarak emniyet marjları** bölümünde, **Gereksinim tarihine eklenen giriş marjı** alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="4edb8-122">Örneğin giriş marjı bir gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir giriş için bir satın alma siparişi satırı planlanırsa, nazım planlama ayarlanan giriş tarihini 16 mayıs olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="4edb8-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="4edb8-123">**Gereksinim tarihinden kesilen çıkış marjı** alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="4edb8-124">Örneğin emniyet marjı 1 gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir teslimat için bir satış siparişi satırı planlanırsa, nazım planlama ayarlanan teslim tarihini 14 mayıs olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="4edb8-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="4edb8-125">**Madde sağlama süresine eklenen sipariş yenileme sınırı** alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="4edb8-126">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="4edb8-127">Yeni ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="4edb8-127">Create a new product</span></span>
1. <span data-ttu-id="4edb8-128">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="4edb8-129">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-129">Click **New**.</span></span>
3. <span data-ttu-id="4edb8-130">**Ürün numarası** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="4edb8-131">**Ürün adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="4edb8-132">**Madde modeli grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4edb8-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4edb8-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4edb8-135">**Madde modeli** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4edb8-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4edb8-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4edb8-138">**Depolama boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4edb8-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="4edb8-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4edb8-141">**İzleme boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4edb8-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="4edb8-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="4edb8-144">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="4edb8-145">Varsayılan sipariş ayarlarını yapma</span><span class="sxs-lookup"><span data-stu-id="4edb8-145">Setup default order settings</span></span>
1. <span data-ttu-id="4edb8-146">**Eylem Bölmesi**'nde **Plan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="4edb8-147">**Sipariş ayarları**'nın altında, **Varsayılan sipariş ayarları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="4edb8-148">**Satınalma siparişi**'nin altında, **Varsayılan site** alanında satınalma siparişleri oluşturulurken varsayılan olarak kullanılan tesisi yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="4edb8-149">**Varsayılan ambar** alanına, maddenin depolandığı sahayı yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="4edb8-150">**Stok** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="4edb8-151">**Çoklu** alanına '10' yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="4edb8-152">**Minimum sipariş miktarı** alanına '10' yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="4edb8-153">**Maksimum sipariş miktarı** alanına '100' yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="4edb8-154">**Standart sipariş miktarı** alanına '10' yazın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="4edb8-155">**Satınalma sağlama süresi** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="4edb8-156">**Çalışma günleri** onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="4edb8-157">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-157">Click **Save**.</span></span>
13. <span data-ttu-id="4edb8-158">**Varsayılan sipariş türü** alanında 'Satınalma siparişi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="4edb8-159">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-159">Click **Save**.</span></span>
15. <span data-ttu-id="4edb8-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-160">Close the page.</span></span> <span data-ttu-id="4edb8-161">Varsayılan sipariş ayarları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="4edb8-162">Kapsama grubuna bir madde ekleme</span><span class="sxs-lookup"><span data-stu-id="4edb8-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="4edb8-163">**Plan** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="4edb8-164">**Kapsam grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4edb8-165">Listede, oluşturduğunuz **Kapsam grubu**'nu bulun.</span><span class="sxs-lookup"><span data-stu-id="4edb8-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="4edb8-166">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="4edb8-167">Madde kapsama kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="4edb8-167">Create item coverage rules</span></span>
1. <span data-ttu-id="4edb8-168">**Eylem Bölmesi**'nde **Plan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="4edb8-169">**Kapsam**altında, **Madde karşılama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="4edb8-170">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-170">Click **New**.</span></span>
4. <span data-ttu-id="4edb8-171">**Genel** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="4edb8-172">**Karşılama grubu** ayarlarını geçersiz kılma başlığı kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="4edb8-173">**Kapsam zaman dilimi (gün)** alanına '60' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="4edb8-174">Gereklilik grubu kapsamındaki maddeler 90 gün önceden planlanmasına rağmen, bu madde 60 gün önceden planlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="4edb8-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="4edb8-175">**Negatif günler** alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="4edb8-176">**Pozitif günler** alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="4edb8-177">**Sağlama süresi** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="4edb8-178">**Satınalma** başlığındaki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="4edb8-179">**Satınalma zamanı** alanına '5' girin.</span><span class="sxs-lookup"><span data-stu-id="4edb8-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="4edb8-180">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4edb8-180">Click **Save**.</span></span>

