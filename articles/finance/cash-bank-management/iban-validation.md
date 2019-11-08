---
title: Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme
description: Bu konuda, Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme işlemi açıklanmaktadır.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2aaccd7c09d6daf8a237a433cc22ac1bfc3c1541
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551281"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="1d424-103">Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme</span><span class="sxs-lookup"><span data-stu-id="1d424-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d424-104">Uluslararası Banka Hesap Numarası (IBAN) doğrulaması bir banka hesabına IBAN eklediğinizde gerçekleştirilen doğrulamanın miktarını artırır.</span><span class="sxs-lookup"><span data-stu-id="1d424-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="1d424-105">Microsoft Dynamics 365 Finance içinde depolanmış IBAN yapısı hakkında bilgi.</span><span class="sxs-lookup"><span data-stu-id="1d424-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="1d424-106">Banka hesaplarında IBAN'ı ilk kez kullandığınızda, bu bilgiler otomatik olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1d424-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="1d424-107">IBAN uzunluğu, banka hesap numarasının başlangıç konun ve rota numarası, banka hesap numarası uzunluğu ve rota numarasını içerir.</span><span class="sxs-lookup"><span data-stu-id="1d424-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="1d424-108">IBAN yapılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="1d424-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="1d424-109">**Nakit ve banka yönetimi \> Kurulum \> IBAN yapıları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="1d424-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="1d424-110">Her ülkenin veya bölgenin IBAN yapılarının otomatik olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="1d424-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="1d424-111">Yapıları belirli bir ülke veya bölge için özelleştirmek isterseniz bunları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d424-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="1d424-112">Yapı tanımları her yeni sürümün parçası olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="1d424-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="1d424-113">**Yapıları sıfırla** menüsünü her güncelleştirmeden sonra en son tanımları yüklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d424-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="1d424-114">Banka hesabındaki IBAN yapısını doğrulama</span><span class="sxs-lookup"><span data-stu-id="1d424-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="1d424-115">**Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="1d424-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="1d424-116">Banka hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1d424-116">Create a bank account.</span></span>
3. <span data-ttu-id="1d424-117">**Ek bilgiler** hızlı sekmesinde bir IBAN girin.</span><span class="sxs-lookup"><span data-stu-id="1d424-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="1d424-118">Her ülke veya bölge için tanımlanan uzunlukla IBAN'ın uzunluğu eşleşmiyorsa, bir uyarı iletisi alacaksınız.</span><span class="sxs-lookup"><span data-stu-id="1d424-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="1d424-119">IBAN'ın uzunluğu IBAN yapısında belirtilen uzunlukla eşleşmezse işleme devam edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d424-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="1d424-120">Doğrulama, banka hesap numarasının IBAN'ın banka hesap numarasını temsil eden kısmıyla eşleştiğini de doğrular.</span><span class="sxs-lookup"><span data-stu-id="1d424-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="1d424-121">Banka hesap numarası eşleşmiyorsa bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="1d424-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="1d424-122">Bir ileti yalnızca bir uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="1d424-122">This message is only a warning.</span></span> <span data-ttu-id="1d424-123">Banka hesap numarası eşleşmese de işleme devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d424-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="1d424-124">Doğrulama, banka rota numarasının IBAN'ın banka rota numarasını temsil eden kısmıyla eşleştiğini de doğrular.</span><span class="sxs-lookup"><span data-stu-id="1d424-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="1d424-125">Rota numarası, banka numarası ve genellikle bir ek banka şubesi içerir.</span><span class="sxs-lookup"><span data-stu-id="1d424-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="1d424-126">Banka rota numarası eşleşmiyorsa bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="1d424-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="1d424-127">Bir ileti yalnızca bir uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="1d424-127">This message is only a warning.</span></span> <span data-ttu-id="1d424-128">Banka rota numarası eşleşmese de işleme devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d424-128">You can continue even if the bank routing number doesn't match.</span></span>
