---
title: Müşteri ödeme yöntemi oluşturma
description: Müşteri ödemeleri için bir ödeme yöntemi oluşturun.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 477f1ff72fd8012c3403d22aa128d97e45d5559f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842917"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="72701-103">Müşteri ödeme yöntemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="72701-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72701-104">Müşteri ödemeleri için bir ödeme yöntemi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="72701-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="72701-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="72701-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="72701-106">Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="72701-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="72701-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72701-107">Click New.</span></span>
3. <span data-ttu-id="72701-108">Ödeme yöntemi alanına, ödeme yöntemi için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="72701-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="72701-109">Ödeme yöntemi kodu faturalarda ve ödemelerde gösterilir ve bu sayede, kaydedilmekte olan ödemenin türü ve ödeme yapılacak banka hesabının yeterince anlaşılması sağlanır.</span><span class="sxs-lookup"><span data-stu-id="72701-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="72701-110">Açıklama alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="72701-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="72701-111">Ödemelerin nakledilmesi için gereken ödeme durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="72701-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="72701-112">Bir müşteri ödemesi oluşturulurken, yalnızca, ödeme durumu burada tanımladığınız ödeme durumuyla eşleştiği zaman nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="72701-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="72701-113">Faturalar için müşteri ödemelerinin nasıl oluşturulacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="72701-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="72701-114">Bu seçenek, yalnızca bir ödeme teklifi çalıştırılırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="72701-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="72701-115">Doğrudan ödemeler yapılırken ve müşterilerin banka hesaplarından fonlar çekilirken müşteri ödemeleri için bir ödeme teklifi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="72701-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="72701-116">Ödeme türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="72701-116">Select the type of payment.</span></span>
    * <span data-ttu-id="72701-117">Ödeme türü, ödemede bazı doğrulamalar yapılıp yapılmayacağını belirlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="72701-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="72701-118">Ödemelerin nakledileceği hesap türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="72701-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="72701-119">Genellikle bu seçenek için Banka seçili olacaktır.</span><span class="sxs-lookup"><span data-stu-id="72701-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="72701-120">Bu ödemenin kaydedileceği banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="72701-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="72701-121">Bankanızın kullandığı ödeme türünü tanımak için Banka hareketi türünü girin.</span><span class="sxs-lookup"><span data-stu-id="72701-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="72701-122">Banka hareket türü, banka mutabakat işlemi sırasında kullanılır ve mutabakatı kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="72701-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="72701-123">Bu ödemenin geçici olarak bir bağlantılı hesaba nakledilip nakledilmeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="72701-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="72701-124">Ödemenin bankadan çekilmesinde kasa devri zamanını denemek istiyorsanız Bağlantı işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72701-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="72701-125">Ödeme bankadan çekilene kadar (ödemenin burada tanımladığınız banka hesabına geçtiği zamana kadar) geçici olarak bir Genel muhasebe hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="72701-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="72701-126">Bağlantılı nakil için kullanılacak ana hesabı girin.</span><span class="sxs-lookup"><span data-stu-id="72701-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="72701-127">Bu, bağlantı kullanıldığı zaman ödemenin geçici olarak nakledileceği ana hesaptır.</span><span class="sxs-lookup"><span data-stu-id="72701-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="72701-128">Elektronik ödemelere ilişkin ayarı tanımlamak için Dosya biçimi sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72701-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="72701-129">Zorunlu alanlar tanımlamak için Ödeme kontrolü sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72701-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="72701-130">Örneğin, bu ödeme yöntemiyle yapılan tüm ödemelerin yatırılmasını zorunlu kılıyorsanız, o seçeneği bu sekmede seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72701-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="72701-131">Bu ödeme yönteminde kullanmak istediğiniz ödeme özniteliklerini tanımlamak için Ödeme öznitelikleri sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72701-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="72701-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72701-132">Click Save.</span></span>

