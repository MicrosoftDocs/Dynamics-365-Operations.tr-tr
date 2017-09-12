---
title: "Genel muhasebe ve Mali raporlama giriş sayfası"
description: "Tüzel kişinin mali kayıtlarını tanımlamak ve yönetmek için genel muhasebeyi kullanın. Genel muhasebe, borç ve alacak girişlerinin bir kaydıdır. Bu girişler, hesap planında listelenen hesaplar kullanılarak sınıflandırılır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="4631c-105">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="4631c-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4631c-106">Tüzel kişinin mali kayıtlarını tanımlamak ve yönetmek için genel muhasebeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="4631c-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="4631c-107">Genel muhasebe, borç ve alacak girişlerinin bir kaydıdır.</span><span class="sxs-lookup"><span data-stu-id="4631c-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="4631c-108">Bu girişler, hesap planında listelenen hesaplar kullanılarak sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="4631c-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="4631c-109">Tahsis kurallarına göre parasal tutarları bir veya daha fazla hesaba veya hesap ve boyut birleşimlerine tahsis edebilir veya dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4631c-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="4631c-110">İki tür tahsisat vardır: sabit ve değişken.</span><span class="sxs-lookup"><span data-stu-id="4631c-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="4631c-111">Genel muhasebe hesapları arasındaki hareketleri kapatabilir ve para birimi tutarlarını yeniden değerleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4631c-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="4631c-112">Bir mali yılın sonunda, sonraki mali yıl için kapanış hareketleri oluşturmanız ve hesaplarınızı hazırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4631c-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="4631c-113">Tek bir, konsolide kuruluş sonuçları için birkaç yan yasal kuruluş için mali sonuçları birleştirmek için konsolidasyon işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4631c-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="4631c-114">Yan şirketler aynı Microsoft Dynamics 365 for Finance and Operations veritabanında veya farklı veritabanlarında olabilir.</span><span class="sxs-lookup"><span data-stu-id="4631c-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="4631c-115">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="4631c-115">Sales tax</span></span>
<span data-ttu-id="4631c-116">Her şirket vergi toplar ve çeşitli vergi kurumlarına vergi öder.</span><span class="sxs-lookup"><span data-stu-id="4631c-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="4631c-117">Kurallar ve oranlar ülke/bölge, il, ilçe ve şehre göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="4631c-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="4631c-118">Ayrıca, vergi dairesi gereksinimleri değiştirdiğinde kuralların düzenli olarak güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="4631c-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="4631c-119">Satış vergisi kodları yetkili kurumlardan aldığınız ve yetkili kurumlara ödediğiniz tutarla ilgili temel ilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="4631c-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="4631c-120">Satış vergisi kodlarını ayarladığınızda, toplanması gereken tutarları veya yüzdeleri tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="4631c-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="4631c-121">Ayrıca bu tutarların veya yüzdelerin hareket tutarlarına uygulanması için çeşitli yöntemleri de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="4631c-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="4631c-122">Bu bölümdeki konular, vergi dairelerinin gerektirdiği yöntemler ve oranlar için satış vergisi kodlarının nasıl ayarlanacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4631c-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







