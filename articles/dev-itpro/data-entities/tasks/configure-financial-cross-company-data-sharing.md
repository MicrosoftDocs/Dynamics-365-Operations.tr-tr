--- 
title: "Şirketler arası mali veri paylaşımını yapılandırma"
description: "Bu yordam, şirketler arasında veri paylaşımı sırasında gerçekleşebilecek çakışmaları yapılandırma, etkinleştirme, doğrulamak ve çözümlemeyi gösterir."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5ae6b30d2d0948efbf86f2c2693e643b383f8406
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="configure-cross-company-financial-data-sharing"></a><span data-ttu-id="71dd0-103">Şirketler arası mali veri paylaşımını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="71dd0-103">Configure cross-company financial data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71dd0-104">Bu yordam, şirketler arasında veri paylaşımı sırasında gerçekleşebilecek çakışmaları yapılandırma, etkinleştirme, doğrulamak ve çözümlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="71dd0-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="71dd0-105">USMF şirketini ve finansal veri paylaşım şablonunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="71dd0-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="71dd0-106">Bu görev kılavuzu Dynamics AX platformu 7.1 veya sonrasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="71dd0-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="71dd0-107">Sistem yönetimi > Çalışma alanları > Veri yönetimi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="71dd0-108">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-108">Click Import.</span></span>
3. <span data-ttu-id="71dd0-109">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="71dd0-110">Kaynak veri biçimi alanında, Paket türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="71dd0-111">Karşıya yükle seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-111">Click Upload.</span></span> <span data-ttu-id="71dd0-112">Ticari veri paylaşma şablon paket dosyasına gidin ve bu dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="71dd0-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-113">Click Save.</span></span>
6. <span data-ttu-id="71dd0-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="71dd0-115">Yeni oluşturulan veri paylaşımı ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="71dd0-116">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-116">Click Import.</span></span>
8. <span data-ttu-id="71dd0-117">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-117">Click Close.</span></span>
9. <span data-ttu-id="71dd0-118">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-118">Refresh the page.</span></span>
10. <span data-ttu-id="71dd0-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-119">Close the page.</span></span>
11. <span data-ttu-id="71dd0-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-120">Close the page.</span></span>
12. <span data-ttu-id="71dd0-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-121">Close the page.</span></span>
13. <span data-ttu-id="71dd0-122">Sistem yönetimi > Kurulum > Şirketler arası veri paylaşımını yapılandır öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="71dd0-123">Listede, Ödeme günleri'ni bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="71dd0-124">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-124">Click Add.</span></span>
16. <span data-ttu-id="71dd0-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="71dd0-126">Şirket alanına 'USSI' yazın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="71dd0-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-127">Click Add.</span></span>
19. <span data-ttu-id="71dd0-128">Şirket alanına 'USMF' yazın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="71dd0-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-129">Click Save.</span></span>
21. <span data-ttu-id="71dd0-130">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-130">Click Enable.</span></span>
22. <span data-ttu-id="71dd0-131">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-131">Click Yes.</span></span>
23. <span data-ttu-id="71dd0-132">Paylaşım sorunlarını bul'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="71dd0-133">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-133">Click Yes.</span></span>
25. <span data-ttu-id="71dd0-134">Alan değerini güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-134">Click Update field value.</span></span>
26. <span data-ttu-id="71dd0-135">Şirket 1'den değer kullan'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="71dd0-136">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="71dd0-136">Refresh the page.</span></span>
28. <span data-ttu-id="71dd0-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="71dd0-137">Close the page.</span></span>


