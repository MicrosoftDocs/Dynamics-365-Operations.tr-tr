---
title: Bölmeden sonra azalan bakiyeli amortisman
description: Bu konu, Sabit varlıklarda bir varlık bölündükten sonra amortismanı hesaplamak için azalan bakiye yönteminin kullanılmasını açıklamaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f276f49e5b1bc2814dc851f1ad4204a151d86c43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222395"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="8c5a9-103">Bölmeden sonra azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="8c5a9-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c5a9-104">Bu konu, Sabit varlıklarda varlık başka bir varlığa bölündükten sonra amortismanı hesaplamak için azalan bakiye yönteminin kullanılmasını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="8c5a9-105">Varlık defterinde yapılandırılan amortisman yılı mali yıldır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="8c5a9-106">Daha fazla bilgi için bkz. [Azalan bakiyeli amortisman](reduce-balance-depreciation.md) ve [Sabit varlığı bölme](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="8c5a9-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="8c5a9-107">Sabit bir varlığı, varlığın elde edildiği dönemden sonraki mali dönemde bölerseniz, varlığın önceki yıl için net defter değeri (NDD) azalan bakiyeli amortisman ile hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="8c5a9-108">Ayrıca, varlığı bölecek hareketten oluşturulan alım ve amortisman düzeltme hareketlerini de hesaplar.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="8c5a9-109">Bu davranış, varlığın bir mali yılda edinildiği ve sonraki bir mali yılda bölündüğü varsayılır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="8c5a9-110">Bölünmeden sonra özgün varlık için amorti edilmesi gereken tutar, varlık bölünmeden önce varlığın NDD'sini ve bölünme için deftere nakledilen alım ve amortisman düzeltme hareketini yansıtır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="8c5a9-111">Örneğin, aşağıdaki durumlar geçerli olacaktır:</span><span class="sxs-lookup"><span data-stu-id="8c5a9-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="8c5a9-112">Mali dönem 30 Haziran ile 1 Temmuz arasındadır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="8c5a9-113">Azalan bakiye oranı yüzde 18'dir ve bir varlık Haziran 2019'da 10.000 ABD doları alım fiyatına alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="8c5a9-114">İlk mali yılın amortismanı 18.000 ABD dolarına eşittir, aylık amortisman 150 ABD dolarına eşittir ve varlık Kasım 2019'a kadar 738,75 ABD doları tutarında amorti edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="8c5a9-115">Kasım 2019'da varlığın yüzde 80'i başka bir sabit varlığa bölünmüştür.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="8c5a9-116">[![Bölmeden sonra azalan bakiyeli amortisman](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="8c5a9-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="8c5a9-117">Orijinal varlık için amortisman tutarı 1.822,25 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="8c5a9-118">Bu tutar, bölünme hareketi deftere nakledilmeden önceki NDD (9.111,25 ABD doları), artı bölünme hareketinin deftere nakli sırasında oluşan alım düzeltme (-8.000 ABD doları), artı bölünme hareketi sırasında oluşan amortisman düzeltme (711 ABD doları) sonucuna eşittir.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="8c5a9-119">Bu nedenle, ikinci yılın amortismanı (1.822,25 × yüzde 18) ÷ 12 = 27,33 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="8c5a9-120">İlk yılda yeni sabit varlığın amortisman tutarı (8.000 × yüzde 18) ÷ 12 = 120 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="8c5a9-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]