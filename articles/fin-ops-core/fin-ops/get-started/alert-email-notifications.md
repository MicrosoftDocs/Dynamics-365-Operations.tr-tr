---
title: İstemci e-postayla uyarı bildirimleri
description: Bu konu, gönderdiğiniz e-posta bildirimleri önceden tanımlanmış oluşur kuralları ayarlamak hakkında bilgi sağlar.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: d132ed979a84c2906298c05708cef1ee87f47078
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752926"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="51464-103">E-postayla istemci uyarı bildirimleri</span><span class="sxs-lookup"><span data-stu-id="51464-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51464-104">Verilerin filtre uygulanmış görünümlerini izleyen ve otomatik olarak önceden belirlenmiş olaylar oluştuğunda e-posta bildirimleri gönderen özel uyarı kuralları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51464-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="51464-105">E-posta bildirimleri gönderme seçeneği desteklenen tüm uyarı türleri için kullanılabilir ve bunları mevcut uyarı kuralları için de açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51464-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="51464-106">Yerleşik denetimleri, filtre uygulanmış görünümleri sistem toplu işlerin izleyen uyarı kuralları oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51464-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="51464-107">**Durum** alanının değerini izleyerek, toplu iş başarısız olursa e-posta gönderen uyarı kuralları da yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51464-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="51464-108">Bu uyarı kurallarını oluşturduktan sonra iş verilerindeki değişiklikler için raporları denetlemenize gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="51464-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="51464-109">Bunun yerine, akıllı değişiklik algılama hizmeti izlemeyi sizin yerinize yapar.</span><span class="sxs-lookup"><span data-stu-id="51464-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="51464-110">İstemci uyarıları, Microsoft Office tümleştirmesi aracılığıyla sağlanmış e-posta alt istemine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51464-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="51464-111">Simple Mail Transfer Protocol (SMTP) sağlayıcısını kullanmanızı öneririz, böylece e-posta dağıtımının yerel posta istemcisine dayanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="51464-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="51464-112">Bildirimleri e-posta ile göndermek için müşterilerin tümleşik e-posta hizmetlerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="51464-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="51464-113">Uyarı sahibi adına e-posta bildirimlerini alıcılara gönderilir.</span><span class="sxs-lookup"><span data-stu-id="51464-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="51464-114">E-postayı yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="51464-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="51464-115">Aşağıdaki görüntü **Uyarı kuralı oluştur** iletişim kutusunu gösterir, bu da şimdi bir **E-posta gönder** seçeneği içerir.</span><span class="sxs-lookup"><span data-stu-id="51464-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="51464-116">[![Kural oluştur iletişim kutusu, E-posta gönder seçeneği Evet olarak ayarlanmış](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="51464-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="51464-117">**E-posta gönder** seçeneği **Evet** olarak ayarlanmışsa, bildirimler Eylem Merkezinden teslim edilmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="51464-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="51464-118">Uyarı bildirimi e-posta şablonları</span><span class="sxs-lookup"><span data-stu-id="51464-118">Alert notification email templates</span></span>

<span data-ttu-id="51464-119">Servis, uyarı bildiriminin temel ayrıntılarını gönderen e-posta bildirimlerini önceden tanımlanmış e-posta şablonlarını kullanarak gönderir.</span><span class="sxs-lookup"><span data-stu-id="51464-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="51464-120">Aşağıdaki görüntüde, e-postayla alınan uyarı bildirimlerinin yapısı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="51464-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="51464-121">[![Kayıt oluşturma, alan değişiklikleri, şablon silinmesi için şablon temelli uyarı bildirimleri](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="51464-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]