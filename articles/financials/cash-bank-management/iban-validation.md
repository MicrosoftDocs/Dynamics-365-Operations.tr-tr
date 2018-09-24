---
title: "Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme"
description: "Bu konuda, Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme işlemi açıklanmaktadır."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: tr-tr
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="7c6be-103">Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme</span><span class="sxs-lookup"><span data-stu-id="7c6be-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c6be-104">Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulaması bir banka hesabına IBAN eklediğinizde gerçekleştirilen doğrulamanın miktarını artırır.</span><span class="sxs-lookup"><span data-stu-id="7c6be-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="7c6be-105">IBAN'ın yapısı Microsoft Dynamics 365 for Finance and Operation içinde depolanır ve IBAN'ı banka hesaplarında ilk kez kullandığınızda otomatik olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="7c6be-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="7c6be-106">Banka hesap numarası bir IBAN numarası için tanımlanan yapının parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="7c6be-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="7c6be-107">Bu yapıya göre IBAN'daki hesap numarasının konumu ve uzunluğu her ülke veya bölge için yapıda tanımlanan konumla eşleşmezse bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7c6be-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="7c6be-108">IBAN yapılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7c6be-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="7c6be-109">**Nakit ve banka yönetimi \> Kurulum \> IBAN yapıları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="7c6be-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="7c6be-110">Her ülkenin veya bölgenin IBAN yapılarının otomatik olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7c6be-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="7c6be-111">Yapıları belirli bir ülke veya bölge için özelleştirmeniz gerekirse bunları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c6be-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="7c6be-112">Yapı tanımları her yeni sürümün parçası olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="7c6be-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="7c6be-113">**Yapıları sıfırla** menüsünü her güncelleştirmeden sonra en son tanımları yüklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c6be-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="7c6be-114">Banka hesabındaki IBAN yapısını doğrulama</span><span class="sxs-lookup"><span data-stu-id="7c6be-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="7c6be-115">**Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7c6be-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="7c6be-116">Banka hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7c6be-116">Create a bank account.</span></span>
3. <span data-ttu-id="7c6be-117">**Ek bilgiler** hızlı sekmesinde bir IBAN girin.</span><span class="sxs-lookup"><span data-stu-id="7c6be-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="7c6be-118">IBAN'daki hesap numarasının konumu ve uzunluğu her ülke veya bölge için yapıda tanımlanan konumla eşleşmezse bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7c6be-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="7c6be-119">IBAN'ın uzunluğu IBAN yapısındaki uzunlukla eşleşmezse işleme devam edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c6be-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="7c6be-120">Doğrulama, banka hesap numarasının IBAN'ın banka hesap numarasını temsil eden kısmıyla eşleştiğini de doğrular.</span><span class="sxs-lookup"><span data-stu-id="7c6be-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="7c6be-121">Banka hesap numarası eşleşmiyorsa bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7c6be-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="7c6be-122">Bir ileti yalnızca bir uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="7c6be-122">This message is only a warning.</span></span> <span data-ttu-id="7c6be-123">Banka hesap numarası eşleşmese de işleme devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c6be-123">You can continue even if the bank account number doesn't match.</span></span>

