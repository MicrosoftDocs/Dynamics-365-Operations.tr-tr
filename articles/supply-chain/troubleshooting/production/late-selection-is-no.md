---
title: Üretim emirleri bir toplu iş aracılığıyla sıfırlanırsa, geç seçim dikkate alınmaz
description: Bir üretim emrinin durumunu sıfırlamak için tekrarlayan bir toplu iş kullandığınızda, geç seçimler dikkate alınmaz.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026977"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="c37f3-103">Üretim emirleri bir toplu iş aracılığıyla sıfırlanırsa, geç seçim dikkate alınmaz</span><span class="sxs-lookup"><span data-stu-id="c37f3-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="c37f3-104">KB numarası: 4614634</span><span class="sxs-lookup"><span data-stu-id="c37f3-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="c37f3-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="c37f3-105">Symptoms</span></span>

<span data-ttu-id="c37f3-106">Bir üretim emrinin durumunu sıfırlamak için tekrarlayan bir toplu iş kullandığınızda, geç seçimler dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="c37f3-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="c37f3-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="c37f3-107">Resolution</span></span>

<span data-ttu-id="c37f3-108">Mevcut tasarım, *Durumu sıfırla* işlemi için geç seçimlerinin kullanımını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="c37f3-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
