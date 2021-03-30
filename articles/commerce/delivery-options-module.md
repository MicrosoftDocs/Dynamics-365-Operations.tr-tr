---
title: Teslimat seçenekleri modülü
description: Bu konu teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d0e5fa731d4b808cda9863074d17d1917410f399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213686"
---
# <a name="delivery-options-module"></a>Teslimat seçenekleri modülü

[!include [banner](includes/banner.md)]

Bu konu teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.

Teslimat seçenekleri modülleri, müşterilerin çevrimiçi siparişleri için sevkiyat veya çekme gibi bir teslimat şekli seçmesine olanak tanır. Teslimat şeklini belirlemek için bir sevkiyat adresi gereklidir. Sevkiyat adresi değiştirilirse, teslimat seçenekleri tekrar alınmalıdır. Siparişte yalnızca mağazadan teslim alınacak maddeler varsa, bu modül otomatik olarak gizlenir.

Teslimat şekillerinin nasıl yapılandırılacağı hakkında bilgi için bkz. [Çevrimiçi kanal kurulumu](channel-setup-online.md) ve [Teslimat şekillerini ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Her teslimat şeklinin ilişkilendirilmiş masrafı olabilir. Çevrimiçi mağaza için masrafları yapılandırma hakkında bilgi için bkz. [Çok yönlü kanal Gelişmiş otomatik masraflar](omni-auto-charges.md).

Commerce sürümü 10.0.13'te, teslimat seçenekleri modülü **Eşit dağıtım olmadan başlık masrafları** ve **Satır masrafı olarak sevkiyat** özelliklerini destekleyecek şekilde güncelleştirilmiştir. Eşit dağıtma kapalıysa, beklenti e-Ticaret iş akışının sepetteki maddeler için karışık bir teslimat şekline (yani, bazı maddeler sevkiyat için seçilmiş, diğerleri teslim alma için seçilmiş) izin vermeyeceği yönündedir. **Eşit dağıtım olmadan başlık masrafları** özelliği  Commerce Headquarters'da **Kanalda tutarlı teslimat şekli işlemeyi etkinleştir** bayrağının açık olmasını gerektirir. Bu bayrak açık olduğundai sevkiyat masrafları Commerce Headquarters'taki yapılandırmaya bağlı olarak başlık düzeyinde veya satır düzerinde uygulanır.

Fabrikam teması, bazı maddelerin sevkiyat için diğerlerinin tesli alma için seçildiği karma teslimat modunu destekler. Bu modda, sevkiyat masrafları sevkiyat şekli için seçilen tüm maddeler için eşit olarak dağıtılır. Bir karma teslimat şeklinin çalışması için, ilk olarak **Eşit dağıtımlı başlık masrafları** özelliğini Commerce Headquarters'ta yapılandırmanız gerekir. Bu yapılandırma hakkında daha fazla bilgi için bkz. [Satış satırlarıyla eşleştirmek için başlık masraflarını eşit dağırma](pro-rate-charges-matching-lines.md).

Sevkiyat giderleri satır maddeleri için geçerliyse, her madde için sepet satırında gösterilebilir. Bu işlev **Sevkiyat masraflarını satır maddesinde göster** özelliğinin hem sepet modülü hem de ödeme modülü için etkinleştirilmesini gerektirir. Daha fazla bilgi için bkz. [Sepet modülü](add-cart-module.md) ve [Ödeme modülü](add-checkout-module.md).

Aşağıdaki şekilde ödeme sayfasında kullanılan bir teslimat seçenekleri modülü örneği gösterilmektedir.

![Ödeme sayfasındaki teslimat seçenekleri modülü örneği](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Teslimat seçenekleri modülü özellikleri

| Özellik | Değerler | Tanım |
|----------|--------|-------------|
| Başlık | Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Teslimar seçenekleri modülü için isteğe bağlı bir başlık. |
| Özel CSS sınıfı adı | Metin | Varsa bu modülü işlemek için kullanılacak özel Geçişli Stil Sayfaları (CSS) sınıfı adı. |
| Teslimat Modu Seçeneğini Filtrele | **Filtreleme** veya **Sevkiyat dışı modlar** | Teslimat seçenekleri modülünün tüm sevkiyat dışı teslimat modlarına filtre uygulayıp uygulamayacağını belirten bir değer. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Ödeme sayfasına teslimat seçenekleri modülü ekleme ve gerekli özellikleri ayarlama

Teslimat seçenekleri modülü yalnızca bir ödeme modülüne eklenebilir. Teslimat seçenekleri modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Alışveriş sepeti modülü](add-cart-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)

[Çevrimiçi kanal kurulumu](channel-setup-online.md)

[Çok yönlü kanal Gelişmiş otomatik masraflar](omni-auto-charges.md)

[Başlık masraflarını satış satırlarıyla eşleştirmek için eşit dağıtma](pro-rate-charges-matching-lines.md)

[Teslimat şekillerini ayarla](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]