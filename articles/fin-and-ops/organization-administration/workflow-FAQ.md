---
title: İş akışı SSS
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509303"
---
# <a name="workflow-system"></a><span data-ttu-id="f8a7e-103">İş akışı sistemi</span><span class="sxs-lookup"><span data-stu-id="f8a7e-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8a7e-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="f8a7e-105">Bildirimler</span><span class="sxs-lookup"><span data-stu-id="f8a7e-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="f8a7e-106">Bir iş öğesi reddedildiğinde neden birden fazla uyarı alınır?</span><span class="sxs-lookup"><span data-stu-id="f8a7e-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="f8a7e-107">Bir iş öğesi reddedildiğinde, bu iş maddesi reddedildi olarak tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="f8a7e-108">Başka bir iş öğesi oluşturulur ve başlatıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="f8a7e-109">Bu, reddedilen iş öğesi için başlatan bir uyarı olacağı ve ayrı bir uyarının, yeni "değişim talebi" iş öğesine atanan kullanıcıya gönderileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="f8a7e-110">Her bir uyarı farklı bir iş öğesi içindir, ancak benzerlik karışıklığa neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="f8a7e-111">Gelecekteki bir sürümde bunu iyileştirmenin yollarını arıyoruz.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="f8a7e-112">İş akışı dışa aktarma işlemlerin neden başarısız oluyor?</span><span class="sxs-lookup"><span data-stu-id="f8a7e-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="f8a7e-113">İş akışı dışa aktarma özelliğinde, iş akışı adlarının 48 karakter sınırını aşmasını önleyen bir sınırlama vardır.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="f8a7e-114">48 karakterden daha uzun bir ad kullanmak, "Sunucu isteği doğrulayamadı" hatasına neden olabilir ve/veya dosya türü olmadan bir dosyanın dışa aktarılmasını önleyebilir.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="f8a7e-115">[İş Akışı Dışa Aktarma Sorunlarını Giderme](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) blog gönderisinde daha fazla ayrıntı verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f8a7e-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
