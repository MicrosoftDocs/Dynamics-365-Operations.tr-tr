---
title: İş akışı SSS
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/01/2019
ms.locfileid: "773237"
---
# <a name="workflow-system"></a><span data-ttu-id="abcae-103">İş akışı sistemi</span><span class="sxs-lookup"><span data-stu-id="abcae-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abcae-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.</span><span class="sxs-lookup"><span data-stu-id="abcae-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="abcae-105">Bildirimler</span><span class="sxs-lookup"><span data-stu-id="abcae-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="abcae-106">Bir iş öğesi reddedildiğinde neden birden fazla uyarı alınır?</span><span class="sxs-lookup"><span data-stu-id="abcae-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="abcae-107">Bir iş öğesi reddedildiğinde, bu iş maddesi reddedildi olarak tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="abcae-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="abcae-108">Başka bir iş öğesi oluşturulur ve başlatıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="abcae-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="abcae-109">Bu, reddedilen iş öğesi için başlatan bir uyarı olacağı ve ayrı bir uyarının, yeni "değişim talebi" iş öğesine atanan kullanıcıya gönderileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="abcae-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="abcae-110">Her bir uyarı farklı bir iş öğesi içindir, ancak benzerlik karışıklığa neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="abcae-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="abcae-111">Gelecekteki bir sürümde bunu iyileştirmenin yollarını arıyoruz.</span><span class="sxs-lookup"><span data-stu-id="abcae-111">We are looking at ways to improve this in a future release.</span></span>
