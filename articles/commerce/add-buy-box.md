---
title: Satın alma kutusu modülü
description: Bu konu satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811153"
---
# <a name="buy-box-module"></a>Satın alma kutusu modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Terim *satın alma kutusu* genellikle, ürün satın alma işlemi yapmak için gereken en önemli bilgileri barındıran, ürün Ayrıntıları sayfasının "manşet" alanını belirtir. (Sayfanın ilk yüklendiği sırada "manşet" olan alan görünür, böylece görmek için kullanıcıların aşağı kaydırılması gerekmez.)

Satın alma kutusu modülü, Ürün Ayrıntıları sayfasının satın alma kutusu alanında gösterilen tüm modülleri barındırmak için kullanılan özel bir konteynerdir.

Ürün Ayrıntıları sayfasının URL'SI ürün kodunu içerir. Bir satınalma kutusu modülünü işlemek için gereken tüm bilgiler bu ürün kimliğinden türetilir. Bir ürün kodu sağlanmazsa, satın alma kutusu modülü sayfada doğru olarak işlenmez. Bu nedenle, satın alma kutusu modülü, ürün bağlamı bulunmayan herhangi bir sayfada (örneğin, giriş sayfası veya pazarlama sayfası) kullanılamaz.

## <a name="buy-box-module-properties-and-slots"></a>Satın alma kutusu modülü özelliklerini ve yuvaları 

Konteyner olarak, satınalma kutusu modülü genişlik gibi bazı temel özellikleri denetler. Genişlik ayarı, konteynerdeki modüllerin o konteynerin içine sığması gerekip gerekmediğini veya ekranı doldurup dolduramayacağını belirler.

Ürün Ayrıntıları sayfasında, satınalma kutusu iki bölgeye ayrılmıştır: soldaki ortam bölgesi ve sağda bulunan bir içerik bölgesi. Bu iki bölge, satınalma kutusu modülünde yuvalar ile temsil edilir. Her yuva, yalnızca yuva tarafından desteklenen belirli modülleri kabul edecek şekilde önceden yapılandırılmıştır. Örneğin, **ortam** yuvası yalnızca ortam Galerisi modülünü destekler.

Varsayılan olarak, ortam bölgesi ve içerik bölgesinin sütun genişlikleri oranı 2:1. Ancak, sütun genişlikleri Tema tarafından geçersiz kılınabilir. Ek olarak, mobil cihazlarda iki bölge yığılır, böylece diğer bölgenin altında bir alan görünür.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Satınalma kutusu modülünde kullanılabilen modüller

- **Ortam Galerisi** – bu modül, ürün ayrıntıları sayfasındaki bir ürünün görüntülerini sergilemesinde kullanılır. Bir ile birçok görüntüyü destekleyebilir. Küçük resimleri de destekler. Küçük resimler yatay (görüntünün altında bir satır olarak) veya dikey olarak (görüntünün yanında bir sütun olarak) düzenlenebilir. Ortam Galerisi modülü, satın alma kutusu modülündeki **ortam** yuvasına eklenebilir. Şu anda yalnızca resimleri ve videoları desteklemektedir.
- **Ürün başlığı** – bu modül, ürün ayrıntıları sayfasında ürünün başlığını gösterir. Varsayılan olarak **H1** başlık etiketi kullanılır, ancak başlık etiketi gerektiği gibi değiştirilebilir.
- **Ürün değerlendirmesi** – bu modül bir ürünle ilgili müşteri derecelendirmelerine dayalı olarak yıldız derecelendirmelerini gösterir. Satınalma kutusu modülü, derecelendirmeler hizmetinden her bir ürünün derecelendirmelerini alır.
- **Ürün Fiyatı** – bu modül ürünün fiyatını gösterir. Fiyat, üzeri çizili fiyatları ve iskontoları içerir.
- **Ürün açıklaması** – bu modül ürünün açıklamasını gösterir.
- **Ürün konfigüre et** – bu modül ürünün boyut, stil ve boyutlarını gösterir. Boyut seçiciler dikey olarak yığılmış ya da yan yana görüntülenebilir. Bir ürün çeşidi seçildiğinde, satınalma kutusundaki diğer Özellikler (örneğin, ürün açıklaması ve görüntüler) değişken bilgilerini yansıtacak şekilde güncelleştirilir.
- **Ürün miktarı** – bu modül ürünün miktarını konfigüre etmek için kullanılır. Ayar, sepete eklenebilen bir ürün veya çeşit miktarını sınırlandırır.
- **Alışveriş sepetine ekle** – Bu modül, "Sepete Ekle" eylemi gerçekleştirmek için kullanılır. Alışveriş sepetine yalnızca bir ürün veya çeşit eklenebilir. Başka bir deyişle, bir ana ürün alışveriş sepetine eklenemez. Modül, Site yazarının ayarlayabileceği bir **Sepete git** özelliğine sahip olabilir. Bu özellik **doğru** olarak ayarlandığında, Kullanıcı her "Sepete Ekle" eylemine her tetiklenişinde sepet sayfasına alınır. **Yanlış** olarak ayarlandığında, maddeler alışveriş sepetine eklendikten sonra müşteri ürün ayrıntıları sayfasında gözatmaya devam edebilir.
- **İstek listesine Ekle** – Bu modül, müşterinin istek listesine madde eklemek için kullanılır. İstek listesine yalnızca bir ürün veya çeşit eklenebilir. Ek olarak, müşteri bu sitede oturum açmış olmalıdır. Modül, bu koşulların her ikisi de sağlandığından emin olmak için hata işleme mantığı içerir.
- **Mağazada bul** – bu modül, "çevrimiçi satın alma, mağaza içinde çekme" akışını tetikler.
- **Mağazada Seç** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Varsayılan olarak bu modül, müşterinin bulunduğu yerin 50 mil yarıçapı dahilinde olan depoları gösterir. Ancak, arama yarıçapı modülde özelleştirilebilir. Her mağaza için, stok denetimi işlevi açıksa ve uygun stokta ya da stokta bulunmayan iletiler gösterildiğinde stok denetimi yapılır.
- **Bing Haritalarla mağaza araması** - Mağazadan al modülü içindeki bu modül kullanılabilir. Müşterilerimiz, bir konum girerek mağaza arayabilir. Bing Haritalar coğrafi kodlamaya sahip uygulama programlama arabirimi (API) belirtilen konumu Enlem ve Boylam dönüştürmek için kullanılır. Bu modül kullanılırsa, yalnızca müşterinin bulunduğu yerin yakınında olan mağazalar görüntülenir ve müşteri farklı bir konumu aramaz.
- **İçerik zengin bloğu** – bu modül, satın al kutusunda, "sipariş sorunları için 1-800-FABRIKAM" veya "$100 üzerinde ücretsiz sevkiyat" gibi, Site yazarının veya satıcı tarafından yükseltmek istediğini belirten bir ileti gösterebilir. İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır.

## <a name="buy-box-module-settings"></a>Satın alma kutusu modülü ayarları

Satın alma kutusu modüllerinin konfigüre edilebilecek üç ayarı vardır:

- **Maksimum miktar** - Alışveriş sepetine eklenebilecek maksimum madde sayısı. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir. Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir. Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.
- **Stok tamponu** – stok gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir. Bu nedenle, stok için bir arabellek tanımlanabilir. Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir. Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.

## <a name="retail-server-interaction"></a>Perakende sunucu etkileşimi

Satınalma kutusu modülü, ürün bilgilerini Retail Server API'leri kullanarak alır. Ürün Ayrıntıları sayfasındaki ürün kimliği tüm bilgileri almak için kullanılır.

## <a name="add-a-buy-box-module-to-a-page"></a>Sayfaya satınalma kutusu modülü ekleme

Bir yeni sayfaya satın alma kutusu modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Satınalma kutusu parçası** olarak adlandırılan bir parça oluşturun ve buna satınalma kutusu birimi ekleyin.
1. Ortam Galerisi modülünü, satın alma kutusu modülündeki **ortam** yuvasına ekleyin.
1. Satın alma kutusu modülünün **içerik** yuvasında aşağıdaki modülleri ekleyin: ürün başlığı, ürün değerlendirmesi, ürün fiyatı, ürün açıklaması, ürün yapılandırma, alışveriş sepetine ekle, istek listesine ekle ve depoda bul. İstenen düzene ulaşmak için **içerik** yuvasındaki modülleri yeniden düzenleyebilirsiniz.
1. Mağazada bul modülünü belirleyin. Bu modülün içindeki yuvada, depo modülünde bir çekme ekleyin.
1. Mağazadan al modülü içindeki yuvada Bing Haritalarla mağazada ara modülü ekleyin.
1. Sayfayı giriş yapın ve yayımlayın.
1. Ürün Ayrıntıları sayfası için bir şablon oluşturun ve bunu **PDP şablonu** olarak adlandırın.
1. Varsayılan sayfa ekleyin.
1. Varsayılan sayfanın **ana** yuvasına bir satın alma parçası ekleyin.
1. Şablonu kaydedin, giriş yapın ve yayımlayın.
1. **PDF sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir satın alma parçası ekleyin.
1. Sayfayı kaydet ve önizleyin. **?productid=&lt;Product ID&gt;** sorgu dizesi parametresini önizleme sayfasının URL 'sine ekleyin. Bu şekilde, ürün bağlamı Önizleme sayfasını yüklemek ve oluşturmak için kullanılır.
1. Sayfayı giriş yapın ve yayımlayın. Ürün Ayrıntıları sayfasında bir satınalma kutusu görünmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
