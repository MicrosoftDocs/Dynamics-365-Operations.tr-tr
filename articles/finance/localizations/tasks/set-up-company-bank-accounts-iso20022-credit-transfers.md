---
title: ISO20022 alacak transferleri için şirket banka hesapları ayarlama
description: Bu yordam, ödeme dosya oluşturması için gerekli olan şirkete özel banka hesap bilgilerinin nasıl ayarlanacağını gösterir.
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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca0f0af3cccd4110c3da1703112a5b0f29bd64ad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988182"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="20d45-103">ISO20022 alacak transferleri için şirket banka hesapları ayarlama</span><span class="sxs-lookup"><span data-stu-id="20d45-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="20d45-104">Bu yordam, ödeme dosya oluşturması için gerekli olan şirkete özel banka hesap bilgilerinin nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20d45-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="20d45-105">ISO 20022 alacak transferi biçimi oluşturmak için gereken bilgileri ayarladınız ancak biçime bağlı olarak Şirket Kodu veya Sıralama kodu gibi başka bilgiler de gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="20d45-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="20d45-106">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="20d45-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="20d45-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın ikincisidir.</span><span class="sxs-lookup"><span data-stu-id="20d45-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="20d45-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="20d45-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="20d45-109">IBAN ve SWIFT kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="20d45-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="20d45-110">Nakit ve banka yönetimi > Banka hesapları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="20d45-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="20d45-111">Banka hesabı alanında "DEMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="20d45-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="20d45-112">Banka hesabı ayrıntılarını açmak için DEMF OPER'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20d45-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="20d45-113">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20d45-113">Click Edit.</span></span>
5. <span data-ttu-id="20d45-114">Ek kimlik bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="20d45-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="20d45-115">IBAN alanına "DE89370400440532013000" yazın.</span><span class="sxs-lookup"><span data-stu-id="20d45-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="20d45-116">SWIFT kodu alanına "DEUTDEFF" yazın.</span><span class="sxs-lookup"><span data-stu-id="20d45-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="20d45-117">Birçok ödeme biçimi için SWIFT\BIC gerekli değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.</span><span class="sxs-lookup"><span data-stu-id="20d45-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="20d45-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20d45-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="20d45-119">Tüzel kişilik için banka hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="20d45-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="20d45-120">Organizasyon yönetimi > Kuruluşlar > Tüzel kişilikler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="20d45-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="20d45-121">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20d45-121">Click Edit.</span></span>
3. <span data-ttu-id="20d45-122">Banka hesabı bilgileri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="20d45-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="20d45-123">Banka hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="20d45-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="20d45-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="20d45-124">Click Save.</span></span>

