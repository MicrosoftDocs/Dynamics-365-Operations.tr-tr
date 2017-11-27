--- 
title: "Maddeler için kapsam kurallarını tanımlama"
description: "Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: fe92393cc264df68f084db6974f7d4607d37d3ab
ms.contentlocale: tr-tr
ms.lasthandoff: 11/02/2017

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="99b2f-103">Maddeler için kapsam kurallarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="99b2f-103">Define coverage rules for items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99b2f-104">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="99b2f-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="99b2f-105">Bu yordam, kapsam kurallarını oluşturmayı ve belirli bir madde için kapsama ayarlarını geçersiz kılmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="99b2f-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="99b2f-106">Ayrıca varsayılan stok ayarlarının nasıl belirleneceğini de açıklar.</span><span class="sxs-lookup"><span data-stu-id="99b2f-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="99b2f-107">Bir kapsam grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="99b2f-107">Create a coverage group</span></span>
1. <span data-ttu-id="99b2f-108">Kapsam gruplarına gidin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="99b2f-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-109">Click New.</span></span>
3. <span data-ttu-id="99b2f-110">Kapsam grubu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="99b2f-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="99b2f-112">Takvim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="99b2f-113">Nazım planlamanın bu gruptaki maddelerin stok yenilemesi önerilerini oluşturmak için kullandığı takvimi seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="99b2f-114">Kapsam kodu alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="99b2f-115">Bu yordam için gereksinimi seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="99b2f-116">Kapsam zaman dilimi (gün) alanına '90' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="99b2f-117">Bu gruptaki maddeler için, master planlama gelecek en fazla 90 gün için stok yenileme önerileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99b2f-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="99b2f-118">Negatif günler alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="99b2f-119">Pozitif günler alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="99b2f-120">Diğer bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="99b2f-121">Gereksinim tarihine eklenen giriş marjı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="99b2f-122">Örneğin giriş marjı bir gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir giriş için bir satın alma siparişi satırı planlanırsa, nazım planlama ayarlanan giriş tarihini 16 mayıs olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="99b2f-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="99b2f-123">Gereksinim tarihinden kesilen çıkış marjı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="99b2f-124">Örneğin emniyet marjı 1 gün olarak ayarlanırsa ve 15 mayıs tarihindeki bir teslimat için bir satış siparişi satırı planlanırsa, nazım planlama ayarlanan teslim tarihini 14 mayıs olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="99b2f-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="99b2f-125">Madde sağlama süresine eklenen sipariş yenileme sınırı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="99b2f-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="99b2f-127">Yeni bir ürün oluştur</span><span class="sxs-lookup"><span data-stu-id="99b2f-127">Create a new product</span></span>
1. <span data-ttu-id="99b2f-128">Serbest bırakılan ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-128">Go to Released products.</span></span>
2. <span data-ttu-id="99b2f-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-129">Click New.</span></span>
3. <span data-ttu-id="99b2f-130">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="99b2f-131">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="99b2f-132">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="99b2f-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="99b2f-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="99b2f-135">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="99b2f-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="99b2f-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="99b2f-138">Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="99b2f-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="99b2f-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="99b2f-141">İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="99b2f-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="99b2f-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="99b2f-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="99b2f-145">Varsayılan sipariş ayarlarını yapma</span><span class="sxs-lookup"><span data-stu-id="99b2f-145">Setup default order settings</span></span>
1. <span data-ttu-id="99b2f-146">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="99b2f-147">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-147">Click Default order settings.</span></span>
3. <span data-ttu-id="99b2f-148">Satınalma tesisi alanına, satınalma siparişleri oluşturulurken varsayılan olarak kullanılan tesisi yazın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="99b2f-149">Stok sahası alanına, maddenin depolandığı sahayı yazın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="99b2f-150">Stok bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="99b2f-151">Birden çok ayarını '10' olarak belirleyin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="99b2f-152">Min.</span><span class="sxs-lookup"><span data-stu-id="99b2f-152">Set Min.</span></span> <span data-ttu-id="99b2f-153">sipariş miktarını '10' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="99b2f-154">Maks.</span><span class="sxs-lookup"><span data-stu-id="99b2f-154">Set Max.</span></span> <span data-ttu-id="99b2f-155">sipariş miktarını '100' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="99b2f-156">Standart sipariş miktarını '10' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="99b2f-157">Satınalma sağlama süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="99b2f-158">Çalışma günleri onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="99b2f-159">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-159">Click Save.</span></span>
13. <span data-ttu-id="99b2f-160">Varsayılan sipariş türü alanında 'Satınalma siparişi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="99b2f-161">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-161">Click Save.</span></span>
15. <span data-ttu-id="99b2f-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-162">Close the page.</span></span>
    * <span data-ttu-id="99b2f-163">Varsayılan sipariş ayarları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="99b2f-164">Kapsama grubuna bir madde ekleme</span><span class="sxs-lookup"><span data-stu-id="99b2f-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="99b2f-165">Plan bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="99b2f-166">Kapsam grup alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="99b2f-167">Listede, oluşturduğunuz Kapsam grubunu bulun.</span><span class="sxs-lookup"><span data-stu-id="99b2f-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="99b2f-168">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="99b2f-169">Madde kapsama kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="99b2f-169">Create item coverage rules</span></span>
1. <span data-ttu-id="99b2f-170">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="99b2f-171">Madde kapsamı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-171">Click Item coverage.</span></span>
3. <span data-ttu-id="99b2f-172">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-172">Click New.</span></span>
4. <span data-ttu-id="99b2f-173">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-173">Click the General tab.</span></span>
5. <span data-ttu-id="99b2f-174">Karşılama grubu ayarlarını geçersiz kılma başlığı kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="99b2f-175">Kapsam zaman dilimi (gün) alanına '60' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="99b2f-176">Gereklilik grubu kapsamındaki maddeler 90 gün önceden planlanmasına rağmen, bu madde 60 gün önceden planlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="99b2f-176">Although items in coverage group Requirement are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="99b2f-177">Negatif günler alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="99b2f-178">Pozitif günler alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="99b2f-179">Sağlama süresi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="99b2f-180">Satın alma başlığındaki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="99b2f-181">Satınalma zamanı alanına '5' girin.</span><span class="sxs-lookup"><span data-stu-id="99b2f-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="99b2f-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b2f-182">Click Save.</span></span>


