---
title: POS cihazlarında hareket ekranına öneriler denetimi ekleme
description: Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811228"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="6d2a2-103">POS cihazlarında hareket ekranına öneriler denetimi ekleme</span><span class="sxs-lookup"><span data-stu-id="6d2a2-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="6d2a2-104">Bu konu, öneri denetiminin bir satış noktası (POS) cihazına, Microsoft Dynamics 365 Retail'de ekran düzeni tasarımcısını kullanarak nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="6d2a2-105">Ürün önerileri hakkında daha fazla bilgi için [POS belgelerindeki ürün önerilerini okuyun](product.md).</span><span class="sxs-lookup"><span data-stu-id="6d2a2-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="6d2a2-106">Microsoft Dynamics 365 Retail kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="6d2a2-107">Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="6d2a2-108">Açık Düzen tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="6d2a2-108">Open Layout designer</span></span>

1. <span data-ttu-id="6d2a2-109">**Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="6d2a2-110">Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="6d2a2-111">**Örneğin Ekran düzeni kimliği** üzerinde, **F2CP16:9M** kullanarak filtrele.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="6d2a2-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="6d2a2-113">Örneğin, **Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M** seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="6d2a2-114">**Düzen tasarımcısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="6d2a2-115">Düzeni tasarımcısını başlatmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="6d2a2-116">Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="6d2a2-117">Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="6d2a2-118">Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="6d2a2-119">[![Düzen tasarımcısı](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="6d2a2-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="6d2a2-120">Bir görüntüleme seçeneği seçin</span><span class="sxs-lookup"><span data-stu-id="6d2a2-120">Choose a display option</span></span>

<span data-ttu-id="6d2a2-121">İki yapılandırma seçeneği mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-121">There are two configurations options available.</span></span> <span data-ttu-id="6d2a2-122">Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="6d2a2-123">İki seçenek şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d2a2-123">The two options are:</span></span>

- <span data-ttu-id="6d2a2-124">Önerileri her zaman görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="6d2a2-125">Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="6d2a2-126">Önerileri her zaman görünür yapmak</span><span class="sxs-lookup"><span data-stu-id="6d2a2-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="6d2a2-127">Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="6d2a2-128">[![Hareket satırı ayrıntıları alanının yüksekliği azaltıldı](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="6d2a2-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="6d2a2-129">Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="6d2a2-130">Bu alana sığacak şekilde yeniden boyutlandırın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="6d2a2-131">[![Öneriler denetimi düzene eklendi](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="6d2a2-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="6d2a2-132">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="6d2a2-133">Dynamics 365 for Retail içinde, **Retail** &gt; **Retail IT** &gt; **Dağıtım planları**.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="6d2a2-134">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="6d2a2-135">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="6d2a2-136">Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek</span><span class="sxs-lookup"><span data-stu-id="6d2a2-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="6d2a2-137">Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="6d2a2-138">**Özelleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-138">Click **Customize**.</span></span>

    <span data-ttu-id="6d2a2-139">[![Özelleştirme - Sekme denetimi iletişim kutusu](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="6d2a2-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="6d2a2-140">**Yeni sekme** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-140">Click **New tab**.</span></span>
4. <span data-ttu-id="6d2a2-141">Şimdi eklemiş olduğunuz yeni sekmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-141">Find the new tab that you just added.</span></span> <span data-ttu-id="6d2a2-142">Aşağı doğru gitmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="6d2a2-143">**İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="6d2a2-144">[![Önerilen ürünleri İçerik alanında seçmek](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="6d2a2-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="6d2a2-145">**Etiket** alanı içinde, öneriler sekmesi için bir ad girin. Örneğin, 'Önerilen ürünler' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="6d2a2-146">**Resim** alanında, sekme üzerinde görünecek resmi seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="6d2a2-147">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-147">Click **OK**.</span></span> <span data-ttu-id="6d2a2-148">Yeni sekme düğme kılavuzunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="6d2a2-149">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="6d2a2-150">Dynamics 365 for Retail içinde, **Retail** &gt; **Retail IT** &gt; **Dağıtım planları**.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="6d2a2-151">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="6d2a2-152">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d2a2-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d2a2-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6d2a2-153">Additional resources</span></span>

[<span data-ttu-id="6d2a2-154">POS'ta ürün önerileri</span><span class="sxs-lookup"><span data-stu-id="6d2a2-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="6d2a2-155">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6d2a2-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
