---
title: İade siparişinde para iadesi reddedildi
description: Bu konu, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 8880d72d702758d611755bce48a331e3f2e28ca1b7abf485e8b4f7301317c875
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738636"
---
# <a name="refund-on-a-return-order-is-declined"></a>İade siparişinde para iadesi reddedildi

[!include [banner](../../includes/banner.md)]

Bu konu, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

İade siparişini faturalamak için kullanılan kredi kartı, orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğunda para iadesi reddediliyor. Şu hata iletisini alırsınız: "Bazı Ödemeler deftere nakil için doğru durumda değil. Lütfen faturalamadan önce tüm ödemelerin durumunu yeniden doğrulayın."

Ödeme onayı ayrıntıları aşağıdaki hata iletisini içerecektir: "adyen Gateway SendRequest (), 'InternalServerError'.22144 durumuyla başarısız oldu; Adyen'den boş yanıt döndürüldü.(22001);"

![İade siparişinde reddedilen para iadesi hatası.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Çözüm

### <a name="enable-blind-returns-in-adyen"></a>Adyen'de görünmeyen iadeleri etkinleştirme

Görünmeyen iadeleri etkinleştirmek için, Adyen destek ekibiyle iletişim kurmak ve Adyen satıcı hesabınızda görünmeyen iadelerin etkinleştirilmesini istemek için [Adyen için Dynamics 365 Payment Connector sorunlarını giderme](adyen-support.md) adımlarını izleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Adyen için Dynamics 365 Ödeme Bağlayıcısı](../dev-itpro/adyen-connector.md)

[Dynamics 365 için Adyen Payment Connector sorunlarını giderme](https://docs.adyen.com/plugins/microsoft-dynamics)
