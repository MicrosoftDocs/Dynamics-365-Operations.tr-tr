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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11e006e41f467a594521dfc601f46b4d1b492ce5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982970"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="9c491-103">Belgelerde satış vergisi hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9c491-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c491-104">Belgelerdeki satış vergisi, belge satırlarında birer Satış vergisi grubu ve Madde satış vergisi grubu belirtilerek hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9c491-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="9c491-105">Bu verilerin varsayılan değerleri ana verilerden alınabilir, ancak gerekirse el ile değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9c491-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="9c491-106">Hesaplanan satış vergisi satır ve belge düzeyinde denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9c491-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="9c491-107">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9c491-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9c491-108">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9c491-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9c491-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-109">Click New.</span></span>
3. <span data-ttu-id="9c491-110">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9c491-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9c491-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9c491-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9c491-113">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9c491-113">Click OK.</span></span>
7. <span data-ttu-id="9c491-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9c491-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="9c491-115">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="9c491-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9c491-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9c491-117">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9c491-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="9c491-118">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="9c491-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="9c491-119">Kurulum sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9c491-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="9c491-120">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="9c491-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="9c491-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9c491-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9c491-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="9c491-123">Finansal öğeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-123">Click Financials.</span></span>
17. <span data-ttu-id="9c491-124">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-124">Click Sales tax.</span></span>
18. <span data-ttu-id="9c491-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-125">Click OK.</span></span>
19. <span data-ttu-id="9c491-126">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-126">Click Add line.</span></span>
20. <span data-ttu-id="9c491-127">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9c491-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="9c491-128">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="9c491-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="9c491-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9c491-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="9c491-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="9c491-131">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9c491-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="9c491-132">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="9c491-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="9c491-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9c491-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="9c491-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="9c491-135">Eylem Bölmesinde, Satış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="9c491-136">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-136">Click Sales tax.</span></span>
30. <span data-ttu-id="9c491-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9c491-137">Click OK.</span></span>

