---
title: Yeni müşteriler oluşturulduğunda karşılama e-postası gönderilmiyor
description: Bu makale, Microsoft Dynamics 365 Commerce'te yeni bir müşteri oluşturulurken hoş geldiniz e-posta bildirimi gönderilmiyorsa size yardımcı olacak sorun giderme kılavuzu sağlar.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219417"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Yeni müşteriler oluşturulduğunda karşılama e-postası gönderilmiyor

[!include [banner](../../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'te yeni bir müşteri oluşturulurken hoş geldiniz e-posta bildirimi gönderilmiyorsa size yardımcı olacak sorun giderme kılavuzu sağlar.

## <a name="description"></a>Açıklama

Commerce genel merkezinde yeni bir müşteri oluşturulduğunda, **Müşteri tarafından oluşturulan** e-posta bildirim türü için konfigüre edilmiş olsa bile müşteriye hoş geldiniz e-postası gönderilmez.

## <a name="resolution"></a>Çözüm

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>E-posta bildirim profilini Commerce parametreleri altında ilişkilendirme

1. Commerce Headquarters'da **Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> Commerce parametreleri \> Genel**'e gidin.
2. **E-posta bildirimi profili** açılan listesinde, müşteri tarafından oluşturulan bildirim türü ile müşteri tarafından oluşturulan e-posta şablonu arasında bir eşleme içeren e-posta bildirim profilini seçin.  

> [!NOTE] 
> Müşteri tarafından oluşturulan bildirimleri etkinleştirdiğinizde, tüzel kişilik içindeki tüm kanallarda oluşturulan müşteriler müşteri tarafından oluşturulan bir e-posta alır. Şu anda, müşteri tarafından oluşturulan bildirimler tek bir kanalla sınırlanamamaktadır.

Daha fazla bilgi için bkz. [İşlem tabanlı olaylar için e-posta şablonları oluşturma](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Ek kaynaklar

[E-posta bildirimi profili ayarlama](../email-notification-profiles.md)
