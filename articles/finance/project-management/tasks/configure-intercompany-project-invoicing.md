---
title: Şirketlerarası proje faturalamasını yapılandırma
description: Bu konu, kuruluşunuzdaki iki şirket arasında proje faturalandırmasını ayarlamayı gösterir.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144291"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="32cf2-103">Şirketlerarası proje faturalamasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="32cf2-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32cf2-104">Bu konu, kuruluşunuzdaki iki şirket arasında proje faturalandırmasını ayarlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="32cf2-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="32cf2-105">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="32cf2-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="32cf2-106">Gezinti Bölmesi'nde **Modüller > Borç hesapları > Satıcılar > Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="32cf2-107">**Tüm satıcılar** listesinde, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="32cf2-108">Eylem Bölmesinde, **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="32cf2-109">**Şirketlerarası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="32cf2-110">Şirketlerarası ticareti etkinleştirmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="32cf2-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="32cf2-111">**Müşteri şirketi** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="32cf2-112">**Hesabım** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="32cf2-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-113">Select **Save**.</span></span>
9. <span data-ttu-id="32cf2-114">Ana sayfaya dönmek için sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="32cf2-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="32cf2-115">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Proje yönetimi ve muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="32cf2-116">**Şirketlerarası** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="32cf2-117">Şirketlerarası kaynak planlama ve zaman çizelgelerini etkinleştirmek için kaydırma çubuğunu **Evet** konumuna getirin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="32cf2-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="32cf2-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-119">Select **New**.</span></span>
15. <span data-ttu-id="32cf2-120">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="32cf2-121">**Gelir tahakkuku** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="32cf2-122">**Varsayılan zaman çizelgesi kategorisi** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="32cf2-123">**Varsayılan gider kategorisi** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="32cf2-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-124">Select **Save**.</span></span>
20. <span data-ttu-id="32cf2-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="32cf2-125">Close the page.</span></span>
21. <span data-ttu-id="32cf2-126">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Deftere nakletme > Deftere Nakil kurulumu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="32cf2-127">**Genel muhasebe hesap türleri** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="32cf2-128">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-128">Select **New**.</span></span>
24. <span data-ttu-id="32cf2-129">Yeni satırın **Ana hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="32cf2-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-130">Select **Save**.</span></span>
26. <span data-ttu-id="32cf2-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="32cf2-131">Close the page.</span></span>
27. <span data-ttu-id="32cf2-132">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Transfer fiyatı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="32cf2-133">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-133">Select **New**.</span></span>
29. <span data-ttu-id="32cf2-134">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="32cf2-135">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="32cf2-136">**Transfer fiyatı modeli** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="32cf2-137">**Fiyatlandırma** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="32cf2-138">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32cf2-138">Select **Save**.</span></span>

