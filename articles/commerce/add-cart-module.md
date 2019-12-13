---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696773"
---
# <a name="cart-module"></a>Sepet modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir sepet modülü, sepetteki öğelerin gösterimi için gerekli olan tüm modülleri barındırmak için kullanılan bir kapsayıcıdır. Örneğin, alışveriş sepetine, sipariş özetine ve promosyon kodlarına eklenen tüm maddeleri içerir.

Sepet modülü, verileri sepet koduna göre işler. Sepet kodu, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisidir.

## <a name="cart-module-properties-and-slots"></a>Sepet modülü özelliklerini ve yuvaları

Konteyner olarak, sepet modülü başlık ve genişlik gibi bazı temel özellikleri denetler. Başlık genellikle **alışveriş çantası**, **sepetiniz**veya **sepetinizdeki maddeler** gibi bir metindir. Genişlik ayarı, konteynerdeki modüllerin o konteynerin içine sığması gerekip gerekmediğini veya ekranı doldurup dolduramayacağını belirler.

Sepet sayfası birden çok bölgeye ayrılmıştır: sepet kalemlerine, sipariş özetine ve kullanıma almayı ve "mağazada bul" işlevselliğini. Her bölge, sepet modülündeki bir yuvaya eşlenir ve her yuva, önceden tanımlanmış modüller kümesini kabul eder.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Sepet modülünde kullanılabilen modüller

- **Alışveriş sepetinin maddeleri** – bu modül, alışveriş sepetine eklenen her maddenin bir özetini gösterir. Bilgiler ürün başlığı, Seçili boyutlar, Fiyat, miktar ve iskontoları içerir. Bu modül ayrıca "Sepetten kaldır" ve "istek listesine ekle" gibi eylemleri destekler. Her satır maddesi için maddeyi sevk etme veya mağazadan çekme ile ilgili bir seçenek vardır. Bu seçenek, mağazadan al modülünde ayrı olarak konfigüre edilmelidir.
- **Sipariş Özeti** – bu modül bir sipariş Özeti gösterir. Bu bilgiler, alt toplam, Sevkiyat, vergiler ve tasarruf olanakları içerir. Bu modül için bir başlık konfigüre edilebilir.
- **Promosyon kodu** – bu modül müşterinin promosyon kodları kullanmaya olanak tanır. Promosyon kodu uygulanabilir veya çıkarılabilir.
- **Ödeme** – bu modül kullanıma alma eylemini başlatır ve kullanıcıyı kullanıma alma sayfasına yönlendirir. Bu modül için üç bağlantı konfigüre edilmelidir:

    - **Ödeme** – Bu bağlantı, önceden oturum açmadıklarında müşterileri oturum açmaya zorlar.
    - **Misafir ödemesi** – Bu bağlantı, anonim müşterilerin sipariş eklemesine olanak verir. Yalnızca müşteriler oturum açmadığında gösterilir.
    - **Alışverişe dön** – Bu bağlantı, müşteriye giriş sayfasına veya başka bir sayfaya gidip alışveriş yapmaya devam edebilmek için bir sayfa sağlar.

- **İçerik zengin bloğu** – bu modül sepet modülündeki özel iletileri destekler. İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır. "Sipariş sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.
- **Mağazada Seç** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Varsayılan olarak bu modül, müşterinin bulunduğu yerin 50 mil yarıçapı dahilinde olan depoları gösterir. Ancak, arama yarıçapı modülde özelleştirilebilir. Her mağaza için, stok denetimi işlevi açıksa ve uygun stokta ya da stokta bulunmayan iletiler gösterildiğinde stok denetimi yapılır.
- **Bing Haritalarla mağaza araması** - Mağazadan al modülü içindeki bu modül kullanılabilir. Müşterilerimiz, bir konum girerek mağaza arayabilir. Bing Haritalar coğrafi kodlamaya sahip uygulama programlama arabirimi (API) müşterinin girdiği konumu Enlem ve Boylam dönüştürmek için kullanılır. Bu modül kullanılmazsa, yalnızca müşterinin bulunduğu yerin yakınında olan mağazalar görüntülenir ve müşteri farklı bir konumu aramaz.

## <a name="cart-module-settings"></a>Sepet modülü ayarları

Sepet modüllerinin konfigüre edilebilecek üç ayarı vardır:

- **Maksimum miktar** - Alışveriş sepetine eklenebilecek maksimum madde sayısı. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir. Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir. Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.
- **Stok tamponu** – stok gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir. Bu nedenle, stok için bir arabellek tanımlanabilir. Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir. Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.

## <a name="retail-server-interaction"></a>Perakende sunucu etkileşimi

Sepet modülü, ürün bilgilerini Retail Server API'leri kullanarak alır. Retail Server'daki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.

## <a name="add-a-cart-module-to-a-page"></a>Sayfaya sepet modülü ekleme

Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Sepet parçası** olarak adlandırılan bir parça oluşturun ve buna sepet birimi ekleyin.
1. Sepet modülünün **sepet satırı öğeleri** yuvasında bir alışveriş kalemi satırı öğeleri modülü ekleyin.
1. **Sipariş özeti** yuvasında bir sipariş Özeti modülü ekleyin.
1. **Promosyon kodu** yuvasına bir promosyon kodu modülü ekleyin.
1. **Ödeme** yuvasında bir kullanıma alma modülü ekleyin.
1. **Mağazda bul** yuvasında, mağazadan al modülü ekleyin.
1. Mağazadan al modülü içinde **Mağazayı ara** yuvasını seçin ve Bing Haritalarla mağazada ara modülü ekleyin.
1. Parçayı giriş yapın ve yayımlayın.
1. **Sepet şablonu** adlı bir şablon oluşturun ve yeni oluşturduğunuz sepet parçasını ekleyin.
1. Şablonu kaydedin, giriş yapın ve yayımlayın.
1. Yeni şablonu kullanan bir sayfa oluşturun.
1. Sayfayı kaydet ve önizleyin.
1. Sayfayı giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
