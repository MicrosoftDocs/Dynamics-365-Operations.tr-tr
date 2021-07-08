---
title: Master plan için parametreler yok
description: Planlı siparişi kesinleştirmeye çalıştığınızda, master plan için hiçbir parametre belirtilmediğini belirten bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294202"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="1f000-103">Master plan için parametreler yok</span><span class="sxs-lookup"><span data-stu-id="1f000-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="1f000-104">Hata kodu: SYS25368</span><span class="sxs-lookup"><span data-stu-id="1f000-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="1f000-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="1f000-105">Symptoms</span></span>

<span data-ttu-id="1f000-106">Planlı siparişi kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="1f000-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="1f000-107">%1 master planına ait parametreler yok.</span><span class="sxs-lookup"><span data-stu-id="1f000-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="1f000-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="1f000-108">Cause</span></span>

<span data-ttu-id="1f000-109">Yapılandırma sorunları nedeniyle, sistem belirtilen planın ayarlarını bulamıyor.</span><span class="sxs-lookup"><span data-stu-id="1f000-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="1f000-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="1f000-110">Resolution</span></span>

- <span data-ttu-id="1f000-111">**Master planlama \> Kurulum \> Planlar \> Master planlar**'a gidin ve belirtilen ada sahip bir plan olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1f000-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
