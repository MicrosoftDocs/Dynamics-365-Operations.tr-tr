---
title: Sepet simgesi modülü
description: Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e0238e9d464fc1d44cbc5091638ac7270d5b6ae3
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479316"
---
# <a name="cart-icon-module"></a>Sepet simgesi modülü

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.

Sepet simgesi modülü, sayfanın başlık modülündeki sepeti temsil eder ve sepetteki öğe sayısını gösterir. Sepet simgesi modülü, sepet simgesi üzerine gelindiğinde sepet özetini de (mini sepet olarak da bilinir) görüntüler. Mini sepet, sepet sayfasına gitmek zorunda kalmadan sepetteki öğelerin özetini kullanıcıya sağlar. Ayrıca, kullanıcının özetten memnun olması durumunda doğrudan ödeme sayfasına gitmesine olanak tanır. Bu, sayfa gezinti sayısını azaltır ve ödemenin daha hızlı yapılmasını sağlar. 

Aşağıdaki resimde, Fabrikam üstbilgisinde mini sepet görüntüleyen bir alışveriş sepeti simge modülü örneği gösterilmektedir.

![Sepet simgesi modülü örneği.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modül özellikleri

- **Mini sepeti göster** – Doğru olduğunda, bu özellik sepet simgesi üzerine gelindiğinde sepet özetinin (mini sepet) görüntülenmesini sağlar. Bu işlev yalnızca masaüstü görünüm bağlantı noktaları için desteklenir.

## <a name="module-properties-in-the-adventure-works-theme"></a>Adventure Works temasında modül özellikleri

Adventure Works temalarında, sepet simge modülü mini sepet için iki ek yuva içerir. Bu yuvalar, modül tanımı uzantısı olarak bulunur.

- **Boş sepet yükseltmeleri** – Bu yuva bir içerik bloğu modülü alır. Sepet boş olduğunda, belirtilen içerik bloğu modülü gösterilir. İçerik bloğu modülü, müşterilerin alışveriş amaçlı yolculuğuyla devam etmesine yardımcı olmak için promosyonlar, pazarlama içeriği ve kategori sayfalarına bağlantılar için kullanılabilir.
- **Promosyon içeriği** – Bu yuva, "$100 üzerinden siparişlere ücretsiz sevkiyat" gibi promosyonları sergileyebilecek şekilde kullanılabilir. Tanıtım içeriği yuvasında içerik bloğu, metin bloğu ve görüntü listesi modülleri kullanılabilir.

Aşağıdaki resimde, Mini sepette tanıtım içeriği görüntüleyen Adventure Works temasıyla ilgili alışveriş simgesi modülünün bir örneği gösterilmektedir.

![Adventure Works temasıyla ilgili alışveriş simgesi modülü örneği](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works teması yuvaları Dynamics 365 Commerce Sürüm 10.0.20 itibarıyla kullanılabilir.

## <a name="add-a-cart-icon-module-to-a-page"></a>Sayfaya sepet simgesi modülü ekleme

Bir sepet simgesi modülü eklemek için, bkz. [Başlık modülü](author-header-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
