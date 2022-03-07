---
title: Sipariş onayı modülü
description: Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te kullanılacağını açıklamaktadır ve kapsamaktadır.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6914f8c968b03c05a2311a31a4f391c828db5b8b35bc864504dad78f43b3623f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733858"
---
# <a name="order-confirmation-module"></a>Sipariş onayı modülü

[!include [banner](includes/banner.md)]

Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te kullanılacağını açıklamaktadır ve kapsamaktadır.

Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş onayı modülü kullanılabilir. Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri, teslim alma seçenekleri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.

## <a name="order-confirmation-module-properties"></a>Sipariş onayı modülü özellikleri

| Özellik adı  | Değerler | Tanım |
|----------------|--------|-------------|
| Başlık        | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Sipariş teyidi modülünün başlığı olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| İlgili kişi numarası | Text | Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir. |
| Malzeme çekme zaman lotu bilgilerini göster | Doğru veya Yanlış | Bu özellik Dynamics 365 Commerce 10.0.15 ve daha yüksek sürümlerde kullanılabilir. Doğru olduğunda, malzeme çekme maddesi için sağlanmışsa malzeme çekme zaman Lot bilgilerini görüntüler|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Sipariş onayı sayfası modülünde kullanılabilen modüller

Sipariş onayı sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş onayı modülünün yanı sıra ekleyebilirsiniz. Burada bazı örnekler verilmiştir:

- **Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.
- **Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş onayı sayfasına herhangi bir pazarlama modülü eklenebilir.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Sayfaya sipariş onayı modülü ekleme

Bir yeni sayfaya sipariş onayı modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Sipariş onayı şablonu** adını girin ve ve **Tamam**'ı seçin.
1. **Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Sipariş onayı** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından şablonu önizlemek için **Önizleme**'yi seçin. Sipariş onay numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seç** iletişim kutusunda **Sipariş onayı şablonu**'nu seçin. **Sayfa adı** altından **Sipariş onayı sayfası** girin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Sipariş onayı** modülünü seçin ve **Tamam**'ı seçin.
1. Sipariş onayı modülünün özellikler bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.
1. **Başlık** iletişim kutusunun **Başlık Metni** alanında, **Sipairş onayı** başlık metnini girin ve ardından **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Hediye kartı modülü](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]