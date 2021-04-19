---
title: Plaka etiketi yazdırmayı etkinleştirme
description: Bu konu, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a608e9a2356f9dd49bbec1bcbe5489af5931d44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830894"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="f4ee0-103">Plaka etiketi yazdırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f4ee0-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4ee0-104">Bu konu, satış malzeme çekme işinde stoktan son madde çekildikten sonra Seri sevkiyat konteyner kodu (SSCC) etiketini otomatik olarak yazdırma konusunda açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="f4ee0-105">Bu yordamı USMF demo veri şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="f4ee0-106">Kendi verilerinizi kullanarak çalıştırırsanız, lisans plakaları için ayarlanmış bir numara seriniz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="f4ee0-107">Bu göreve başlamadan önce bir etiket yazdırıcı kurulumu yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="f4ee0-108">Organizasyon yönetimi > Kurulum > Ağ yazıcıları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="f4ee0-109">Eylem Bölmesi'nde, Seçenekler'e ve ardından Belge rota aracısı yükleyicisini indir düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="f4ee0-110">Yükleyiciyi çalıştırın ve yordama devam etmeden önce Etkin olarak ayarlanmış çalışır durumda bir ağ yazıcınız olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="f4ee0-111">GS1 şirket önekini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="f4ee0-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="f4ee0-112">**Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Ambar > Yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="f4ee0-113">**GS1 şirket öneki** alanına, GS1 şirket numaranız için 7 sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="f4ee0-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-114">Select **Save**.</span></span>
4. <span data-ttu-id="f4ee0-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="f4ee0-116">SSCC lisans plaka numarası serisini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="f4ee0-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="f4ee0-117">**Gezinti bölmesi > Modüller > Kuruluş yönetimi > Numara serileri > Numara serileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="f4ee0-118">**Alan** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="f4ee0-119">**Referans** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="f4ee0-120">**Şirket** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="f4ee0-121">**Segmentler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="f4ee0-122">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-122">Select **Edit**.</span></span>
7. <span data-ttu-id="f4ee0-123">**Segment** tablosunda ilk satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="f4ee0-124">**Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-124">Select **Remove**.</span></span>
9. <span data-ttu-id="f4ee0-125">**Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-125">Select **Remove**.</span></span>
10. <span data-ttu-id="f4ee0-126">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-126">Select **Save**.</span></span>
11. <span data-ttu-id="f4ee0-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="f4ee0-128">Belge yönlendirme düzenini oluşturun</span><span class="sxs-lookup"><span data-stu-id="f4ee0-128">Create the document route layout</span></span>
1. <span data-ttu-id="f4ee0-129">**Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Belge rotası > Belge rotası düzenleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="f4ee0-130">SSCC düzenini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="f4ee0-131">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-131">Select **New**.</span></span>
3. <span data-ttu-id="f4ee0-132">**Düzen kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="f4ee0-133">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f4ee0-134">**Metnin sonuna ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="f4ee0-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-135">Select **Save**.</span></span>
7. <span data-ttu-id="f4ee0-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="f4ee0-137">Belge yönlendirmeyi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="f4ee0-137">Set up the document routing</span></span>
1. <span data-ttu-id="f4ee0-138">**Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Belge rotası > Belge rotası** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="f4ee0-139">**İş emri türü** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="f4ee0-140">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-140">Select **New**.</span></span>
4. <span data-ttu-id="f4ee0-141">**Ambar** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="f4ee0-142">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="f4ee0-143">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-143">Select **New**.</span></span>
7. <span data-ttu-id="f4ee0-144">**Düzen kodu** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="f4ee0-145">**Ad** alanında kullanmak istediğiniz yazıcı adını girin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="f4ee0-146">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-146">Select **Save**.</span></span>
10. <span data-ttu-id="f4ee0-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="f4ee0-148">Mobil cihaz menüsü oluşturun</span><span class="sxs-lookup"><span data-stu-id="f4ee0-148">Create mobile device menu</span></span>
1. <span data-ttu-id="f4ee0-149">**Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="f4ee0-150">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-150">Select **New**.</span></span>
3. <span data-ttu-id="f4ee0-151">**Menü öğesi adı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="f4ee0-152">**Başlık** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="f4ee0-153">**Mod** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="f4ee0-154">**Mevcut işi kullan** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="f4ee0-155">**Lisans plakası oluştur** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="f4ee0-156">**İş sınıfları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="f4ee0-157">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-157">Select **New**.</span></span>
10. <span data-ttu-id="f4ee0-158">**İş sınıfı kodu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="f4ee0-159">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-159">Select **Save**.</span></span>
12. <span data-ttu-id="f4ee0-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-160">Close the page.</span></span>
13. <span data-ttu-id="f4ee0-161">**Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="f4ee0-162">Ağaçta, daha önce oluşturduğunuz menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="f4ee0-163">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-163">Select **Edit**.</span></span>
16. <span data-ttu-id="f4ee0-164">Menüye menü öğesi eklemek için oku seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="f4ee0-165">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-165">Select **Save**.</span></span>
18. <span data-ttu-id="f4ee0-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="f4ee0-167">İş şablonu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f4ee0-167">Update a work template</span></span>
1. <span data-ttu-id="f4ee0-168">**Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > İş > İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="f4ee0-169">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-169">Select **Edit**.</span></span>
3. <span data-ttu-id="f4ee0-170">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-170">Select **New**.</span></span>
4. <span data-ttu-id="f4ee0-171">**İş türü** alanında **Yazdır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="f4ee0-172">**İş sınıfı kodu** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="f4ee0-173">**Yukarı taşı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-173">Select **Move up**.</span></span>
7. <span data-ttu-id="f4ee0-174">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-174">Select **Save**.</span></span>
8. <span data-ttu-id="f4ee0-175">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f4ee0-175">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]