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
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53091f2e3c159f73f11b3dfcefd597f2c1494d19
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253098"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="9e202-104">İşlem yapılacak yerleşimler ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="9e202-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9e202-105">Bu konuda Varlık Yönetimi'ndeki işlem yapılacak yerleşimler ve varlıklar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e202-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="9e202-106">Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve bakım işlerinin yönetilmesine yönelik gelişmiş bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="9e202-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="9e202-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="9e202-107">Overview</span></span>

<span data-ttu-id="9e202-108">Varlık Yönetimi, diğer Finance and Operations uygulamalarındaki çeşitli modüller ile sorunsuz şekilde tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9e202-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="9e202-109">Aşağıdaki örnekte diğer modüllerle olan arabirimler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9e202-109">The following illustration shows the interfaces with other modules.</span></span>

![Varlık Yönetiminin diğer modüllerle olan arabirimlerini gösteren diyagram](media/01-overview-image.png)

<span data-ttu-id="9e202-111">Varlık Yönetimi, şirketinizdeki birçok donanım türünün yönetimi ve bakımı ile ilgili tüm görevleri etkili bir şekilde yönetmenize ve gerçekleştirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="9e202-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="9e202-112">Bu donanıma makineler, üretim ekipmanı ve taşıtlar dahildir.</span><span class="sxs-lookup"><span data-stu-id="9e202-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="9e202-113">Varlık Yönetimi birçok sektördeki çözümleri de destekler.</span><span class="sxs-lookup"><span data-stu-id="9e202-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="9e202-114">Aşağıdaki şekilde, Varlık Yönetimi kapsamında olan ana işlevlerin genel görünümü gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9e202-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Varlık Yönetiminde ana işlevleri gösteren diyagram](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="9e202-116">İşlem yapılacak yerleşimler ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="9e202-116">Functional locations and assets</span></span>

<span data-ttu-id="9e202-117">İşlem yapılacak yerleşimler yerleşimlerdeki varlıkları yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9e202-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="9e202-118">Bu yönetim, İşlem yapılacak yerleşimlerdeki varlık maliyetlerinin izlenmesini içerir.</span><span class="sxs-lookup"><span data-stu-id="9e202-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="9e202-119">İşlem yapılacak yerleşimler hiyerarşik olarak yapılandırılır ve yerleşimlerin alt yerleşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="9e202-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="9e202-120">İşlem yapılacak yerleşimlerin yapısı statiktir.</span><span class="sxs-lookup"><span data-stu-id="9e202-120">The structure of functional locations is static.</span></span> <span data-ttu-id="9e202-121">Başka bir deyişle, yerleşimlerin yerinde değişiklik yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="9e202-121">In other words, locations can't change place.</span></span> <span data-ttu-id="9e202-122">Varlıklar işlem yapılacak yerleşimlere yüklenebilir ve gerekirse daha sonra başka İşlem yapılacak yerleşimlere yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="9e202-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="9e202-123">Varlık maliyetleri her zaman varlığın yerleşimini izler.</span><span class="sxs-lookup"><span data-stu-id="9e202-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="9e202-124">Başka bir deyişle, bir varlığı yeni bir İşlem yapılacak yerleşime yüklerseniz, varlık otomatik olarak yeni İşlem yapılacak yerleşimle ilgili mali boyutları kullanır.</span><span class="sxs-lookup"><span data-stu-id="9e202-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="9e202-125">Bu nedenle, varlık maliyetleri her zaman varlığın halizahırda yüklü olduğu işlem yapılacak yerleşim ile ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="9e202-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="9e202-126">Mali boyutların bu şekilde otomatik olarak işlenmesi, şirketiniz işlem yapılacak yerleşimlerde kontrol ve raporlama yaparken maliyetlerin tam olarak izlenmesini garanti eder.</span><span class="sxs-lookup"><span data-stu-id="9e202-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="9e202-127">İşlem yapılacak yerleşimler hiyerarşinizi oluşturma şekliniz, şirketinizin dahili ekipmanların korunması veya müşteri ekipmanlarına bakım hizmeti yapılması gereksinimlerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e202-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="9e202-128">Aşağıdaki şekil, coğrafi konumları temel alan işlem yapılacak yerleşimler örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e202-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Coğrafi konumlara dayalı işlem yapılacak yerleşimleri gösteren diyagram](media/03-overview-image.png)

<span data-ttu-id="9e202-130">Aşağıdaki şekil, müşterileri temel alan işlem yapılacak yerleşimler örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e202-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Müşterilere dayalı işlem yapılacak yerleşimleri gösteren diyagram](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]