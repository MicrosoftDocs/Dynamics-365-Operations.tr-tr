---
title: "POS aygıt hareket sayfasında önerileri denetimi ekleyin"
description: "Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 0d366997fbb6f23474047fa8c465a594491c46ad
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="56f96-103">POS aygıt hareket sayfasında önerileri denetimi ekleyin</span><span class="sxs-lookup"><span data-stu-id="56f96-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="56f96-104">Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Retail kullanarak nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="56f96-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="56f96-105">Microsoft Dynamics 365 for Retail kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="56f96-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="56f96-106">*Öneriler*, satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerinizin ilgi duyabilecekleri maddelerdir.</span><span class="sxs-lookup"><span data-stu-id="56f96-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="56f96-107">Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="56f96-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="56f96-108">Açık Düzen tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="56f96-108">Open Layout designer</span></span>
1.  <span data-ttu-id="56f96-109">**Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="56f96-110">Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="56f96-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="56f96-111">Örneğin **Ekran düzeni kimliği** üzerinde, 'F2CP16:9M' kullanarak filtrele.</span><span class="sxs-lookup"><span data-stu-id="56f96-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="56f96-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="56f96-113">Örneğin, ‘Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M’ seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="56f96-114">**Düzen tasarımcısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56f96-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="56f96-115">Düzeni tasarımcısını başlatmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="56f96-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="56f96-116">Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="56f96-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="56f96-117">Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="56f96-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="56f96-118">Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="56f96-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="56f96-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Bir görüntüleme seçeneği seçin</span><span class="sxs-lookup"><span data-stu-id="56f96-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="56f96-120">İki yapılandırma seçeneği mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="56f96-120">There are two configurations options available.</span></span> <span data-ttu-id="56f96-121">Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="56f96-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="56f96-122">İki seçenek şunlardır:</span><span class="sxs-lookup"><span data-stu-id="56f96-122">The two options are:</span></span>
-   <span data-ttu-id="56f96-123">Önerileri her zaman görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="56f96-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="56f96-124">Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="56f96-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="56f96-125">Önerileri her zaman görünür yapmak için</span><span class="sxs-lookup"><span data-stu-id="56f96-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="56f96-126">Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="56f96-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="56f96-127">Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın.</span><span class="sxs-lookup"><span data-stu-id="56f96-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="56f96-128">Bu alana sığacak şekilde yeniden boyutlandırın.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="56f96-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="56f96-129">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56f96-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="56f96-130">Dynamics 365 for Retail içinde, **Perakende** &gt; **Perakende BT** &gt; **Dağıtım tabloları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="56f96-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="56f96-131">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="56f96-132">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56f96-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="56f96-133">Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek için</span><span class="sxs-lookup"><span data-stu-id="56f96-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="56f96-134">Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56f96-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="56f96-135">**Özelleştir** üzerine tıklayın.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="56f96-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="56f96-136">**Yeni sekme** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56f96-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="56f96-137">Şimdi eklemiş olduğunuz yeni sekmeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="56f96-137">Find the new tab that you just added.</span></span> <span data-ttu-id="56f96-138">Aşağı doğru gitmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="56f96-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="56f96-139">**İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="56f96-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="56f96-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="56f96-141">**Etiket** alanı içinde, öneriler sekmesi için bir ad girin. Örneğin, 'Önerilen ürünler' yazın.</span><span class="sxs-lookup"><span data-stu-id="56f96-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="56f96-142">**Resim** alanında, sekme üzerinde görünecek resmi seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="56f96-143">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56f96-143">Click **OK**.</span></span> <span data-ttu-id="56f96-144">Yeni sekme düğme kılavuzunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="56f96-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="56f96-145">Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56f96-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="56f96-146">Dynamics 365 for Retail içinde, **Perakende** &gt; **Perakende BT** &gt; **Dağıtım tabloları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="56f96-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="56f96-147">Listede **1090 Kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="56f96-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="56f96-148">**Şimdi çalıştır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56f96-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="56f96-149">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="56f96-149">See also</span></span>
--------

[<span data-ttu-id="56f96-150">Kişiselleştirilmiş ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="56f96-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




