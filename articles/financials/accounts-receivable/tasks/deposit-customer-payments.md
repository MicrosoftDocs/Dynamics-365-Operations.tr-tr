---
title: Müşteri ödemelerini havale etme
description: Müşteri ödemelerini havale edin.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565497"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="04531-103">Müşteri ödemelerini havale etme</span><span class="sxs-lookup"><span data-stu-id="04531-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04531-104">Müşteri ödemelerini havale edin.</span><span class="sxs-lookup"><span data-stu-id="04531-104">Deposit customer payments.</span></span> <span data-ttu-id="04531-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="04531-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="04531-106">Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="04531-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="04531-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04531-107">Click New.</span></span>
3. <span data-ttu-id="04531-108">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="04531-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="04531-109">Ödeme günlüğünü seçin.</span><span class="sxs-lookup"><span data-stu-id="04531-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="04531-110">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04531-110">Click Lines.</span></span>
6. <span data-ttu-id="04531-111">Hesap alanında, bir ödemesini kaydettiğiniz Müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="04531-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="04531-112">Alacak alanına, ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="04531-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="04531-113">Tutarı boş bırakmayı ve ödenen faturaları seçerek hesaplamayı sistemin yapmasını tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04531-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="04531-114">Ödeme referansı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04531-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="04531-115">Ödeme referansı, girmekte olduğunuz ödemenin çek numarası olabilir.</span><span class="sxs-lookup"><span data-stu-id="04531-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="04531-116">Ödemenin havale makbuzuna eklenmesi için ödeme referansı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="04531-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="04531-117">Depozito makbuzu kullan kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="04531-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="04531-118">Ödeme depozitoya eklenecekse bu ayarı değiştirip Evet yapın.</span><span class="sxs-lookup"><span data-stu-id="04531-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="04531-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04531-119">Click New.</span></span>
11. <span data-ttu-id="04531-120">Hesap alanında, sonraki ödemenin Müşterisini seçin.</span><span class="sxs-lookup"><span data-stu-id="04531-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="04531-121">Alacak alanına, ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="04531-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="04531-122">Ödeme referansı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04531-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="04531-123">Depozito makbuzu kullan kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="04531-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="04531-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04531-124">Click Post.</span></span>
    * <span data-ttu-id="04531-125">Havale makbuzu oluşturulabilmesi için ödemelerin deftere nakledilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="04531-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="04531-126">Bu, havale makbuzu oluşturulduktan sonra ödemelerin değiştirilmediğinden emin olmak için yapılır.</span><span class="sxs-lookup"><span data-stu-id="04531-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="04531-127">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04531-127">Click Functions.</span></span>
17. <span data-ttu-id="04531-128">Havale makbuzu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04531-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="04531-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04531-129">Click OK.</span></span>
    * <span data-ttu-id="04531-130">Havale makbuzu oluşturmak için ilk sayfa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="04531-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="04531-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04531-131">Click OK.</span></span>
    * <span data-ttu-id="04531-132">İkinci adım havale makbuzunu yazdırmaktır, ancak bu adım zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="04531-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

