---
title: İşlem yapılacak yerleşimler ve varlıklar
description: Bu konuda Varlık Yönetimi'ndeki işlem yapılacak yerleşimler ve varlıklar açıklanmaktadır. Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve bakım işlerinin yönetilmesine yönelik gelişmiş bir modüldür.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe3e82f425421acdae81a02032ac6252765e1c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439585"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="50ead-104">İşlem yapılacak yerleşimler ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="50ead-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="50ead-105">Bu konuda Varlık Yönetimi'ndeki işlem yapılacak yerleşimler ve varlıklar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="50ead-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="50ead-106">Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve bakım işlerinin yönetilmesine yönelik gelişmiş bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="50ead-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="50ead-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="50ead-107">Overview</span></span>

<span data-ttu-id="50ead-108">Varlık Yönetimi, diğer Finance and Operations uygulamalarındaki çeşitli modüller ile sorunsuz şekilde tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="50ead-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="50ead-109">Aşağıdaki örnekte diğer modüllerle olan arabirimler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="50ead-109">The following illustration shows the interfaces with other modules.</span></span>

![Varlık Yönetiminin diğer modüllerle olan arabirimlerini gösteren diyagram](media/01-overview-image.png)

<span data-ttu-id="50ead-111">Varlık Yönetimi, şirketinizdeki birçok donanım türünün yönetimi ve bakımı ile ilgili tüm görevleri etkili bir şekilde yönetmenize ve gerçekleştirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="50ead-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="50ead-112">Bu donanıma makineler, üretim ekipmanı ve taşıtlar dahildir.</span><span class="sxs-lookup"><span data-stu-id="50ead-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="50ead-113">Varlık Yönetimi birçok sektördeki çözümleri de destekler.</span><span class="sxs-lookup"><span data-stu-id="50ead-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="50ead-114">Aşağıdaki şekilde, Varlık Yönetimi kapsamında olan ana işlevlerin genel görünümü gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="50ead-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Varlık Yönetiminde ana işlevleri gösteren diyagram](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="50ead-116">İşlem yapılacak yerleşimler ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="50ead-116">Functional locations and assets</span></span>

<span data-ttu-id="50ead-117">İşlem yapılacak yerleşimler yerleşimlerdeki varlıkları yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="50ead-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="50ead-118">Bu yönetim, İşlem yapılacak yerleşimlerdeki varlık maliyetlerinin izlenmesini içerir.</span><span class="sxs-lookup"><span data-stu-id="50ead-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="50ead-119">İşlem yapılacak yerleşimler hiyerarşik olarak yapılandırılır ve yerleşimlerin alt yerleşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="50ead-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="50ead-120">İşlem yapılacak yerleşimlerin yapısı statiktir.</span><span class="sxs-lookup"><span data-stu-id="50ead-120">The structure of functional locations is static.</span></span> <span data-ttu-id="50ead-121">Başka bir deyişle, yerleşimlerin yerinde değişiklik yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="50ead-121">In other words, locations can't change place.</span></span> <span data-ttu-id="50ead-122">Varlıklar işlem yapılacak yerleşimlere yüklenebilir ve gerekirse daha sonra başka İşlem yapılacak yerleşimlere yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="50ead-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="50ead-123">Varlık maliyetleri her zaman varlığın yerleşimini izler.</span><span class="sxs-lookup"><span data-stu-id="50ead-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="50ead-124">Başka bir deyişle, bir varlığı yeni bir İşlem yapılacak yerleşime yüklerseniz, varlık otomatik olarak yeni İşlem yapılacak yerleşimle ilgili mali boyutları kullanır.</span><span class="sxs-lookup"><span data-stu-id="50ead-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="50ead-125">Bu nedenle, varlık maliyetleri her zaman varlığın halizahırda yüklü olduğu işlem yapılacak yerleşim ile ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="50ead-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="50ead-126">Mali boyutların bu şekilde otomatik olarak işlenmesi, şirketiniz işlem yapılacak yerleşimlerde kontrol ve raporlama yaparken maliyetlerin tam olarak izlenmesini garanti eder.</span><span class="sxs-lookup"><span data-stu-id="50ead-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="50ead-127">İşlem yapılacak yerleşimler hiyerarşinizi oluşturma şekliniz, şirketinizin dahili ekipmanların korunması veya müşteri ekipmanlarına bakım hizmeti yapılması gereksinimlerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="50ead-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="50ead-128">Aşağıdaki şekil, coğrafi konumları temel alan işlem yapılacak yerleşimler örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="50ead-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Coğrafi konumlara dayalı işlem yapılacak yerleşimleri gösteren diyagram](media/03-overview-image.png)

<span data-ttu-id="50ead-130">Aşağıdaki şekil, müşterileri temel alan işlem yapılacak yerleşimler örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="50ead-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Müşterilere dayalı işlem yapılacak yerleşimleri gösteren diyagram](media/04-overview-image.png)
