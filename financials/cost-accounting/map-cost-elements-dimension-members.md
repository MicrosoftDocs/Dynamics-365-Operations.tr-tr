---
title: "Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme"
description: "Farklı maliyet öğesi boyut üyelerini ortak bir maliyet öğesi boyut üyesi kümesine eşleyerek verileri analiz amacıyla ortak bir biçimde birleştirirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 645154eadfdbdda93dde5ddff31fe86816cc7cba
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="a4e96-103">Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme</span><span class="sxs-lookup"><span data-stu-id="a4e96-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a4e96-104">Farklı maliyet öğesi boyut üyelerini ortak bir maliyet öğesi boyut üyesi kümesine eşleyerek verileri analiz amacıyla ortak bir biçimde birleştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4e96-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="a4e96-105">Global bir şirketseniz ve yasal muhasebe gereksinimlerine uymanız gerekiyorsa birden fazla hesap planı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4e96-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="a4e96-106">Farklı hesap planlarından maliyet öğesi boyut üyelerini içe aktardığınızda hesaplar birbirine karışabilir.</span><span class="sxs-lookup"><span data-stu-id="a4e96-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="a4e96-107">Ancak bu hesaplar aynı yapıda olabilir ve ortak bir biçim kullanarak tüm hesapların maliyetlerini analiz ve tahsis edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4e96-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="a4e96-108">Maliyet öğesi boyut üyelerini ortak bir biçime eşleme</span><span class="sxs-lookup"><span data-stu-id="a4e96-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="a4e96-109">Aşağıdaki örnekte bir maliyet denetleyicisi olarak, ABD hesap planı yapısından ve Fransız hesap planı yapısından maliyet öğesi boyut üyelerinin ortak bir maliyet öğesi boyut üyesi kümesine eşlendiği bir Maliyet muhasebesinde yeni bir maliyet öğesi boyutunu nasıl oluşturabileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a4e96-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="a4e96-110">Bu ortak maliyet öğesi boyut üyesi kümesini iki tüzel kişiliğin maliyet verilerini bir maliyet muhasebesi genel muhasebesinde analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4e96-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="a4e96-111">Kaynak: ABD hesap planı</span><span class="sxs-lookup"><span data-stu-id="a4e96-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="a4e96-112">Kaynak: Fransız hesap planı</span><span class="sxs-lookup"><span data-stu-id="a4e96-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="a4e96-113">Yeni maliyet öğesi boyut üyeleri ortak kümesi</span><span class="sxs-lookup"><span data-stu-id="a4e96-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a4e96-114">ABD hesap planından içe aktarılmış maliyet öğesi boyut üyeleri</span><span class="sxs-lookup"><span data-stu-id="a4e96-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="a4e96-115">Fransız hesap planından içe aktarılmış maliyet öğesi boyut üyeleri</span><span class="sxs-lookup"><span data-stu-id="a4e96-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="a4e96-116">ABD ve Fransız maliyet öğesi boyut üyelerini ortak bir kümeye eşleme</span><span class="sxs-lookup"><span data-stu-id="a4e96-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="a4e96-117">5001: Satış</span><span class="sxs-lookup"><span data-stu-id="a4e96-117">5001: Sales</span></span>                                                           | <span data-ttu-id="a4e96-118">5001: Satış ve reklam</span><span class="sxs-lookup"><span data-stu-id="a4e96-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="a4e96-119">5000: Satış ve reklam</span><span class="sxs-lookup"><span data-stu-id="a4e96-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="a4e96-120">5030: Reklam</span><span class="sxs-lookup"><span data-stu-id="a4e96-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="a4e96-121">6390: Stok satınalma\*</span><span class="sxs-lookup"><span data-stu-id="a4e96-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="a4e96-122">7000: Temizlik giderleri</span><span class="sxs-lookup"><span data-stu-id="a4e96-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="a4e96-123">7001: Temizlik giderleri</span><span class="sxs-lookup"><span data-stu-id="a4e96-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="a4e96-124">7001: Seyahat gideri</span><span class="sxs-lookup"><span data-stu-id="a4e96-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="a4e96-125">7001: Seyahat giderleri</span><span class="sxs-lookup"><span data-stu-id="a4e96-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="a4e96-126">\*Stok satınalma Fransız maliyet öğesi boyut üyesi eşlenmedi.</span><span class="sxs-lookup"><span data-stu-id="a4e96-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="a4e96-127">Para birimi dönüştürme</span><span class="sxs-lookup"><span data-stu-id="a4e96-127">Currency conversion</span></span>
<span data-ttu-id="a4e96-128">Kullandığınız çeşitli hesap planları farklı para birimlerini kullanmak üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a4e96-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="a4e96-129">Bu durumda bir para birimi dönüşümü belirlediğinizden emin olun ve maliyet verilerinin maliyet öğesi boyut üyelerinin kullanıldığı maliyet muhasebesi genel muhasebesinde tanımlanan, doğru para birimini kullanarak işlenmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="a4e96-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="a4e96-130">Önceki örnekte, maliyet muhasebesi genel muhasebesinde ABD doları (USD) kullanılıyorsa eşlenen maliyet öğesi boyut üyeleri için hareketleri işlemek üzere ABD Doları'ndan (USD) Euro'ya (EUR) para birimi dönüşümü oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a4e96-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="a4e96-131">Eşlemeleri herhangi bir anda güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a4e96-131">Update mappings at any time</span></span>
<span data-ttu-id="a4e96-132">Maliyet öğesi boyutunun eşleme tanımlarını istediğiniz zaman güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4e96-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="a4e96-133">Eşlemeler tarihe göre geçerli olmadığından, değişiklikler maliyet hareketlerini bir sonraki işlemenizde veya maliyet hesaplamalarını çalıştırdığınızda uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a4e96-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




