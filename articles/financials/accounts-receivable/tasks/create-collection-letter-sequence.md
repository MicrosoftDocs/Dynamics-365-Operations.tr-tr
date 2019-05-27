---
title: Tahsilat mektubu sırası oluşturma
description: Tahsilat mektubu sırası oluşturmak için bu görev kılavuzunu kullanın.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567456"
---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="4b2ac-103">Tahsilat mektubu sırası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4b2ac-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b2ac-104">Tahsilat mektubu sırası oluşturmak için bu görev kılavuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="4b2ac-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="4b2ac-106">Alacak ve tahsilatlar > Kurulum > Tahsilat mektubu sırasını ayarla'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="4b2ac-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-107">Click New.</span></span>
3. <span data-ttu-id="4b2ac-108">Tahsilat mektubu sırası alanında, sırayı temsil edecek bir sıra kodu girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="4b2ac-109">Bir deftere nakil profili ayarladığınız zaman kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="4b2ac-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4b2ac-111">Ödeme şartları isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-111">The terms of payment is optional.</span></span> <span data-ttu-id="4b2ac-112">Buraya bir değer girerseniz, tahsilat mektubu ücreti faturasında, müşteriyle depolanan ödeme şartları yerine bu ödeme şartları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="4b2ac-113">Tahsilat mektubu kodu alanında, göndermek istediğiniz ilk tahsilat mektubunun kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="4b2ac-114">İlk tahsilat mektubu, faturadaki vade tarihine, bu satırdaki Gün alanında mehil süresi için girdiğiniz değere ve bu satıra girdiğiniz diğer bilgilere göre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="4b2ac-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4b2ac-116">Ücretin para birimi, müşteri para biriminin varsayılan değeri olur.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="4b2ac-117">Bu para birimi kodu, fatura para biriminden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="4b2ac-118">Sırada gönderilecek sonraki tahsilat mektubunu eklemek için Ekle'ye tıklayın</span><span class="sxs-lookup"><span data-stu-id="4b2ac-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="4b2ac-119">Çoğu durumda, ilk tahsilat mektubu yalnızca bir uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="4b2ac-120">Gerekirse ücretler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="4b2ac-121">Tahsilat mektubu kodu alanında, sıradaki gönderilecek sonraki tahsilat mektubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="4b2ac-122">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="4b2ac-123">Ana hesap alanında, ücretler için kullanılacak gelir hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="4b2ac-124">Bu tahsilat mektubu deftere nakledilince yansıtılacak ücreti girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="4b2ac-125">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="4b2ac-126">Ücret üzerinden satış vergileri hesaplamak gerekiyorsa bir madde satış vergisi grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="4b2ac-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4b2ac-128">Tahsilat mektubu gönderilmeden önce gereken minimum vadesi geçmiş bakiyeyi girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="4b2ac-129">İzin vereceğiniz mehil süresi gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="4b2ac-130">Bu, bir tahsilat mektubunun oluşturulabileceği son tarihten sonraki gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="4b2ac-131">Hesaplama için kullanılan vade tarihi, tahsilat mektubunun tahsilat mektubu sırasındaki konumuna bağlıdır:   ⦁    Tahsilat mektubu 1 için mehil süresi, faturadaki vade tarihine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="4b2ac-132">⦁ Tahsilat mektubu 2 ve sonraki tahsilat mektupları için mehil süresi, Alacak hesapları parametreleri sayfasının Tahsilat mektubu kodunu güncelleştir alanındaki seçime bağlı olarak, önceki tahsilat mektubunun deftere nakledildiği veya yazdırıldığı tarihe göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="4b2ac-133">Sıradaki son tahsilat mektubunu eklemek için Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="4b2ac-134">Bir tahsilat mektubu sırası için en fazla beş tahsilat mektubu kodu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="4b2ac-135">Tahsilat mektubu kodu alanında, sıradaki gönderilecek sonraki tahsilat mektubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="4b2ac-136">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="4b2ac-137">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="4b2ac-138">Para birimi cinsinden ücret alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="4b2ac-139">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="4b2ac-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="4b2ac-141">Minimum vadesi geçmiş bakiye alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="4b2ac-142">Gün alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="4b2ac-143">Müşterinin ek teslimat ve faturalamalarını durdurmak için bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="4b2ac-144">Hesap üzerindeki engeli kaldırmak için Müşteriler sayfasındaki Faturalama ve beklemedeki teslimat alanında Hayır seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="4b2ac-145">Not hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="4b2ac-146">Seçili tahsilat mektubu kodu için tahsilat mektubunda görünecek metni girin.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="4b2ac-147">Not kutusunun yukarısındaki Çeviriler menüsünü kullanarak bu metni birden fazla dile çevirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  

