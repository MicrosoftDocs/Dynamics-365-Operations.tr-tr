---
title: Hareket ekranına öneriler ekleme
description: Bu konu, öneri denetiminin bir satış noktası (POS) cihazına, Microsoft Dynamics 365 Commerce'de ekran düzeni tasarımcısını kullanarak nasıl ekleneceğini açıklar.
author: bebeale
manager: AnnBe
ms.date: 03/19/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a39389da0908953cbbc161f07d067ce3fc569a1b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154144"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="7491d-103">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="7491d-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="7491d-104">Bu konu, öneri denetiminin bir satış noktası (POS) cihazına, Microsoft Dynamics 365 Commerce'de ekran düzeni tasarımcısını kullanarak nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="7491d-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="7491d-105">Ürün önerileri hakkında daha fazla bilgi için [POS belgelerindeki ürün önerilerini okuyun](product.md).</span><span class="sxs-lookup"><span data-stu-id="7491d-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="7491d-106">Commerce kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7491d-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="7491d-107">Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7491d-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="7491d-108">Açık Düzen tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="7491d-108">Open Layout designer</span></span>

1. <span data-ttu-id="7491d-109">**Retail ve Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="7491d-110">Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="7491d-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="7491d-111">**Örneğin Ekran düzeni kimliği** üzerinde, **F2CP16:9M** kullanarak filtrele.</span><span class="sxs-lookup"><span data-stu-id="7491d-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="7491d-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="7491d-113">Örneğin, **Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M** seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="7491d-114">**Düzen tasarımcısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="7491d-115">Düzeni tasarımcısını başlatmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="7491d-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="7491d-116">Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="7491d-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="7491d-117">Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7491d-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="7491d-118">Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7491d-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="7491d-119">[![Düzen tasarımcısı](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="7491d-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="7491d-120">Bir görüntüleme seçeneği seçin</span><span class="sxs-lookup"><span data-stu-id="7491d-120">Choose a display option</span></span>

<span data-ttu-id="7491d-121">İki yapılandırma seçeneği mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="7491d-121">There are two configurations options available.</span></span> <span data-ttu-id="7491d-122">Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="7491d-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="7491d-123">İki seçenek şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7491d-123">The two options are:</span></span>

- <span data-ttu-id="7491d-124">Önerileri her zaman görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="7491d-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="7491d-125">Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7491d-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="7491d-126">Önerileri her zaman görünür yapmak</span><span class="sxs-lookup"><span data-stu-id="7491d-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="7491d-127">Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.</span><span class="sxs-lookup"><span data-stu-id="7491d-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="7491d-128">[![Hareket satırı ayrıntıları alanının yüksekliği azaltıldı](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="7491d-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="7491d-129">Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın.</span><span class="sxs-lookup"><span data-stu-id="7491d-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="7491d-130">Bu alana sığacak şekilde yeniden boyutlandırın.</span><span class="sxs-lookup"><span data-stu-id="7491d-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="7491d-131">[![Öneriler denetimi düzene eklendi](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="7491d-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="7491d-132">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7491d-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="7491d-133">Commerce içinde, **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım tabloları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7491d-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="7491d-134">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="7491d-135">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="7491d-136">Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek</span><span class="sxs-lookup"><span data-stu-id="7491d-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="7491d-137">Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="7491d-138">**Özelleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-138">Click **Customize**.</span></span>

    <span data-ttu-id="7491d-139">[![Özelleştirme - Sekme denetimi iletişim kutusu](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="7491d-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="7491d-140">**Yeni sekme** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-140">Click **New tab**.</span></span>
4. <span data-ttu-id="7491d-141">Şimdi eklemiş olduğunuz yeni sekmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="7491d-141">Find the new tab that you just added.</span></span> <span data-ttu-id="7491d-142">Aşağı doğru gitmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="7491d-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="7491d-143">**İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="7491d-144">[![Önerilen ürünleri İçerik alanında seçmek](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="7491d-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="7491d-145">**Etiket** alanı içinde, öneriler sekmesi için bir ad girin. Örneğin, 'Önerilen ürünler' yazın.</span><span class="sxs-lookup"><span data-stu-id="7491d-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="7491d-146">**Resim** alanında, sekme üzerinde görünecek resmi seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="7491d-147">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-147">Click **OK**.</span></span> <span data-ttu-id="7491d-148">Yeni sekme düğme kılavuzunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7491d-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="7491d-149">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7491d-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="7491d-150">Commerce içinde, **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım tabloları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7491d-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="7491d-151">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7491d-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="7491d-152">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7491d-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7491d-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7491d-153">Additional resources</span></span>

[<span data-ttu-id="7491d-154">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7491d-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="7491d-155">Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7491d-155">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="7491d-156">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="7491d-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="7491d-157">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7491d-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="7491d-158">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="7491d-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="7491d-159">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="7491d-159">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="7491d-160">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7491d-160">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="7491d-161">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="7491d-161">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="7491d-162">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="7491d-162">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="7491d-163">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="7491d-163">Product recommendations FAQ</span></span>](faq-recommendations.md)
