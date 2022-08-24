---
title: Sevkiyat adresi modülü
description: Bu makale sevkiyat adresi modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
ms.date: 02/11/2021
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
ms.openlocfilehash: 48e6909b4dac9722830a83ec3a63a58876768d7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275018"
---
# <a name="shipping-address-module"></a>Sevkiyat adresi modülü

[!include [banner](includes/banner.md)]

Bu makale sevkiyat adresi modülünü ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.

Sevkiyat adresi modülü, müşteriye ödeme akışı sırasında bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir. Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir ve müşteri bunlar arasından seçim yapabilir. Müşteri Ayrıca yeni bir adres ekleyebilir. Sevkiyat adresi modülü, siparişteki sevkiyat gerektiren tüm maddeler için kullanılır.

Sevkiyat adresi biçimleri her ülke veya bölge için Commerce Headquarters'da tanımlanabilir ve sevkiyat adresi modülü ülkeye/bölgeye özel kurallar zorlar.

Müşteriler, ödeme akışı sırasında bir sevkiyat adresi girerken, adresi birincil adres olarak kaydetme seçeneği vardır. Bu seçenek yalnızca müşterinin oturum açmış olması durumunda gösterilir.

Sevkiyat adresi modülü adres doğrulaması sağlamasa da, bu işlev özelliştirme yoluyla gerçekleştirilebilir.

Aşağıdaki örnekte ödeme sayfasında kullanılan yeni bir teslimat adresi modülü örneği gösterilmektedir.

![Ödeme sayfasındaki sevkiyat adresi modülü örneği.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modül özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık | Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Sevkiyat adresi modülü için isteğe bağlı bir başlık. |
| Adres türünü göster | **Doğru** veya **yanlış** | Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa, **Ev** veya **İş** gibi bir adres türü gösterilir. Herhangi bir adres türü belirtilmezse, adres otomatik olarak **Tür**=**Diğer** olarak kaydedilir. |
| Otomatik öneriyi etkinleştir| **Doğru** veya **yanlış** | Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa otomatik adres önerileri sağlanacaktır. Bu öneriler Bing Haritalar tarafından desteklenmektedir. Sitenizde Bing Haritalar tümleştirmesini ayarlama hakkında bilgi için, bkz [Mağaza seçicisi modülü](store-selector.md). Bu özellik Commerce 10.0.15 sürümünden itibaren mevcuttur.|
|Otomatik öneri seçenekleri| Bir sayı| Otomatik adres önerileri etkinse, sağlanacak maksimum öneri sayısı gibi ek seçenekler belirtebilirsiniz.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Ödeme sayfasına sevkiyat adresi modülü ekleme ve gerekli özellikleri ayarlama

Sevkiyat adresi modülü yalnızca bir ödeme modülüne eklenebilir. Sevkiyat adresi modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)

[Mağaza seçicisi modülü](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
