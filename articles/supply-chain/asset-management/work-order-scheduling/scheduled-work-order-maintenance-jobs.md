---
title: Planlanan iş emri bakım işleri
description: Bu konu, Varlık Yönetiminde planlanan iş emri bakım işlerini açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887194"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="ac8aa-103">Planlanan iş emri bakım işleri</span><span class="sxs-lookup"><span data-stu-id="ac8aa-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ac8aa-104">**Planlanan iş emri bakım işleri** sayfası, kaynağa tahsis edilen iş emirlerinin genel görünümünü almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="ac8aa-105">"İnsan kaynakları", "Araç" ve "Makine" kaynak türlerini kullanan iş emirleri listede gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="ac8aa-106">Liste, belirli bir kaynağa tahsis edilen iş emirlerinin genel görünümünü elde etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="ac8aa-107">Ayrıca, örneğin sabahleyin hastalık durumunda çağrılan bir bakım çalışanına tahsis edilmiş bir iş emrini hızlı bir şekilde bulmak ve işe hızlıca başka bir çalışanı tahsis etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="ac8aa-108">Planlamış iş emri bakım işlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ac8aa-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="ac8aa-109">**Varlık yönetimi** > **Ortak** > **İş emirleri** > **Planlanan iş emri bakım işleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="ac8aa-110">İş emri yaşam döngüsü durumu "Planlandı" veya "Devam ediyor" olarak ayarlanmış tüm iş emirlerinin listesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="ac8aa-111">Listeyi, örneğin bakım çalışanına göre sıralayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="ac8aa-112">Listeyi belirli bir kaynağa veya bakım çalışanına tahsis edilen iş emirlerini gösterecek şekilde sınırlamak için de filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="ac8aa-113">İş emrindeki notları görebilir ve gerekirse iş emri işini seçip **Notlar**'a tıklayarak yeni notlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="ac8aa-114">Bir iş emrine bir bakım çalışanı tahsis etmek istiyorsanız, listeden iş emrini seçin ve **İş emri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="ac8aa-115">**İş emri** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-115">The **Work order** page opens.</span></span> <span data-ttu-id="ac8aa-116">İş emrini belirli bir bakım çalışanına planlamak için **Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="ac8aa-117">Bir veya birden çok iş emri planlama hakkında daha fazla bilgi için [İş emirleri planlama](../work-order-scheduling/schedule-work-orders.md) ve [İş emri gönderme](../work-order-scheduling/dispatch-work-order.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="ac8aa-118">Aşağıdaki şekilde **Planlanan iş emri bakım işleri** sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ac8aa-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Şekil 1](media/07-work-order-scheduling.png)

