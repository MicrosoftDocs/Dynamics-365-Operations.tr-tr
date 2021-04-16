---
title: İleri tarih atılmış çekleri ayarlama
description: Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adb8b969a6e86becaa3c0a3b59d8f8f259e5a64
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834608"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="d1c49-103">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="d1c49-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1c49-104">Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d1c49-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="d1c49-105">Ayrıca, verilen çekler, alınan çekler ve stopaj vergisi takas hesaplarını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1c49-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="d1c49-106">Gelecekte ödeme yapmak veya almak için çıkartılan vadeli çekler.</span><span class="sxs-lookup"><span data-stu-id="d1c49-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="d1c49-107">Çekin hesap defterlerinde, vade tarihinden önce yansıtılmasına gerek olup olmadığını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1c49-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="d1c49-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="d1c49-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="d1c49-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d1c49-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="d1c49-110">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="d1c49-110">Set up postdated checks</span></span>
1. <span data-ttu-id="d1c49-111">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="d1c49-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="d1c49-112">Vadeli çekler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="d1c49-113">Vadeli çekleri etkinleştirin onay kutusunu işaretleyin veya işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="d1c49-114">Vadeli çekler için defter girişlerini nakletme onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="d1c49-115">Verilen çekler için takas hesabı alanında için istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="d1c49-116">Alınan çekler için takas hesabı alanında için istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="d1c49-117">Takas girişleri yevmiye defterine, bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="d1c49-118">İleri tarih atılmış çekleri bu satıcı ödeme günlüğüne transfer et alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="d1c49-119">Stopaj vergisi takas hesabı alanına, istediğiniz değerleri belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="d1c49-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-120">Click Save.</span></span>
11. <span data-ttu-id="d1c49-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-121">Close the page.</span></span>
12. <span data-ttu-id="d1c49-122">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="d1c49-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-123">Click New.</span></span>
14. <span data-ttu-id="d1c49-124">Ödeme yöntemi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="d1c49-125">Çek miktarının takas hesabına nakledildiğini belirtmek için vadeli hesap takas nakli seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="d1c49-126">Hesap türü alanında "Banka"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="d1c49-127">Ödeme yönteminin mahsup hesabı bir banka olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d1c49-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="d1c49-128">Ödeme hesabı alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="d1c49-129">Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="d1c49-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="d1c49-130">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-130">Click Save.</span></span>
19. <span data-ttu-id="d1c49-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d1c49-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]