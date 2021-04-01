---
title: Harita modülü
description: Bu konu harita modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 74991a2979540dab344f39976005250637fab29c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252594"
---
# <a name="map-module"></a>Harita modülü

[!include [banner](includes/banner.md)]


Bu konu harita modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.

Harita modülü, [Bing Haritalar V8 Web Denetimi](https://docs.microsoft.com/bingmaps/v8-web-control/) kullanılarak işlenen etkileşimli bir harita üzerindeki mağazaların konumlarını gösterir. Bir Bing Haritalar API anahtarı gereklidir ve Commerce Headquarters'daki paylaşılan parametreler sayfasına eklenmelidir. Harita modülleri, kullanıcıların harita konumlarını görüntülemek için seçim yapabilen Yol, Uydu ve Streetside görünümü gibi farklı görünümler sağlar. Ayrıca, yakınlaştırma ve kullanıcının konumunu kullanma gibi etkileşimlere de izin verir.

Bir harita modülü, bir haritada işlenmesi gereken mağazaların coğrafi konumlarını belirlemek için mağaza seçici modülüyle birlikte çalışır. Bir kullanıcı site sayfasında bu modüllerden birinde bir mağaza seçtiğinde mağaza seçici ve harita modülleri etkileşime girer. Harita modülleri, mağaza seçici modülleriyle etkileşimi dışında diğer senaryolar için genişletilebilir. Ancak, modül özelleştirmesi gereklidir.

> [!NOTE]
> Harita modülü Dynamics 365 Commerce 10.0.13 sürümünde bulunur.

Aşağıdaki resimde mağaza konumları sayfasında kullanılan bir harita modülü örneği gösterilmektedir.

![Mağaza seçici modülü örneği](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Modül özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Başlık | Metin | Modülün başlığı. |
| Raptiye seçenekleri: Varsayılan simge | Görüntü | Haritada gösterilen mağazalar için kullanılacak raptiye sembolü resmi. |
| Raptiye seçenekleri: Etkin simge | Görüntü | Haritada seçilen bir mağaza için kullanılacak raptiye sembolü resmi. |
| Raptiye seçenekleri: Varsayılan simge rengi | Karakter dizesi | Haritadaki raptiye sembollerinin rengi için metin veya onaltılı değer. |
| Raptiye seçenekleri: Etkin simge rengi | Karakter dizesi | Haritadaki seçili raptiye simgelerinin rengi için metin veya onaltılı değer. |
| Dizini göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa bir mağazayı gösteren her raptiye sembolü, bir dizin gösterir. Bu dizin, mağaza seçici modülünün gösterdiği liste görünümündeki dizinle eşleşir. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>İzin verilen eşleme URL'lerini sitenin içerik güvenlik ilkesi yönergelerinden ekleme

Haritalar modülünün Bing Haritalar ile etkileşime girmesini istiyorsanız, sitenizin içerik güvenlik ilkesi (CSP) uyarınca aşağıdaki eşleme URL'lerine izin verildiğinden emin olmanız gerekir. Bu kurulum, çeşitli site CSP yönergelerine (örneğin, **img-src**) izin verilen URL'leri ekleyerek Commerce site oluşturucuda gerçekleştirilir. Daha fazla bilgi için bkz. [İçerik güvenlik ilkesi](manage-csp.md). 

- **connect-src** yönergesine **&#42;.bing.com** ekleyin.
- **img-src** yönergesine **&#42;.virtualearth.net** ekleyin.
- **Script-src** yönergesine **&#42;.bing.com, &#42;.virtualearth.net** ekleyin.
- **script style-src** yönergesine **&#42;.bing.com** ekleyin.

## <a name="add-a-map-module-to-a-page"></a>Sayfaya harita modülü ekleme

Bir sayfada harita modülünü yapılandırma hakkında ayrıntılı bilgi için bkz. [Mağaza seçici modülü](store-selector.md). 
 
## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[Mağaza seçicisi modülü](store-selector.md)

[Kuruluşunuz için Bing Haritalar'ı yönetme](./dev-itpro/manage-bing-maps.md)

[Bing Haritalar V8 Web Denetimi](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]