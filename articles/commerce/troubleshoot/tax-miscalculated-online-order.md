---
title: Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı
description: Bu konu, çevrimiçi siparişlerdeki vergilerin yanlış hesaplandığı veya satış satırındaki vergi grubunun doğru ayarlanmadığı durumlarda yardımcı olabilecek hata giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585569"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı

[!include [banner](../../includes/banner.md)]

Bu konu, çevrimiçi siparişlerdeki vergilerin yanlış hesaplandığı veya satış satırındaki vergi grubunun doğru ayarlanmadığı durumlarda yardımcı olabilecek hata giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Bir e-ticaret siparişi verildiğinde vergiler yanlış hesaplanıyor veya satış satırındaki vergi grubu yanlış ayarlanıyor.

## <a name="resolution"></a>Çözünürlük

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Commerce Headquarters'da bir perakende mağazası için satış vergisini yapılandırın

Commerce Headquarters'da bir perakende mağazası için satış vergisini yapılandırmak için şu adımları izleyin.

1. **Retail ve Commerce \> Kanallar \> Tüm mağazalar**'a gidin.
1. Satış vergisinin yapılandırılacağı mağazayı seçin.
1. **Genel** hızlı sekmesinde, **Satış vergisi** bölümünde, mağazanın satış vergisi bilgilerini yapılandırın.

> [!NOTE]
> Bir mağazadan ürün çekme işlemi için vergi grubu malzeme çekme için seçilen mağazadan gelir. Daha fazla bilgi için bkz. [Mağazalar için diğer vergi seçeneklerini ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Commerce Headquarters'da bir müşterinin adresi için satış vergisini yapılandırın

Commerce Headquarters'da bir müşterinin adresi için satış vergisini yapılandırmak için şu adımları izleyin.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Satış vergisini yapılandıracağınız müşteriyi seçin.
1. **Adresler** hızlı sekmesinde, satış vergilerini yapılandıracağınız adresi seçin, **diğer seçenekleri** ve sonra **Gelişmiş**'i seçin.
1. **Genel** hızlı sekmesinde, **Vergi grubu**'nu seçin.
1. **Satış vergisi** alanında uygun değeri seçin.

> [!NOTE]
> Müşterinin adresinde satış vergisi içeren sevkiyat için satırın teslimat adresi satırın vergi grubunu belirler. Müşteri zaten yapılandırılmış bir vergi grubuna sahip mevcut bir adrese ürün gönderiyorsa mevcut vergi grubu kullanılır. Varsayılan olarak, adresler oluşturuldukları sırada bir vergi grubuna sahip değildir.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Commerce Headquarters'da genel satış vergisi gruplarını yapılandırın

Commerce Headquarters'da genel satış vergisi grupları yapılandırmak için şu adımları izleyin.

1. **Vergi \> Dolaylı vergiler \> Satış vergisi \> Satış vergisi grubu**'na gidin.
1. Sol gezinti bölmesinde yapılandırılacak vergi grubunu seçin.
1. **Mağaza hedefi tabanlı vergi** hızlı sekmesinde, satış vergi grubuyla ilgili vergileri yapılandırın.

> [!NOTE]
> Müşteri adresinde satış vergisi içermeyen sevkiyat için vergi grubu, vergi grubu için yapılandırılan satırın teslimat adresi ve hedef tabanlı vergiler tarafından belirlenir. Daha fazla bilgi için, bkz [Hedefe bağlı olara çevrimiçi mağazalar için vergiler ayarlayın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi siparişler için satış vergisini yapılandırma](../sales-tax-config.md)
