---
title: Sipariş onayı modülü
description: Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698338"
---
# <a name="order-confirmation-module"></a>Sipariş onayı modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Sipariş onay modülü sipariş onay sayfasında bir sipariş yerleştirildikten sonra onay iletisi göstermek için kullanılır. Sipariş teyidi modülü, teslim alma sırasında sağlanan sipariş onay numarasını ve müşteri e-posta adresini gösterir.

Teslim alma sırasında bir sipariş verildiğinde, sipariş onay numarası ve müşteri e-posta adresi, sayfanın URL 'sinde sorgu dizesi olarak sipariş onayı sayfasına geçirilir. Sipariş onayı modülü bu bilgileri alır ve sipariş onayı sayfasında sipariş durumunu işler. Sipariş teyidi modülü siparişin durumunu sağlamak için bu sayfa bağlamını gerektiriyor.

## <a name="order-confirmation-module-properties"></a>Sipariş onayı modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık       | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Sipariş teyidi modülünün başlığı olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Sipariş onayı sayfası modülünde kullanılabilen modüller 

- **Öneriler** – müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.
- **Pazarlama** – Pazarlama modülü, pazarlama içeriğini sipariş onayı sayfasına ekleyebilir.

## <a name="create-an-order-confirmation-page-module"></a>Sipariş onayı sayfa modülü oluşturma

1. **Sipariş onayı şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir sipariş onayı modülü ekleyin.
1. Sipariş onayı modülünde bir öneri modülü ekleyin.
1. Şablonu kaydet ve önizleyin. Sipariş onay numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.
1. Şablonu giriş yapın ve yayımlayın.
1. **Sipariş onayı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz sipariş onayı şablonunu kullanın.
1. Sayfa anahattına varsayılan sayfayı ekleyin.
1. **Üstbilgi** yuvasında bir üstbilgi parçası ekleyin.
1. **Altbilgi** yuvasında bir altbilgi parçası ekleyin.
1. **Ana** yuvasına bir sipariş onayı modülü ekleyin.
1. Sipariş onayı modülünün Özellik bölmesinde Başlık **Sipariş onayını** ekleyin.
1. Sipariş onayı modülünün altında, bir öneri modülü ekleyin ve bunu **yeni** ve **en iyi satış** ayarlarını kullanacak şekilde konfigüre edin.
1. Sayfayı önizleyin ve kaydedin, giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
