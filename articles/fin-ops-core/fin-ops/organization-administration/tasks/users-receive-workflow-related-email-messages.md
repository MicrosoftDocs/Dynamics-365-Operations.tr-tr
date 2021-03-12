---
title: Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme
description: İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 221e38cbe31e2ad24a56cb2e71206a1ebcdd619e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4799016"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="7c826-103">Kullanıcıların iş akışı ile ilgili e-posta iletileri almasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7c826-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c826-104">İş akışı ile ilgili olaylar gerçekleştiğinde, sistem kullanıcılara e-posta iletileri gönderecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c826-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="7c826-105">Örneğin, belgeler onay için kendilerine atandığında kullanıcılara e-posta iletileri gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="7c826-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="7c826-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="7c826-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7c826-107">**Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="7c826-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="7c826-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7c826-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7c826-109">**Eylem bölmesi**'nde, **Kullanıcı seçenekleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c826-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="7c826-110">**İş akışı** sekmesine tıklayın. **Bildirimler** bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7c826-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="7c826-111">**Bildirimler** bölümünde, kullanıcının iş akışı ile ilgili olaylar hakkında nasıl bilgilendirilmesini istediğinizi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c826-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="7c826-112">**Satır maddesi iş akışı bildirim türü** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7c826-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="7c826-113">Gruplandırıldı: Satır maddeleri için bildirimler tek bir e-posta iletisine gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="7c826-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="7c826-114">Tek tek: Her satır maddesi için bir e-posta iletisi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="7c826-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="7c826-115">Kullanıcının, istemcide bildirimler almasını istiyorsanız **E-postada bildirimler gönder** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7c826-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="7c826-116">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c826-116">Click **Save**.</span></span>
7. <span data-ttu-id="7c826-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7c826-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="7c826-118">İş akışı e-posta şablonları, iş akışının sistem düzeyi (şirkete özel değil) veya organizasyon düzeyi (Şirket özel) iş akışı olmasına bağlı olarak, sistem e-posta şablonlarından veya kuruluş e-posta şablonlarından kaynakdan alınır.</span><span class="sxs-lookup"><span data-stu-id="7c826-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>
