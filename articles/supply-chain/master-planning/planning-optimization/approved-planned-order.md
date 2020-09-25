---
title: Planlı siparişleri onayla
description: Bu konu, planlama optimizasyonu sırasında desteklenen planlı siparişlerin onayını açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759700"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="1ecca-103">Planlı siparişleri onayla</span><span class="sxs-lookup"><span data-stu-id="1ecca-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ecca-104">Bu konu, planlama optimizasyonunda planlı siparişlerin durumunun nasıl güncelleştirileceği hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1ecca-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="1ecca-105">Planlı siparişlerden kesinleştirilmiş sipariş oluşturmak üzere planlı siparişler onayının isteğe bağlı adımı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1ecca-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="1ecca-106">Değiştirilmiş Planlı siparişlerin onaylanması önerilir, aksi durumda sonraki planlama çalışması sırasında düzenlemeler yok sayılır ve üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1ecca-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Planlı sipariş akışı](media/approved-planned-orders-1.png)

<span data-ttu-id="1ecca-108">**Durum** alanı, aşağıdaki değerleri kullanarak ilerlemenizi izlemenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="1ecca-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="1ecca-109">**İşlem görmedi:** Master planlama, planlı siparişler ürettiğinde, planlı siparişler *İşlem görmedi* durumunda olur.</span><span class="sxs-lookup"><span data-stu-id="1ecca-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="1ecca-110">Bu durumdaki planlı siparişler sonraki planlama çalışmasında silinir.</span><span class="sxs-lookup"><span data-stu-id="1ecca-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="1ecca-111">**Tamamlandı:** Planlı siparişi kesinleştirmemeye karar verirseniz, durumu *Tamamlandı* olarak değiştirerek bu planlı siparişin değerlendirilmesini tamamladığınızı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ecca-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="1ecca-112">*İşlenmemiş* ve *Tamamlandı* durumlarının sistem tarafından aynı kabul edildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1ecca-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="1ecca-113">**Onaylandı:** Düzenlemeleri korumak istiyorsanız veya planlı bir siparişi kesinleştirmeyi planlıyorsanız, durumunu *Onaylandı* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="1ecca-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="1ecca-114">Sonraki bir master planlama çalışması sırasında değiştirilmemeleri veya silinmemeleri için *Onaylandı* durumundaki planlı siparişler sabit olarak kabul edilerek master planlama tarafından tedarik edilmesi beklenir.</span><span class="sxs-lookup"><span data-stu-id="1ecca-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="1ecca-115">Bunu başarmak için, planlama mantığı, Master planlama sırasında eski plan versiyonundaki *onaylanan* planlı siparişleri yeni plan sürümüne kopyalar.</span><span class="sxs-lookup"><span data-stu-id="1ecca-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="1ecca-116">*Onaylandı* durumundaki planlı siparişlerinin yalnızca belirli master plan içinde tedarik edildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1ecca-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="1ecca-117">Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ecca-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
