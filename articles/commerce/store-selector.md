---
title: Mağaza seçicisi modülü
description: Bu konu mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5400a2e743a78124dca4bf9be3ccaf7870ea8b7d
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665284"
---
# <a name="store-selector-module"></a>Mağaza seçicisi modülü

[!include [banner](includes/banner.md)]

Bu konu mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

Müşteriler, çevrimiçi bir satın alma işleminden sonra seçili bir mağazadan bir ürünü almak için mağaza seçici modülünü kullanabilirler. Commerce sürüm 10.0.13'te mağaza seçici modülü yakındaki mağazaları gösteren bir **Mağaza Bulun** sayfası gösterebilecek ek özellikler de içerir.

Mağaza seçici modülü, arama yarıçapı içindeki mağazaları aramak için kullanıcıların bir konum (şehir, eyalet, adres vb.) girmesini sağlar. Modül ilk açıldığında, mağazaları bulmak için müşterinin tarayıcı konumunu kullanır (izin sağlanırsa).

## <a name="store-selector-module-usage-in-e-commerce"></a>e-Ticarette mağaza seçici modül kullanımı

- Bir mağaza seçici modülü malzeme çekme amacıyla bir mağaza seçmek için ürün ayrıntıları sayfasında (PDP) kullanılabilir.
- Bir mağaza seçici modülü malzeme çekme amacıyla bir mağaza seçmek için sepet sayfasında kullanılabilir.
- Mağaza seçici modülü, kullanılabilir tüm mağazaları gösteren bağımsız bir sayfada kullanılabilir.

## <a name="bing-maps-integration"></a>Bing Haritalar tümleştirmesi

Mağaza seçici modülü, [Bing Haritalar REST uygulama programlama arabirimleri (API'ler)](https://docs.microsoft.com/bingmaps/rest-services/) ile Bing'in Coğrafi Kodlama ve Otomatik Öneri özelliklerini kullanacak şekilde Bing Haritalar ile tümleştirilmiştir. Bir Bing Haritalar API anahtarı gereklidir ve Commerce Headquarters'daki paylaşılan parametreler sayfasına eklenmelidir. Geocoding API, bir konumu enlem ve boylam değerlerine dönüştürmek için kullanılır. Autosuggest API ile tümleştirme, kullanıcılar arama alanına konum girerken arama önerilerini göstermek için kullanılır.

Autosuggest REST API için sitenizin içerik güvenlik ilkesi (CSP) uyarınca aşağıdaki URL'lere izin verildiğinden emin olmanız gerekir. Bu kurulum, site için çeşitli CSP yönergelerine (örneğin, **img-src**) izin verilen URL'leri ekleyerek Commerce site oluşturucuda gerçekleştirilir. Daha fazla bilgi için bkz. [İçerik güvenlik ilkesi](manage-csp.md). 

- **connect-src** yönergesine **&#42;.bing.com** ekleyin.
- **img-src** yönergesine **&#42;.virtualearth.net** ekleyin.
- **script-src** yönergesine, **&#42;.bing.com, &#42;.virtualearth.net** ekleyin.
- **script style-src** yönergesine **&#42;.bing.com** ekleyin.
 
## <a name="pickup-in-store-mode"></a>Mağazadan teslim alma modu

Mağaza seçici modülü,bir ürünün teslim alınabileceği mağazaların listesini gösteren bir **Mağazadan teslim alma** modunu destekler. Ayrıca, listedeki her mağaza için mağaza çalışma saatlerini ve ürün stokunu gösterir. Mağaza seçici modülü, ürün kullanılabilirliğini işlemek ve ürünün seçili mağazadaki teslimat modu **mağazadan teslim** olarak ayarlandığında kullanıcının ürünü sepete eklemesini sağlamak için ürünün bağlamını gerektirir. Daha fazla bilgi için bkz. [Stok ayarları](inventory-settings.md). 

Bir ürünün teslim alma için uygun olduğu mağazaları görüntüleyen bir PDF'de bir satın alma kutusu modülüne mağaza seçici modülü eklenebilir. Bir sepet modülüne da eklenebilir. Bu durumda, depo seçici modülü alışveriş sepetindeki her kalem için teslim alma seçeneklerini gösterir. Mağaza seçici modülü uzantılar ve özelleştirmeler aracılığıyla diğer sayfalara veya modüllere de eklenebilir.

Bu senaryosunun çalışması için ürünlerin **teslim alma** modu kullanılacak şekilde yapılandırılması gerekir. Aksi durumda, modül ürün sayfalarında gösterilmez. Teslimat modunun yapılandırılmasına ilişkin daha fazla bilgi için bkz. [Teslimat modlarını ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Aşağıdaki resimde, PDP üzerinde kullanılan bir Mağaza Seçicisi modülü örneği gösterilmektedir.

![Bir ürün detayı sayfasında (PDP) kullanılan mağaza seçici modülü örneği](./media/BOPIS.PNG)

> [!NOTE]
> Sürüm 10.0.16 ve sonrasında, bir organizasyonun müşteriler için birden çok malzeme çekme modu tanımlamasına izin veren yeni bir özellik etkinleştirilebilir.  Bu özellik etkinleştirilirse, mağaza Seçicisi ve e-ticaretin diğer modülleri, yapılandırıldıysa, büyük olasılıkla çoklu çekme teslim seçenekleri arasından seçim yapmasına olanak verecek şekilde geliştirilecektir.  Bu özellik hakkında daha fazla bilgi edinmek için [Bu belgeye bakın](https://docs.microsoft.com/dynamics365/commerce/multiple-pickup-modes). 

## <a name="find-stores-mode"></a>Mağaza bulma modu

Mağaza seçici modülü **Mağazaları bul** modunu da destekler. Bu mod, kullanılabilir mağazaları ve bunların bilgilerini gösteren bir mağaza konumları sayfası oluşturmak için kullanılabilir. Bu modda, mağaza seçici modülü, ürün bağlamı olmadan çalışır ve herhangi bir site sayfasında bağımsız modül olarak kullanılabilir. Ayrıca, modül için ilgili ayarlar açıksa, kullanıcılar bir mağazayı tercih edilen mağaza olarak seçebilir. Bir mağaza kullanıcının tercih edilen mağazası olarak seçildiğinde, mağaza kimliği tarayıcı tanımlama bilgisinde tutulur. Bu nedenle, kullanıcı, tanımlama bilgisi onay iletisini kabul etmelidir.

Aşağıdaki çizimde, bir mağaza konumları sayfasındaki harita modülüyle birlikte kullanılan bir mağaza seçici modülü örneği gösterilmektedir.

![Mağaza konumları sayfasında mağaza seçici modülü ile harita modülü örneği](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Harita oluşturma

Bir haritada mağaza konumlarını göstermek için mağaza seçici modülü harita modülüyle birlikte kullanılabilir. Harita modülüyle ilgili daha fazla bilgi için bkz. [Harita modülü](map-module.md)

## <a name="store-selector-module-properties"></a>Mağaza seçicisi modülü özellikleri

| Özellik adı | Değer | Tanım |
|---------------|-------|-------------|
| Başlık | Metin | Modülün başlığı. |
| Mod | **Mağaza bulma** veya **Mağazadan teslim alma** | **Mağaza bulma** modu, mevcut mağazaları gösterir. **Mağazadan teslim alma** modu, kullanıcıların teslim alma için bir mağaza seçmelerini sağlar. |
| Stil | **İletişim kutusu** veya **Satır içi** | Modül, satır içi olarak veya bir iletişim kutusunda oluşturulabilir. |
| Tercih edilen mağaza olarak ayarla | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlandığında, kullanıcılar tercih edilen bir mağaza ayarlayabilir. Bu özellik, kullanıcıların bir tanımlama bilgisi izni iletisini kabul etmesini gerektirir. |
| Tüm mağazaları göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlandığında, kullanıcılar **Arama çapı** özelliğini atlayabilir ve tüm mağazaları görüntüleyebilir. |
| Otomatik öneri seçenekleri: Maksimum sonuç sayısı | Sayı | Bu özellik, Bing Autosuggest API ile gösterilebilecek otomatik öneri sonuçları sayısının üst sınırını tanımlar. |
| Arama yarıçapı | Sayı | Bu özellik mil cinsinden arama yarıçapını tanımlar. Herhangi bir değer belirtilmezse, varsayılan arama yarıçapı olan 50 mil değeri kullanılır. |
| Hizmet koşulları | URL |  Bu özellik, Bing Haritalar hizmetini kullanmak için gerekli olan hizmet koşulları URL'sini belirtir. |

## <a name="add-a-store-selector-module-to-a-page"></a>Bir sayfaya mağaza seçici modülü ekleme

**Mağazadam teslim alma** modunda modül yalnızca PDP'ler ve speet sayfalarında kullanılabilir. Modülün özellik bölmesinde modu **Mağazadan teslim alma** olarak ayarlayın.

- Satın alma kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Satın alma kutusu modülü](add-buy-box.md). 
- Sepet kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Sepet modülü](add-cart-module.md).

Mağaza seçici modülünü bu konunun yukarısında gösterilen çizimde olduğu gibi mağaza konumları sayfasında mevcut mağazaları gösterecek şekilde yapılandırmak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda **Pazarlama şablonu** şablonunu seçin. **Sayfa adı** altında **Mağaza konumları** girin ve **Tamam**'ı seçin.
1. Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **2 sütunlu kapsayıcı** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **X küçük görünüm bağlantı noktası sütunu yapılandırması** değerini **%100** olarak ayarlayın.
1. **Küçük görünüm bağlantı noktası sütunu yapılandırması** değerini **%100** olarak ayarlayın.
1. **Orta görünüm bağlantı noktası sütunu yapılandırması** değerini **%33 %67** olarak ayarlayın.
1. **Büyük görünüm bağlantı noktası sütunu yapılandırması** değerini **%33 %67** olarak ayarlayın.
1. **2 sütunlu kapsayıcı** yuvasında, üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Mod** değerini **Mağaza bul** olarak ayarlayın.
1. Mil cinsinden **Arama yarıçapı** değerini ayarlayın.
1. İhtiyaçlarınıza göre **Tercih edilen mağaza olarak ayarla**, **Tüm mağazaları göster** ve **Otomatik öneriyi etkinleştir** gibi diğer özellikleri ayarlayın.
1. **2 sütunlu kapsayıcı** yuvasında, üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Harita** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde istediğiniz ek özellikleri ayarlayın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
 
## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[PDP'ye hızlı gezinti](quick-tour-pdp.md)

[Sepet ve ödemede hızlı tur](quick-tour-cart-checkout.md)

[Teslimat şekillerini ayarla](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Kuruluşunuz için Bing Haritalar'ı yönetme](dev-itpro/manage-bing-maps.md)

[Bing Maps REST API'leri](https://docs.microsoft.com/bingmaps/rest-services/)

[Harita modülü](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]