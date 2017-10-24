--- 
title: "Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme"
description: "İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1ff7de584631563939104c87b00fdc26bdb1a3cb
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="92c7d-103">Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="92c7d-103">Enable users to receive workflow-related email messages</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92c7d-104">İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92c7d-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="92c7d-105">Örneğin, belgeler onay için kendilerine atandığında kullanıcılara e-posta iletileri gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="92c7d-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="92c7d-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="92c7d-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="92c7d-107">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="92c7d-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="92c7d-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="92c7d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="92c7d-109">Kullanıcı seçenekleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="92c7d-109">Click User options.</span></span>
4. <span data-ttu-id="92c7d-110">İş Akışı sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="92c7d-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="92c7d-111">Bildirimler bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="92c7d-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="92c7d-112">Bildirimler bölümünde, kullanıcının iş akışı ile ilgili olaylar hakkında nasıl bilgilendirilmesini istediğinizi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92c7d-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="92c7d-113">Satır maddesi iş akışı bildirim türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="92c7d-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="92c7d-114">Gruplandırıldı: Satır maddeleri için bildirimler tek bir e-posta iletisine gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="92c7d-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="92c7d-115">Tek tek: Her satır maddesi için bir e-posta iletisi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="92c7d-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="92c7d-116">Kullanıcının, istemcide bildirimler almasını istiyorsanız E-postada bildirimler gönder onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="92c7d-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="92c7d-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="92c7d-117">Click Save.</span></span>
7. <span data-ttu-id="92c7d-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="92c7d-118">Close the page.</span></span>


