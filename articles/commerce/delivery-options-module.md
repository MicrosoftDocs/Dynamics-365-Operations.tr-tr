---
title: Teslimat seçenekleri modülü
description: Bu makale teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
ms.date: 02/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c3fb60c61878fc790a44178fabc8a7be5809806b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268460"
---
# <a name="delivery-options-module"></a>Teslimat seçenekleri modülü

[!include [banner](includes/banner.md)]

Bu makale teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.

Teslimat seçenekleri modülleri, müşterilerin çevrimiçi siparişleri için sevkiyat veya çekme gibi bir teslimat şekli seçmesine olanak tanır. Teslimat şeklini belirlemek için bir sevkiyat adresi gereklidir. Sevkiyat adresi değiştirilirse, teslimat seçenekleri tekrar alınmalıdır. Siparişte yalnızca mağazadan teslim alınacak maddeler varsa, bu modül otomatik olarak gizlenir.

Teslimat şekillerinin nasıl yapılandırılacağı hakkında bilgi için bkz. [Çevrimiçi kanal kurulumu](channel-setup-online.md) ve [Teslimat şekillerini ayarlama](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Her teslimat şeklinin ilişkilendirilmiş masrafı olabilir. Çevrimiçi mağaza için masrafları yapılandırma hakkında bilgi için bkz. [Çok yönlü kanal Gelişmiş otomatik masraflar](omni-auto-charges.md).

Commerce sürümü 10.0.13'te, teslimat seçenekleri modülü **Eşit dağıtım olmadan başlık masrafları** ve **Satır masrafı olarak sevkiyat** özelliklerini destekleyecek şekilde güncelleştirilmiştir. Eşit dağıtma kapalıysa, beklenti e-Ticaret iş akışının sepetteki maddeler için karışık bir teslimat şekline (yani, bazı maddeler sevkiyat için seçilmiş, diğerleri teslim alma için seçilmiş) izin vermeyeceği yönündedir. **Eşit dağıtım olmadan başlık masrafları** özelliği Commerce Genel merkezde **Kanalda tutarlı teslimat şekli işlemeyi etkinleştir** bayrağının açık olmasını gerektirir. Bu özellik bayrağı açık olduğunda sevkiyat masrafları Commerce genel merkezdeki yapılandırmaya bağlı olarak başlık düzeyinde veya satır düzeyinde uygulanır.

Fabrikam teması, bazı maddelerin sevkiyat için diğerlerinin tesli alma için seçildiği karma teslimat modunu destekler. Bu modda, sevkiyat masrafları sevkiyat şekli için seçilen tüm maddeler için eşit olarak dağıtılır. Bir karma teslimat şeklinin çalışması için, ilk olarak **Eşit dağıtımlı başlık masrafları** özelliğini Commerce Headquarters'ta yapılandırmanız gerekir. Bu yapılandırma hakkında daha fazla bilgi için bkz. [Satış satırlarıyla eşleştirmek için başlık masraflarını eşit dağırma](pro-rate-charges-matching-lines.md).

Sevkiyat giderleri satır maddeleri için geçerliyse, her madde için sepet satırında gösterilebilir. Bu işlev **Sevkiyat masraflarını satır maddesinde göster** özelliğinin hem sepet modülü hem de ödeme modülü için etkinleştirilmesini gerektirir. Daha fazla bilgi için bkz. [Sepet modülü](add-cart-module.md) ve [Ödeme modülü](add-checkout-module.md).

Aşağıdaki şekilde ödeme sayfasında kullanılan bir teslimat seçenekleri modülü örneği gösterilmektedir.

![Ödeme sayfasındaki teslimat seçenekleri modülü örneği.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Teslimat seçenekleri modülü özellikleri

| Özellik | Değerler | Tanım |
|----------|--------|-------------|
| Başlık | Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Teslimar seçenekleri modülü için isteğe bağlı bir başlık. |
| Özel CSS sınıfı adı | Metin | Varsa bu modülü işlemek için kullanılacak özel Geçişli Stil Sayfaları (CSS) sınıfı adı. |
| Teslimat Modu Seçeneğini Filtrele | **Filtreleme** veya **Sevkiyat dışı modlar** | Teslimat seçenekleri modülünün tüm sevkiyat dışı teslimat modlarına filtre uygulayıp uygulamayacağını belirten bir değer. |
| Teslimat seçeneğini otomatik olarak belirleme | **Filtre uygulama**, **Teslimat seçeneğini otomatik olarak belirle ve özeti göster** veya **Teslimat seçeneğini otomatik olarak seç ve özet gösterme** | Bu özellik, kullanıcının seçim yapmasını gerektirmeden, ilk kullanılabilir teslimat seçeneğini ödeme için otomatik olarak uygular. Yalnızca bir kullanılabilir teslimat seçeneği varsa kullanılmalıdır. Bu özellik, Commerce 10.0.19 sürümüyle birlikte desteklenmeye başlanmıştır. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Ödeme sayfasına teslimat seçenekleri modülü ekleme ve gerekli özellikleri ayarlama

Teslimat seçenekleri modülü yalnızca bir ödeme modülüne eklenebilir. Teslimat seçenekleri modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).

> [!NOTE]
> Tutarsız teslimat işleme ile karşılaşabilirsiniz veya e-ticaret kanalınızda eşit olmayan başlık düzeyi harcamalarını görmeyebilirsiniz. Bu sorunları giderme konusunda rehberlik için, bkz. [E-ticaret kanallarında tutarlı teslimat modu işlemesini etkinleştirme](consistent-delivery-mode-handling.md).

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

[Teslimat şekillerini ayarla](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
