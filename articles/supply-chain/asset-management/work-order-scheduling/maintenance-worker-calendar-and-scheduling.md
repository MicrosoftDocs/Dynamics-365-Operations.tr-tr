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
ms.openlocfilehash: aa2d50a976af7ee7dde5335f94336b995fdc2d11
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652069"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="a547e-103">Bakım görevlisi takvimi ve zamanlama</span><span class="sxs-lookup"><span data-stu-id="a547e-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a547e-104">İş emirlerini zamanlarken bakım görevlileri, araçlar ve varlıklar için bir zamanlama oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="a547e-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="a547e-105">Bakım görevlilerini zamanlamak için, her bakım görevlisi için bir takvim ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a547e-105">In order to schedule maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="a547e-106">Bakım görevlileri kaynakla ilgilidir ve çalışma zamanı takvimleri kaynaklar için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a547e-106">Maintenance workers are related to a resource, and working time calendars are set up for resources.</span></span> <span data-ttu-id="a547e-107">Kaynak ve takvimi **Varlık yönetimi** > **Kurulum** > **Çalışanlar** > **Çalışanlar** altından ayarlarsınız. Bu işlem [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) bölümünde açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a547e-107">You set up the resource and calendar in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="a547e-108">Aşağıdaki ekran görüntüsünde, çalışma zamanı takvimi "Üretim" kullanan bir kaynakla ilişkili bir bakım görevlisi örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a547e-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![Şekil 1](media/01-work-order-scheduling.png)

<span data-ttu-id="a547e-110">Araçlar ve varlıklar için takvim kurulumunun iş emri zamanlayla ilgili olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="a547e-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="a547e-111">Varsayım, araçların ve varlıkların bakım için günde 24 saat kullanılabilir durumda olduğudur.</span><span class="sxs-lookup"><span data-stu-id="a547e-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>

