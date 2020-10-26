---
title: Genel muhasebe ve Mali raporlamaya genel bakış
description: Tüzel kişinin mali kayıtlarını tanımlamak ve yönetmek için genel muhasebeyi kullanın.
author: ShylaThompson
manager: AnnBe
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ade10020e4bab02490c9104c37fe1f234d634e8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975232"
---
# <a name="general-ledger-home-page"></a><span data-ttu-id="64289-103">Genel muhasebe ana sayfası</span><span class="sxs-lookup"><span data-stu-id="64289-103">General ledger home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64289-104">Tüzel kişinin mali kayıtlarını tanımlamak ve yönetmek için genel muhasebeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="64289-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="64289-105">Genel muhasebe, borç ve alacak girişlerinin bir kaydıdır.</span><span class="sxs-lookup"><span data-stu-id="64289-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="64289-106">Bu girişler, hesap planında listelenen hesaplar kullanılarak sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="64289-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="64289-107">Hesap planınızı planlama</span><span class="sxs-lookup"><span data-stu-id="64289-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="64289-108">Ana hesap türleri</span><span class="sxs-lookup"><span data-stu-id="64289-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="64289-109">Tahsis kurallarına göre parasal tutarları bir veya daha fazla hesaba veya hesap ve boyut birleşimlerine tahsis edebilir veya dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64289-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="64289-110">İki tür tahsisat vardır: sabit ve değişken.</span><span class="sxs-lookup"><span data-stu-id="64289-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="64289-111">Genel muhasebe hesapları arasındaki hareketleri kapatabilir ve para birimi tutarlarını yeniden değerleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64289-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="64289-112">Bir mali yılın sonunda, sonraki mali yıl için kapanış hareketleri oluşturmanız ve hesaplarınızı hazırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="64289-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="64289-113">Tek bir, konsolide kuruluş sonuçları için birkaç yan yasal kuruluş için mali sonuçları birleştirmek için konsolidasyon işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64289-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="64289-114">Yan şirketler aynı veritabanında veya farklı veritabanlarında olabilir.</span><span class="sxs-lookup"><span data-stu-id="64289-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="64289-115">Birleştirmeye ve elemeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="64289-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="64289-116">Genel muhasebe hesap bakiyeleri</span><span class="sxs-lookup"><span data-stu-id="64289-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="64289-117">Mali boyutlar</span><span class="sxs-lookup"><span data-stu-id="64289-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="64289-118">[![İş süreci](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="64289-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="64289-119">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="64289-119">Sales tax</span></span>
<span data-ttu-id="64289-120">Her şirket vergi toplar ve çeşitli vergi kurumlarına vergi öder.</span><span class="sxs-lookup"><span data-stu-id="64289-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="64289-121">Kurallar ve oranlar ülke/bölge, il, ilçe ve şehre göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="64289-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="64289-122">Ayrıca, vergi dairesi gereksinimleri değiştirdiğinde kuralların düzenli olarak güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="64289-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="64289-123">Satış vergisi kodları yetkili kurumlardan aldığınız ve yetkili kurumlara ödediğiniz tutarla ilgili temel ilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="64289-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="64289-124">Satış vergisi kodlarını ayarladığınızda, toplanması gereken tutarları veya yüzdeleri tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="64289-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="64289-125">Ayrıca bu tutarların veya yüzdelerin hareket tutarlarına uygulanması için çeşitli yöntemleri de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="64289-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="64289-126">Bu bölümdeki konular, vergi dairelerinin gerektirdiği yöntemler ve oranlar için satış vergisi kodlarının nasıl ayarlanacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="64289-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="64289-127">Satış vergisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="64289-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="64289-128">Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları</span><span class="sxs-lookup"><span data-stu-id="64289-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="64289-129">Satış vergisi ödemeleri ve yuvarlama kuralları</span><span class="sxs-lookup"><span data-stu-id="64289-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="64289-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="64289-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="64289-131">Yenilikler ve geliştirilen özellikler</span><span class="sxs-lookup"><span data-stu-id="64289-131">What's new and in development</span></span>

<span data-ttu-id="64289-132">Planlanmış yeni özellikleri görmek için [Microsoft Dynamics 365 sürüm planlarına](https://go.microsoft.com/fwlink/?linkid=2010158) bakın.</span><span class="sxs-lookup"><span data-stu-id="64289-132">Go to the [Microsoft Dynamics 365 release plans](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="financial-reporting"></a><span data-ttu-id="64289-133">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="64289-133">Financial reporting</span></span>
<span data-ttu-id="64289-134">Mali raporlar hakkındaki bilgiler için [Financial Reporting'e genel bakış](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) konusuna gidin.</span><span class="sxs-lookup"><span data-stu-id="64289-134">Go to the [Financial reporting overview](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) topic for information about financial reports.</span></span>

#### <a name="blogs"></a><span data-ttu-id="64289-135">Bloglar</span><span class="sxs-lookup"><span data-stu-id="64289-135">Blogs</span></span>

<span data-ttu-id="64289-136">[Microsoft Dynamics 365 blogunda](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ve [Microsoft Dynamics 365 Finance and Operations - Financials blogunda](https://community.dynamics.com/365/financeandoperations/b/financials) fikir, haber ve diğer bilgilere ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64289-136">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="64289-137">[Microsoft Dynamics Operations İş Ortağı Topluluk Blogu](https://community.dynamics.com/partner/b/operationspartnercommunityblog)'nda Microsoft Dynamics İş Ortakları'na Dynamics 365'teki yenilikler ve eğilimler hakkında bilgi edinebilecekleri tek bir kaynak sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="64289-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in Dynamics 365.</span></span>

### <a name="videos"></a><span data-ttu-id="64289-138">Videolar</span><span class="sxs-lookup"><span data-stu-id="64289-138">Videos</span></span>

<span data-ttu-id="64289-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Kanalı](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)'nda bulunan nasıl yapılır videolarına hemen göz atın.</span><span class="sxs-lookup"><span data-stu-id="64289-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="64289-140">Topluluk blogları</span><span class="sxs-lookup"><span data-stu-id="64289-140">Community blogs</span></span>

- [<span data-ttu-id="64289-141">Dynamics 365 for Finance and Operations muhasebe defteri hakkında bilmeniz gerekenler</span><span class="sxs-lookup"><span data-stu-id="64289-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

