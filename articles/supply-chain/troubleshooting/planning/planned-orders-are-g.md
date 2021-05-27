---
title: Master planlama, hayali ürünler için planlı siparişler oluşturuyor
description: Bir master planlama çalıştırıldıktan sonra hayali ürünler için planlı siparişler oluşturuluyor.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026990"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="31d76-103">Master planlama, hayali ürünler için planlı siparişler oluşturuyor</span><span class="sxs-lookup"><span data-stu-id="31d76-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="31d76-104">KB numarası: 4614729</span><span class="sxs-lookup"><span data-stu-id="31d76-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="31d76-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="31d76-105">Symptoms</span></span>

<span data-ttu-id="31d76-106">Bir master planlama çalıştırıldıktan sonra hayali ürünler için planlı siparişler oluşturuluyor.</span><span class="sxs-lookup"><span data-stu-id="31d76-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="31d76-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="31d76-107">Resolution</span></span>

<span data-ttu-id="31d76-108">Serbest bırakılan ürünlerin **Hayali** seçeneğinin ayarı, ürün reçetesindeki (BOM) varsayılan satır türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="31d76-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="31d76-109">**Hayali** seçeneği *Evet* olarak ayarlandığında, sistem madde için planlanan siparişler oluşturur, ancak her planlı sipariş için **Doğrudan türetilmiş gereksinim** seçeneği *Evet* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="31d76-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="31d76-110">Bu nedenle, planlı üretim emri kendi başına kesinleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="31d76-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="31d76-111">Bunun yerine, üst üretim emri kesinleştirildiğinde her zaman otomatik olarak dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="31d76-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="31d76-112">Ayrıca, planlı hayali siparişin ürün reçetesi satırları üst üretim emrinin ürün reçetesine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="31d76-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
