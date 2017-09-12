---
title: "Hesap planınızı planlama"
description: "Bu makalede, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="d764b-103">Hesap planınızı planlama</span><span class="sxs-lookup"><span data-stu-id="d764b-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d764b-104">Bu makalede, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d764b-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="d764b-105">Bir kuruluşun finansal bilgilerini takip etmek ve kaydetmek için bir hesap planı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d764b-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="d764b-106">Hesap planı bir finansal çerçeveyi tanımlayan bir hesaplar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="d764b-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="d764b-107">Bu hesaplardaki işlemleri daha yakından takip etmek için finansal boyutlar olarak bilinen segmentler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d764b-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="d764b-108">Örneğin, bir gider hesabı Departman, Maliyet merkezi ve Amaç adlı finansal boyutlar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="d764b-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="d764b-109">Hesap yapıları ve gelişmiş kurallar olarak bilinen, kullanıcı tanımlı kurallar finansal boyutların ana hesaplara ve diğer finansal boyutlara nasıl ekleneceğini ve ayrıca işlemlerin nasıl girileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d764b-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="d764b-110">Hesap planı bir yasal kuruluşun genel muhasebe hesaplarının yapılandırılmış bir listesidir.</span><span class="sxs-lookup"><span data-stu-id="d764b-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="d764b-111">Liste, yetkililer ve sahipler için mali raporlar hazırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d764b-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="d764b-112">Hesaplar, hesap türlerine göre gruplanır ve daha büyük kategorilere daha birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d764b-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="d764b-113">En genel düzeyde, hesaplar gelirler ve maliyetler (çalışan hesaplar) ile varlıklar ve borçlar (bilanço hesapları) olarak gruplanır.</span><span class="sxs-lookup"><span data-stu-id="d764b-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="d764b-114">Hesap planı paylaşılabilir ve kuruluştaki herhangi bir tüzel kişilik tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d764b-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="d764b-115">Tüzel kişilik tarafından kullanılan hesap planı **Genel muhasebe** sayfasında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="d764b-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="d764b-116">Burada kurumunuz için hesap planının yapısını planlarken mutlaka göz önünde bulundurmanız gereken bazı faktörler açıklanmıştır:</span><span class="sxs-lookup"><span data-stu-id="d764b-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="d764b-117">Kurulumunuzun bulunduğu ülkenin/bölgenin raporlama gereksinimleri.</span><span class="sxs-lookup"><span data-stu-id="d764b-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="d764b-118">Yasal biriminizin raporlama gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="d764b-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="d764b-119">Hem dış kurumlar hem kendi kurumunuz için gerekli olan tanımlama derecesi</span><span class="sxs-lookup"><span data-stu-id="d764b-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="d764b-120">**Hesap planı** sayfasından hesap planınızı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d764b-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="d764b-121">Ana hesaplar **Hesap planı** sayfasından veya **Ana hesaplar** sayfasından oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d764b-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="d764b-122">Ana hesaplarınız, hesap planı sınırlayıcıları olarak kullanılan hiçbir özel karakteri kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="d764b-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="d764b-123">Hesap planı sınırlayıcınızla aynı olan bir özel karakter bulunuyorsa tutarsızlık yaşayabilir veya hesap ve boyut kombinasyonları girerken daima arama veya sorgulama özelliklerini kullanmak durumunda kalabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d764b-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="d764b-124">Daha fazla bilgi için bkz. [Ana hesap oluşturma](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="d764b-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="d764b-125">Ana hesapların ana hesap kategorileriyle ilişkilendirilmesi iyi bir fikirdir, böylece herhangi bir değişiklik yapmak zorunda kalmadan varsayılan finansal raporları istediğiniz gibi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d764b-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="d764b-126">Böylece, raporları daha hızlı ve kolay bir şekilde tasarlayabilir ve tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d764b-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="d764b-127">Hesap yapıları oluşturmak için **Hesap yapıları oluştur** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d764b-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="d764b-128">Hesap yapıları geçerli kombinasyonları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d764b-128">Account structures define valid combinations.</span></span> <span data-ttu-id="d764b-129">Kombinasyonlar, ana hesaplarla birlikte bir hesap planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d764b-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="d764b-130">Daha fazla bilgi için bkz. [Hesap yapıları oluşturma](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="d764b-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="d764b-131">**Tüzel varlık geçersiz kılmaları**</span><span class="sxs-lookup"><span data-stu-id="d764b-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="d764b-132">Tüm yasal birimler için her ana hesap geçerli değildir, bazı ana hesaplar sadece belirli bir zaman aralığı için geçerli olabilir.</span><span class="sxs-lookup"><span data-stu-id="d764b-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="d764b-133">Bu senaryoda, Yasal birim önceliği bölümü, ana hesabın hangi şirketler için askıya alınması gerektiğinin, sahibinin kim olduğunun ve boyutun etkin olacağı zaman diliminin belirlenmesi için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d764b-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="d764b-134">Paylaşılan düzeydeki öncelikler, yasal birim düzeyindeki önceliklerden daha kısıtlayıcı olamaz.</span><span class="sxs-lookup"><span data-stu-id="d764b-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="d764b-135">Daha fazla bilgi için aşağıdaki konulara bkz.: [Mali boyutlar](financial-dimensions.md)
[Gelişmiş kural yapıları oluştur ve ata](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="d764b-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




