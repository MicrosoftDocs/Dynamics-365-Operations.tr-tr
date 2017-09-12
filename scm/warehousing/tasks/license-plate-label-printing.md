--- 
title: "Plaka etiketi yazdırmayı etkinleştirme"
description: "Bu yordam, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="48508-103">Plaka etiketi yazdırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="48508-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48508-104">Bu yordam, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="48508-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="48508-105">Bu yordamı USMF demo veri şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="48508-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="48508-106">Kendi verilerinizi kullanarak çalıştırırsanız, lisans plakaları için ayarlanmış bir numara seriniz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="48508-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="48508-107">Bu göreve başlamadan önce bir etiket yazdırıcı kurulumu yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="48508-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="48508-108">Organizasyon yönetimi > Kurulum > Ağ yazıcıları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="48508-109">Eylem bölmesinde, Seçenekler'e ve ardından Belge rota aracısı yükleyicisini indir düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="48508-110">Yükleyiciyi çalıştırın ve yordama devam etmeden önce Etkin olarak ayarlanmış çalışır durumda bir ağ yazıcınız olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="48508-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="48508-111">GS1 şirket önekini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="48508-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="48508-112">Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="48508-113">GS1 şirket öneki alanına, GS1 şirket numaranız için 7 sayı girin.</span><span class="sxs-lookup"><span data-stu-id="48508-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="48508-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-114">Click Save.</span></span>
4. <span data-ttu-id="48508-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="48508-116">SSCC lisans plaka numarası serisini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="48508-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="48508-117">(Kuruluş yönetim > Numara serileri > Numara serileri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="48508-118">Alan alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="48508-119">Referans alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="48508-120">Şirket alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="48508-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="48508-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="48508-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="48508-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="48508-123">Segmentler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="48508-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="48508-124">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-124">Click Edit.</span></span>
9. <span data-ttu-id="48508-125">Segment tablosunda ilk satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="48508-126">Kaldır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-126">Click Remove.</span></span>
11. <span data-ttu-id="48508-127">Kaldır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-127">Click Remove.</span></span>
12. <span data-ttu-id="48508-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-128">Click Save.</span></span>
13. <span data-ttu-id="48508-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="48508-130">Belge yönlendirme düzenini oluşturun</span><span class="sxs-lookup"><span data-stu-id="48508-130">Create the document route layout</span></span>
1. <span data-ttu-id="48508-131">Ambar yönetimi > Kurulum > Belge rotası > Belge rotası düzenleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="48508-132">SSCC düzenini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="48508-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="48508-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-133">Click New.</span></span>
3. <span data-ttu-id="48508-134">Düzen kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="48508-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="48508-135">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="48508-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="48508-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="48508-137">Metnin sonuna ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="48508-138">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-138">Click Save.</span></span>
8. <span data-ttu-id="48508-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="48508-140">Belge yönlendirmeyi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="48508-140">Set up the document routing</span></span>
1. <span data-ttu-id="48508-141">Ambar yönetimi > Kurulum > Belge rotası > Belge rotası öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="48508-142">İş siparişi türü alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="48508-143">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48508-143">Click New.</span></span>
4. <span data-ttu-id="48508-144">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="48508-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="48508-145">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="48508-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="48508-146">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48508-146">Click New.</span></span>
7. <span data-ttu-id="48508-147">Düzen kodu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="48508-148">Ad alanında kullanmak istediğiniz yazıcı adını girin.</span><span class="sxs-lookup"><span data-stu-id="48508-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="48508-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-149">Click Save.</span></span>
10. <span data-ttu-id="48508-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="48508-151">Mobil cihaz menüsü oluşturun</span><span class="sxs-lookup"><span data-stu-id="48508-151">Create mobile device menu</span></span>
1. <span data-ttu-id="48508-152">Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="48508-153">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-153">Click New.</span></span>
3. <span data-ttu-id="48508-154">Menü öğesi adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="48508-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="48508-155">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="48508-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="48508-156">Mod alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="48508-157">Mevcut işi kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="48508-158">Lisans plakası oluştur alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="48508-159">İş sınıfları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="48508-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="48508-160">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-160">Click New.</span></span>
10. <span data-ttu-id="48508-161">İş sınıfı kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="48508-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="48508-162">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-162">Click Save.</span></span>
12. <span data-ttu-id="48508-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-163">Close the page.</span></span>
13. <span data-ttu-id="48508-164">Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="48508-165">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="48508-166">Ağaçta, 'Ağaçta, daha önce oluşturduğunuz menü öğesini seçin' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="48508-167">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48508-167">Click Edit.</span></span>
17. <span data-ttu-id="48508-168">Menüye menü öğesi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="48508-169">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-169">Click Save.</span></span>
19. <span data-ttu-id="48508-170">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="48508-171">İş şablonu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="48508-171">Update a work template</span></span>
1. <span data-ttu-id="48508-172">Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="48508-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="48508-173">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="48508-174">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-174">Click Edit.</span></span>
4. <span data-ttu-id="48508-175">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48508-175">Click New.</span></span>
5. <span data-ttu-id="48508-176">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="48508-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="48508-177">İş türü alanında 'Yazdır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="48508-178">İş sınıfı kodu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="48508-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="48508-179">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="48508-180">Yukarı taşı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-180">Click Move up.</span></span>
10. <span data-ttu-id="48508-181">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48508-181">Click Save.</span></span>
11. <span data-ttu-id="48508-182">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48508-182">Close the page.</span></span>


