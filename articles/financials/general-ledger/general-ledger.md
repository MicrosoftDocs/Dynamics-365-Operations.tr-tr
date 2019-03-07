---
title: Genel muhasebe ve Mali raporlama giriş sayfası
description: Tüzel kişinin mali kayıtlarını tanımlamak ve yönetmek için genel muhasebeyi kullanın.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85afebcc88ad1c087d5f1dabaac56f694534cf98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "363373"
---
# <a name="general-ledger"></a><span data-ttu-id="ee720-103">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="ee720-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee720-104">Tüzel kişinin mali kayıtlarını tanımlamak ve yönetmek için genel muhasebeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ee720-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="ee720-105">Genel muhasebe, borç ve alacak girişlerinin bir kaydıdır.</span><span class="sxs-lookup"><span data-stu-id="ee720-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="ee720-106">Bu girişler, hesap planında listelenen hesaplar kullanılarak sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="ee720-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="ee720-107">Hesap planınızı planlama</span><span class="sxs-lookup"><span data-stu-id="ee720-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="ee720-108">Ana hesap türleri</span><span class="sxs-lookup"><span data-stu-id="ee720-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="ee720-109">Tahsis kurallarına göre parasal tutarları bir veya daha fazla hesaba veya hesap ve boyut birleşimlerine tahsis edebilir veya dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee720-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="ee720-110">İki tür tahsisat vardır: sabit ve değişken.</span><span class="sxs-lookup"><span data-stu-id="ee720-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="ee720-111">Genel muhasebe hesapları arasındaki hareketleri kapatabilir ve para birimi tutarlarını yeniden değerleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee720-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="ee720-112">Bir mali yılın sonunda, sonraki mali yıl için kapanış hareketleri oluşturmanız ve hesaplarınızı hazırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee720-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="ee720-113">Tek bir, konsolide kuruluş sonuçları için birkaç yan yasal kuruluş için mali sonuçları birleştirmek için konsolidasyon işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee720-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="ee720-114">Yan şirketler Microsoft Dynamics 365 for Finance and Operations veritabanında veya farklı veritabanlarında olabilir.</span><span class="sxs-lookup"><span data-stu-id="ee720-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="ee720-115">Birleştirmeye ve elemeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="ee720-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="ee720-116">Genel muhasebe hesap bakiyeleri</span><span class="sxs-lookup"><span data-stu-id="ee720-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="ee720-117">Mali boyutlar</span><span class="sxs-lookup"><span data-stu-id="ee720-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="ee720-118">[![İş süreci](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="ee720-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="ee720-119">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="ee720-119">Sales tax</span></span>
<span data-ttu-id="ee720-120">Her şirket vergi toplar ve çeşitli vergi kurumlarına vergi öder.</span><span class="sxs-lookup"><span data-stu-id="ee720-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="ee720-121">Kurallar ve oranlar ülke/bölge, il, ilçe ve şehre göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee720-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="ee720-122">Ayrıca, vergi dairesi gereksinimleri değiştirdiğinde kuralların düzenli olarak güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee720-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="ee720-123">Satış vergisi kodları yetkili kurumlardan aldığınız ve yetkili kurumlara ödediğiniz tutarla ilgili temel ilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="ee720-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="ee720-124">Satış vergisi kodlarını ayarladığınızda, toplanması gereken tutarları veya yüzdeleri tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="ee720-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="ee720-125">Ayrıca bu tutarların veya yüzdelerin hareket tutarlarına uygulanması için çeşitli yöntemleri de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="ee720-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="ee720-126">Bu bölümdeki konular, vergi dairelerinin gerektirdiği yöntemler ve oranlar için satış vergisi kodlarının nasıl ayarlanacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ee720-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="ee720-127">Satış vergisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ee720-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="ee720-128">Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları</span><span class="sxs-lookup"><span data-stu-id="ee720-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="ee720-129">Satış vergisi ödemeleri ve yuvarlama kuralları</span><span class="sxs-lookup"><span data-stu-id="ee720-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="ee720-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ee720-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="ee720-131">Yenilikler</span><span class="sxs-lookup"><span data-stu-id="ee720-131">What's new</span></span>

<span data-ttu-id="ee720-132">Kullanıma sunulmuş yeni sürümleri görmek için [Sürüm notları](https://docs.microsoft.com/en-us/business-applications-release-notes/)'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ee720-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="ee720-133">Videolar</span><span class="sxs-lookup"><span data-stu-id="ee720-133">Videos</span></span>

<span data-ttu-id="ee720-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Kanalı](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)'nda bulunan nasıl yapılır videolarına hemen göz atın.</span><span class="sxs-lookup"><span data-stu-id="ee720-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="ee720-135">Bloglar</span><span class="sxs-lookup"><span data-stu-id="ee720-135">Blogs</span></span>

<span data-ttu-id="ee720-136">[Microsoft Dynamics 365 bloğunda](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) Borç hesapları ve diğer çözümler hakkındaki fikir, haber ve diğer bilgilere ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee720-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="ee720-137">[Microsoft Dynamics AX ürün ekibi bloğunda](https://blogs.msdn.microsoft.com/dax/) Genel muhasebe defteri hakkında pek çok gönderi bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ee720-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="ee720-138">Bu gönderilerin bazıları Genel muhasebenin önceki sürümü için yazılmıştır ancak aynı kavramlar hala geçerlidir ve yordamlar da geçerli sürümdekine benzerdir.</span><span class="sxs-lookup"><span data-stu-id="ee720-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="ee720-139">[Microsoft Dynamics Operations İş Ortağı Topluluk Bloğu](https://community.dynamics.com/partner/b/operationspartnercommunityblog)'nda Microsoft Dynamics İş Ortakları'na MBS Operations'daki yenilikler ve eğilimler hakkında bilgi edinebilecekleri tek bir kaynak sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ee720-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="ee720-140">Topluluk blogları</span><span class="sxs-lookup"><span data-stu-id="ee720-140">Community blogs</span></span>

- [<span data-ttu-id="ee720-141">Dynamics 365 for Finance and Operations muhasebe defteri hakkında bilmeniz gerekenler</span><span class="sxs-lookup"><span data-stu-id="ee720-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

