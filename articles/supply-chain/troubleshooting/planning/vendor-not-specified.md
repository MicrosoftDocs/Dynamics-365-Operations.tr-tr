---
title: Planlı siparişler kesinleştirildiğinde satıcı belirtilmedi
description: Planlı siparişleri kesinleştirmeye çalıştığınızda, hiçbir satıcı belirtilmediğini belirten bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cf41295045211f8a714194494028922d573c9e9e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294197"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a><span data-ttu-id="3aab2-103">Planlı siparişler kesinleştirildiğinde satıcı belirtilmedi</span><span class="sxs-lookup"><span data-stu-id="3aab2-103">Vendor isn't specified when planned orders are firmed</span></span>

<span data-ttu-id="3aab2-104">Hata kodu: SYS23532</span><span class="sxs-lookup"><span data-stu-id="3aab2-104">Error code: SYS23532</span></span>

## <a name="symptoms"></a><span data-ttu-id="3aab2-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="3aab2-105">Symptoms</span></span>

<span data-ttu-id="3aab2-106">Planlı siparişleri kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="3aab2-106">When you try to firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="3aab2-107">Satıcı belirlenmedi</span><span class="sxs-lookup"><span data-stu-id="3aab2-107">Vendor is not specified</span></span>

## <a name="resolution"></a><span data-ttu-id="3aab2-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="3aab2-108">Resolution</span></span>

<span data-ttu-id="3aab2-109">Satıcı belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3aab2-109">To specify a vendor, follow these steps.</span></span>

1. <span data-ttu-id="3aab2-110">Satıcının eksik olduğu planlı siparişi açın.</span><span class="sxs-lookup"><span data-stu-id="3aab2-110">Open the planned order that is missing a vendor.</span></span>
1. <span data-ttu-id="3aab2-111">**Planlı tedarik** hızlı sekmesinde, **Satıcı** alanında bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="3aab2-111">On the **Planned supply** FastTab, in the **Vendor** field, select a vendor.</span></span>
