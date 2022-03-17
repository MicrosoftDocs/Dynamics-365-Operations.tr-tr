---
title: Yeni müşteriler oluşturulduğunda karşılama e-postası gönderilmiyor
description: Bu konu, Microsoft Dynamics 365 Commerce'te yeni bir müşteri oluşturulurken hoş geldiniz e-posta bildirimi gönderilmiyorsa size yardımcı olacak sorun giderme kılavuzu sağlar.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349968"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Yeni müşteriler oluşturulduğunda karşılama e-postası gönderilmiyor

[!include [banner](../../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'te yeni bir müşteri oluşturulurken hoş geldiniz e-posta bildirimi gönderilmiyorsa size yardımcı olacak sorun giderme kılavuzu sağlar.

## <a name="description"></a>Açıklama

Commerce genel merkezinde yeni bir müşteri oluşturulduğunda, **Müşteri tarafından oluşturulan** e-posta bildirim türü için konfigüre edilmiş olsa bile müşteriye hoş geldiniz e-postası gönderilmez.

## <a name="resolution"></a>Çözüm

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Müşteri tarafından oluşturulan e-posta bildirim türü için doğru e-posta kimlik değerini ayarlama

Genel merkezde **Müşterinin oluşturulduğu** e-posta bildirim türü için doğru **e-posta kodu** değerini ayarlamak üzere, aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Genel merkez ayarı \> Commerce e-posta bildirim profili**'ne gidin.
1. Soldaki gezinti bölmesinde e-posta bildirim profilini seçin.
1. **Perakende olay bildirimleri ayarları** altında, **Müşteri tarafından oluşturulan** e-posta bildirimi türü için **E-posta kimliği** alanını **NewCust** olarak ayarlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[E-posta bildirimi profili ayarlama](../email-notification-profiles.md)
