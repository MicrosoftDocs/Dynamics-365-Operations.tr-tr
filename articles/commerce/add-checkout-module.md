---
title: Ödeme modülü
description: Bu konuda, bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak açıklanır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697095"
---
# <a name="checkout-module"></a>Ödeme modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak açıklanır.

## <a name="overview"></a>Genel Bakış

Ödeme modülü, sipariş oluşturmak için gerekli olan tüm modülleri barındıran özel bir konteynerdir. Bir ödeme modülü sevkiyat adresini, Sevkiyat yöntemlerini, fatura bilgilerini, sipariş özetini ve bir müşteri emriyle ilişkili diğer bilgileri ele alan modüller içerebilir. Müşterinin satın alma yapmak üzere ilgili tüm bilgileri girmek için kullandığı adım adım bir akış sunar.

Ödeme modülü, verileri sepet koduna göre işler. Bu sepet kodu tarayıcı tanımlama bilgisi olarak kaydedilir. Sipariş edilen maddeler, toplam tutar ve iskontolar gibi ödeme modülündeki bilgileri oluşturmak için bir sepet kodu gereklidir.

## <a name="checkout-module-properties"></a>Ödeme modülü özellikleri

Bir ödeme modülü bunun içinde bir dizi modül barındırır. Genişlik özelliği, ödeme modülündeki öğelerin genişliği için uygun olup olmayacağını belirtmenize veya ekranı doldurmasına olanak tanır.

Bir ödeme modülü, **Ödeme bilgileri** yuvası, **sipariş özeti** yuvası ve **sipariş ver** yuvası gibi birden çok yuvaya sahiptir. Her yuva, sayfadaki belirli bir düzende görünecek bir modül kümesini destekler. Örneğin, **Ödeme bilgileri** yuvası, sevkiyat adresi ve ödeme yöntemine ait modüller gibi, ödeme tetiklemesi için gerekli tüm modülleri içerir. **Sipariş özeti** yuvası sipariş özetini gösterir ve siparişi yerleştirme eylemini destekler. **Sipariş ver** yuvası sipariş yerleştirme eylemini de destekler. Sipariş ver modülleri, çeşitli platformlarda sipariş verme sürecini en iyi duruma getirmek için iki yuva içinde tanımlanabilir.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Ödeme modülünde kullanılabilen modüller

- **Sevkiyat adresi** – bu modül, müşteriye bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir. Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir. Müşteri daha sonra bu adresler arasından seçim yapabilir. Müşteri Ayrıca yeni bir adres ekleyebilir. Sevkiyat adresi, Sevkiyat gerektiren siparişteki tüm maddeler için kullanılır. Özel satır maddeleri için özelleştirilemez. Sevkiyat Adresi formatları her ülke veya bölge için tanımlanır ve ülkeye/bölgeye özel kurallar bu modül tarafından zorlanır. Bu modül adres doğrulaması sağlamasa da, adres doğrulama Özelliştirme yoluyla gerçekleştirilebilir. Siparişte yalnızca mağazada çekilecek maddeler varsa, bu modül otomatik olarak gizlenir.
- **Teslimat seçenekleri** – bu modül bir müşteriye sipariş için teslimat seçeneği seçmesini sağlar. Teslimat seçenekleri sevkiyat adresine göre yapılır. Sevkiyat Adresi değiştirilirse, teslimat seçenekleri tekrar alınmalıdır. Siparişte yalnızca mağazada çekilecek maddeler varsa, bu modül otomatik olarak gizlenir.
- **Ödeme bölümü konteyneri** – bu modül, ödeme akışında bir bölüm oluşturmak üzere birden fazla modül koyacağınız bir konteynerdir. Örneğin, bu konteynerdeki ödemeyle ilgili tüm modülleri tek bir bölüm olarak görünmelerini sağlamak için yerleştirebilirsiniz. Bu modül yalnızca akışın düzenini etkiler.
- **Hediye kartı** – bu modül, bir hediye kartı kullanarak müşteriye sipariş ödemesine olanak tanır. Yalnızca Microsoft Dynamics 365 Commerce hediye kartlarını destekler. Bir siparişe bir veya daha fazla hediye kartı uygulanabilir. Hediye kartının bakiyesi sepetteki tutarı kapsamıyorsa, hediye kartı başka bir ödeme yöntemiyle birleştirilebilir. Hediye kartları ancak müşteri oturum açtığında kullanılabilir.
- **Bağlılık programı puanları** – Bu modül, bağlılık programı puanları kullanarak bir müşteriye sipariş ödemesine olanak tanır. Mevcut puan ve süresi dolan noktaların özetini verir ve müşterinin kullanılacak puan sayısını seçmesini sağlar. Müşteri oturum açmamış veya bir bağlılık programı üyesi değilse veya alışveriş sepetindeki toplam tutar 0 (sıfır) ise, bu modül otomatik olarak gizlenir.
- **Kredi kartı** – bu modül, bir kredi kartı kullanarak müşteriye sipariş ödemesine olanak tanır. Sepetteki toplam miktar bağlılık puanları veya hediye kartı tarafından kapsanıyorsa ya da 0 (sıfır) ise bu modül otomatik olarak gizlenir. Kredi kartı tümleştirmesi, Adyen ödeme Bağlayıcısı tarafından sağlanır. Bu bağlayıcının nasıl kullanılacağı hakkında daha fazla bilgi için, bkz: [Adyen ödeme konnektörü](https://).
- **Fatura adresi** – bu modül müşterinin faturalama bilgileri sağlamasına olanak tanır. Bu bilgiler, Adyen tarafından kredi kartı bilgileriyle birlikte işlenir. Bu modül, müşterilerinin sevkiyat adresi olarak kendi faturalama adreslerini kullanmasına olanak tanıyan bir seçenek içerir.
- **İlgili kişi bilgileri** – bu modül müşterinin bir sipariş için iletişim bilgilerini (e-posta adresi) eklemesine veya değiştirmesine olanak tanır.
- **Sipariş ver** – bu modül müşterinin sipariş eklemesine olanak sağlar.
- **İçerik zengin bloğu** – bu modül, içerik yönetimi sistemi (CMS) tarafından yönlendirilen tüm iletileri içerir. Örneğin, "Siparişiniz ile ilgili sorunlar için, lütfen 1-800-FABRIKAM ile bağlantı kurun" iletisini içeren bir ileti bulunabilir. 
- **Sipariş Özeti** – bu modül bir siparişin maliyet dökümünü gösterir.
- **Sipariş satırı maddeleri** – bu modül bir siparişe dahil edilecek maddelerin özetini gösterir.

## <a name="retail-server-interaction"></a>Perakende sunucu etkileşimi

Sevkiyat adresi ve sevkiyat yöntemi gibi, ödeme bilgilerinin çoğu sepette depolanır ve siparişin bir parçası olarak işlenir. Tek özel durum kredi kartı bilgisi içindir. Bu bilgiler, adyen ödeme bağlayıcısı kullanılarak doğrudan işlenir. Ödeme yetkilendirildi, ancak ücretlendirilmemiştir.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Bir yeni sayfaya ödeme modülü ekleyin ve gerekli özellikleri ayarlayın

Bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Parça \> Yeni parça**ya gidin ve yeni parça **Ödeme parçası** olarak adlandırın.
1. Parçaya ödeme modülü ekleyin.
1. Ödeme modülüne başlık ekleyin.
1. **Ödeme bilgileri** yuvasında sevkiyat adresi, teslim seçenekleri, ödeme bölümü konteyneri ve ilgili kişi bilgi modülleri ekleyin. Şimdi, **Ödeme bilgileri** yuvasında dört bölüm olmalıdır.
1. Ödeme bölümü konteyner modülünde hediye kartı, bağlılık programı puanları ve kredi kartı modülleri ekleyin. Bu şekilde, tüm ödeme yöntemlerinin bir bölümde birlikte göründüğünden emin olabilirsiniz.
1. **Sipariş özeti** yuvasında sipariş özeti, sipariş yerleştirme ve içerik zengin blok modüller ekleyin.
1. İçerik zengin blok modülünde aşağıdaki metni ekleyin: **Siparişiniz hakkında sorular için 1-800-FABRIKAM ile bağlantı kurun.**
1. **Sipariş verin** yuvasında bir sipariş ver modülü ekleyin.
1. **Kaydet**'i seçin. Bir sepet bağlamına sahip olmadıkları için bazı modüller önizlemede işlenmeyebilir.
1. Parçayı giriş yapın ve yayımlayın.
1. Yeni ödeme parçasını kullanan bir şablon oluşturun.
1. Yeni şablon kullanan bir ödeme sayfası oluşturun.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
