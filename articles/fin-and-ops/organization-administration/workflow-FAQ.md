---
title: İş akışı SSS
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
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
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2019
ms.locfileid: "1689012"
---
# <a name="workflow-faq"></a><span data-ttu-id="9801c-103">İş akışıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="9801c-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9801c-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.</span><span class="sxs-lookup"><span data-stu-id="9801c-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="9801c-105">Bir iş öğesi reddedildiğinde neden birden fazla uyarı alınır?</span><span class="sxs-lookup"><span data-stu-id="9801c-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="9801c-106">Bir iş öğesi reddedildiğinde, bu iş maddesi reddedildi olarak tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="9801c-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="9801c-107">Başka bir iş öğesi oluşturulur ve başlatıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="9801c-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="9801c-108">Bu, reddedilen iş öğesi için başlatan bir uyarı olacağı ve ayrı bir uyarının, yeni "değişim talebi" iş öğesine atanan kullanıcıya gönderileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9801c-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="9801c-109">Her bir uyarı farklı bir iş öğesi içindir, ancak benzerlik karışıklığa neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="9801c-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="9801c-110">Gelecekteki bir sürümde bunu iyileştirmenin yollarını arıyoruz.</span><span class="sxs-lookup"><span data-stu-id="9801c-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="9801c-111">İş akışı dışa aktarma işlemlerin neden başarısız oluyor?</span><span class="sxs-lookup"><span data-stu-id="9801c-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="9801c-112">İş akışı dışa aktarma özelliğinde, iş akışı adlarının 48 karakter sınırını aşmasını önleyen bir sınırlama vardır.</span><span class="sxs-lookup"><span data-stu-id="9801c-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="9801c-113">48 karakterden daha uzun bir ad kullanmak, "Sunucu isteği doğrulayamadı" hatasına neden olabilir ve/veya dosya türü olmadan bir dosyanın dışa aktarılmasını önleyebilir.</span><span class="sxs-lookup"><span data-stu-id="9801c-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="9801c-114">[İş Akışı Dışa Aktarma Sorunlarını Giderme](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) blog gönderisinde daha fazla ayrıntı verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9801c-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="9801c-115">Bir iş akışının sağlayıcısı da iş akışını onaylayabilir mi?</span><span class="sxs-lookup"><span data-stu-id="9801c-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="9801c-116">Evet, iş akışı bu şekilde yapılandırılırsa iş akışını da onaylayabilir.</span><span class="sxs-lookup"><span data-stu-id="9801c-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="9801c-117">Bu davranışı engellemek için **İş akışı parametreleri > Genel > Onaylayan > Gönderen onayına izin verme**'yi **Evet** olarak ayarlayın–.</span><span class="sxs-lookup"><span data-stu-id="9801c-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="9801c-118">Kullanıcılara bildirim sağlamak için iş akışlarına uyarı ekleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="9801c-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="9801c-119">Bildirim sağlamak amacıyla iş akışlarına uyarı ekleme hakkında dikkat edilecek bir kaç kilit alan şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9801c-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="9801c-120">Uyarılar ve iş akışı bildirim mekanizmaları</span><span class="sxs-lookup"><span data-stu-id="9801c-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="9801c-121">Kayıt değişiklikleri için uyarılar ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9801c-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="9801c-122">İş akışları kayıtları değiştirir, bu nedenle bir iş akışının neden olduğu bir kayıt değişikliğiyle ilgili bir uyarı ayarlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="9801c-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="9801c-123">Ancak, iş akışlarının farklı yerleşik bildirim seçenekleri olduğundan, uyarılar kullanılması ideal değildir.</span><span class="sxs-lookup"><span data-stu-id="9801c-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="9801c-124">İş akışlarından ilişkin standart bildirimler</span><span class="sxs-lookup"><span data-stu-id="9801c-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="9801c-125">İş akışları yerleşik e-posta bildirimlerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="9801c-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="9801c-126">Bir müşteri e-posta göndermek için bildirimleri yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="9801c-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="9801c-127">Bu bildirimler, kullanıcılar için Eylem Merkezi iletilerine neden olmaz.</span><span class="sxs-lookup"><span data-stu-id="9801c-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="9801c-128">Gelecekteki bir güncelleştirmede, kullanıcıya bir iş akışı iş maddesi atanacak bir İşlem Merkezi iletisi ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="9801c-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="9801c-129">İş akışına bildirim ekleme</span><span class="sxs-lookup"><span data-stu-id="9801c-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="9801c-130">X++içindeki bir iş akışından oluşturulan ileti gibi belirli kullanıcılar için işlem merkezi iletileri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="9801c-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="9801c-131">[İş Akışının İş Olayları](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) Müşterinin Akışları tetiklemek için kullanabileceği, aradıkları bildirimlere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="9801c-131">[Workflows have Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="9801c-132">Özetle, bir Kullanıcı bir iş akışı iş maddesi atandığında eylem merkezinden uygun bildirimi alamazsanız ek veya farklı bildirimler sağlamak için [İş Akışının İş Olayları](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) ile Microsoft Flow'u ek ya da farklı bildirimler sağlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="9801c-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
