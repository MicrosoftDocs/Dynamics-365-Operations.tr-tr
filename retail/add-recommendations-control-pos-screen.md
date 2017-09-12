---
title: "POS aygıt hareket sayfasında önerileri denetimi ekleyin"
description: "Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 7f8522110c0d7d5277b0b3f3c7b21d8605d43f2c
ms.contentlocale: tr-tr
ms.lasthandoff: 06/29/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="7b4d2-103">POS aygıt hareket sayfasında önerileri denetimi ekleyin</span><span class="sxs-lookup"><span data-stu-id="7b4d2-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="7b4d2-104">Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="7b4d2-105">Microsoft Dynamics 365 for Retail kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="7b4d2-106">*Öneriler*, satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerinizin ilgi duyabilecekleri maddelerdir.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="7b4d2-107">Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="7b4d2-108">Açık Düzen tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="7b4d2-108">Open Layout designer</span></span>
1.  <span data-ttu-id="7b4d2-109">**Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="7b4d2-110">Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="7b4d2-111">Örneğin **Ekran düzeni kimliği** üzerinde, 'F2CP16:9M' kullanarak filtrele.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="7b4d2-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="7b4d2-113">Örneğin, ‘Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M’ seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="7b4d2-114">**Düzen tasarımcısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="7b4d2-115">Düzeni tasarımcısını başlatmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="7b4d2-116">Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="7b4d2-117">Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="7b4d2-118">Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="7b4d2-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Bir görüntüleme seçeneği seçin</span><span class="sxs-lookup"><span data-stu-id="7b4d2-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="7b4d2-120">İki yapılandırma seçeneği mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-120">There are two configurations options available.</span></span> <span data-ttu-id="7b4d2-121">Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="7b4d2-122">İki seçenek şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7b4d2-122">The two options are:</span></span>
-   <span data-ttu-id="7b4d2-123">Önerileri her zaman görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="7b4d2-124">Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="7b4d2-125">Önerileri her zaman görünür yapmak için</span><span class="sxs-lookup"><span data-stu-id="7b4d2-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="7b4d2-126">Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="7b4d2-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="7b4d2-127">Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="7b4d2-128">Bu alana sığacak şekilde yeniden boyutlandırın.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="7b4d2-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="7b4d2-129">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="7b4d2-130">Dynamics 365 for Retail içinde, **Perakende** &gt; **Perakende BT** &gt; **Dağıtım tabloları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="7b4d2-131">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="7b4d2-132">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="7b4d2-133">Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek için</span><span class="sxs-lookup"><span data-stu-id="7b4d2-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="7b4d2-134">Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="7b4d2-135">**Özelleştir** üzerine tıklayın.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="7b4d2-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="7b4d2-136">**Yeni sekme** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="7b4d2-137">Şimdi eklemiş olduğunuz yeni sekmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-137">Find the new tab that you just added.</span></span> <span data-ttu-id="7b4d2-138">Aşağı doğru gitmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="7b4d2-139">**İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="7b4d2-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="7b4d2-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="7b4d2-141">**Etiket** alanında, önerilenler sekmesi için bir ad yazın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-141">In the **Label** field, type a name for the recommendations tab.</span></span> <span data-ttu-id="7b4d2-142">Örneğin, 'Önerilen ürünler' yazın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-142">For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="7b4d2-143">**Resim** alanında, sekme üzerinde görünecek resmi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-143">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="7b4d2-144">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-144">Click **OK**.</span></span> <span data-ttu-id="7b4d2-145">Yeni sekme düğme kılavuzunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-145">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="7b4d2-146">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-146">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="7b4d2-147">Dynamics 365 for Retail içinde, **Perakende** &gt; **Perakende BT** &gt; **Dağıtım tabloları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-147">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="7b4d2-148">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-148">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="7b4d2-149">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-149">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="7b4d2-150">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7b4d2-150">See also</span></span>
--------

[<span data-ttu-id="7b4d2-151">Kişiselleştirilmiş ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7b4d2-151">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




