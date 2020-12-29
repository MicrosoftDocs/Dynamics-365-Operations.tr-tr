---
title: Müşteri ödemelerini havale etme
description: Müşteri ödemelerini havale edin.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448807"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="6a099-103">Müşteri ödemelerini havale etme</span><span class="sxs-lookup"><span data-stu-id="6a099-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a099-104">Müşteri ödemelerini havale edin.</span><span class="sxs-lookup"><span data-stu-id="6a099-104">Deposit customer payments.</span></span> <span data-ttu-id="6a099-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6a099-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6a099-106">**Gezinti bölmesi Modüller > Alacak hesapları > Ödemeler > Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6a099-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="6a099-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-107">Select **New**.</span></span>
3. <span data-ttu-id="6a099-108">**Ad** alanında, açılan menüden **CustPay**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="6a099-109">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-109">Select **Lines**.</span></span>
5. <span data-ttu-id="6a099-110">**Hesap** alanında, bir ödemesini kaydettiğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="6a099-111">**Alacak** alanına, ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="6a099-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="6a099-112">Tutarı boş bırakmayı ve ödenen faturaları seçerek hesaplamayı sistemin yapmasını tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a099-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="6a099-113">**Ödeme referansı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6a099-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="6a099-114">Ödeme referansı, girmekte olduğunuz ödemenin çek numarası olabilir.</span><span class="sxs-lookup"><span data-stu-id="6a099-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="6a099-115">Ödemenin havale makbuzuna eklenmesi için ödeme referansı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6a099-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="6a099-116">Depozito makbuzu kullan kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6a099-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="6a099-117">Ödeme depozitoya eklenecekse bu ayarı değiştirip Evet yapın.</span><span class="sxs-lookup"><span data-stu-id="6a099-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="6a099-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-118">Select **New**.</span></span>
10. <span data-ttu-id="6a099-119">**Hesap** alanında, sonraki ödemenin müşterisini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="6a099-120">**Alacak** alanına, ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="6a099-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="6a099-121">**Ödeme referansı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6a099-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="6a099-122">**Depozito makbuzu kullan** kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6a099-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="6a099-123">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-123">Select **Post**.</span></span> <span data-ttu-id="6a099-124">Havale makbuzu oluşturulabilmesi için ödemelerin deftere nakledilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a099-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="6a099-125">Bu, havale makbuzu oluşturulduktan sonra ödemelerin değiştirilmediğinden emin olmak için yapılır.</span><span class="sxs-lookup"><span data-stu-id="6a099-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="6a099-126">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-126">Select **Functions**.</span></span>
16. <span data-ttu-id="6a099-127">**Havale makbuzu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="6a099-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-128">Select **OK**.</span></span> <span data-ttu-id="6a099-129">Havale makbuzu oluşturmak için ilk sayfa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6a099-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="6a099-130">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a099-130">Select **OK**.</span></span> <span data-ttu-id="6a099-131">İkinci adım havale makbuzunu yazdırmaktır, ancak bu adım zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="6a099-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

