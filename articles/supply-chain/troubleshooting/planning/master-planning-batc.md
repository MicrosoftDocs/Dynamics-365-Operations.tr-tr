---
title: Master planlama maddelerini ilgili karşılama grubu değerlerine göre filtreleyemiyorsunuz
description: Master planlama maddelerini ilgili karşılama grubu değerlerine göre filtreleyemiyorsunuz.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049495"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="7266d-103">Master planlama maddelerini ilgili karşılama grubu değerlerine göre filtreleyemiyorsunuz</span><span class="sxs-lookup"><span data-stu-id="7266d-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="7266d-104">KB numarası: 4612572</span><span class="sxs-lookup"><span data-stu-id="7266d-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="7266d-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="7266d-105">Symptoms</span></span>

<span data-ttu-id="7266d-106">Madde karşılama tablosundaki ilgili kayıtların değerlerini temel alarak, master planlama toplu işlemine dahil edilecek maddelere filtre uygulamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="7266d-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="7266d-107">(Örneğin, öğeleri **Satıcı** ve/veya **Karşılama grubu** değerlerine göre maddeleri filtrelemek istiyorsunuz).</span><span class="sxs-lookup"><span data-stu-id="7266d-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="7266d-108">Toplu işlemin filtre kurulumu, **Maddeler** tablosundan **Madde kapsamı** tablosuna bir birleştirme oluşturmanıza ve ardından sorgunuzdaki madde karşılama tablosundan alan değerlerini belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7266d-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="7266d-109">Ancak, bu kurulumu tamamladıktan sonra, sistem yalnızca madde karşılama tablosundan belirtilen alan değerleriyle eşleşen maddeler için değil, tüm madde kapsamı için planlı siparişler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7266d-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="7266d-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="7266d-110">Resolution</span></span>

<span data-ttu-id="7266d-111">Toplu işlem filtresi yalnızca maddelere filtre yapabilir.</span><span class="sxs-lookup"><span data-stu-id="7266d-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="7266d-112">**Madde kapsama** tablosuna bir birleştirme ekleyebilmenize rağmen, bu tabloya karşı yaptığınız filtre ayarları sorgu çıktısını etkilemez.</span><span class="sxs-lookup"><span data-stu-id="7266d-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="7266d-113">Çalışma zamanında, sistem tüm karşılama grupları ve filtre uygulanmış maddelerin sahip olduğu tüm varyasyonlar için planlama çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="7266d-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="7266d-114">Bir madde zaten çalıştırmaya dahil edildikten sonra, madde filtresine dahil edilen tüm karşılama grupları planlama çıktısını etkilemez.</span><span class="sxs-lookup"><span data-stu-id="7266d-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
