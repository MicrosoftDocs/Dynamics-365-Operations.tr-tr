---
title: "Gider raporundaki dağıtımlar"
description: "Giderler üzerinde bir gider raporunu girdiğinizde, gideri birden fazla proje, tüzel kişilikler veya kuruluşunuzdaki hesaplara dağıtabilirsiniz."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 97f41bd69f979a60eca0b15ddcc6e2245dc93387
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="de2ea-103">Gider raporundaki dağıtımlar</span><span class="sxs-lookup"><span data-stu-id="de2ea-103">Distributions on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de2ea-104"> Giderler üzerinde bir gider raporunu girdiğinizde, gideri birden fazla proje, mali boyutlar veya kuruluşunuzdaki hesaplara dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de2ea-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="de2ea-105">Örneğin bir Fabrikam satış temsilcisi olan Gamze, Kopenhag'dan Frankfurt'a seyahat etmiştir.</span><span class="sxs-lookup"><span data-stu-id="de2ea-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="de2ea-106">Frankfurt'ta, her bir kuruluş için ayrı projeleri tartışmak üzere iki kuruluşla görüşmüştür.</span><span class="sxs-lookup"><span data-stu-id="de2ea-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="de2ea-107">Gamze, kuruluş A ile proje A üzerinde iki yedi iş günü ve kuruluş B ile proje B üzerinde üç iş günü harcamıştır.</span><span class="sxs-lookup"><span data-stu-id="de2ea-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="de2ea-108">Gamze Frankfurt'ta bulunduğunda iki farklı proje üzerinde çalıştığı için, gider raporunu girdiğinde giderlerini her bir projeye uygun olarak dağıtır.</span><span class="sxs-lookup"><span data-stu-id="de2ea-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="de2ea-109">Aşağıdaki tablo Gamze'nin giderlerini nasıl dağıttığını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="de2ea-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="de2ea-110"><strong>Gider türü</strong></span><span class="sxs-lookup"><span data-stu-id="de2ea-110"><strong>Expense type</strong></span></span> | <span data-ttu-id="de2ea-111"><strong>Toplam gider tutarı</strong></span><span class="sxs-lookup"><span data-stu-id="de2ea-111"><strong>Total expense amount</strong></span></span> | <span data-ttu-id="de2ea-112"><strong>Proje A'ya dağıtılan tutar</strong></span><span class="sxs-lookup"><span data-stu-id="de2ea-112"><strong>Amount distributed to project A</strong></span></span> | <span data-ttu-id="de2ea-113"><strong>Proje B'ye dağıtılan tutar</strong></span><span class="sxs-lookup"><span data-stu-id="de2ea-113"><strong>Amount distributed to project B</strong></span></span> |
|-------------------------------|---------------------------------------|--------------------------------------------------|--------------------------------------------------|
|          <span data-ttu-id="de2ea-114">Tren ücreti</span><span class="sxs-lookup"><span data-stu-id="de2ea-114">Train fare</span></span>           |                <span data-ttu-id="de2ea-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="de2ea-115">DKK 578</span></span>                |                     <span data-ttu-id="de2ea-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="de2ea-116">DKK 405</span></span>                      |                     <span data-ttu-id="de2ea-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="de2ea-117">DKK 173</span></span>                      |
|             <span data-ttu-id="de2ea-118">Otel</span><span class="sxs-lookup"><span data-stu-id="de2ea-118">Hotel</span></span>             |                <span data-ttu-id="de2ea-119">725 Euro</span><span class="sxs-lookup"><span data-stu-id="de2ea-119">EUR 725</span></span>                |                     <span data-ttu-id="de2ea-120">557 Euro</span><span class="sxs-lookup"><span data-stu-id="de2ea-120">EUR 557</span></span>                      |                     <span data-ttu-id="de2ea-121">168 Euro</span><span class="sxs-lookup"><span data-stu-id="de2ea-121">EUR 168</span></span>                      |
|             <span data-ttu-id="de2ea-122">Yemekler</span><span class="sxs-lookup"><span data-stu-id="de2ea-122">Meals</span></span>             |                <span data-ttu-id="de2ea-123">346 Euro</span><span class="sxs-lookup"><span data-stu-id="de2ea-123">EUR 346</span></span>                |                     <span data-ttu-id="de2ea-124">284 Euro</span><span class="sxs-lookup"><span data-stu-id="de2ea-124">EUR 284</span></span>                      |                      <span data-ttu-id="de2ea-125">62 Euro</span><span class="sxs-lookup"><span data-stu-id="de2ea-125">EUR 62</span></span>                      |


