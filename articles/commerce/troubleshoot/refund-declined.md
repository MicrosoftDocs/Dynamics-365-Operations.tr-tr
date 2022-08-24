---
title: İade siparişinde para iadesi reddedildi
description: Bu makale, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268245"
---
# <a name="refund-on-a-return-order-is-declined"></a>İade siparişinde para iadesi reddedildi

[!include [banner](../../includes/banner.md)]

Bu makale, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.

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
