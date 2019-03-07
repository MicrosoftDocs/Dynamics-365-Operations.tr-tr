---
title: Belgelerde satış vergisi hareketleri oluşturma
description: Belgelerdeki satış vergisi, belge satırlarında birer Satış vergisi grubu ve Madde satış vergisi grubu belirtilerek hesaplanır.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02e3ea556da9abefd37ce585086241d1e45aa0fa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "313233"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="ba77c-103">Belgelerde satış vergisi hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba77c-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba77c-104">Belgelerdeki satış vergisi, belge satırlarında birer Satış vergisi grubu ve Madde satış vergisi grubu belirtilerek hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ba77c-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="ba77c-105">Bu verilerin varsayılan değerleri ana verilerden alınabilir, ancak gerekirse el ile değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ba77c-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="ba77c-106">Hesaplanan satış vergisi satır ve belge düzeyinde denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ba77c-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="ba77c-107">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ba77c-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ba77c-108">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ba77c-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-109">Click New.</span></span>
3. <span data-ttu-id="ba77c-110">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ba77c-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ba77c-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ba77c-113">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-113">Click OK.</span></span>
7. <span data-ttu-id="ba77c-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ba77c-115">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ba77c-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ba77c-117">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="ba77c-118">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="ba77c-119">Kurulum sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="ba77c-120">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="ba77c-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ba77c-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ba77c-123">Finansal öğeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-123">Click Financials.</span></span>
17. <span data-ttu-id="ba77c-124">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-124">Click Sales tax.</span></span>
18. <span data-ttu-id="ba77c-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-125">Click OK.</span></span>
19. <span data-ttu-id="ba77c-126">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-126">Click Add line.</span></span>
20. <span data-ttu-id="ba77c-127">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="ba77c-128">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="ba77c-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="ba77c-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="ba77c-131">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="ba77c-132">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="ba77c-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba77c-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="ba77c-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="ba77c-135">Eylem Bölmesinde, Satış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="ba77c-136">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-136">Click Sales tax.</span></span>
30. <span data-ttu-id="ba77c-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba77c-137">Click OK.</span></span>

