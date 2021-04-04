---
title: Tümleşik siteler ve ambarlar
description: Bu konu Finance and Operations ile Dataverse arasında site ve depo verileri tümleştirmesini açıklar.
author: t-benebo
manager: AnnBe
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
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560373"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="26671-103">Tümleşik siteler ve ambarlar</span><span class="sxs-lookup"><span data-stu-id="26671-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="26671-104">Bu konu Finance and Operations ile Dataverse arasında site ve depo verileri tümleştirmesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="26671-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="26671-105">Operasyonel tesisler ve ambarlar, Supply Chain Management uygulamasındaki ortak kavramlardır.</span><span class="sxs-lookup"><span data-stu-id="26671-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="26671-106">Bunlar şirketinizin tedarik zincirini modellemek için kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="26671-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="26671-107">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="26671-107">Templates</span></span>

<span data-ttu-id="26671-108">Dataverse ile tümleştirme sayesinde, bu kavramlar ve ilgili tüm bilgiler aşağıdaki tabloda yer alan siteler ve ambar veri tabloları kullanılarak Dataverse'te bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="26671-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="26671-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="26671-109">Finance and Operations apps</span></span> | <span data-ttu-id="26671-110">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="26671-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="26671-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="26671-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="26671-112">Siteler</span><span class="sxs-lookup"><span data-stu-id="26671-112">Sites</span></span> | <span data-ttu-id="26671-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="26671-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="26671-114">Ambarlar</span><span class="sxs-lookup"><span data-stu-id="26671-114">Warehouses</span></span> | <span data-ttu-id="26671-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="26671-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]