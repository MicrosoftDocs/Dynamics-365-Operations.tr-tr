---
title: ISO20022 hesaptan ödemeleri için şirket banka hesapları ayarlama
description: Bu görev, müşteri ödeme dosyaları oluşturmak için gerekli olan, şirkete özel banka hesap bilgilerini ayarlamada size yol gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448735"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="274ec-103">ISO20022 hesaptan ödemeleri için şirket banka hesapları ayarlama</span><span class="sxs-lookup"><span data-stu-id="274ec-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="274ec-104">Bu görev, müşteri ödeme dosyaları oluşturmak için gerekli olan, şirkete özel banka hesap bilgilerini ayarlamada size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="274ec-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="274ec-105">Bu yordam örnek olarak ISO 20022 hesaptan ödeme biçimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="274ec-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="274ec-106">Diğer biçimler Şirket Kimliği veya Sıralama Kodu gibi ek kurulum bilgileri gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="274ec-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="274ec-107">Bu görev, DEMF demo veri şirketi kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="274ec-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="274ec-108">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın ikincisidir.</span><span class="sxs-lookup"><span data-stu-id="274ec-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="274ec-109">IBAN ve SWIFT kodlarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="274ec-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="274ec-110">Nakit ve banka yönetimi > Banka hesapları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="274ec-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="274ec-111">Banka hesabı alanında "DEMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="274ec-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="274ec-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="274ec-113">Örneğin: banka hesabı ayrıntılarını açmak için "DEMF OPER"e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="274ec-114">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-114">Click Edit.</span></span>
5. <span data-ttu-id="274ec-115">Ek kimlik bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="274ec-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="274ec-116">IBAN alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="274ec-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="274ec-117">Örneğin, "DE89370400440532013000" girin.</span><span class="sxs-lookup"><span data-stu-id="274ec-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="274ec-118">SWIFT kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="274ec-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="274ec-119">Örneğin "DEUTDEFF" girin.</span><span class="sxs-lookup"><span data-stu-id="274ec-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="274ec-120">Birçok ödeme biçimi için SWIFT \ BIC zorunlu değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.</span><span class="sxs-lookup"><span data-stu-id="274ec-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="274ec-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="274ec-122">Tüzel kişilik için bir banka hesabı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="274ec-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="274ec-123">Organizasyon yönetimi > Kuruluşlar > Tüzel kişilikler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="274ec-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="274ec-124">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-124">Click Edit.</span></span>
3. <span data-ttu-id="274ec-125">Banka hesabı bilgileri bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="274ec-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="274ec-126">Banka hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="274ec-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="274ec-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="274ec-128">Örneğin, "DEMF OPER" banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="274ec-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="274ec-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="274ec-129">Click Save.</span></span>

