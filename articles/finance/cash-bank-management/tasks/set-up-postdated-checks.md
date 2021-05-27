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
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026217"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="fb75a-103">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="fb75a-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb75a-104">Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fb75a-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="fb75a-105">Ayrıca, verilen çekler, alınan çekler ve stopaj vergisi takas hesaplarını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb75a-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="fb75a-106">Gelecekte ödeme yapmak veya almak için çıkartılan vadeli çekler.</span><span class="sxs-lookup"><span data-stu-id="fb75a-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="fb75a-107">Çekin hesap defterlerinde, vade tarihinden önce yansıtılmasına gerek olup olmadığını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb75a-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="fb75a-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="fb75a-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="fb75a-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fb75a-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="fb75a-110">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="fb75a-110">Set up postdated checks</span></span>
1. <span data-ttu-id="fb75a-111">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="fb75a-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="fb75a-112">Vadeli çekler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="fb75a-113">Vadeli çekleri etkinleştirin onay kutusunu işaretleyin veya işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="fb75a-114">Vadeli çekler için defter girişlerini nakletme onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="fb75a-115">Verilen çekler için takas hesabı alanında için istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="fb75a-116">Alınan çekler için takas hesabı alanında için istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="fb75a-117">Takas girişleri yevmiye defterine, bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="fb75a-118">İleri tarih atılmış çekleri bu satıcı ödeme günlüğüne transfer et alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="fb75a-119">Stopaj vergisi takas hesabı alanına, istediğiniz değerleri belirleyin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="fb75a-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-120">Click Save.</span></span>
11. <span data-ttu-id="fb75a-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-121">Close the page.</span></span>
12. <span data-ttu-id="fb75a-122">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="fb75a-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-123">Click New.</span></span>
14. <span data-ttu-id="fb75a-124">Ödeme yöntemi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="fb75a-125">Çek miktarının takas hesabına nakledildiğini belirtmek için vadeli hesap takas nakli seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="fb75a-126">Hesap türü alanında "Banka"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="fb75a-127">Ödeme yönteminin mahsup hesabı bir banka olacaktır.</span><span class="sxs-lookup"><span data-stu-id="fb75a-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="fb75a-128">Ödeme hesabı alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="fb75a-129">Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="fb75a-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="fb75a-130">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-130">Click Save.</span></span>
19. <span data-ttu-id="fb75a-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="fb75a-132">Oturum tarihi, vade tarihinden büyük veya bu tarihe eşit olduğunda, bir banka hesabına ileri tarihli bir çek nakledebilmek için, **Ödeme günlüğünü naklinin banka hesabına yatırılan ileri tarihli çeklerle vade tarihi doğrulaması** özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fb75a-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="fb75a-133">Bu özellik, oturum tarihi vade tarihine eşit veya bun tarihten büyük olduğunda satıcılar veya müşteriler için ödeme günlüklerini deftere nakletmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb75a-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="fb75a-134">**Ödeme yöntemi**'ni ayarlarken ( **Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri**), **Bağlantılı hesap** alanını doldurmayın.</span><span class="sxs-lookup"><span data-stu-id="fb75a-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="fb75a-135">Bu durumda, mahsup hesap, **Ödeme yöntemi**'nde ayarlanan banka hesabıyla doldurulur.</span><span class="sxs-lookup"><span data-stu-id="fb75a-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="fb75a-136">Özellik etkinleştirildiğinde ve oturum tarihi vade tarihinden erken bir tarihteyse, ödeme günlüğü deftere nakledilirken şu hata iletisi görüntülenir: "Mahsup hesap türü Banka ise, vade tarihinin oturum tarihine eşit veya bu tarihten erken olması gerekir".</span><span class="sxs-lookup"><span data-stu-id="fb75a-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="fb75a-137">Özellik etkinleştirilmemişse, oturum tarihi vade tarihinden erken olduğunda ödeme günlüğünü ileri tarihli bir çekle deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb75a-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
