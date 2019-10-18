---
title: Gider raporundaki dağıtımlar
description: Giderler üzerinde bir gider raporunu girdiğinizde, gideri birden fazla proje, tüzel kişilikler veya kuruluşunuzdaki hesaplara dağıtabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b450c952bd53d6e573b08cfcfd86ad666f743040
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187648"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="a1d4f-103">Gider raporundaki dağıtımlar</span><span class="sxs-lookup"><span data-stu-id="a1d4f-103">Distributions on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1d4f-104"> Giderler üzerinde bir gider raporunu girdiğinizde, gideri birden fazla proje, mali boyutlar veya kuruluşunuzdaki hesaplara dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1d4f-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="a1d4f-105">Örneğin bir Fabrikam satış temsilcisi olan Gamze, Kopenhag'dan Frankfurt'a seyahat etmiştir.</span><span class="sxs-lookup"><span data-stu-id="a1d4f-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="a1d4f-106">Frankfurt'ta, her bir kuruluş için ayrı projeleri tartışmak üzere iki kuruluşla görüşmüştür.</span><span class="sxs-lookup"><span data-stu-id="a1d4f-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="a1d4f-107">Gamze, kuruluş A ile proje A üzerinde iki yedi iş günü ve kuruluş B ile proje B üzerinde üç iş günü harcamıştır.</span><span class="sxs-lookup"><span data-stu-id="a1d4f-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="a1d4f-108">Gamze Frankfurt'ta bulunduğunda iki farklı proje üzerinde çalıştığı için, gider raporunu girdiğinde giderlerini her bir projeye uygun olarak dağıtır.</span><span class="sxs-lookup"><span data-stu-id="a1d4f-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="a1d4f-109">Aşağıdaki tablo Gamze'nin giderlerini nasıl dağıttığını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a1d4f-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="a1d4f-110">Gider türü</span><span class="sxs-lookup"><span data-stu-id="a1d4f-110">Expense type</span></span> | <span data-ttu-id="a1d4f-111">Toplam gider tutarı</span><span class="sxs-lookup"><span data-stu-id="a1d4f-111">Total expense amount</span></span>|<span data-ttu-id="a1d4f-112">Proje A'ya dağıtılan tutar</span><span class="sxs-lookup"><span data-stu-id="a1d4f-112">Amount distributed to project A</span></span>| <span data-ttu-id="a1d4f-113">Proje B'ye dağıtılan tutar</span><span class="sxs-lookup"><span data-stu-id="a1d4f-113">Amount distributed to project B</span></span> |
|--------------|---------------------|-------------------------------|---------------------------------|
|<span data-ttu-id="a1d4f-114">Tren ücreti</span><span class="sxs-lookup"><span data-stu-id="a1d4f-114">Train fare</span></span>   |<span data-ttu-id="a1d4f-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="a1d4f-115">DKK 578</span></span>              |<span data-ttu-id="a1d4f-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="a1d4f-116">DKK 405</span></span>                        |<span data-ttu-id="a1d4f-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="a1d4f-117">DKK 173</span></span>                          |
|<span data-ttu-id="a1d4f-118">Otel</span><span class="sxs-lookup"><span data-stu-id="a1d4f-118">Hotel</span></span>         |<span data-ttu-id="a1d4f-119">725 Euro</span><span class="sxs-lookup"><span data-stu-id="a1d4f-119">EUR 725</span></span>              |<span data-ttu-id="a1d4f-120">557 Euro</span><span class="sxs-lookup"><span data-stu-id="a1d4f-120">EUR 557</span></span>                        |<span data-ttu-id="a1d4f-121">168 Euro</span><span class="sxs-lookup"><span data-stu-id="a1d4f-121">EUR 168</span></span>                          |
|<span data-ttu-id="a1d4f-122">Yemekler</span><span class="sxs-lookup"><span data-stu-id="a1d4f-122">Meals</span></span>         |<span data-ttu-id="a1d4f-123">346 Euro</span><span class="sxs-lookup"><span data-stu-id="a1d4f-123">EUR 346</span></span>              |<span data-ttu-id="a1d4f-124">284 Euro</span><span class="sxs-lookup"><span data-stu-id="a1d4f-124">EUR 284</span></span>                        |<span data-ttu-id="a1d4f-125">62 Euro</span><span class="sxs-lookup"><span data-stu-id="a1d4f-125">EUR 62</span></span>                           |

