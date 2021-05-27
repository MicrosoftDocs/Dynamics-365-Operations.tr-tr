---
title: İşlenen dolaylı maliyetler raporu, silinen üretim emirlerini içerir
description: İşlenen dolaylı maliyetler raporu, kısmen işlenmiş ve daha sonra silinen üretim emirleri hakkında bilgi sunar.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026984"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="c11d4-103">İşlenen dolaylı maliyetler raporu, silinen üretim emirlerini içerir</span><span class="sxs-lookup"><span data-stu-id="c11d4-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="c11d4-104">KB numarası: 4612748</span><span class="sxs-lookup"><span data-stu-id="c11d4-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="c11d4-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="c11d4-105">Symptoms</span></span>

<span data-ttu-id="c11d4-106">**İşlenen dolaylı maliyetler** raporu, kısmen işlenmiş ve daha sonra silinen üretim emirleri hakkında bilgi sunar.</span><span class="sxs-lookup"><span data-stu-id="c11d4-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="c11d4-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="c11d4-107">Resolution</span></span>

<span data-ttu-id="c11d4-108">Bir üretim emrini tersine çevirdiğinizde, aynı zamanda o üretim emrinin tüm hareketlerini de tersine çevirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c11d4-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="c11d4-109">Üretim emrini sildiğinizde, alt genel muhasebe tabloları ve genel muhasebe ile ilişkili tüm hareketler korunur.</span><span class="sxs-lookup"><span data-stu-id="c11d4-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="c11d4-110">Raporlar, alt genel muhasebe tablolarındaki hareketleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="c11d4-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="c11d4-111">Belirli üretim emri için net değerin 0,00 olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c11d4-111">For the specific production order, the net value should be 0.00.</span></span>
