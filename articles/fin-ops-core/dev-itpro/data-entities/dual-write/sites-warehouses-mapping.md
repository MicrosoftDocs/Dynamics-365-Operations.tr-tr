---
title: Tümleşik siteler ve ambarlar
description: Bu konu Finance and Operations ile Dataverse arasında site ve depo verileri tümleştirmesini açıklar.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750678"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="72ad5-103">Tümleşik siteler ve ambarlar</span><span class="sxs-lookup"><span data-stu-id="72ad5-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="72ad5-104">Bu konu Finance and Operations ile Dataverse arasında site ve depo verileri tümleştirmesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="72ad5-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="72ad5-105">Operasyonel tesisler ve ambarlar, Supply Chain Management uygulamasındaki ortak kavramlardır.</span><span class="sxs-lookup"><span data-stu-id="72ad5-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="72ad5-106">Bunlar şirketinizin tedarik zincirini modellemek için kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="72ad5-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="72ad5-107">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="72ad5-107">Templates</span></span>

<span data-ttu-id="72ad5-108">Dataverse ile tümleştirme sayesinde, bu kavramlar ve ilgili tüm bilgiler aşağıdaki tabloda yer alan siteler ve ambar veri tabloları kullanılarak Dataverse'te bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="72ad5-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="72ad5-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="72ad5-109">Finance and Operations apps</span></span> | <span data-ttu-id="72ad5-110">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="72ad5-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="72ad5-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="72ad5-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="72ad5-112">Siteler</span><span class="sxs-lookup"><span data-stu-id="72ad5-112">Sites</span></span> | <span data-ttu-id="72ad5-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="72ad5-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="72ad5-114">Ambarlar</span><span class="sxs-lookup"><span data-stu-id="72ad5-114">Warehouses</span></span> | <span data-ttu-id="72ad5-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="72ad5-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]