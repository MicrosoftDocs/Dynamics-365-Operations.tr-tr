---
title: Satıcı ödeme masraflarını tanımlama
description: Satıcı ödeme masraflarını ayarlayın.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 404bd1e22caa8098f114a2dcc67dd420509cce2b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140479"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="a3aeb-103">Satıcı ödeme masraflarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="a3aeb-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3aeb-104">Satıcı ödeme masraflarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-104">Set up vendor payment fees.</span></span> <span data-ttu-id="a3aeb-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a3aeb-106">Borç hesapları > Ödeme kurulumu > Ödeme masrafı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="a3aeb-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-107">Click New.</span></span>
3. <span data-ttu-id="a3aeb-108">Ücret Kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="a3aeb-109">Ücret kodu, bu ücretin ne zaman kullanılacağını açıklar (örneğin "EFT_Ücreti").</span><span class="sxs-lookup"><span data-stu-id="a3aeb-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="a3aeb-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a3aeb-111">Ücret açıklaması alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="a3aeb-112">Ücretin ne zaman atanacağı hakkında daha ayrıntılı bilgi vermek için bir açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="a3aeb-113">Masraf alanında Satıcı'yı veya Genel muhasebe'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="a3aeb-114">Ücret kuruluşunuza gider olarak yazılacaksa genel muhasebe kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="a3aeb-115">Ücret satıcıya kesilecekse Satıcı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="a3aeb-116">Ücretin gider olarak işleneceği bir ana hesap girin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="a3aeb-117">Bu seçenek, yalnızca, Masraf seçeneği olarak Genel muhasebe belirtildiği zaman kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="a3aeb-118">Bu ücretin kullanılabileceği günlüğü seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="a3aeb-119">Satıcı ödeme masrafı için, "Satıcıya ödeme" günlüğünü seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="a3aeb-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-120">Click Save.</span></span>
10. <span data-ttu-id="a3aeb-121">Ödeme masraf kurulumu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="a3aeb-122">Ücretin, seçtiğiniz günlükte ne zaman varsayılan değer alacağını tanımlamak için Ödeme masrafı kurulumuna geçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="a3aeb-123">Tablo'yu, Grup'u veya Tümü'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="a3aeb-124">Tablo tek bir banka hesabı seçmek için, Grup bir banka grubu seçmek için ve Tümü, bu ücret kurulumunun tüm banka hesaplarında kullanılması için kullanılır</span><span class="sxs-lookup"><span data-stu-id="a3aeb-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="a3aeb-125">Bir banka grubu veya banka hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="a3aeb-126">Aramada, Grup'u seçtiyseniz banka grubu, Tablo'yu seçtiyseniz banka hesapları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="a3aeb-127">Bu ücretin ne zaman kesileceğini belirlemek için ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="a3aeb-128">Seçili ödeme yöntemi için Ödeme belirtimini seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="a3aeb-129">Ödeme belirtimi, elektronik fon transferli ödeme yöntemleriyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="a3aeb-130">Ücretin yüzde mi, tutar mı, yoksa aralık mı olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="a3aeb-131">Ücretin yüzdesini veya tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="a3aeb-132">Ücret bir yüzde ise, yüzdeyi girin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="a3aeb-133">Ücret bir tutarsa, ücretin tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="a3aeb-134">Ücret bir aralıksa, katmanlı ücretleri tanımlamak için Aralık sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="a3aeb-135">Ücret para birimi alanında, ücretin kesileceği para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="a3aeb-136">Ücretin para birimi.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-136">This currency is for the fee.</span></span> <span data-ttu-id="a3aeb-137">Ödeme para birimi, ödemenin para birimine göre ücret kuralının ne zaman yürürlüğe gireceğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="a3aeb-138">Örneğin, bankanız avro olarak yapılan ödemeden bir ücret keserken, diğer ödemelerin hiçbirine ücret kesmeyebilir.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="a3aeb-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3aeb-139">Click Save.</span></span>

