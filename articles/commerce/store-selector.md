---
title: Mağaza seçicisi modülü
description: Bu makale mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268353"
---
# <a name="store-selector-module"></a>Mağaza seçicisi modülü

[!include [banner](includes/banner.md)]

Bu makale mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Müşteriler, çevrimiçi bir satın alma işleminden sonra seçili bir mağazadan bir ürünü almak için mağaza seçici modülünü kullanabilirler. Commerce sürüm 10.0.13'te mağaza seçici modülü yakındaki mağazaları gösteren bir **Mağaza Bulun** sayfası gösterebilecek ek özellikler de içerir.

Mağaza seçici modülü, arama yarıçapı içindeki mağazaları aramak için kullanıcıların bir konum (şehir, eyalet, adres vb.) girmesini sağlar. Modül ilk açıldığında, mağazaları bulmak için müşterinin tarayıcı konumunu kullanır (izin sağlanırsa).

## <a name="store-selector-module-usage"></a>Mağaza seçicisi modülünün kullanımı

- Bir mağaza seçici modülü malzeme çekme amacıyla bir mağaza seçmek için ürün ayrıntıları sayfasında (PDP) kullanılabilir.
- Bir mağaza seçici modülü malzeme çekme amacıyla bir mağaza seçmek için sepet sayfasında kullanılabilir.
- Mağaza seçici modülü, kullanılabilir tüm mağazaları gösteren bağımsız bir sayfada kullanılabilir.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Commerce Headquarters'da karşılama grubu ayarlama

Mağaza seçicinin mevcut mağazaları görüntülemesi için, karşılama grubunun Commerce Headquarters'da ayarlanması gerekir. Daha fazla bilgi için bkz. [Karşılama grupları ayarlama](customer-orders-overview.md#set-up-fulfillment-groups).

Ayrıca, karşılama grubundaki her mağaza için, mağaza yerleşiminin enlem ve boylamı Headquarters'ta tanımlanmalıdır.

Commerce Headquarters'da mağaza konumu için boylam ve enlem değerlerini girmek üzere aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Stok dökümü** öğelerini seçin.
1. Sol bölmede ambar konumunu seçin.
1. **Adresler** hızlı sekmesinde, **Gelişmiş**'i seçin.

    ![Headquarters'daki mağaza ayrıntıları örneği.](./media/Store-address.png)

1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde **Enlem** ve **Boylam** değerlerini girin.

    ![Headquarters'daki bir mağaza için enlem ve boylam ayarı örneği.](./media/Store-latitude-longitude.png)

1. Eylem bölmesinde, **Kaydet**'i seçin. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Mağazayı mağaza seçicisi modülünden gizleme

Bir karşılama grubundaki bazı mağazalar geçerli malzeme çekme yerleşimleri olmayabilir. Mağaza seçici modülünde yalnızca geçerli malzeme çekme yerleşimlerinin seçenek olarak göründüğünden emin olmak için Commerce Headquarters'da aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Commerce kurulumu \> Karşılama grupları \> Tüm mağazalar**'a gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Kurulum** altında, geçerli bir malzeme çekme yerleşimi olmayan her mağaza için, **Malzeme Çekme Yerleşimi** onay kutusunu temizleyin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. 1070 **Kanal yapılandırması** dağıtım planı işini çalıştırın.

## <a name="bing-maps-integration"></a>Bing Haritalar tümleştirmesi

Mağaza seçici modülü, [Bing Haritalar REST uygulama programlama arabirimleri (API'ler)](/bingmaps/rest-services/) ile Bing'in Coğrafi Kodlama ve Otomatik Öneri özelliklerini kullanacak şekilde Bing Haritalar ile tümleştirilmiştir. Bir Bing Haritalar API anahtarı gereklidir ve Commerce Headquarters'daki paylaşılan parametreler sayfasına eklenmelidir. Geocoding API, bir konumu enlem ve boylam değerlerine dönüştürmek için kullanılır. Autosuggest API ile tümleştirme, kullanıcılar arama alanına konum girerken arama önerilerini göstermek için kullanılır.

Autosuggest REST API için sitenizin içerik güvenlik ilkesi (CSP) uyarınca aşağıdaki URL'lere izin verildiğinden emin olmanız gerekir. Bu kurulum, site için çeşitli CSP yönergelerine (örneğin, **img-src**) izin verilen URL'leri ekleyerek Commerce site oluşturucuda gerçekleştirilir. Daha fazla bilgi için bkz. [İçerik güvenlik ilkesi](manage-csp.md). 

- **connect-src** yönergesine **&#42;.bing.com** ekleyin.
- **img-src** yönergesine **&#42;.virtualearth.net** ekleyin.
- **script-src** yönergesine, **&#42;.bing.com, &#42;.virtualearth.net** ekleyin.
- **script style-src** yönergesine **&#42;.bing.com** ekleyin.

## <a name="pickup-in-store-mode"></a>Mağazadan teslim alma modu

Mağaza seçici modülü,bir ürünün teslim alınabileceği mağazaların listesini gösteren bir **Mağazadan teslim alma** modunu destekler. Ayrıca, listedeki her mağaza için mağaza çalışma saatlerini ve ürün stokunu gösterir. Mağaza seçici modülü, ürün kullanılabilirliğini işlemek ve ürünün seçili mağazadaki teslimat modu **mağazadan teslim** olarak ayarlandığında kullanıcının ürünü sepete eklemesini sağlamak için ürünün bağlamını gerektirir. Daha fazla bilgi için bkz. [Stok ayarları](inventory-settings.md). 

Bir ürünün teslim alma için uygun olduğu mağazaları görüntüleyen bir PDF'de bir satın alma kutusu modülüne mağaza seçici modülü eklenebilir. Bir sepet modülüne da eklenebilir. Bu durumda, depo seçici modülü alışveriş sepetindeki her kalem için teslim alma seçeneklerini gösterir. Mağaza seçici modülü uzantılar ve özelleştirmeler aracılığıyla diğer sayfalara veya modüllere de eklenebilir.

Bu senaryosunun çalışması için ürünlerin **teslim alma** modu kullanılacak şekilde yapılandırılması gerekir. Aksi durumda, modül ürün sayfalarında gösterilmez. Teslimat modunun yapılandırılmasına ilişkin daha fazla bilgi için bkz. [Teslimat modlarını ayarlama](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Aşağıdaki resimde, PDP üzerinde kullanılan bir Mağaza Seçicisi modülü örneği gösterilmektedir.

![Bir ürün detayı sayfasında (PDP) kullanılan mağaza seçici modülü örneği.](./media/BOPIS.PNG)

> [!NOTE]
> Sürüm 10.0.16 ve sonrasında, bir organizasyonun müşteriler için birden çok malzeme çekme modu tanımlamasına izin veren yeni bir özellik etkinleştirilebilir.  Bu özellik etkinleştirilirse, mağaza Seçicisi ve e-ticaretin diğer modülleri, yapılandırıldıysa, büyük olasılıkla çoklu çekme teslim seçenekleri arasından seçim yapmasına olanak verecek şekilde geliştirilecektir.  Bu özellik hakkında daha fazla bilgi edinmek için [Bu belgeye bakın](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Mağaza bulma modu

Mağaza seçici modülü **Mağazaları bul** modunu da destekler. Bu mod, kullanılabilir mağazaları ve bunların bilgilerini gösteren bir mağaza konumları sayfası oluşturmak için kullanılabilir. Bu modda, mağaza seçici modülü, ürün bağlamı olmadan çalışır ve herhangi bir site sayfasında bağımsız modül olarak kullanılabilir. Ayrıca, modül için ilgili ayarlar açıksa, kullanıcılar bir mağazayı tercih edilen mağaza olarak seçebilir. Bir mağaza kullanıcının tercih edilen mağazası olarak seçildiğinde, mağaza kimliği tarayıcı tanımlama bilgisinde tutulur. Bu nedenle, kullanıcı, tanımlama bilgisi onay iletisini kabul etmelidir.

Aşağıdaki çizimde, bir mağaza konumları sayfasındaki harita modülüyle birlikte kullanılan bir mağaza seçici modülü örneği gösterilmektedir.

![Mağaza konumları sayfasında mağaza seçici modülü ile harita modülü örneği.](./media/ecommerce-Storelocator.PNG)

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

## <a name="site-settings"></a>Site ayarları

Mağaza Seçici modülü, [Sepete ürün ekle ayarlarına](add-cart-settings.md) uyar. Mağaza seçici modülünden bir öğe alışveriş sepetine eklendikten sonra, site kullanıcıları uygun yapılandırılmış iş akışlarını görürler.

## <a name="add-a-store-selector-module-to-a-page"></a>Bir sayfaya mağaza seçici modülü ekleme

**Mağazadam teslim alma** modunda modül yalnızca PDP'ler ve speet sayfalarında kullanılabilir. Modülün özellik bölmesinde modu **Mağazadan teslim alma** olarak ayarlayın.

- Satın alma kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Satın alma kutusu modülü](add-buy-box.md). 
- Sepet kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Sepet modülü](add-cart-module.md).

Mağaza seçici modülünü bu makalenin yukarısında gösterilen çizimde olduğu gibi mağaza konumları sayfasında mevcut mağazaları gösterecek şekilde yapılandırmak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusunda **Sayfa adı** altında, **Mağaza konumları**'nı girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, oluşturduğunuz **Pazarlama şablonunu** seçin ve sonra **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin. 
1. Yeni sayfanın **Ana** alanında, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **2 sütunlu kapsayıcı** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **X küçük görünüm bağlantı noktası sütunu yapılandırması** değerini **%100** olarak ayarlayın.
1. **Küçük görünüm bağlantı noktası sütunu yapılandırması** değerini **%100** olarak ayarlayın.
1. **Orta görünüm bağlantı noktası sütunu yapılandırması** değerini **%33 %67** olarak ayarlayın.
1. **Büyük görünüm bağlantı noktası sütunu yapılandırması** değerini **%33 %67** olarak ayarlayın.
1. **2 sütunlu kapsayıcı** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Mod** değerini **Mağaza bul** olarak ayarlayın.
1. Mil cinsinden **Arama yarıçapı** değerini ayarlayın.
1. İhtiyaçlarınıza göre **Tercih edilen mağaza olarak ayarla**, **Tüm mağazaları göster** ve **Otomatik öneriyi etkinleştir** gibi diğer özellikleri ayarlayın.
1. **2 sütunlu kapsayıcı** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Harita** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde istediğiniz ek özellikleri ayarlayın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
 
## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[PDP'ye hızlı gezinti](quick-tour-pdp.md)

[Sepet ve ödemede hızlı tur](quick-tour-cart-checkout.md)

[Teslimat şekillerini ayarla](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Kuruluşunuz için Bing Haritalar'ı yönetme](dev-itpro/manage-bing-maps.md)

[Bing Maps REST API'leri](/bingmaps/rest-services/)

[Harita modülü](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
