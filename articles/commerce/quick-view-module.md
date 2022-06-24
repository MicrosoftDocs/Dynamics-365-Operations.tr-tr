---
title: Hızlı görüntüleme modülü
description: Bu makale hızlı görüntüleme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e9066357fda4f5d91c547622ac64d8c4eef253ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847587"
---
# <a name="quick-view-module"></a>Hızlı görüntüleme modülü

[!include [banner](includes/banner.md)]

Bu makale hızlı görüntüleme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Hızlı görüntüleme modülü, kullanıcıların bir liste sayfasındaki ürünlere göz atarken ürün bilgilerini hızlı bir şekilde görüntülemesine ve ürün ayrıntıları sayfasına (PDP) gitmeksizin liste sayfasından bir veya daha fazla ürün eklemesini sağlar. Hızlı görüntüleme modülü, kullanıcıların bir "Sepete Ekle" kararı vermek için gereken ürün bilgilerine genel bakış sağlar. Ayrıca, kullanıcıların ek ürün ayrıntılarını ve satın alma seçeneklerini görebilmesi için PDP'ye bir bağlantı sağlar.

Hızlı görüntüleme modülü, [ürün koleksiyonu](product-collection-module-overview.md) ve [arama sonuçları](search-result-module.md) modülleri tarafından desteklenir.

> [!IMPORTANT]
> Hızlı görüntüleme modülü, Commerce 10.0.17 sürümü itibarıyla kullanılabilir.

Aşağıdaki şekilde ürün listesinde sayfasında kullanılan bir hızlı görüntüleme modülü örneği gösterilmektedir.

![Ürün listesi sayfasındaki hızlı görüntüleme modülü örneği.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Modül özellikleri

Hızlı görüntüleme modülü, satın alma kutusu modülüyle aynı işlevlerden bazılarını destekler. Bu nedenle, Hızlı görünüm modülünün özellikleri bir satın alma kutusu modülünün özelliklerine benzer.

| Özellik | Değerler | Tanım |
|----------------|--------|-------------|
| Başlık etiketi | **H1**, **H2**, **H3**, **H4**, **H5** veya **H6** | Bu özellik, ürün başlığının başlık etiketini tanımlar. Hızlı görüntüleme modülü sayfanın en üstünde ise, erişilebilirlik standartlarını karşılamak için bu özelliğin **H1** olarak ayarlanması gerekir. |
| Özel fiyata izin ver | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, kullanıcı özel bir fiyat girebilir. |
| Minimum fiyat | Tamsayı | Bu özellik yalnızca **Özel fiyata izin ver** özelliği **Doğru** olarak ayarlandığında uygulanabilir. Kullanıcının girebileceği minimum fiyatı tanımlar (örneğin, $1). |
| Maksimum fiyat | Tamsayı | Bu özellik yalnızca **Özel fiyata izin ver** özelliği **Doğru** olarak ayarlandığında uygulanabilir. Kullanıcının girebileceği maksimum fiyatı tanımlar (örneğin, $1000). |

## <a name="commerce-site-builder-settings"></a>Commerce site oluşturucu ayarları

Satın alma kutusu modülü gibi, hızlı görünüm modülü de **Site Ayarları \> Uzantılar \> Alışveriş sepetine ürün ekle** ayarlarına uyar. Ancak kullanıcıların bir liste sayfasında birden fazla ürüne göz atmasına ve liste sayfasından çıkmaksızın alışveriş sepetine eklemesine olanak tanımak olan, hızlı görüntüleme modülü amacıyla uyumlu olmadığından **Sepet sayfasına git** ayarı yoksayılır.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Ürün koleksiyonu modülüne hızlı görüntüleme modülü ekleme

Ürün koleksiyonu ve arama sonuçları modüllerine hızlı görünüm modülü eklenebilir.

Commerce site oluşturucuda bir ürün koleksiyonu modülüne hızlı görüntüleme modülü eklemek için aşağıdaki adımları izleyin.

1. **Sayfalar**'a gidin ve Fabrikam sitesi için giriş sayfasını seçin.
1. Giriş sayfasındaki herhangi bir **Ürün Koleksiyonu** modülüne gidin, üç noktayı (**...**) seçin ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Hızlı Görünüm** modülünü seçin ve **Tamam**'ı seçin.
1. **Hızlı Görünüm** modülünün özellikler bölmesinde **Başlık**'ı seçin. **Başlık** iletişim kutusunda, **Başlık düzeyi** alanını **H** 2 olarak ayarlayın ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Ürün topluluğu modülü](product-collection-module-overview.md)

[Arama sonuçları modülü](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
