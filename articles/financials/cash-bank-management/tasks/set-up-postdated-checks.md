---
title: İleri tarih atılmış çekleri ayarlama
description: Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8696aeccee651368a036ab8d90980e9ed9cea6b3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841885"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="4e642-103">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="4e642-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e642-104">Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4e642-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="4e642-105">Ayrıca, verilen çekler, alınan çekler ve stopaj vergisi takas hesaplarını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e642-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="4e642-106">Gelecekte ödeme yapmak veya almak için çıkartılan vadeli çekler.</span><span class="sxs-lookup"><span data-stu-id="4e642-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="4e642-107">Çekin hesap defterlerinde, vade tarihinden önce yansıtılmasına gerek olup olmadığını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e642-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="4e642-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="4e642-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="4e642-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4e642-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="4e642-110">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="4e642-110">Set up postdated checks</span></span>
1. <span data-ttu-id="4e642-111">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="4e642-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="4e642-112">Vadeli çekler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e642-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="4e642-113">Vadeli çekleri etkinleştirin onay kutusunu işaretleyin veya işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="4e642-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="4e642-114">Vadeli çekler için defter girişlerini nakletme onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="4e642-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="4e642-115">Verilen çekler için takas hesabı alanında için istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e642-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="4e642-116">Alınan çekler için takas hesabı alanında için istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e642-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="4e642-117">Takas girişleri yevmiye defterine, bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4e642-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="4e642-118">İleri tarih atılmış çekleri bu satıcı ödeme günlüğüne transfer et alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4e642-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="4e642-119">Stopaj vergisi takas hesabı alanına, istediğiniz değerleri belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4e642-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="4e642-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e642-120">Click Save.</span></span>
11. <span data-ttu-id="4e642-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e642-121">Close the page.</span></span>
12. <span data-ttu-id="4e642-122">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4e642-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="4e642-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e642-123">Click New.</span></span>
14. <span data-ttu-id="4e642-124">Ödeme yöntemi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4e642-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="4e642-125">Çek miktarının takas hesabına nakledildiğini belirtmek için vadeli hesap takas nakli seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4e642-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="4e642-126">Hesap türü alanında "Banka"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e642-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="4e642-127">Ödeme yönteminin mahsup hesabı bir banka olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4e642-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="4e642-128">Ödeme hesabı alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e642-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="4e642-129">Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="4e642-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="4e642-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e642-130">Close the page.</span></span>
19. <span data-ttu-id="4e642-131">Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="4e642-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="4e642-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e642-132">Click New.</span></span>
21. <span data-ttu-id="4e642-133">Ödeme yöntemi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4e642-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="4e642-134">Çek miktarının takas hesabına nakledildiğini belirtmek için vadeli hesap takas nakli seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4e642-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="4e642-135">Hesap türü alanında "Banka"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e642-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="4e642-136">Ödeme yönteminin mahsup hesabı bir banka olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4e642-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="4e642-137">Ödeme hesabı alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e642-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="4e642-138">Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="4e642-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="4e642-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e642-139">Close the page.</span></span>

