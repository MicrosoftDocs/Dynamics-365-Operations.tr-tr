---
title: POS cihazlarında hareket ekranına öneriler denetimi ekleme
description: Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606861"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="879b5-103">POS cihazlarında hareket ekranına öneriler denetimi ekleme</span><span class="sxs-lookup"><span data-stu-id="879b5-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="879b5-104">Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="879b5-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="879b5-105">Daha fazla bilgi için bkz. [Kaldırılan veya artık kullanılmayan özellikler](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="879b5-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="879b5-106">Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="879b5-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="879b5-107">Microsoft Dynamics 365 for Retail kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879b5-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="879b5-108">*Öneriler*, satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerinizin ilgi duyabilecekleri maddelerdir.</span><span class="sxs-lookup"><span data-stu-id="879b5-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="879b5-109">Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="879b5-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="879b5-110">Açık Düzen tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="879b5-110">Open Layout designer</span></span>

1. <span data-ttu-id="879b5-111">**Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="879b5-112">Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="879b5-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="879b5-113">**Örneğin Ekran düzeni kimliği** üzerinde, **F2CP16:9M** kullanarak filtrele.</span><span class="sxs-lookup"><span data-stu-id="879b5-113">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="879b5-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="879b5-115">Örneğin, **Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M** seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-115">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="879b5-116">**Düzen tasarımcısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="879b5-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="879b5-117">Düzeni tasarımcısını başlatmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="879b5-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="879b5-118">Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="879b5-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="879b5-119">Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="879b5-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="879b5-120">Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="879b5-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="879b5-121">[![Düzen tasarımcısı](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="879b5-121">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="879b5-122">Bir görüntüleme seçeneği seçin</span><span class="sxs-lookup"><span data-stu-id="879b5-122">Choose a display option</span></span>

<span data-ttu-id="879b5-123">İki yapılandırma seçeneği mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="879b5-123">There are two configurations options available.</span></span> <span data-ttu-id="879b5-124">Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="879b5-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="879b5-125">İki seçenek şunlardır:</span><span class="sxs-lookup"><span data-stu-id="879b5-125">The two options are:</span></span>

- <span data-ttu-id="879b5-126">Önerileri her zaman görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="879b5-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="879b5-127">Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="879b5-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="879b5-128">Önerileri her zaman görünür yapmak</span><span class="sxs-lookup"><span data-stu-id="879b5-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="879b5-129">Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.</span><span class="sxs-lookup"><span data-stu-id="879b5-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="879b5-130">[![Hareket satırlarının yüksekliği ayrıntıları alanı azaltıldı](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="879b5-130">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="879b5-131">Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın.</span><span class="sxs-lookup"><span data-stu-id="879b5-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="879b5-132">Bu alana sığacak şekilde yeniden boyutlandırın.</span><span class="sxs-lookup"><span data-stu-id="879b5-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="879b5-133">[![Öneriler denetimi düzene eklendi](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="879b5-133">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="879b5-134">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="879b5-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="879b5-135">Dynamics 365 for Retail içinde, **Retail** &gt; **Retail IT** &gt; **Dağıtım planları**.</span><span class="sxs-lookup"><span data-stu-id="879b5-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="879b5-136">Listede  **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="879b5-137">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="879b5-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="879b5-138">Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek</span><span class="sxs-lookup"><span data-stu-id="879b5-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="879b5-139">Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="879b5-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="879b5-140">Tıklatın  **Özelleştirme**.</span><span class="sxs-lookup"><span data-stu-id="879b5-140">Click **Customize**.</span></span>

    <span data-ttu-id="879b5-141">[![Özelleştirme - Sekme denetimi iletişim kutusu](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="879b5-141">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="879b5-142">**Yeni sekme** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="879b5-142">Click **New tab**.</span></span>
4. <span data-ttu-id="879b5-143">Şimdi eklemiş olduğunuz yeni sekmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="879b5-143">Find the new tab that you just added.</span></span> <span data-ttu-id="879b5-144">Aşağı doğru gitmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="879b5-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="879b5-145">**İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="879b5-146">[![Önerilen ürünleri İçerik alanında seçmek](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="879b5-146">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="879b5-147">**Etiket** alanı içinde, öneriler sekmesi için bir ad girin. Örneğin, 'Önerilen ürünler' yazın.</span><span class="sxs-lookup"><span data-stu-id="879b5-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="879b5-148">**Resim** alanında, sekme üzerinde görünecek resmi seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="879b5-149">Tıklatın **Tamam**.</span><span class="sxs-lookup"><span data-stu-id="879b5-149">Click **OK**.</span></span> <span data-ttu-id="879b5-150">Yeni sekme düğme kılavuzunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="879b5-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="879b5-151">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="879b5-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="879b5-152">Dynamics 365 for Retail içinde, **Retail** &gt; **Retail IT** &gt; **Dağıtım planları**.</span><span class="sxs-lookup"><span data-stu-id="879b5-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="879b5-153">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="879b5-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="879b5-154">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="879b5-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="879b5-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="879b5-155">Additional resources</span></span>

[<span data-ttu-id="879b5-156">Kişiselleştirilmiş ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="879b5-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
