---
title: Satın alma kutusu modülü
description: Bu makale satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5167aac784bb3ab6a63033590178c2eead627b96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863565"
---
# <a name="buy-box-module"></a>Satın alma kutusu modülü

[!include [banner](includes/banner.md)]

Bu makale satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

Terim *satın alma kutusu* genellikle, ürün satın alma işlemi yapmak için gereken en önemli bilgileri barındıran, ürün Ayrıntıları sayfasının (PDP) "manşet" alanını belirtir. (Sayfanın ilk yüklendiği sırada "manşet" olan alan görünür, böylece görmek için kullanıcıların aşağı kaydırılması gerekmez.)

Satın alma kutusu modülü, Ürün Ayrıntıları sayfasının satın alma kutusu alanında gösterilen tüm modülleri barındırmak için kullanılan özel bir konteynerdir.

Ürün Ayrıntıları sayfasının URL'SI ürün kodunu içerir. Bir satınalma kutusu modülünü işlemek için gereken tüm bilgiler bu ürün kimliğinden türetilir. Bir ürün kodu sağlanmazsa, satın alma kutusu modülü sayfada doğru olarak işlenmez. Bu nedenle, satın alma kutusu modülü yalnızca ürün içeriği olan sayfalarda kullanılabilir. Ürün bağlamı bulunmayan bir sayfada (örneğin, giriş sayfası veya pazarlama sayfası) kullanmak için, ek özelleştirmeler yapmanız gerekir.

Aşağıdaki resimde ürün ayrıntıları sayfasında kullanılan bir satın alma kutusu modülü örneği gösterilmektedir.

![Satın alma kutusu modülü örneği.](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Satın alma kutusu modülü özelliklerini ve yuvaları 

Ürün Ayrıntıları sayfasında, satınalma kutusu iki bölgeye ayrılmıştır: soldaki ortam bölgesi ve sağda bulunan bir içerik bölgesi. Varsayılan olarak, ortam bölgesi sütunu genişliğinin içerik bölgesi sütunu genişliğine oranı 2:1'dir. Mobil cihazlarda iki bölge yığılır, böylece diğer bölgenin altında bir alan görünür. Temalar, sütun genişlikleri ve yığınlama derecesini özelleştirmek için kullanılabilir.

Satınalma kutusu modülü bir ürünün başlığını, açıklamasını, fiyatını ve derecelendirmelerini işler. Ayrıca müşteriler boyut, stil ve renk gibi farklı ürün özniteliklerine sahip ürün çeşitlerini da seçmenizi sağlar. Bir ürün çeşidi seçildiğinde, satınalma kutusundaki diğer Özellikler (örneğin, ürün açıklaması ve görüntüler) değişken bilgilerini yansıtacak şekilde güncelleştirilir. 

Müşterilerin satın alınacak maddelerin miktarını belirtebilmesi için bir miktar seçici sağlanır. Satın alınabilecek maksimum miktar, Tesis ayarlarında tanımlanabilir.

Müşteriler, satınalma kutusunda, alışveriş sepetine ürün ekleme, istek listesine ürün ekleme ve malzeme çekme yerleşimi seçme gibi eylemleri gerçekleştirebilirler. Bu eylemler bir ürün veya ürün çeşidi için gerçekleştirilebilir. Bir ürünü bir istek listesine listesine eklemek için müşterinin oturum açmış olması gerekir.

Temalar, satın alma kutusu ürün özelliklerini ve eylem denetimlerini kaldırmak veya değiştirmek için kullanılabilir. 

## <a name="module-properties"></a>Modül özellikleri

- **Başlık etiketi** – bu özellik, ürün başlığının başlık etiketini tanımlar. Satın al kutusu sayfanın en üstünde ise, erişilebilirlik standartlarını karşılamak için bu özelliğin **H1** olarak ayarlanması gerekir. 

- **"Benzer görünümleri araştır" önerilerini etkinleştir**: Bu özellik, satın alma kutusunun şu anda görüntülenmekte olan öğeye benzeyen ürünlerin bağlantılarını göstermesini sağlar. Bu özellik Commerce 10.0.13 sürümü ve sonrasında bulunur.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Satınalma kutusu modülünde kullanılabilen modüller

- **Ortam Galerisi** – bu modül, ürün ayrıntıları sayfasındaki bir ürünün görüntülerini sergilemesinde kullanılır. Bu modülle ilgili daha fazla bilgi için bkz. [Ortam galerisi modülü](media-gallery-module.md).
- **Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar. Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçici modülü](store-selector.md).
- **Sosyal içerik paylaşım**: Bu modül, sosyal medya platformlarında ürün bilgilerini kullanıcıların paylaşmasına olanak sağlamak için satın alma kutusuna eklenebilir. Daha fazla bilgi için bkz. [Sosyal içerik paylaşım modülü](social-share-module.md).

## <a name="buy-box-module-settings"></a>Satın alma kutusu modülü ayarları

Aşağıdaki satın alma kutusu modülü ayarları **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek ayarlara sahiptir:

- **Sepet miktar sınırı** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok** - Stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).
- **Sepete ürün ekle** – **Sepete ürün ekle** ayarlarının nasıl uygulanacağı hakkında bilgi için [Sepete ürün ekleme](add-cart-settings.md) konusuna bakın.

## <a name="buy-box-module-definition-extensions-in-the-adventure-works-theme"></a>Adventure Works temasında satın alma kutusu modülü tanım uzantıları

Adventure Works temasının sağladığı satın alma kutusu modülü, bir ürün özellikleri modülünün, bir PDP satı alma kutusundaki akordeyon modülünde uygulanmasını destekleyen bir modül tanımı uzantısına sahiptir. Bir PDP satın alma kutusundaki ürün özelliklerini sergilemek için, satın alma kutusu yuvasındaki akordeyon modülü yuvasına bir ürün özelliği modülü ekleyin.


> [!IMPORTANT]
> Adventure Works teması Dynamics 365 Commerce Sürüm 10.0.20 itibarıyla kullanılabilir.


## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Satın alma kutusu modülü, ürün bilgilerini Commerce Scale Unit uygulama programlama arayüzleri (API'ler) kullanarak alır. Ürün Ayrıntıları sayfasındaki ürün kimliği tüm bilgileri almak için kullanılır.

## <a name="add-a-buy-box-module-to-a-page"></a>Sayfaya satınalma kutusu modülü ekleme

Bir yeni sayfaya satın alma kutusu modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda, **Satın alma kutusu** modülünü seçin.
1. **Parça adı** altında, **Satın alma kutusu parçası** için bir ad girin ve **Tamam**'ı seçin.
1. Satın alma kutusu modülünün **Medya Galerisi** alanında, üç nokta (**...**) düğmesini ve ardından **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Medya galerisi** modülünü seçin ve **Tamam**'ı seçin.
1. Satın alma kutusu modülünün **Mağaza seçici** alanında, üç nokta (**...**) düğmesini ve ardından **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusundaki **Şablon adı** bölümünde, **PDP şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Gövde** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Varsayılan Sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. Varsayılan sayfanın **Ana** yuvasında, üç nokta düğmesini (**...**) ve sonra **Parça ekle**'yi seçin.
1. **Parça seçin** iletişim kutusunda daha önce oluşturduğunuz **Satın alma kutusu parçası** öğesini ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusundaki **Sayfa adı** bölümünde, bir **PDP sayfası** girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, **PDP şablonu**'nu seçin ve ardından **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin.
1. Yeni sayfanın **Ana** yuvasında, üç nokta düğmesini (**...**) ve sonra **Parça ekle**'yi seçin.
1. **Parça seçin** iletişim kutusunda daha önce oluşturduğunuz **Satın alma kutusu parçası** öğesini ve sonra **Tamam**'ı seçin.
1. Sayfayı kaydet ve önizleyin. **?productid=&lt;Product ID&gt;** sorgu dizesi parametresini önizleme sayfasının URL 'sine ekleyin. Bu şekilde, ürün bağlamı Önizleme sayfasını yüklemek ve oluşturmak için kullanılır.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin. Ürün Ayrıntıları sayfasında bir satınalma kutusu görünmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Mağaza seçicisi modülü](store-selector.md)

[Ortam galerisi modülü](media-gallery-module.md)

[Kapsayıcı modülü](add-container-module.md)

[Sepet modülü](add-cart-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)

[Sosyal paylaşım modülü](social-share-module.md)

[Sepete ürün ekle ayarları](add-cart-settings.md)

[Perakende kanalları için stok kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md)

[SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
