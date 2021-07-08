---
title: Planlı üretim emrinin kesinleştirebilmesi için önce planlanması gerekir
description: Planlı bir siparişi kesinleştirmeye çalıştığınızda, siparişin kesinleştirilebilmesi için önce zamanlanması gerektiğini bildiren bir hata iletisi alırsınız.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294204"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="b2de2-103">Planlı üretim emrinin kesinleştirebilmesi için önce planlanması gerekir</span><span class="sxs-lookup"><span data-stu-id="b2de2-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="b2de2-104">Hata kodu: SYS309802</span><span class="sxs-lookup"><span data-stu-id="b2de2-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="b2de2-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="b2de2-105">Symptoms</span></span>

<span data-ttu-id="b2de2-106">Planlı siparişi kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="b2de2-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="b2de2-107">Planlanlı üretim emrinin kesinleştirilmeden önce zaman çizelgesinin yapılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b2de2-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="b2de2-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="b2de2-108">Cause</span></span>

<span data-ttu-id="b2de2-109">Zamanlanan başlangıç ve bitiş tarihleri boş olamaz.</span><span class="sxs-lookup"><span data-stu-id="b2de2-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="b2de2-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="b2de2-110">Resolution</span></span>

<span data-ttu-id="b2de2-111">Planlı siparişin başlangıç ve bitiş tarihlerini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b2de2-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="b2de2-112">**Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="b2de2-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="b2de2-113">İlgili planlı siparişi açın.</span><span class="sxs-lookup"><span data-stu-id="b2de2-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="b2de2-114">**Genel** Hızlı Sekmesinde, **Zamanlanmış** bölümünde, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında tarihleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="b2de2-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
