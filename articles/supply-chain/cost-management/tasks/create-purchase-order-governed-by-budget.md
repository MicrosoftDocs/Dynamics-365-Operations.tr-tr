---
title: Bütçeyle yönetilen bir satınalma siparişi oluşturma
description: Bu yordamı, kullanılabilir bütçeye karşı denetleyen bir satınalma siparişi oluşturmak için kullanın.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 100db102f74d477bcfde48a24828b817fd65e033
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239528"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="a1dec-103">Bütçeyle yönetilen bir satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1dec-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1dec-104">Bu yordamı, kullanılabilir bütçeye karşı denetleyen bir satınalma siparişi oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="a1dec-105">Bu kayıt USMF demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a1dec-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="a1dec-106">Bütçe kontrol konfigürasyonunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="a1dec-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="a1dec-107">Bütçeleme > Kurulum > Bütçe kontrolü > Bütçe kontrol yapılandırması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="a1dec-108">Kullanılabilir bütçe fonları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="a1dec-109">Belgeler ve günlükler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="a1dec-110">Bütçe kontrol kuralları sekmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="a1dec-111">Bütçe grupları sekmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="a1dec-112">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="a1dec-113">Satınalma siparişi başlığını oluşturun</span><span class="sxs-lookup"><span data-stu-id="a1dec-113">Create the purchase order header</span></span>
1. <span data-ttu-id="a1dec-114">Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a1dec-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-115">Click New.</span></span>
3. <span data-ttu-id="a1dec-116">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="a1dec-117">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-117">Expand the General section.</span></span>
5. <span data-ttu-id="a1dec-118">Muhasebe tarih alanında, tarihi '2016-01-01' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="a1dec-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="a1dec-120">Bir satınalma siparişi satırı ekleyin</span><span class="sxs-lookup"><span data-stu-id="a1dec-120">Add a purchase order line</span></span>
1. <span data-ttu-id="a1dec-121">Satın alma kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="a1dec-122">Miktarı '2' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="a1dec-123">Birim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="a1dec-124">Birim fiyatını '10000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="a1dec-125">Finansal öğeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-125">Click Financials.</span></span>
6. <span data-ttu-id="a1dec-126">Dağıtım tutarlarını'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="a1dec-127">Genel muhasebe defteri hesabı alanında, '601300-001-023--' değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="a1dec-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="a1dec-129">Bütçe kontrolü gerçekleştir</span><span class="sxs-lookup"><span data-stu-id="a1dec-129">Perform budget checking</span></span>
1. <span data-ttu-id="a1dec-130">Finansal öğeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-130">Click Financials.</span></span>
2. <span data-ttu-id="a1dec-131">Bütçe kontrolü gerçekleştir üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="a1dec-132">Finansal öğeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-132">Click Financials.</span></span>
4. <span data-ttu-id="a1dec-133">Bütçe denetim hataları veya uyarılarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="a1dec-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="a1dec-134">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a1dec-134">Click Close.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]