--- 
title: "Müşteri ödeme koşulları oluşturma"
description: "Bu prosedürde bir nakit iskontosu ve vade tarihi kurulumu tanımlanmaktadır."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4e0e43962bea3ff1c3adafa73da4ce3862963a51
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="41d3a-103">Müşteri ödeme koşulları oluşturma</span><span class="sxs-lookup"><span data-stu-id="41d3a-103">Establish customer payment terms</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41d3a-104">Bu prosedürde bir nakit iskontosu ve vade tarihi kurulumu tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="41d3a-105">Bu görev kılavuzunda USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="41d3a-106">Alacak hesapları > Ödemeler >kurulumu > Ödeme günleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="41d3a-107">Ödeme şartları için kurulum, Alacak hesapları ve Borç hesapları için paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="41d3a-108">Bunu modül içinde tanımlarsanız, diğer modülde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="41d3a-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="41d3a-109">Bu görev kılavuzu için, tüm ödeme şartlarını Alacak hesapları altına aldım.</span><span class="sxs-lookup"><span data-stu-id="41d3a-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="41d3a-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-110">Click New.</span></span>
    * <span data-ttu-id="41d3a-111">Ödeme şartlarınız haftanın belirli bir gününü (Pazartesi, Salı vb.) veya ayın belirli bir tarihini (5'i, 6'sı vb.) gerektiriyorsa bir ödeme günü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="41d3a-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="41d3a-112">Ödeme günü alanına, ödeme günü alanındaki Ödeme günü için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="41d3a-113">Açıklama alanına, ödeme günü için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="41d3a-114">Hafta/Ay alanında ya Hafta'yı veya Ay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="41d3a-115">Haftanın bir gününü girmek istiyorsanız (örneğin Pazartesi), Hafta'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="41d3a-116">Ay içinde bir tarih girmek istiyorsanız (örneğin ayın 10'), Ay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="41d3a-117">Bu örnek için Ay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="41d3a-118">Ayın günü alanına tarih girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="41d3a-119">Tarih bir sayı olarak girilmelidir (örneğin "10"; yani "10'u" değil).</span><span class="sxs-lookup"><span data-stu-id="41d3a-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="41d3a-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-120">Click Save.</span></span>
8. <span data-ttu-id="41d3a-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-121">Close the page.</span></span>
9. <span data-ttu-id="41d3a-122">Alacak hesapları > Ödemeler kurulumu > Ödeme şartları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="41d3a-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-123">Click New.</span></span>
    * <span data-ttu-id="41d3a-124">Ödeme şartları, vade tarihlerinin nasıl hesaplanacağını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="41d3a-125">Nakit iskontosu tarihi kurulumu ayrı bir sayfada tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="41d3a-126">Ödeme şartları alanına, Ödeme şartları için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="41d3a-127">Açıklama alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="41d3a-128">Ödeme yöntemi (örneğin TÖ, Net, Geçerli ay vb.) seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="41d3a-129">Ödeme yöntemi, vade tarihi hesaplamasında başlangıcı tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="41d3a-130">Örneğin, vade tarihi, fatura tarihinden sonra mutlaka bir dizi ay veya gün sayısıysa Net kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="41d3a-131">Fatura üzerine ödeme gerekiyorsa TÖ kullanılabilir ve böylece vade tarihi hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="41d3a-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="41d3a-132">Bu görev kılavuzu için Geçerli ay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="41d3a-133">Hesaplamaya belirli bir hafta günü veya tarih eklendiyse bir Ödeme tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="41d3a-134">Ödeme şartlarınıza bağlı olarak bir tutarı Ay veya Gün olarak girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41d3a-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="41d3a-135">Veya, Ödeme yönteminin sonuna 'eklemek' için Ödeme planını veya Ödeme gününü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41d3a-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="41d3a-136">Vade tarihi daima sonraki ayın 10'u olacaksa Ödeme günü olarak 10'unu seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="41d3a-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-137">Click Save.</span></span>
16. <span data-ttu-id="41d3a-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-138">Close the page.</span></span>
17. <span data-ttu-id="41d3a-139">Alacak hesapları > Ödemeler kurulumu > Nakit iskontoları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="41d3a-140">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-140">Click New.</span></span>
    * <span data-ttu-id="41d3a-141">Bu sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41d3a-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="41d3a-142">Nakit iskontosu alanına, nakit iskontosu için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="41d3a-143">Açıklama alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="41d3a-144">Katmanlı bir nakit iskontosu varsa, bu yeni nakit iskontosundan sonra ilgili Sonraki iskonto kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="41d3a-145">Nakit iskontosu tarihini hesaplamak için kullanılacak gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-145">Enter the number of days used to calculate the cash dicount date.</span></span>
    * <span data-ttu-id="41d3a-146">Net ilkesi seçilirse, nakit iskontosu tarihini hesaplamak için fatura tarihine gün sayısı eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="41d3a-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="41d3a-147">Nakit iskontosunun yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="41d3a-148">Müşteri faturaları için nakit iskontosunun nakledileceği ana hesabı girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="41d3a-149">İskonto mahsup hesapları alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="41d3a-150">"Fatura satırlarındaki hesaplar"ı seçerseniz, nakit iskontosu, satıcı faturası satırlarındaki aynı kıymet/gider ana hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="41d3a-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="41d3a-151">"Satıcı faturaları için ana hesabı kullan"ı seçerseniz, nakit iskontosu, "Satıcı faturaları için ana hesap"ta tanımladığınız ana hesaba nakledilir.</span><span class="sxs-lookup"><span data-stu-id="41d3a-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="41d3a-152">Bu örnek için, "Satıcı faturaları için ana hesabı kullan"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="41d3a-153">Satıcı faturaları için nakit iskontosunun nakledileceği ana hesabı girin.</span><span class="sxs-lookup"><span data-stu-id="41d3a-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="41d3a-154">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41d3a-154">Click Save.</span></span>


