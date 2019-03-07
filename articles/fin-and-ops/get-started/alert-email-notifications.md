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
# <a name="client-alert-notifications-by-email"></a>İstemci e-postayla uyarı bildirimleri

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operations içinde , filtre uygulanmış görünümler veri izleyen ve otomatik olarak önceden belirlenmiş olaylar oluştuğunda e-posta bildirimleri göndermek özel uyarı kuralları tanımlayabilirsiniz. E-posta bildirimleri gönderme seçeneği desteklenen tüm uyarı türleri için kullanılabilir ve ayrıca varolan uyarı kurallar için açık olabilir.

Yerleşik denetimleri, filtre uygulanmış görünümleri sistem toplu işlerin izleyen uyarı kuralları oluşturmak için kullanabilirsiniz. **Durum** alanının değerini izleyerek, toplu iş başarısız olursa e-posta gönderen uyarı kuralları da yapılandırabilirsiniz. Bu uyarı kurallarını oluşturduktan sonra iş verilerindeki değişiklikler için raporları denetlemenize gerek kalmaz. Bunun yerine, Finance and Operations akıllı değişiklik algılama hizmeti izlemeyi sizin yerinize yapar.

İstemci uyarıları, Microsoft Office tümleştirmesi aracılığıyla sağlanmış e-posta alt istemine bağlıdır. Simple Mail Transfer Protocol (SMTP) sağlayıcısını kullanmanızı öneririz, böylece e-posta dağıtımının yerel posta istemcisine dayanması gerekmez.

Bildirimleri e-posta ile göndermek için müşterilerin tümleşik e-posta hizmetlerini yapılandırmanız gerekir. Uyarı sahibi adına e-posta bildirimlerini alıcılara gönderilir.

Finance and Operations içinde e-postayı yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırmak ve göndermek](../organization-administration/configure-email.md).

Aşağıdaki görüntü **Uyarı kuralı oluştur** iletişim kutusunu gösterir, bu da şimdi bir **E-posta gönder** seçeneği içerir.

[![Kural oluştur iletişim kutusu, E-posta gönder seçeneği Evet olarak ayarlanmış](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> **E-posta gönder** seçeneği **Evet** olarak ayarlanmışsa, bildirimler Eylem Merkezinden teslim edilmeye devam eder.

## <a name="alert-notification-email-templates"></a>Uyarı bildirimi e-posta şablonları

Servis, uyarı bildiriminin temel ayrıntılarını gönderen e-posta bildirimlerini önceden tanımlanmış e-posta şablonlarını kullanarak gönderir. Bu ayrıntılar, uyarı kuralının tanımlandığı sayfaya bir doğrudan bağlantı içerir.

Aşağıdaki görüntü, bir e-posta tarafından alındıklarında uyarı bildirimlerinin yapısını gösterir.

[![Kayıt oluşturma, alan değişiklikleri, şablon silinmesi için şablon temelli uyarı bildirimleri](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
