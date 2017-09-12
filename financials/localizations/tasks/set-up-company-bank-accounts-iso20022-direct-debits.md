--- 
title: "ISO20022 hesaptan ödemeleri için şirket banka hesapları ayarlama"
description: "Bu görev, müşteri ödeme dosyaları oluşturmak için gerekli olan, şirkete özel banka hesap bilgilerini ayarlamada size yol gösterir."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 836433a1a280efde5accba3391519f3c0ce08353
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="aaa2c-103">ISO20022 hesaptan ödemeleri için şirket banka hesapları ayarlama</span><span class="sxs-lookup"><span data-stu-id="aaa2c-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aaa2c-104">Bu görev, müşteri ödeme dosyaları oluşturmak için gerekli olan, şirkete özel banka hesap bilgilerini ayarlamada size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="aaa2c-105">Bu yordam örnek olarak ISO 20022 hesaptan ödeme biçimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="aaa2c-106">Diğer biçimler Şirket Kimliği veya Sıralama Kodu gibi ek kurulum bilgileri gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="aaa2c-107">Bu görev, DEMF demo veri şirketi kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="aaa2c-108">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın ikincisidir.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="aaa2c-109">IBAN ve SWIFT kodlarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="aaa2c-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="aaa2c-110">Nakit ve banka yönetimi > Banka hesapları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="aaa2c-111">Banka hesabı alanında "DEMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="aaa2c-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aaa2c-113">Örneğin: banka hesabı ayrıntılarını açmak için "DEMF OPER"e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="aaa2c-114">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-114">Click Edit.</span></span>
5. <span data-ttu-id="aaa2c-115">Ek kimlik bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="aaa2c-116">IBAN alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="aaa2c-117">Örneğin, "DE89370400440532013000" girin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="aaa2c-118">SWIFT kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="aaa2c-119">Örneğin "DEUTDEFF" girin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="aaa2c-120">Birçok ödeme biçimi için SWIFT \ BIC zorunlu değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="aaa2c-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="aaa2c-122">Tüzel kişilik için bir banka hesabı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="aaa2c-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="aaa2c-123">Organizasyon yönetimi > Kuruluşlar > Tüzel kişilikler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="aaa2c-124">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-124">Click Edit.</span></span>
3. <span data-ttu-id="aaa2c-125">Banka hesabı bilgileri bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="aaa2c-126">Banka hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="aaa2c-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aaa2c-128">Örneğin, "DEMF OPER" banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="aaa2c-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaa2c-129">Click Save.</span></span>


