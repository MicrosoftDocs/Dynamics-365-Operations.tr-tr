---
title: Çeşit grubu oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir ürün için boyut, stil veya renk çeşidi grubunun nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b47f38375fc8925288db36f066ed7820bab3fe9b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353168"
---
# <a name="create-a-variant-group"></a>Çeşit grubu oluşturma


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te bir ürün için boyut, stil veya renk çeşidi grubunun nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce, ürünler için birden çok çeşidi destekliyor. Farklı ürün kategorileri için çeşit grupları ayarlamak idealdir. Örneğin, çok küçük, küçük, orta, büyük ve ekstra büyük boyutlarda tişörtler için bir boyut grubu oluşturulabilir veya bir ürünün mevcut tüm renklerini eklemek için bir renk grubu oluşturulabilir. Ürünler eklenmeden önce çeşit grupları eklenmelidir.

Bu konuda, bir boyut grubu oluşturulacak ve yapılandırılacak. Stil gruplarını ve renk gruplarını ekleyip yapılandırmak için benzer yordamlar kullanılabilir.

## <a name="create-a-size-group"></a>Boyut grubu oluşturma

Boyut grubu oluşturmak için bu adımları izleyin.
 
1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Çeşit grupları \> Boyut grupları**'na gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Boyut grubu** kutusuna, boyut grubu için bir ad girin.
1. **Açıklama** kutusuna, uygun bir açıklama girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="add-attributes-to-the-size-group"></a>Boyut grubuna öznitelikler ekleme

Bir boyut grubuna öznitelikler eklemek için bu adımları izleyin.

1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Çeşit grupları \> Boyut grupları**'na gidin.
1. Gezinti bölmesinde bir boyut grubu seçin.
1. **Boyut grubu satırları** altında, **Ekle** 'yi seçin.
1. **Boyut** kutusuna, boyutu temsil eden bir dize girin (örneğin "XL").
1. **Boyut adı** kutusuna boyut için bir ad girin (örneğin, "Çok Büyük").
1. **Stok yenileme ağırlığı** kutusuna, stok yenileme ağırlığını temsil eden bir sayı girin.
1. **Barkoddaki sayı** kutusunda, barkodu temsil eden bir sayı girin.
1. **Görüntüleme sırası** kutusuna, görüntüleme sırasını temsil eden bir numara girin.
1. Boyutları eklemeyi bitirince, eylem bölmesinde **Kaydet**'i seçin.

Aşağıdaki resimde, "tişört boyutları" için bir boyut grubu örneği gösteriliyor.

![Boyut grubu oluşturma.](media/create-variant-group.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün bilgilerine genel bakış](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Perakende ürünlerini ayarlama](set-up-retail-products.md)

[Ürün boyutları](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]