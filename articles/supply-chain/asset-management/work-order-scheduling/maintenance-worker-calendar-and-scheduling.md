---
title: Bakım görevlisi takvimi ve zamanlama
description: Bu konu, Varlık Yönetiminde zamanlamayla ilgili olarak bakım çalışanı takvimini açıklar.
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
ms.openlocfilehash: 3f86f6475e5226443f5e4d43fb91acafe2afdbb9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887400"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="dcbd9-103">Bakım görevlisi takvimi ve zamanlama</span><span class="sxs-lookup"><span data-stu-id="dcbd9-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="dcbd9-104">İş emirlerini zamanlarken bakım görevlileri, araçlar ve varlıklar için bir zamanlama oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="dcbd9-105">Bakım görevlileri zamanlaması gerçekleştirebilmek için, her bakım görevlisi için bir takvim ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-105">In order to carry out scheduling on maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="dcbd9-106">Bakım görevlileri kaynakla ilgilidir ve çalışma zamanı takvimleri kaynaklarda ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-106">Maintenance workers are related to a resource, and working time calendars are set up on resoures.</span></span> <span data-ttu-id="dcbd9-107">Bir çalışanla ilgili kaynak ve takvimi **Varlık yönetimi** > **Kurulum** > **Çalışanlar** > **Çalışanlar** altından ayarlarsınız. Bu işlem [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) bölümünde açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-107">You set up the resource and calendar related to a worker in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="dcbd9-108">Aşağıdaki ekran görüntüsünde, çalışma zamanı takvimi "Üretim" kullanan bir kaynakla ilişkili bir bakım görevlisi örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![Şekil 1](media/01-work-order-scheduling.png)

<span data-ttu-id="dcbd9-110">Araçlar ve varlıklar için takvim kurulumunun iş emri zamanlayla ilgili olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="dcbd9-111">Varsayım, araçların ve varlıkların bakım için günde 24 saat kullanılabilir durumda olduğudur.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>

