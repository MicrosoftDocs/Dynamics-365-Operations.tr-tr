---
title: Müşteri ödemelerini havale etme
description: Müşteri ödemelerini havale edin.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bf44570a0eaceab94765b100bdd8b4d507a0f54
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822383"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="59ccf-103">Müşteri ödemelerini havale etme</span><span class="sxs-lookup"><span data-stu-id="59ccf-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59ccf-104">Müşteri ödemelerini havale edin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-104">Deposit customer payments.</span></span> <span data-ttu-id="59ccf-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="59ccf-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="59ccf-106">**Gezinti bölmesi Modüller > Alacak hesapları > Ödemeler > Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="59ccf-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-107">Select **New**.</span></span>
3. <span data-ttu-id="59ccf-108">**Ad** alanında, açılan menüden **CustPay**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="59ccf-109">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-109">Select **Lines**.</span></span>
5. <span data-ttu-id="59ccf-110">**Hesap** alanında, bir ödemesini kaydettiğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="59ccf-111">**Alacak** alanına, ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="59ccf-112">Tutarı boş bırakmayı ve ödenen faturaları seçerek hesaplamayı sistemin yapmasını tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59ccf-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="59ccf-113">**Ödeme referansı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="59ccf-114">Ödeme referansı, girmekte olduğunuz ödemenin çek numarası olabilir.</span><span class="sxs-lookup"><span data-stu-id="59ccf-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="59ccf-115">Ödemenin havale makbuzuna eklenmesi için ödeme referansı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="59ccf-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="59ccf-116">Depozito makbuzu kullan kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="59ccf-117">Ödeme depozitoya eklenecekse bu ayarı değiştirip Evet yapın.</span><span class="sxs-lookup"><span data-stu-id="59ccf-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="59ccf-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-118">Select **New**.</span></span>
10. <span data-ttu-id="59ccf-119">**Hesap** alanında, sonraki ödemenin müşterisini seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="59ccf-120">**Alacak** alanına, ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="59ccf-121">**Ödeme referansı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="59ccf-122">**Depozito makbuzu kullan** kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="59ccf-123">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-123">Select **Post**.</span></span> <span data-ttu-id="59ccf-124">Havale makbuzu oluşturulabilmesi için ödemelerin deftere nakledilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="59ccf-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="59ccf-125">Bu, havale makbuzu oluşturulduktan sonra ödemelerin değiştirilmediğinden emin olmak için yapılır.</span><span class="sxs-lookup"><span data-stu-id="59ccf-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="59ccf-126">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-126">Select **Functions**.</span></span>
16. <span data-ttu-id="59ccf-127">**Havale makbuzu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="59ccf-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-128">Select **OK**.</span></span> <span data-ttu-id="59ccf-129">Havale makbuzu oluşturmak için ilk sayfa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="59ccf-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="59ccf-130">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="59ccf-130">Select **OK**.</span></span> <span data-ttu-id="59ccf-131">İkinci adım havale makbuzunu yazdırmaktır, ancak bu adım zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="59ccf-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]