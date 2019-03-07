---
title: İstemci e-postayla uyarı bildirimleri
description: Bu konu, gönderdiğiniz e-posta bildirimleri önceden tanımlanmış oluşur kuralları ayarlamak hakkında bilgi sağlar.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2019
ms.locfileid: "373838"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="828e4-103">İstemci e-postayla uyarı bildirimleri</span><span class="sxs-lookup"><span data-stu-id="828e4-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="828e4-104">Microsoft Dynamics 365 for Finance and Operations içinde , filtre uygulanmış görünümler veri izleyen ve otomatik olarak önceden belirlenmiş olaylar oluştuğunda e-posta bildirimleri göndermek özel uyarı kuralları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="828e4-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="828e4-105">E-posta bildirimleri gönderme seçeneği desteklenen tüm uyarı türleri için kullanılabilir ve ayrıca varolan uyarı kurallar için açık olabilir.</span><span class="sxs-lookup"><span data-stu-id="828e4-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="828e4-106">Yerleşik denetimleri, filtre uygulanmış görünümleri sistem toplu işlerin izleyen uyarı kuralları oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="828e4-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="828e4-107">**Durum** alanının değerini izleyerek, toplu iş başarısız olursa e-posta gönderen uyarı kuralları da yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="828e4-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="828e4-108">Bu uyarı kurallarını oluşturduktan sonra iş verilerindeki değişiklikler için raporları denetlemenize gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="828e4-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="828e4-109">Bunun yerine, Finance and Operations akıllı değişiklik algılama hizmeti izlemeyi sizin yerinize yapar.</span><span class="sxs-lookup"><span data-stu-id="828e4-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="828e4-110">İstemci uyarıları, Microsoft Office tümleştirmesi aracılığıyla sağlanmış e-posta alt istemine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="828e4-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="828e4-111">Simple Mail Transfer Protocol (SMTP) sağlayıcısını kullanmanızı öneririz, böylece e-posta dağıtımının yerel posta istemcisine dayanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="828e4-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="828e4-112">Bildirimleri e-posta ile göndermek için müşterilerin tümleşik e-posta hizmetlerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="828e4-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="828e4-113">Uyarı sahibi adına e-posta bildirimlerini alıcılara gönderilir.</span><span class="sxs-lookup"><span data-stu-id="828e4-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="828e4-114">Finance and Operations içinde e-postayı yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırmak ve göndermek](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="828e4-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="828e4-115">Aşağıdaki görüntü **Uyarı kuralı oluştur** iletişim kutusunu gösterir, bu da şimdi bir **E-posta gönder** seçeneği içerir.</span><span class="sxs-lookup"><span data-stu-id="828e4-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="828e4-116">[![Kural oluştur iletişim kutusu, E-posta gönder seçeneği Evet olarak ayarlanmış](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="828e4-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="828e4-117">**E-posta gönder** seçeneği **Evet** olarak ayarlanmışsa, bildirimler Eylem Merkezinden teslim edilmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="828e4-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="828e4-118">Uyarı bildirimi e-posta şablonları</span><span class="sxs-lookup"><span data-stu-id="828e4-118">Alert notification email templates</span></span>

<span data-ttu-id="828e4-119">Servis, uyarı bildiriminin temel ayrıntılarını gönderen e-posta bildirimlerini önceden tanımlanmış e-posta şablonlarını kullanarak gönderir.</span><span class="sxs-lookup"><span data-stu-id="828e4-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span> <span data-ttu-id="828e4-120">Bu ayrıntılar, uyarı kuralının tanımlandığı sayfaya bir doğrudan bağlantı içerir.</span><span class="sxs-lookup"><span data-stu-id="828e4-120">These details include a direct link to the page where the alert rule was defined.</span></span>

<span data-ttu-id="828e4-121">Aşağıdaki görüntü, bir e-posta tarafından alındıklarında uyarı bildirimlerinin yapısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="828e4-121">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="828e4-122">[![Kayıt oluşturma, alan değişiklikleri, şablon silinmesi için şablon temelli uyarı bildirimleri](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="828e4-122">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
