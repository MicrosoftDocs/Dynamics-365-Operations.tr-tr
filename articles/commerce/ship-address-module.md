---
title: Sevkiyat adresi modülü
description: Bu konu sevkiyat adresi modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2020
ms.locfileid: "4416587"
---
# <a name="shipping-address-module"></a>Sevkiyat adresi modülü

[!include [banner](includes/banner.md)]

Bu konu sevkiyat adresi modülünü ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.

## <a name="overview"></a>Genel bakış

Sevkiyat adresi modülü, müşteriye ödeme akışı sırasında bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir. Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir ve müşteri bunlar arasından seçim yapabilir. Müşteri Ayrıca yeni bir adres ekleyebilir. Sevkiyat adresi modülü, siparişteki sevkiyat gerektiren tüm maddeler için kullanılır.

Sevkiyat adresi biçimleri her ülke veya bölge için Commerce Headquarters'da tanımlanabilir ve sevkiyat adresi modülü ülkeye/bölgeye özel kurallar zorlar.

Müşteriler, ödeme akışı sırasında bir sevkiyat adresi girerken, adresi birincil adres olarak kaydetme seçeneği vardır. Bu seçenek yalnızca müşterinin oturum açmış olması durumunda gösterilir.

Sevkiyat adresi modülü adres doğrulaması sağlamasa da, bu işlev özelliştirme yoluyla gerçekleştirilebilir.

Aşağıdaki örnekte ödeme sayfasında kullanılan yeni bir teslimat adresi modülü örneği gösterilmektedir.

![Ödeme sayfasındaki sevkiyat adresi modülü örneği](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modül özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık | Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Sevkiyat adresi modülü için isteğe bağlı bir başlık. |
| Adres türünü göster | **Doğru** veya **yanlış** | Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa, **Ev** veya **İş** gibi bir adres türü gösterilir. Herhangi bir adres türü belirtilmezse, adres otomatik olarak **Tür**=**Diğer** olarak kaydedilir. |

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
