---
title: E-postayla istemci uyarı bildirimleri
description: Bu makalede, önceden tanımlı olaylar gerçekleştiğinde e-posta bildirimleri gönderen kuralların nasıl oluşturulacağı hakkında bilgi verilmektedir.
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
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878292"
---
# <a name="client-alert-notifications-by-email"></a>E-postayla istemci uyarı bildirimleri

[!include [banner](../includes/banner.md)]

Verilerin filtre uygulanmış görünümlerini izleyen ve otomatik olarak önceden belirlenmiş olaylar oluştuğunda e-posta bildirimleri gönderen özel uyarı kuralları tanımlayabilirsiniz. E-posta bildirimleri gönderme seçeneği desteklenen tüm uyarı türleri için kullanılabilir ve bunları mevcut uyarı kuralları için de açabilirsiniz.

Yerleşik denetimleri, filtre uygulanmış görünümleri sistem toplu işlerin izleyen uyarı kuralları oluşturmak için kullanabilirsiniz. **Durum** alanının değerini izleyerek, toplu iş başarısız olursa e-posta gönderen uyarı kuralları da yapılandırabilirsiniz. Bu uyarı kurallarını oluşturduktan sonra iş verilerindeki değişiklikler için raporları denetlemenize gerek kalmaz. Bunun yerine, akıllı değişiklik algılama hizmeti izlemeyi sizin yerinize yapar.

İstemci uyarıları, Microsoft Office tümleştirmesi aracılığıyla sağlanmış e-posta alt istemine bağlıdır. Simple Mail Transfer Protocol (SMTP) sağlayıcısını kullanmanızı öneririz, böylece e-posta dağıtımının yerel posta istemcisine dayanması gerekmez.

Bildirimleri e-posta ile göndermek için müşterilerin tümleşik e-posta hizmetlerini yapılandırmanız gerekir. Uyarı sahibi adına e-posta bildirimlerini alıcılara gönderilir.

E-postayı yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../organization-administration/configure-email.md).

Aşağıdaki görüntü **Uyarı kuralı oluştur** iletişim kutusunu gösterir, bu da şimdi bir **E-posta gönder** seçeneği içerir.

[![Kural oluştur iletişim kutusu, E-posta gönder seçeneği Evet olarak ayarlanmış.](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> **E-posta gönder** seçeneği **Evet** olarak ayarlanmışsa, bildirimler Eylem Merkezinden teslim edilmeye devam eder.

## <a name="alert-notification-email-templates"></a>Uyarı bildirimi e-posta şablonları

Servis, uyarı bildiriminin temel ayrıntılarını gönderen e-posta bildirimlerini önceden tanımlanmış e-posta şablonlarını kullanarak gönderir.

Aşağıdaki görüntüde, e-postayla alınan uyarı bildirimlerinin yapısı gösterilmektedir.

[![Kayıt oluşturma, alan değişiklikleri, şablon silinmesi için şablon temelli uyarı bildirimleri.](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]