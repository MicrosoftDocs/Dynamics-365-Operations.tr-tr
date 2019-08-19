---
title: Müşteri ödeme masrafları oluşturma
description: Müşteri ödemeleri için ödeme masrafları oluşturun.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f18b88cfdeef2e66003cd4411ace4b4c49e42f6f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834451"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="8d5c2-103">Müşteri ödeme masrafları oluşturma</span><span class="sxs-lookup"><span data-stu-id="8d5c2-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d5c2-104">Müşteri ödemeleri için ödeme masrafları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="8d5c2-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8d5c2-106">Alacak hesapları > Ödemeler kurulumu > Ödeme masrafı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="8d5c2-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-107">Click New.</span></span>
3. <span data-ttu-id="8d5c2-108">Ücret Kodu alanına bir ücret kodu girin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="8d5c2-109">Ödeme günlüklerinde görüntülenen ücret kodu, yazılan ücretin ne ücreti olduğunu anlaşılır kılar.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="8d5c2-110">Ad alanına bir ücret adı girin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="8d5c2-111">Ücret açıklaması alanına ücret için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="8d5c2-112">Ücretin Müşteriye mi, yoksa bir Genel muhasebe hesabına mı çıkarılacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="8d5c2-113">Ücret müşteriye yazılacaksa, Müşteri'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="8d5c2-114">Ücret kuruluşunuza gider olarak yazılacaksa, Genel muhasebe'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="8d5c2-115">Bu görev için Müşteri'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="8d5c2-116">Bu ödeme masrafının kullanılabileceği günlük türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="8d5c2-117">Bu ücretler müşteri ödemeleri için kullanılıyorsa, günlük türü büyük olasılıkla Müşteri ödemesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="8d5c2-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-118">Click Save.</span></span>
9. <span data-ttu-id="8d5c2-119">Ödeme masraf kurulumu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="8d5c2-120">Ödeme masrafı kurulumu, ödeme ücreti yazılırken kullanılacak ölçütleri tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="8d5c2-121">Örneğin, banka hesabı USMF OPER ve ödeme yöntemi çek olduğu zaman ücretin hesaplanacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="8d5c2-122">Bu ücret için kullanılabilecek banka hesaplarını tanımlamak için Tablo'yu, Grup'u veya Tümü'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="8d5c2-123">Tümü'nü seçerseniz, bu ücret tüm banka hesaplarına yatırılabilir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="8d5c2-124">Tablo'yu seçerseniz, yalnızca seçtiğiniz banka hesabı bu ücret için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="8d5c2-125">Grup'u seçerseniz, bu ücret için yalnızca seçili banka grubundaki banka hesapları kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="8d5c2-126">Bir banka grubu veya banka hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="8d5c2-127">Tablo'yu seçtiyseniz, aramada banka hesapları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="8d5c2-128">Grup'u seçtiyseniz, aramada banka grupları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="8d5c2-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8d5c2-130">Bu ücretin atanacağı Ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="8d5c2-131">Örneğin, ödemeleri elektronik ödeme yerine çekle gönderen müşterilerinize bir ücret ödetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="8d5c2-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8d5c2-133">Uygunsa, ödeme para birimi girin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="8d5c2-134">Ödeme para birimi, ücret alınıp alınmayacağını belirlemede ek bir ölçüt olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="8d5c2-135">Örneğin, bankanız normalde avro para birimiyle işlem yaptığı için, ABD doları para birimiyle alınan ödemeler için ek bir ücret talep edebilir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="8d5c2-136">Ücretin yüzde mi, tutar mı, yoksa aralık mı olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="8d5c2-137">Ücretin yüzdesini veya tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="8d5c2-138">Yüzde/Tutar alanı Yüzde'yse, buraya girilen değer bir yüzde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="8d5c2-139">Yüzde/Tutar alanı Tutar'sa, buraya girdiğiniz değer bir tutar olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="8d5c2-140">Yüzde/Tutar alanı Aralık'sa, katmanları tanımlamak için Aralık sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="8d5c2-141">Ücret para birimi alanında Ücretin para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="8d5c2-142">Bu, ücretin oluşturulacağı para birimidir.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="8d5c2-143">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-143">Click Save.</span></span>

