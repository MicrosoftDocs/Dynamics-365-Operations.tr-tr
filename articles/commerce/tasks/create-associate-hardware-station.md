---
title: " Donanım istasyonu oluşturma ve ilişkilendirme"
description: Bu yordamda yeni bir donanım istasyonu oluşturma konusu açıklanmaktadır.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0c02246a20ef28c0f4f28b73dfe5ff56f38a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247056"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="40773-103"> Donanım istasyonu oluşturma ve ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="40773-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40773-104">Bu yordamda yeni bir donanım istasyonu oluşturma konusu açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="40773-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="40773-105">Yeni bir donanım profili oluşturulur ve yeni donanım istasyonlarını önceden tanımlanmış bir mağazaya (kanal) eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="40773-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="40773-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="40773-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="40773-107">Ticaret temel gider > Kanallar >...</span><span class="sxs-lookup"><span data-stu-id="40773-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="40773-108">> ..</span><span class="sxs-lookup"><span data-stu-id="40773-108">> ..</span></span> <span data-ttu-id="40773-109">> ..</span><span class="sxs-lookup"><span data-stu-id="40773-109">> ..</span></span> <span data-ttu-id="40773-110">> Donanım istasyonu profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="40773-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="40773-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-111">Click New.</span></span>
3. <span data-ttu-id="40773-112">Donanım istasyonu kimliği alanına 'TestHWProfile' yazın.</span><span class="sxs-lookup"><span data-stu-id="40773-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="40773-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="40773-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="40773-114">Bağlantı noktası numarası alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="40773-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="40773-115">Donanım profili alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="40773-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="40773-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="40773-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="40773-118">Paket adı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="40773-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="40773-120">Yeni bir ortam ile birlikte gelen standart pakettir.</span><span class="sxs-lookup"><span data-stu-id="40773-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="40773-121">Sürüm numarası farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="40773-121">The version number may vary.</span></span>  
11. <span data-ttu-id="40773-122">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="40773-122">Click Save.</span></span>
12. <span data-ttu-id="40773-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="40773-123">Close the page.</span></span>
13. <span data-ttu-id="40773-124">Perakende ve Ticaret > Kanallar > Tüm mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="40773-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="40773-125">Listede satır 17'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="40773-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="40773-126">USRT demo veri şirketini kullanıyorsanız, Houston mağazasıdır.</span><span class="sxs-lookup"><span data-stu-id="40773-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="40773-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="40773-128">Donanım istasyonları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="40773-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="40773-129">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="40773-129">Click Add.</span></span>
18. <span data-ttu-id="40773-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="40773-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="40773-131">Profil kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="40773-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="40773-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40773-133">Bu, önceki adımlarda oluşturulan yeni donanım istasyonu profili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="40773-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="40773-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="40773-135">Ana bilgisayar adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40773-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="40773-136">EFT terminali kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40773-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="40773-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40773-137">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]