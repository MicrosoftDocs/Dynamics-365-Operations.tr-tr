---
title: Ürün reçetesi sürümünü belirleme
description: Bir talep açılımı sırasında bir maddenin varsayılan bir Üretim emri varsa, planlama altyapısı tesise göre geçerli bir ürün reçetesi sürümü bulur.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833629"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="a899b-103">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="a899b-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a899b-104">Bir talep açılımı sırasında bir maddenin varsayılan bir Üretim emri varsa, planlama altyapısı tesise göre geçerli bir ürün reçetesi sürümü bulur.</span><span class="sxs-lookup"><span data-stu-id="a899b-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="a899b-105">Tesis boyutu her zaman bilinir ve talep hareketinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="a899b-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="a899b-106">Sıradaki süreç kullanılacak ürün reçetesi sürümünü belirlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="a899b-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="a899b-107">Talep tesisindeki madde için tanımlanmış bir ürün reçetesi sürümü varsa, bu tesise özgü ürün reçetesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a899b-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="a899b-108">Talep tesisindeki madde için tanımlanmış belirli bir ürün reçetesi sürümü yoksa, genel bir ürün reçetesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a899b-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="a899b-109">Genel ürün reçetesinde tesis belirtilmez ve birden çok tesis için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a899b-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="a899b-110">Genel bir ürün reçetesi varsa, o kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a899b-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="a899b-111">Kullanılacak bir genel ürün reçetesi yoksa, talep açılımı bu noktada durur.</span><span class="sxs-lookup"><span data-stu-id="a899b-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="a899b-112">Geçerli bir ürün reçetesi sürümü, ister tesise özgü ister genel bir ürün reçetesi olsun, tarih ve miktar ölçütlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a899b-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]