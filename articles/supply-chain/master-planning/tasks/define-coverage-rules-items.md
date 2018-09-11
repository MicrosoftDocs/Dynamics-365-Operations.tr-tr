--- 
title: "Maddeler için kapsam kurallarını tanımlama"
description: "Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 56b0135816e4e3b91a0a1fb986a0dff4e2bc38d7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="ca54a-103">Maddeler için kapsam kurallarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="ca54a-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca54a-104">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ca54a-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ca54a-105">Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca54a-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="ca54a-106">Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.</span><span class="sxs-lookup"><span data-stu-id="ca54a-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="ca54a-107">Bir kapsam grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca54a-107">Create a coverage group</span></span>
1. <span data-ttu-id="ca54a-108">Kapsam gruplarına gidin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="ca54a-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-109">Click New.</span></span>
3. <span data-ttu-id="ca54a-110">Kapsam grubu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="ca54a-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ca54a-112">Takvim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="ca54a-113">Nazım planlamanın bu gruptaki maddelerin stok yenilemesi önerilerini oluşturmak için kullandığı takvimi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="ca54a-114">Kapsam kodu alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="ca54a-115">Bu yordam için gereksinimi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="ca54a-116">Kapsam zaman dilimi (gün) alanına '90' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="ca54a-117">Bu gruptaki maddeler için, master planlama gelecek en fazla 90 gün için stok yenileme önerileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca54a-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="ca54a-118">Negatif günler alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="ca54a-119">Pozitif günler alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="ca54a-120">Diğer bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="ca54a-121">Gereksinim tarihine eklenen giriş marjı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="ca54a-122">Örneğin giriş marjı bir gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir giriş için bir satın alma siparişi satırı planlanırsa, nazım planlama ayarlanan giriş tarihini 16 mayıs olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="ca54a-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="ca54a-123">Gereksinim tarihinden kesilen çıkış marjı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="ca54a-124">Örneğin emniyet marjı 1 gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir teslimat için bir satış siparişi satırı planlanırsa, nazım planlama ayarlanan teslim tarihini 14 mayıs olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="ca54a-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="ca54a-125">Madde sağlama süresine eklenen sipariş yenileme sınırı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="ca54a-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="ca54a-127">Yeni bir ürün oluştur</span><span class="sxs-lookup"><span data-stu-id="ca54a-127">Create a new product</span></span>
1. <span data-ttu-id="ca54a-128">Serbest bırakılan ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-128">Go to Released products.</span></span>
2. <span data-ttu-id="ca54a-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-129">Click New.</span></span>
3. <span data-ttu-id="ca54a-130">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="ca54a-131">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="ca54a-132">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ca54a-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ca54a-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ca54a-135">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ca54a-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ca54a-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ca54a-138">Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ca54a-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="ca54a-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ca54a-141">İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ca54a-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ca54a-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="ca54a-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="ca54a-145">Varsayılan sipariş ayarlarını yapma</span><span class="sxs-lookup"><span data-stu-id="ca54a-145">Setup default order settings</span></span>
1. <span data-ttu-id="ca54a-146">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="ca54a-147">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-147">Click Default order settings.</span></span>
3. <span data-ttu-id="ca54a-148">Satınalma tesisi alanına, satınalma siparişleri oluşturulurken varsayılan olarak kullanılan tesisi yazın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="ca54a-149">Stok sahası alanına, maddenin depolandığı sahayı yazın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="ca54a-150">Stok bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="ca54a-151">Birden çok ayarını '10' olarak belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="ca54a-152">Min.</span><span class="sxs-lookup"><span data-stu-id="ca54a-152">Set Min.</span></span> <span data-ttu-id="ca54a-153">sipariş miktarını '10' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="ca54a-154">Maks.</span><span class="sxs-lookup"><span data-stu-id="ca54a-154">Set Max.</span></span> <span data-ttu-id="ca54a-155">sipariş miktarını '100' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="ca54a-156">Standart sipariş miktarını '10' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="ca54a-157">Satınalma sağlama süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="ca54a-158">Çalışma günleri onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="ca54a-159">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-159">Click Save.</span></span>
13. <span data-ttu-id="ca54a-160">Varsayılan sipariş türü alanında 'Satınalma siparişi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="ca54a-161">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-161">Click Save.</span></span>
15. <span data-ttu-id="ca54a-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-162">Close the page.</span></span>
    * <span data-ttu-id="ca54a-163">Varsayılan sipariş ayarları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="ca54a-164">Kapsama grubuna bir madde ekleme</span><span class="sxs-lookup"><span data-stu-id="ca54a-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="ca54a-165">Plan bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="ca54a-166">Kapsam grup alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ca54a-167">Listede, oluşturduğunuz Kapsam grubunu bulun.</span><span class="sxs-lookup"><span data-stu-id="ca54a-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="ca54a-168">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="ca54a-169">Madde kapsama kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca54a-169">Create item coverage rules</span></span>
1. <span data-ttu-id="ca54a-170">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="ca54a-171">Madde kapsamı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-171">Click Item coverage.</span></span>
3. <span data-ttu-id="ca54a-172">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-172">Click New.</span></span>
4. <span data-ttu-id="ca54a-173">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-173">Click the General tab.</span></span>
5. <span data-ttu-id="ca54a-174">Karşılama grubu ayarlarını geçersiz kılma başlığı kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="ca54a-175">Kapsam zaman dilimi (gün) alanına '60' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="ca54a-176">Gereklilik grubu kapsamındaki maddeler 90 gün önceden planlanmasına rağmen, bu madde 60 gün önceden planlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="ca54a-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="ca54a-177">Negatif günler alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="ca54a-178">Pozitif günler alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="ca54a-179">Sağlama süresi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="ca54a-180">Satın alma başlığındaki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="ca54a-181">Satınalma zamanı alanına '5' girin.</span><span class="sxs-lookup"><span data-stu-id="ca54a-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="ca54a-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca54a-182">Click Save.</span></span>


