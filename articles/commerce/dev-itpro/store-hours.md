---
title: Mağaza çalışma saatleri oluşturma ve güncelleştirme
description: Bu konu, Commerce Headquarters'ta mağaza saatlerini oluşturmayı ve güncelleştirmeyi açıklar.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 96ae5f33b1ab5fda98da4fc48b1fb883ca4d54b8
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024490"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="f3848-103">Mağaza çalışma saatleri oluşturma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f3848-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="f3848-104">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="f3848-104">Overview</span></span>

<span data-ttu-id="f3848-105">Perakendeciler tek bir yerden, coğrafi bölgeler arasında farklı mağazalar için mağaza saatleri oluşturabilir, bakımını yapabilir ve bunları yönetebilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="f3848-106">Depolama saatleri daha sonra satış noktasında (POS) gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="f3848-107">Böylece kasiyerler, mağaza saatlerini müşterilerle paylaşabilir ve diğer mağazalarda stoğa ilgilenen alışverişçilere daha iyi yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="f3848-108">Müşteriler mağazaya sonradan geri dönmek istiyorsanız, mağaza saatleri girişlere de yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="f3848-109">Farklı kanallar arasında birden fazla depolama saati yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="f3848-110">Bu kanallar arasında gerçek mekan depoları, çağrı merkezleri, mobil aygıtlar ve e-ticaret siteleri sayılabilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="f3848-111">Bir müşterinin farklı bir mağaza için bir malzeme çekme siparişi varsa, malzeme çekme bu mağazada kullanılabilir olduğunda, kasiyer program seçebilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="f3848-112">Mağaza arama, tarihlere ve depolama zamanlarında bir başvuru sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="f3848-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="f3848-113">Kasiyer bir tarih ve yerleşim seçebilir ve mağaza saatlerini içeren bir teslim alma girişi de yazdırabilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="f3848-114">Bu işlevsellik, Microsoft Dynamics 365 Retail 8.1.2 ve daha ileri sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="f3848-115">Mağaza saatlerini yapılandır</span><span class="sxs-lookup"><span data-stu-id="f3848-115">Configure store hours</span></span>

<span data-ttu-id="f3848-116">Mağaza saatlerini yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3848-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="f3848-117">**Retail ve Commerce** \> **Kanal kurulumu** \> **Mağaza saatleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f3848-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="f3848-118">Yeni bir mağaza saatleri şablonu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f3848-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="f3848-119">Varolan bir şablonu kullanmak için, sol bölmedeki şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="f3848-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="f3848-120">**Aralık Ekle** iletişim kutusunda Tarih aralığını, mağaza saatlerini ve gerekli tüm tatilleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f3848-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="f3848-121">Mağaza saatleri değişmiyorsa, **bitiş tarihi** alanında **hiçbir zaman bitmemesi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f3848-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="f3848-122">Depolama saatleri belirli bir ay, hafta veya gün için ise, **başlangıç tarihi** ve **bitiş tarihi** alanlarında uygun tarihleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f3848-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3848-123">Örtüşen başlangıç ve bitiş tarihlerine sahip birden çok şablon oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3848-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="f3848-124">Bu nedenle, örneğin, farklı saat dilimlerindeki Mağazalar için mağaza saatleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3848-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="f3848-125">![Aralık Ekle iletişim kutusu](../dev-itpro/media/Storehours1.png "Aralık Ekle iletişim kutusu")</span><span class="sxs-lookup"><span data-stu-id="f3848-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="f3848-126">Mağaza saatleri şablonunu, kullanılacak mağazalar ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="f3848-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="f3848-127">**Kuruluş düğümlerini Seç** iletişim kutusunda, şablonun ilişkilendirilmesi gereken depoları, bölgeleri ve organizasyonları seçin.</span><span class="sxs-lookup"><span data-stu-id="f3848-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="f3848-128">Her bir mağaza ile yalnızca bir depolama saatleri şablonu ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="f3848-129">Mağaza, bölge veya organizasyon seçmek için ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3848-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="f3848-130">Takvim mağazalar veya mağaza grupları tarafından kullanılabilir ve burada referans olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="f3848-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="f3848-131">![Organizasyon kırılımını seç iletişim kutusu](../dev-itpro/media/Storehours2.png "Organizasyon kırılımını seç iletişim kutusu")</span><span class="sxs-lookup"><span data-stu-id="f3848-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="f3848-132">**Dağıtım zamanlaması** sayfasında **1070** ve **1090** işlerini çalıştırarak mağaza saatlerini POS'ta kullanılabilir kılın.</span><span class="sxs-lookup"><span data-stu-id="f3848-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="f3848-133">Yazdırılmış fişlere mağaza saatlerini ekle</span><span class="sxs-lookup"><span data-stu-id="f3848-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="f3848-134">Yazdırılan POS alış irsaliyelerine mağaza saatleri eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3848-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="f3848-135">Fiş tasarımcısını açın.</span><span class="sxs-lookup"><span data-stu-id="f3848-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="f3848-136">Sol alt köşedeki **Alt bilgi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f3848-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="f3848-137">**Mağaza saatleri** öğesini sol panodan fiş şablonunun altındaki alt bilgi bölmesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="f3848-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="f3848-138">Varsayılan etiketi ihtiyaç duyduğunuz şekilde **Mağaza saatleri** öğesinde düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3848-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="f3848-139">Fişi kaydedin ve fiş tasarımcısını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3848-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="f3848-140">**Dağıtım zamanlaması** sayfasında **1070** ve **1090** işlerini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f3848-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="f3848-141">POS'ta oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f3848-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="f3848-142">Bir satışı tamamlayın ve bir makbuz yazdırmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="f3848-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="f3848-143">POS makbuzları şimdi mağaza saatlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="f3848-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="f3848-144">Şablonda herhangi bir tatil varsa, bunlar alındı bilgisi içinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f3848-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="f3848-145">![Makbuz örneği](../dev-itpro/media/Storehours3.png "Makbuz örneği")</span><span class="sxs-lookup"><span data-stu-id="f3848-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
