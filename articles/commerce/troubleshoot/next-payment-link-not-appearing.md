---
title: Sonraki ödemelerim için kaydet seçeneği görünmüyor
description: Bu konu, bir e-ticaret sitesinin ödeme sayfasında ödeme yöntemi altında sonraki ödemelerim için kaydet onay kutusu görüntülenmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4887cde3e4243ae7a4da6402782e69e780ae20331ed80df63ba1239ef5187e41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769283"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>"Sonraki ödemelerim için kaydet" seçeneği görünmüyor

[!include [banner](../../includes/banner.md)]

Bu konu, bir e-ticaret sitesinin ödeme sayfasında **ödeme yöntemi** altında **sonraki ödemelerim için kaydet** onay kutusu görüntülenmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

**Sonraki ödemelerim için Kaydet** onay kutusu bir e-ticaret sitesinin ödeme sayfasındaki **ödeme yöntemi** bölümünde görünmüyor.

Aşağıdaki resimde **sonraki ödemelerim için kaydet** onay kutusunun yer aldığı bir ödeme sayfası örneği gösterilmektedir.

![Ödeme modülündeki sonraki ödemelerim için kaydet onay kutusu.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Çözüm

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Commerce Headquarters'da Adyen için Dynamics 365 Paymet Connector'ın doğru yapılandırıldığını doğrulayın

Commerce Headquarters'da Adyen için Dynamics 365 Paymet Connector'ın doğru yapılandırıldığını doğrulamak için şu adımları izleyin.

1. **Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.
1. Çevrimiçi mağazayı seçin.
1. **Ödeme Hesapları** hızlı sekmesinde, **e-ticarette ödeme bilgilerinin kaydedilmesine izin ver** alanındaki değerin **Doğru** olarak ayarlandığından emin olun.

![Commerce Headquarters'da e-ticaret alanında ödeme bilgilerinin kaydedilmesine izin verme.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Ek kaynaklar

[Ödeme modülü](../payment-module.md)

[Adyen bağlayıcısı ile çevrimiçi ödeme araçlarını kaydetme](../dev-itpro/adyen-connector-listPI.md)
