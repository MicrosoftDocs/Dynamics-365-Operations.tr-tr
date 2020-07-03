---
title: Sipariş ayrıntıları modülü
description: Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464942"
---
# <a name="order-details-module"></a>Sipariş ayrıntıları modülü


[!include [banner](includes/banner.md)]

Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş ayrıntıları modülü kullanılabilir. Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.

## <a name="order-details-module-properties"></a>Sipariş ayrıntıları modülü özellikleri

| Özellik adı  | Değerler | Tanım |
|----------------|--------|-------------|
| Başlık        | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Sipariş ayrıntıları modülünün başlığı olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| İlgili kişi numarası | Text | Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Sipariş ayrıntıları sayfası modülünde kullanılabilen modüller

Sipariş Ayrıntıları sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş ayrıntıları modülünün yanı sıra ekleyebilirsiniz. Burada bazı örnekler verilmiştir:

- **Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.
- **Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş ayrıntıları sayfasına herhangi bir pazarlama modülü eklenebilir.

## <a name="add-an-order-details-module-to-a-page"></a>Sayfaya sipariş ayrıntıları modülü ekleme

Bir yeni sayfaya sipariş ayrıntıları modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Sipariş ayrıntıları şablonu** adını girin ve ve **Tamam**'ı seçin.
1. **Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Sipariş ayrıntıları** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından şablonu önizlemek için **Önizleme**'yi seçin. Sipariş ayrıntıları numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seç** iletişim kutusunda **Sipariş ayrıntıları şablonu**'nu seçin. **Sayfa adı** altından **Sipariş ayrıntıları sayfası** girin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Sipariş ayrıntıları** modülünü seçin ve **Tamam**'ı seçin.
1. Sipariş ayrıntılatı modülünün özellikler bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.
1. **Başlık** iletişim kutusunun **Başlık Metni** alanında, **Sipairş ayrıntıları** başlık metnini girin ve ardından **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Kapsayıcı modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
