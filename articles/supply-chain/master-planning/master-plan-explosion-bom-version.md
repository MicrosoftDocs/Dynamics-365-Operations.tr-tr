---
title: Bir ürün reçetesi versiyonu açılımı
description: Bu makalede ürün reçetesi (BOM) sürümü açılımı içeren bir master planlama senaryosu açıklanmaktadır.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f3c800d96805df38a2e31018f2d6c305e3ed7da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "353920"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="49476-103">Bir ürün reçetesi versiyonu açılımı</span><span class="sxs-lookup"><span data-stu-id="49476-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49476-104">Bu makalede ürün reçetesi (BOM) sürümü açılımı içeren bir master planlama senaryosu açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="49476-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="49476-105">Bir ürün reçetesi sürümünün talep açılımı, belirli bir tesisteki ve muhtemelen belirli bir ambardaki her ürün satırı maddesine yönelik bir talep oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49476-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="49476-106">Bir tesise özel ürün reçetesinde, her ürün reçetesi satırı için belirli bir ambar tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="49476-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="49476-107">Ek olarak, her ürün reçetesi satırı için maddenin boyut ayarları ambarın gerekli olup olmadığını belirlemektedir.</span><span class="sxs-lookup"><span data-stu-id="49476-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="49476-108">Her ürün reçetesi satırı maddesi için sonuçta elde edilen talep, ardından ilave talep açılımının başlangıç noktasını oluşturmaktadır.</span><span class="sxs-lookup"><span data-stu-id="49476-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="49476-109">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="49476-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="49476-110">Tesis boyutları zorunludur ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="49476-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="49476-111">Tesis boyutu tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="49476-111">The site dimension is consistent.</span></span> <span data-ttu-id="49476-112">Bu nedenle, daha düşük düzeydeki talep için tasarlanmış tesis başlangıçtaki talep hareketindeki tesisle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="49476-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="49476-113">Aşağıdaki resimde, master planlama talep açılımının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="49476-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Ürün reçetesi versiyonu kullanılarak talep açılımı](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="49476-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="49476-115">Additional resources</span></span>
--------

[<span data-ttu-id="49476-116">Master planlama - ürün reçetesi sürümünün nasıl belirlendiği</span><span class="sxs-lookup"><span data-stu-id="49476-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="49476-117">Master planlama ve birden çok tesis işlevi</span><span class="sxs-lookup"><span data-stu-id="49476-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)



