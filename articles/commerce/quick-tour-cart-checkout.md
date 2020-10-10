---
title: Sepet ve ödeme sayfalarına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta sepet ve ödeme sayfalarına genel bakış sağlar.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: e932be31a301ef5aacb68fa4e710d8a9137b7263
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817790"
---
# <a name="cart-and-checkout-pages-overview"></a>Sepet ve ödeme sayfalarına genel bakış

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta sepet ve ödeme sayfalarına genel bakış sağlar.

## <a name="overview"></a>Genel Bakış

Bir e-ticaret web sitesinin alışveriş sayfası bir müşterinin sepete eklediği tüm maddeleri gösterir. Alışveriş sepeti sayfası, sepet modülü kullanılarak oluşturulur. Bir sepet modülü, sepetteki öğelerin gösterimi için gerekli olan tüm modülleri barındırmak için kullanılan bir konteynerdir. Sepet modülü ayrıca sipariş özetini ve müşteri emrine uygulanan promosyon kodlarını göstermek için diğer modülleri de kullanabilir.

Bir e-ticaret Web sitesinin kullanıma alma sayfası, müşterinin sipariş vermek için gereken tüm bilgileri girmesi için takip eden adım adım bir akış sunar. Bir ödeme modülü sevkiyat adresini, Sevkiyat yöntemlerini, fatura bilgilerini, sipariş özetini ve bir müşteri emriyle ilişkili diğer bilgileri ele alan modüller içerebilir.

## <a name="cart-page"></a>Sepet sayfası

Sepet sayfası, alışveriş çantası olarak hizmet görür ve sepete eklenen tüm maddeleri içerir.

Aşağıdaki çizimde, modül kitaplığı ve "Fabrikam" teması kullanılarak oluşturulmuş bir sepet sayfası örneği gösterilmektedir.

![Sepet sayfası örneği](./media/cart2.PNG)

Sepet sayfasının ana bölümü bir müşterinin sepete eklediği tüm maddeleri gösterir. İlgili tüm indirimler göster. Bu iskontolar karmaşık iskontolar içerir. Örneğin, "3 öğe satın alın ve %10 indirim" veya "%10 indirim için şişe ve sırt çantası satın alın" gibi örnekler verilebilir. Sipariş Özeti modülü iskontolar, Sevkiyat, vergiler vb. sonrasında ödenmesi gereken tutarı gösterir. Ayrıca, müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlayan bir promosyon kodu modülü de vardır.

Müşteri anonim olarak veya oturum açmış bir kullanıcı olarak alışveriş yapabilir. Bir müşteri oturum açmışsa, sepetteki öğeler oturumlar arasında korunur. Bu şekilde, müşteri birden çok cihazda alışveriş yapmaya devam edebilir.

Müşteri sepetten itibaren teslim almayı devam edebilir. Müşteri, konuk kullanıcı veya oturum açmış kullanıcı olarak kullanıma almayı başlatabilir.

Bir sepet sayfasının nasıl yazılacağıyla ilgili bilgi için, bkz. [Sayfaya sepet modülü ekleme](add-cart-module.md).

## <a name="checkout-page"></a>Kullanıma alma sayfası

Kullanıma alma sayfası, müşterinin bir siparişi yerleştirmek için gereken bilgileri girebildiği yerdir.

Aşağıdaki çizimde, modül kitaplığı kullanılarak oluşturulmuş bir ödeme sayfası örneği gösterilmektedir.

![Ödeme sayfası örneği](./media/Checkout.PNG)

Kullanıma alma sayfasının ana gövdesi tüm sipariş bilgilerinin toplandığı yerdir. Bu bilgiler sevkiyat adresi, teslimat seçenekleri ve ödeme bilgilerini içerir. Bilgilerin işlenmesi için belirli bir sırada girilmesi gerektiğinden, teslim alma sırasında adım adım bir akış vardır. Örneğin, Sevkiyat maliyetleri hesaplanmadan ödeme yetkilendirilebileceği şekilde, sevkiyat adresi girilmelidir.

### <a name="shipping-address"></a>Sevkiyat adresi

Maddelerin sevk edilmesi gerekiyorsa sevkiyat adresi gereklidir. Her bir yerel ayarın sevkiyat adreslerinin biçimi Dynamics 365 Commerce'de yapılandırılabilir. Örneğin, maddeler Amerika Birleşik Devletleri sevk edilecekse, sevkiyat adresi bir sokak adresi, il ve Posta Kodu içermelidir. Bazı temel giriş doğrulamaları, alfasayısal karakterler, maksimum uzunluk ve sayıların doğrulaması gibi adres alanlarının sevkiyatı için yapılır. Adresin geçerliliği doğrulanmasa da, bu doğrulama özelleştirilmiş üçüncü taraf hizmetler kullanılarak yapılabilir.

Sevkiyat adresi, "sevk et" seçeneğinin işaretli olduğu sepetteki tüm maddelere uygulanır. Çevrimiçi modül kitaplığı içinde sağlanan kullanıma alma akışını kullanırsanız, bireysel alışveriş maddeleri farklı adreslere sevk edilebilir. Bu yeteneğe gereksinim duyarsanız, kullanıma alma modülleri özelleştirilmesiyle gerçekleştirilebilir.

Sevkiyat Adresi sağlandığında, Dynamics 365 Commerce çevrimiçi mağazadan kullanılabilen Sevkiyat Yöntemleri gösterilir. Sevkiyat Yöntemleri ve destekledikleri adresler Commerce'de konfigüre edilebilir.

### <a name="payment"></a>Ödeme

Ödeme akışındaki sonraki adım ödemedir. E-ticaret'te kredi kartları, hediye kartları ve bağlılık programı puanları gibi siparişler yerleştirmek için çoklu ödeme yöntemleri kullanılabilir. Bu ödeme yöntemlerinin bir birleşimi de kullanılabilir. Kullanılan ödeme yöntemlerine bağlı olarak ek bilgiler gerekebilir. Örneğin, kredi kartı ödemesi bir faturalama adresi gerektirir. Kredi kartı ödemeleri, Adyen ödeme bağlayıcısı kullanılarak işlenir.

#### <a name="loyalty-points"></a>Bağlılık programı puanları

Sağlama akışı sırasında, bir bağlılık programına üye olan ve tahakkuk eden bağlılık programı puanları olan bir müşteri bir sipariş için bu bağlılık programı puanlarını kullanmaya çalışabilir. Bağlılık programı puanları modülü yalnızca müşterinin varolan bağlılık programı üyeliği varsa görüntülenir. Üye olmayanlar ve Konuk kullanıcılar için bu modül gizlenir.

#### <a name="gift-cards"></a>Hediye kartları

Çevrimiçi modül kitaplığı, bir sipariş için dahili hediye kartlarından daha fazla kullanılabilir olmasını sağlar. Dahili bir hediye kartı uygulamak için, müşterinin oturum açmış olması gerekir. Ek güvenlik için, dahili hediye kartları için bir kişisel kimlik numarası (PIN) kullanarak akışı özelleştirmenizi öneririz.

### <a name="signed-in-and-guest-users"></a>Oturum açmış ve konuk kullanıcılar

Müşteri, konuk kullanıcı veya oturum açmış kullanıcı olarak kullanıma almayı tamamlayabilir. Müşteri oturum açtığında, kaydedilen sevkiyat adresleri ve kaydedilmiş kredi kartı ayrıntıları gibi hesap bilgileri otomatik olarak alınır.

### <a name="order-summary"></a>Sipariş özeti

Ödeme, müşteriye siparişi vermeden önce bir sipariş doğrulayabilmesi için sepetteki satır maddelerinin bir özetini gösterir. Satır maddeleri, kullanıma alma akışı sırasında düzenlenemez. Ancak, kullanıcının geri gitmek ve satır öğelerini düzenlemek istediği durumda alışveriş sepetine bir bağlantı sağlanır.

Müşteri sevkiyat ve faturalama bilgilerini girdikten sonra, bağlılık programı noktaları, hediye kartları ve diğer ödemeler uygulandıktan sonra ödenmesi gereken tutarı yansıtır.

### <a name="order-confirmation-and-email"></a>Satış onayı ve e-postası

Müşteri bir sipariş yerleştirdiğinde, bir onay numarası sağlanır. Bu aşamada, ödeme yetkilendirilemez, ancak ücretlendirilmemiştir. Ödeme, yalnızca sipariş yerine getirilmişse (yani, sevk edildiğinde veya çekildiğinde) ücretlendirilecektir.

Bir sipariş oluşturulduktan sonra, müşteriye bir sipariş teyidi e-postası gönderilir.

Bir ödeme sayfasının nasıl yazılacağıyla ilgili daha fazla bilgi için, bkz. [Sayfaya ödeme modülü ekleme](add-checkout-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Giriş sayfasına genel bakış](quick-tour-home-page.md)

[Ürün ayrıntıları sayfalarına genel bakış](quick-tour-pdp.md)

[Hesap yönetimi sayfalarına genel bakış](quick-tour-account-management.md)
