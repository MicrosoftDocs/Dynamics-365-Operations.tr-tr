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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d36f19b5fa617169d33e7720e6a7602581cb525a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="063e3-103">Şirketler arası mali veri paylaşımını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="063e3-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="063e3-104">Bu yordam, şirketler arasında veri paylaşımı sırasında gerçekleşebilecek çakışmaları yapılandırma, etkinleştirme, doğrulamak ve çözümlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="063e3-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="063e3-105">USMF şirketini ve finansal veri paylaşım şablonunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="063e3-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="063e3-106">Bu görev kılavuzu Dynamics AX platformu 7.1 veya sonrasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="063e3-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="063e3-107">Sistem yönetimi > Çalışma alanları > Veri yönetimi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="063e3-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="063e3-108">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-108">Click Import.</span></span>
3. <span data-ttu-id="063e3-109">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="063e3-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="063e3-110">Kaynak veri biçimi alanında, Paket türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="063e3-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="063e3-111">Karşıya yükle seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-111">Click Upload.</span></span> <span data-ttu-id="063e3-112">Ticari veri paylaşma şablon paket dosyasına gidin ve bu dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="063e3-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="063e3-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="063e3-113">Click Save.</span></span>
6. <span data-ttu-id="063e3-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="063e3-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="063e3-115">Yeni oluşturulan veri paylaşımı ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="063e3-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="063e3-116">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-116">Click Import.</span></span>
8. <span data-ttu-id="063e3-117">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="063e3-117">Click Close.</span></span>
9. <span data-ttu-id="063e3-118">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="063e3-118">Refresh the page.</span></span>
10. <span data-ttu-id="063e3-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-119">Close the page.</span></span>
11. <span data-ttu-id="063e3-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-120">Close the page.</span></span>
12. <span data-ttu-id="063e3-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-121">Close the page.</span></span>
13. <span data-ttu-id="063e3-122">Sistem yönetimi > Kurulum > Şirketler arası veri paylaşımını yapılandır öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="063e3-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="063e3-123">Listede, Ödeme günleri'ni bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="063e3-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="063e3-124">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-124">Click Add.</span></span>
16. <span data-ttu-id="063e3-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="063e3-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="063e3-126">Şirket alanına 'USSI' yazın.</span><span class="sxs-lookup"><span data-stu-id="063e3-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="063e3-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-127">Click Add.</span></span>
19. <span data-ttu-id="063e3-128">Şirket alanına 'USMF' yazın.</span><span class="sxs-lookup"><span data-stu-id="063e3-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="063e3-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="063e3-129">Click Save.</span></span>
21. <span data-ttu-id="063e3-130">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-130">Click Enable.</span></span>
22. <span data-ttu-id="063e3-131">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-131">Click Yes.</span></span>
23. <span data-ttu-id="063e3-132">Paylaşım sorunlarını bul'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="063e3-133">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-133">Click Yes.</span></span>
25. <span data-ttu-id="063e3-134">Alan değerini güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-134">Click Update field value.</span></span>
26. <span data-ttu-id="063e3-135">Şirket 1'den değer kullan'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="063e3-136">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="063e3-136">Refresh the page.</span></span>
28. <span data-ttu-id="063e3-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="063e3-137">Close the page.</span></span>


