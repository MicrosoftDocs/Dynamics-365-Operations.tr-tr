---
title: Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme
description: Farklı maliyet öğesi boyut üyelerini ortak bir maliyet öğesi boyut üyesi kümesine eşleyerek verileri analiz amacıyla ortak bir biçimde birleştirirsiniz.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb752ef853aedbe492dc2880b90d1683c5433a12
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217374"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="37ab4-103">Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme</span><span class="sxs-lookup"><span data-stu-id="37ab4-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37ab4-104">Farklı maliyet öğesi boyut üyelerini ortak bir maliyet öğesi boyut üyesi kümesine eşleyerek verileri analiz amacıyla ortak bir biçimde birleştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ab4-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="37ab4-105">Global bir şirketseniz ve yasal muhasebe gereksinimlerine uymanız gerekiyorsa birden fazla hesap planı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ab4-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="37ab4-106">Farklı hesap planlarından maliyet öğesi boyut üyelerini içe aktardığınızda hesaplar birbirine karışabilir.</span><span class="sxs-lookup"><span data-stu-id="37ab4-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="37ab4-107">Ancak bu hesaplar aynı yapıda olabilir ve ortak bir biçim kullanarak tüm hesapların maliyetlerini analiz ve tahsis edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ab4-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="37ab4-108">Maliyet öğesi boyut üyelerini ortak bir biçime eşleme</span><span class="sxs-lookup"><span data-stu-id="37ab4-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="37ab4-109">Aşağıdaki örnekte bir maliyet denetleyicisi olarak, ABD hesap planı yapısından ve Fransız hesap planı yapısından maliyet öğesi boyut üyelerinin ortak bir maliyet öğesi boyut üyesi kümesine eşlendiği bir Maliyet muhasebesinde yeni bir maliyet öğesi boyutunu nasıl oluşturabileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="37ab4-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="37ab4-110">Bu ortak maliyet öğesi boyut üyesi kümesini iki tüzel kişiliğin maliyet verilerini bir maliyet muhasebesi genel muhasebesinde analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ab4-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="37ab4-111">Kaynak: ABD hesap planı</span><span class="sxs-lookup"><span data-stu-id="37ab4-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="37ab4-112">Kaynak: Fransız hesap planı</span><span class="sxs-lookup"><span data-stu-id="37ab4-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="37ab4-113">Yeni maliyet öğesi boyut üyeleri ortak kümesi</span><span class="sxs-lookup"><span data-stu-id="37ab4-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="37ab4-114">ABD hesap planından içe aktarılmış maliyet öğesi boyut üyeleri</span><span class="sxs-lookup"><span data-stu-id="37ab4-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="37ab4-115">Fransız hesap planından içe aktarılmış maliyet öğesi boyut üyeleri</span><span class="sxs-lookup"><span data-stu-id="37ab4-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="37ab4-116">ABD ve Fransız maliyet öğesi boyut üyelerini ortak bir kümeye eşleme</span><span class="sxs-lookup"><span data-stu-id="37ab4-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="37ab4-117">5001: Satış</span><span class="sxs-lookup"><span data-stu-id="37ab4-117">5001: Sales</span></span>                                                           | <span data-ttu-id="37ab4-118">5001: Satış ve reklam</span><span class="sxs-lookup"><span data-stu-id="37ab4-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="37ab4-119">5000: Satış ve reklam</span><span class="sxs-lookup"><span data-stu-id="37ab4-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="37ab4-120">5030: Reklam</span><span class="sxs-lookup"><span data-stu-id="37ab4-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="37ab4-121">6390: Stok satınalma\*</span><span class="sxs-lookup"><span data-stu-id="37ab4-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="37ab4-122">7000: Temizlik giderleri</span><span class="sxs-lookup"><span data-stu-id="37ab4-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="37ab4-123">7001: Temizlik giderleri</span><span class="sxs-lookup"><span data-stu-id="37ab4-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="37ab4-124">7001: Seyahat gideri</span><span class="sxs-lookup"><span data-stu-id="37ab4-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="37ab4-125">7001: Seyahat giderleri</span><span class="sxs-lookup"><span data-stu-id="37ab4-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="37ab4-126">\*Stok satınalma Fransız maliyet öğesi boyut üyesi eşlenmedi.</span><span class="sxs-lookup"><span data-stu-id="37ab4-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="37ab4-127">Para birimi dönüştürme</span><span class="sxs-lookup"><span data-stu-id="37ab4-127">Currency conversion</span></span>
<span data-ttu-id="37ab4-128">Kullandığınız çeşitli hesap planları farklı para birimlerini kullanmak üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="37ab4-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="37ab4-129">Bu durumda bir para birimi dönüşümü belirlediğinizden emin olun ve maliyet verilerinin maliyet öğesi boyut üyelerinin kullanıldığı maliyet muhasebesi genel muhasebesinde tanımlanan, doğru para birimini kullanarak işlenmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="37ab4-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="37ab4-130">Önceki örnekte, maliyet muhasebesi genel muhasebesinde ABD doları (USD) kullanılıyorsa eşlenen maliyet öğesi boyut üyeleri için hareketleri işlemek üzere ABD Doları'ndan (USD) Euro'ya (EUR) para birimi dönüşümü oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="37ab4-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="37ab4-131">Eşlemeleri herhangi bir anda güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="37ab4-131">Update mappings at any time</span></span>
<span data-ttu-id="37ab4-132">Maliyet öğesi boyutunun eşleme tanımlarını istediğiniz zaman güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ab4-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="37ab4-133">Eşlemeler tarihe göre geçerli olmadığından, değişiklikler maliyet hareketlerini bir sonraki işlemenizde veya maliyet hesaplamalarını çalıştırdığınızda uygulanır.</span><span class="sxs-lookup"><span data-stu-id="37ab4-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]