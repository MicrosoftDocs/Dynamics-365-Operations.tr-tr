---
title: Ürün reçetesi sürümünü belirleme
description: Bir talep açılımı sırasında bir maddenin varsayılan bir Üretim emri varsa, planlama altyapısı tesise göre geçerli bir ürün reçetesi sürümü bulur.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efc980e3a3dfff6d163812396613a1493f4428a4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213803"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="790ab-103">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="790ab-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="790ab-104">Bir talep açılımı sırasında bir maddenin varsayılan bir Üretim emri varsa, planlama altyapısı tesise göre geçerli bir ürün reçetesi sürümü bulur.</span><span class="sxs-lookup"><span data-stu-id="790ab-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="790ab-105">Tesis boyutu her zaman bilinir ve talep hareketinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="790ab-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="790ab-106">Sıradaki süreç kullanılacak ürün reçetesi sürümünü belirlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="790ab-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="790ab-107">Talep tesisindeki madde için tanımlanmış bir ürün reçetesi sürümü varsa, bu tesise özgü ürün reçetesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="790ab-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="790ab-108">Talep tesisindeki madde için tanımlanmış belirli bir ürün reçetesi sürümü yoksa, genel bir ürün reçetesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="790ab-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="790ab-109">Genel ürün reçetesinde tesis belirtilmez ve birden çok tesis için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="790ab-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="790ab-110">Genel bir ürün reçetesi varsa, o kullanılır.</span><span class="sxs-lookup"><span data-stu-id="790ab-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="790ab-111">Kullanılacak bir genel ürün reçetesi yoksa, talep açılımı bu noktada durur.</span><span class="sxs-lookup"><span data-stu-id="790ab-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="790ab-112">Geçerli bir ürün reçetesi sürümü, ister tesise özgü ister genel bir ürün reçetesi olsun, tarih ve miktar ölçütlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="790ab-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





