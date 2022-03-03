---
title: Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı
description: Bu konu, çevrimiçi siparişlerdeki vergilerin yanlış hesaplandığı veya satış satırındaki vergi grubunun doğru ayarlanmadığı durumlarda yardımcı olabilecek hata giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 02/16/2022
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
ms.openlocfilehash: 0e4361b436cc78eccaff29dfa2927d342e26072d
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312043"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı

[!include [banner](../../includes/banner.md)]

Bu konu, çevrimiçi siparişlerdeki vergilerin yanlış hesaplandığı veya satış satırındaki vergi grubunun doğru ayarlanmadığı durumlarda yardımcı olabilecek hata giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Bir e-ticaret siparişi verildiğinde vergiler yanlış hesaplanıyor veya satış satırındaki vergi grubu yanlış ayarlanıyor.

## <a name="resolution"></a>Çözüm

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Commerce Headquarters'da genel satış vergisi gruplarını yapılandırın

Commerce Headquarters'da genel satış vergisi grupları yapılandırmak için şu adımları izleyin.

1. **Vergi \> Dolaylı vergiler \> Satış vergisi \> Satış vergisi grubu**'na gidin.
1. Sol gezinti bölmesinde yapılandırılacak vergi grubunu seçin.
1. **Mağaza hedefi tabanlı vergi** hızlı sekmesinde, satış vergi grubuyla ilgili vergileri yapılandırın.

> [!NOTE]
> Müşteri adresi ile belirlenen satış vergisi içermeyen sevkiyat için vergi grubu, vergi grubu için yapılandırılan satırın teslimat adresi ve hedef tabanlı vergiler tarafından belirlenir. Daha fazla bilgi için, bkz [Hedefe bağlı olara çevrimiçi mağazalar için vergiler ayarlayın](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Commerce Headquarters'da bir perakende mağazası için satış vergisini yapılandırın

Commerce Headquarters'da bir perakende mağazası için satış vergisini yapılandırmak için şu adımları izleyin.

1. **Retail ve Commerce \> Kanallar \> Tüm mağazalar**'a gidin.
1. Satış vergisinin yapılandırılacağı mağazayı seçin.
1. **Genel** hızlı sekmesinde, **Satış vergisi** bölümünde, mağazanın satış vergisi bilgilerini yapılandırın.

> [!NOTE]
> Bir mağazadan ürün çekme işlemi için vergi grubu malzeme çekme için seçilen mağazadan gelir. Daha fazla bilgi için bkz. [Mağazalar için diğer vergi seçeneklerini ayarlama](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Commerce Headquarters'da bir müşterinin adresi için satış vergisini yapılandırın

Commerce Headquarters'da bir müşterinin adresi için satış vergisini yapılandırmak için şu adımları izleyin.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Satış vergisini yapılandıracağınız müşteriyi seçin.
1. **Adresler** hızlı sekmesinde, satış vergilerini yapılandıracağınız adresi seçin, **diğer seçenekleri** ve sonra **Gelişmiş**'i seçin.
1. **Genel** hızlı sekmesinde, **Vergi grubu**'nu seçin.
1. **Satış vergisi** alanında uygun değeri seçin.

> [!NOTE]
> Müşterinin adresinde satış vergisi içeren sevkiyat için satırın teslimat adresi satırın vergi grubunu belirler. Müşteri zaten yapılandırılmış bir vergi grubuna sahip mevcut bir adrese ürün gönderiyorsa mevcut vergi grubu kullanılır. Varsayılan olarak, adresler oluşturuldukları sırada bir vergi grubuna sahip değildir.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi siparişler için satış vergisini yapılandırma](../sales-tax-config.md)
