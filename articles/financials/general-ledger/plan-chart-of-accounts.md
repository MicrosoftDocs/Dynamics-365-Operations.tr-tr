---
title: "Hesap planınızı planlama"
description: "Bu konuda, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir."
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3f8d97fc42cde9053b0552fc1dfe8e6de0f5e03b
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="34877-103">Hesap planınızı planlama</span><span class="sxs-lookup"><span data-stu-id="34877-103">Plan your chart of accounts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="34877-104">Bu konuda, kuruluşunuzun hesap planını yapmanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="34877-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="34877-105">Bir kuruluşun finansal bilgilerini takip etmek ve kaydetmek için bir hesap planı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="34877-106">Hesap planı bir finansal çerçeveyi tanımlayan bir hesaplar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="34877-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="34877-107">Bu hesaplardaki hareketleri daha da ayrıntılı izlemek için segmentler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="34877-108">Bu segmentler mali boyutlar olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="34877-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="34877-109">Örneğin, bir gider hesabı Departman, Maliyet merkezi ve Amaç adlı finansal boyutlar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="34877-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="34877-110">Kullanıcı tanımlı kurallar finansal boyutların ana hesaplara ve diğer finansal boyutlara nasıl ekleneceğini ve ayrıca işlemlerin nasıl girileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="34877-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="34877-111">Kullanıcı tanımlı kurallar hesap yapıları ve gelişmiş kurallar olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="34877-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="34877-112">Hesap planı bir tüzel kişiliğin genel muhasebe hesaplarının yapılandırılmış bir listesidir.</span><span class="sxs-lookup"><span data-stu-id="34877-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="34877-113">Liste, yetkililer ve sahipler için mali raporlar hazırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34877-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="34877-114">Hesaplar, önce hesap türlerine göre gruplanır ve daha büyük kategorilere daha birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="34877-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="34877-115">En genel düzeyde, hesaplar gelirler ve maliyetler (çalışan hesaplar) ile varlıklar ve borçlar (bilanço hesapları) olarak gruplanır.</span><span class="sxs-lookup"><span data-stu-id="34877-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="34877-116">Hesap planı paylaşılabilir ve kuruluştaki herhangi bir tüzel kişilik tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34877-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="34877-117">Tüzel kişilik tarafından kullanılan hesap planı **Genel muhasebe** sayfasında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="34877-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="34877-118">Burada kurumunuz için hesap planının yapısını planlarken mutlaka göz önünde bulundurmanız gereken bazı faktörler açıklanmıştır:</span><span class="sxs-lookup"><span data-stu-id="34877-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="34877-119">Kurulumunuzun bulunduğu ülkenin veya bölgenin raporlama gereksinimleri.</span><span class="sxs-lookup"><span data-stu-id="34877-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="34877-120">Yasal biriminizin raporlama gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="34877-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="34877-121">Hem dış kurumlar hem kendi kurumunuz için gerekli olan tanımlama derecesi</span><span class="sxs-lookup"><span data-stu-id="34877-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="34877-122">**Hesap planı** sayfasından hesap planınızı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="34877-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="34877-123">Ana hesapları **Hesap planı** sayfasından veya **Ana hesaplar** sayfasından oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="34877-124">Ana hesaplarınız, hesap planı sınırlayıcıları olarak kullanılan hiçbir özel karakteri kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="34877-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="34877-125">Aksi takdirde, tutarsızlıkla karşılaşabilir veya hesap ve boyut birleşimleri girerken her zaman aramaları veya iletişim kutusunu kullanmak zorunda kalabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="34877-126">Daha fazla bilgi için bkz. [Ana hesap oluşturma](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="34877-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="34877-127">Microsoft Dynamics for Finance and Operations sürüm 8.0'da (Nisan 2018), hesap planı sınırlayıcısını **Genel muhasebe parametreleri** sayfasından değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="34877-128">Ana hesapların ana hesap kategorileriyle ilişkilendirilmesi iyi bir fikirdir, böylece herhangi bir değişiklik yapmak zorunda kalmadan varsayılan finansal raporları istediğiniz gibi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="34877-129">Böylece, raporları daha hızlı ve kolay bir şekilde tasarlayabilir ve tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="34877-130">Hesap yapılarını **Hesap yapıları oluştur** sayfasından oluşturun.</span><span class="sxs-lookup"><span data-stu-id="34877-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="34877-131">Hesap yapıları geçerli kombinasyonları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="34877-131">Account structures define valid combinations.</span></span> <span data-ttu-id="34877-132">Bu birleşimler, ana hesaplarla birlikte bir hesap planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34877-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="34877-133">Daha fazla bilgi için bkz. [Hesap yapıları oluşturma](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="34877-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="34877-134">**Tüzel varlık geçersiz kılmaları**</span><span class="sxs-lookup"><span data-stu-id="34877-134">**Legal entity overrides**</span></span>

<span data-ttu-id="34877-135">Tüm tüzel kişilikler için her ana hesap geçerli değildir, bazı ana hesaplar sadece belirli bir dönem için geçerli olabilir.</span><span class="sxs-lookup"><span data-stu-id="34877-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="34877-136">Bu senaryoda, **Tüzel varlık geçersiz kılmaları** bölümünü, ana hesabın askıya alınacağı şirketleri, sahibini ve boyutun etkin olacağı dönemi belirlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34877-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="34877-137">Paylaşılan düzeydeki öncelikler, yasal birim düzeyindeki önceliklerden daha kısıtlayıcı olamaz.</span><span class="sxs-lookup"><span data-stu-id="34877-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="34877-138">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="34877-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="34877-139">Mali boyutlar</span><span class="sxs-lookup"><span data-stu-id="34877-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="34877-140">Gelişmiş kural yapıları oluşturma ve atama</span><span class="sxs-lookup"><span data-stu-id="34877-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)

