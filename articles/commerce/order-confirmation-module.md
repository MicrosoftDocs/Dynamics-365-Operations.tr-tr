---
title: Sipariş ayrıntıları modülü
description: Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026029"
---
# <a name="order-details-module"></a>Sipariş ayrıntıları modülü


[!include [banner](includes/banner.md)]

Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş ayrıntıları modülü kullanılabilir. Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.

## <a name="order-confirmation-module-properties"></a>Sipariş onayı modülü özellikleri

| Özellik adı  | Değerler | Tanım |
|----------------|--------|-------------|
| Başlık        | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Sipariş teyidi modülünün başlığı olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| İlgili kişi numarası | Text | Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Sipariş ayrıntıları sayfası modülünde kullanılabilen modüller

Sipariş Ayrıntıları sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş ayrıntıları modülünün yanı sıra ekleyebilirsiniz. Burada bazı örnekler verilmiştir:

- **Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.
- **Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş ayrıntıları sayfasına herhangi bir pazarlama modülü eklenebilir.

## <a name="create-an-order-details-page-module"></a>Sipariş ayrıntıları sayfa modülü oluşturma

1. **Sipariş ayrıntıları şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir sipariş ayrıntıları modülü ekleyin.
1. Sipariş ayrıntıları modülünde bir öneri modülü ekleyin.
1. Şablonu kaydet ve önizleyin. Sipariş ayrıntıları numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.
1. Şablon düzenlemeyi tamamlayın ve sonra yayımlayın.
1. **Sipariş ayrıntıları sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz sipariş ayrıntıları şablonunu kullanın.
1. Sayfa anahattına varsayılan sayfayı ekleyin.
1. **Üstbilgi** yuvasında bir üstbilgi parçası ekleyin.
1. **Altbilgi** yuvasında bir altbilgi parçası ekleyin.
1. **Ana** yuvasına bir sipariş ayrıntıları modülü ekleyin.
1. Sipariş ayrıntıları modülünün Özellik bölmesinde Başlık **Sipariş ayrıntıları** ekleyin.
1. Sipariş ayrıntıları modülünün altında, bir öneri modülü ekleyin ve bunu **yeni** ve **en iyi satış** ayarlarını kullanacak şekilde konfigüre edin.
1. Sayfayı kaydet ve önizleyin.
1. Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
