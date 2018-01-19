--- 
title: " Donanım istasyonu oluşturma ve ilişkilendirme"
description: "Bu yordamda yeni bir donanım istasyonu oluşturma konusu açıklanmaktadır."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8fc271873cc95b7d6388574f21dea49363ae1ec5
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="e2e67-103"> Donanım istasyonu oluşturma ve ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="e2e67-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e2e67-104">Bu yordamda yeni bir donanım istasyonu oluşturma konusu açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e2e67-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="e2e67-105">Yeni bir donanım profili oluşturulur ve yeni donanım istasyonlarını önceden tanımlanmış bir mağazaya (kanal) eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2e67-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="e2e67-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2e67-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e2e67-107">Ticaret temel gider > Kanallar >...</span><span class="sxs-lookup"><span data-stu-id="e2e67-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="e2e67-108">> ..</span><span class="sxs-lookup"><span data-stu-id="e2e67-108">> ..</span></span> <span data-ttu-id="e2e67-109">> ..</span><span class="sxs-lookup"><span data-stu-id="e2e67-109">> ..</span></span> <span data-ttu-id="e2e67-110">> Donanım istasyonu profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="e2e67-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-111">Click New.</span></span>
3. <span data-ttu-id="e2e67-112">Donanım istasyonu kimliği alanına 'TestHWProfile' yazın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="e2e67-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e2e67-114">Bağlantı noktası numarası alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="e2e67-115">Donanım profili alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e2e67-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e2e67-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e2e67-118">Paket adı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e2e67-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2e67-120">Yeni bir ortam ile birlikte gelen standart pakettir.</span><span class="sxs-lookup"><span data-stu-id="e2e67-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="e2e67-121">Sürüm numarası farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e2e67-121">The version number may vary.</span></span>  
11. <span data-ttu-id="e2e67-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-122">Click Save.</span></span>
12. <span data-ttu-id="e2e67-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-123">Close the page.</span></span>
13. <span data-ttu-id="e2e67-124">Perakende ve ticaret > Kanallar > Tüm perakende mağazaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="e2e67-125">Listede satır 17'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="e2e67-126">USRT demo veri şirketini kullanıyorsanız, Houston mağazasıdır.</span><span class="sxs-lookup"><span data-stu-id="e2e67-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="e2e67-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="e2e67-128">Donanım istasyonları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="e2e67-129">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-129">Click Add.</span></span>
18. <span data-ttu-id="e2e67-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="e2e67-131">Profil kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="e2e67-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e2e67-133">Bu, önceki adımlarda oluşturulan yeni donanım istasyonu profili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e2e67-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="e2e67-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="e2e67-135">Ana bilgisayar adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="e2e67-136">EFT terminali kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e2e67-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="e2e67-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2e67-137">Click Save.</span></span>


