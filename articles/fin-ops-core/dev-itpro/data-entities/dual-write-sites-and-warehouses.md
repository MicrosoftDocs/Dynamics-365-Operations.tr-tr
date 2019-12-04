---
title: Tümleşik siteler ve ambarlar
description: Bu konu Finance and Operations ile Common Data Service arasında site ve ambar verileri tümleştirmesini açıklar.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771011"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="cacbd-103">Tümleşik siteler ve ambarlar</span><span class="sxs-lookup"><span data-stu-id="cacbd-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cacbd-104">Bu konu Finance and Operations ile Common Data Service arasında site ve ambar verileri tümleştirmesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="cacbd-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="cacbd-105">Operasyonel tesisler ve ambarlar, Supply Chain Management uygulamasındaki ortak kavramlardır.</span><span class="sxs-lookup"><span data-stu-id="cacbd-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="cacbd-106">Bunlar şirketinizin tedarik zincirini modellemek için kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="cacbd-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="cacbd-107">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="cacbd-107">Templates</span></span>

<span data-ttu-id="cacbd-108">Common Data Service ile tümleştirme sayesinde, bu kavramlar ve ilgili tüm bilgiler aşağıdaki tabloda yer alarak siteler ve Common Data Service ambarlar veri varlıkları kullanılarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cacbd-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="cacbd-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="cacbd-109">Finance and Operations apps</span></span> | <span data-ttu-id="cacbd-110">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="cacbd-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="cacbd-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="cacbd-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="cacbd-112">Siteler</span><span class="sxs-lookup"><span data-stu-id="cacbd-112">Sites</span></span> | <span data-ttu-id="cacbd-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="cacbd-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="cacbd-114">Ambarlar</span><span class="sxs-lookup"><span data-stu-id="cacbd-114">Warehouses</span></span> | <span data-ttu-id="cacbd-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="cacbd-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

