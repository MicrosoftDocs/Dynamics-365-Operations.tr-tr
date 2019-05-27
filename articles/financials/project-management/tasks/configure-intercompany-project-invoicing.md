---
title: Şirketlerarası proje faturalamasını yapılandırma
description: Bu yordam, kuruluşunuzdaki iki şirket arasında proje faturalandırmasını ayarlamayı gösterir.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572431"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="29113-103">Şirketlerarası proje faturalamasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="29113-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29113-104">Bu yordam, kuruluşunuzdaki iki şirket arasında proje faturalandırmasını ayarlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="29113-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="29113-105">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="29113-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="29113-106">Borç hesapları > Satıcılar > Tüm satıcılar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="29113-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="29113-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="29113-108">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="29113-109">Şirketlerarası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-109">Click Intercompany.</span></span>
5. <span data-ttu-id="29113-110">Şirketlerarası ticareti etkinleştirmek için Etkin seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="29113-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="29113-111">Müşteri şirketi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="29113-112">Hesabım alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="29113-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-113">Click Save.</span></span>
9. <span data-ttu-id="29113-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29113-114">Close the page.</span></span>
10. <span data-ttu-id="29113-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29113-115">Close the page.</span></span>
11. <span data-ttu-id="29113-116">Proje yönetimi ve muhasebe > Kurulum > Proje yönetimi ve muhasebe parametreleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="29113-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="29113-117">Şirketlerarası sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="29113-118">Şirketlerarası kaynak planlama ve zaman çizelgelerini etkinleştirmek için kaydırma çubuğunu Evet konumuna getirin.</span><span class="sxs-lookup"><span data-stu-id="29113-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="29113-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="29113-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-120">Click New.</span></span>
16. <span data-ttu-id="29113-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="29113-122">Ödünç alma tüzel kişiliği alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="29113-123">Gelir tahakkuku onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="29113-124">Varsayılan zaman çizelgesi kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="29113-125">Varsayılan gider kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="29113-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-126">Click Save.</span></span>
22. <span data-ttu-id="29113-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29113-127">Close the page.</span></span>
23. <span data-ttu-id="29113-128">Proje yönetimi ve muhasebe > Kurulum > Deftere Nakil > Deftere Nakil kurulumu öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="29113-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="29113-129">Genel muhasebe hesap türleri alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="29113-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-130">Click New.</span></span>
26. <span data-ttu-id="29113-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="29113-132">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="29113-133">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="29113-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="29113-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-134">Click Save.</span></span>
30. <span data-ttu-id="29113-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29113-135">Close the page.</span></span>
31. <span data-ttu-id="29113-136">Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Transfer fiyatı öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="29113-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="29113-137">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-137">Click New.</span></span>
33. <span data-ttu-id="29113-138">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="29113-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="29113-139">Ödünç alma tüzel kişiliği alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="29113-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="29113-140">Transfer fiyatı modeli alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="29113-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="29113-141">Fiyatlandırma alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="29113-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="29113-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29113-142">Click Save.</span></span>

