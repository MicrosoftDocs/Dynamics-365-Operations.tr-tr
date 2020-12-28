---
title: Şirketler arası mali veri paylaşımını yapılandırma
description: Bu yordam, şirketler arasında veri paylaşımı sırasında gerçekleşebilecek çakışmaları yapılandırma, etkinleştirme, doğrulamak ve çözümlemeyi gösterir.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aeb9e85d3263d78a8412bd3c300dae8bb1d840ef
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685205"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="fcaa6-103">Şirketler arası mali veri paylaşımını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fcaa6-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcaa6-104">Bu yordam, şirketler arasında veri paylaşımı sırasında gerçekleşebilecek çakışmaları yapılandırma, etkinleştirme, doğrulamak ve çözümlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="fcaa6-105">USMF şirketini ve finansal veri paylaşım şablonunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="fcaa6-106">Bu görev kılavuzu Dynamics AX platformu 7.1 veya sonrasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="fcaa6-107">**Gezinti bölmesi > Modüller > Sistem yönetimi > Çalışma alanları > Veri yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="fcaa6-108">**İçe aktar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-108">Click **Import**.</span></span>
3. <span data-ttu-id="fcaa6-109">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="fcaa6-110">**Kaynak veri biçimi** alanında, 'Paket' türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="fcaa6-111">**Karşıya yükle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-111">Click **Upload**.</span></span> <span data-ttu-id="fcaa6-112">Ticari veri paylaşma şablon paket dosyasına gidin ve bu dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="fcaa6-113">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-113">Click **Save**.</span></span>
6. <span data-ttu-id="fcaa6-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-114">In the list, mark the selected row.</span></span> <span data-ttu-id="fcaa6-115">Yeni oluşturulan veri paylaşımı ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="fcaa6-116">**İçe aktar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-116">Click **Import**.</span></span>
8. <span data-ttu-id="fcaa6-117">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-117">Click **Close**.</span></span>
9. <span data-ttu-id="fcaa6-118">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-118">Refresh the page.</span></span>
10. <span data-ttu-id="fcaa6-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-119">Close the page.</span></span>
11. <span data-ttu-id="fcaa6-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-120">Close the page.</span></span>
12. <span data-ttu-id="fcaa6-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-121">Close the page.</span></span>
13. <span data-ttu-id="fcaa6-122">**Gezinti bölmesi > Modüller > Sistem yönetimi > Kurulum > Şirketler arası veri paylaşımı yapılandır** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="fcaa6-123">Listede **Ödeme günleri** öğesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="fcaa6-124">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-124">Click **Add**.</span></span>
16. <span data-ttu-id="fcaa6-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="fcaa6-126">**Şirket** alanına 'USSI' yazın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="fcaa6-127">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-127">Click **Add**.</span></span>
19. <span data-ttu-id="fcaa6-128">**Şirket** alanına 'USMF' yazın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="fcaa6-129">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-129">Click **Save**.</span></span>
21. <span data-ttu-id="fcaa6-130">**Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-130">Click **Enable**.</span></span>
22. <span data-ttu-id="fcaa6-131">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-131">Click **Yes**.</span></span>
23. <span data-ttu-id="fcaa6-132">**Paylaşım sorunlarını bul**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="fcaa6-133">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-133">Click **Yes**.</span></span>
25. <span data-ttu-id="fcaa6-134">**Alan değerini güncelleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="fcaa6-135">**Şirket 1'den değer kullan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="fcaa6-136">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-136">Refresh the page.</span></span>
28. <span data-ttu-id="fcaa6-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-137">Close the page.</span></span>

