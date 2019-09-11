---
title: Şablon kullanarak yevmiye defteri girişi oluşturun
description: Deftere nakledilen günlük fişleri Fiş şablonu olarak kaydedilebilir ve yeni bir günlük fişine uygulanabilir.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: babbc5ee067743d368680970556f8e5d3d8585f0
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916173"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="ce78f-103">Şablon kullanarak yevmiye defteri girişi oluşturun</span><span class="sxs-lookup"><span data-stu-id="ce78f-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce78f-104">Deftere nakledilen günlük fişleri Fiş şablonu olarak kaydedilebilir ve yeni bir günlük fişine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="ce78f-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="ce78f-105">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ce78f-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="ce78f-106">**Gezinti bölmesi > Modüller > Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="ce78f-107">**Eylem bölmesinde** **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="ce78f-108">Bu prosedür, bir günlük fişi oluşturup deftere naklederek başlar, ancak daha önce nakledilmiş günlük fişi bir şablon olarak kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="ce78f-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="ce78f-109">**Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ce78f-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ce78f-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ce78f-112">**Satırlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-112">Click **Lines**.</span></span>
7. <span data-ttu-id="ce78f-113">**Hesap türü** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="ce78f-114">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="ce78f-115">**Borç** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="ce78f-116">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-116">Click **New**.</span></span>
11. <span data-ttu-id="ce78f-117">**Hesap türü** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="ce78f-118">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="ce78f-119">**Borç** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="ce78f-120">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-120">Click **New**.</span></span>
14. <span data-ttu-id="ce78f-121">**Hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="ce78f-122">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="ce78f-123">**Alacak** alanına fişi dengelemek için bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="ce78f-124">**Eylem bölmesinde** **Deftere naklet** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="ce78f-125">**İşlevler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-125">Click **Functions**.</span></span>
19. <span data-ttu-id="ce78f-126">**Fiş şablonunu kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="ce78f-127">Bu prosedürde bir **Yüzde Şablonu** türü kullanıldığı varsayılır.</span><span class="sxs-lookup"><span data-stu-id="ce78f-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="ce78f-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-128">Click OK.</span></span>
    - <span data-ttu-id="ce78f-129">Yüzde: Fişteki tutarlar yüzde katsayılarına dönüştürülür ve bu, Fiş şablonu seçilirken herhangi bir tutarın uygulanmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce78f-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="ce78f-130">Tutar: Gerçek tutarlar depolanır ve uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ce78f-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="ce78f-131">**Genel günlükler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-131">Click **General journals**.</span></span>
22. <span data-ttu-id="ce78f-132">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-132">Click **New**.</span></span>
23. <span data-ttu-id="ce78f-133">**Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="ce78f-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="ce78f-135">**Satırlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-135">Click **Lines**.</span></span>
26. <span data-ttu-id="ce78f-136">**İşlevler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-136">Click **Functions**.</span></span>
27. <span data-ttu-id="ce78f-137">**Fiş şablonu seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="ce78f-138">Daha önce oluşturduğunuz şablonu bulun.</span><span class="sxs-lookup"><span data-stu-id="ce78f-138">Find the template that you created earlier.</span></span> <span data-ttu-id="ce78f-139">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-139">Click **OK**.</span></span> <span data-ttu-id="ce78f-140">Başka şablonlar varsa, **Önceki adım**'a tıklayıp uygun şablonu seçmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="ce78f-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="ce78f-141">**Tutar** alanına, fişe uygulanacak tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="ce78f-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="ce78f-142">**Tutar** alanı yalnızca fiş şablonu türü Yüzde olduğu zaman görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ce78f-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="ce78f-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce78f-143">Click **OK**.</span></span>

