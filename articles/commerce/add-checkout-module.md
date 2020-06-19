---
title: Ödeme modülü
description: Bu konuda, bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak açıklanır.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411236"
---
# <a name="checkout-module"></a>Ödeme modülü


[!include [banner](includes/banner.md)]

Bu konuda, bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak açıklanır.

## <a name="overview"></a>Genel Bakış

Ödeme modülü, sipariş oluşturmak için gerekli olan tüm modülleri barındıran özel bir konteynerdir. Müşterinin satın alma yapmak üzere ilgili tüm bilgileri girmek için kullandığı adım adım bir akış sunar. Sevkiyat adresi, sevkiyat yöntemi ve fatura bilgilerini yakalar. Ayrıca bir sipariş özeti ve bir müşteri siparişiyle ilgili başka bilgiler de sağlar.

Ödeme modülü, verileri sepet koduna göre işler. Bu sepet kodu tarayıcı tanımlama bilgisi olarak kaydedilir. Sipariş edilen maddeler, toplam tutar ve iskontolar gibi ödeme modülündeki bilgileri oluşturmak için bir sepet kodu gereklidir. 

Aşağıdaki resimde ödeme sayfasında kullanılan bir Fabrikam ödeme modülü örneği gösterilmektedir.

![Ödeme modülü örneği](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Ödeme modülü özellikleri

Kullanıma alma modülü bir sipariş Özeti gösterir ve sipariş yerleştirilmesi için işlevsellik sağlar. Bir siparişin yerleştirilmeleri için gerekli tüm müşteri bilgilerini toplamak üzere, kullanıma alma modülüne ek modüller eklenmesi gerekir. Bu nedenle, perakendeciler, kullanıma alma akışına özel modüller ekleme veya bunların gereksinimlerine göre modülleri hariç tutma esnekliği taşır.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Ödeme modülünde kullanılabilen modüller

- **Sevkiyat adresi** – bu modül, müşteriye bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir. Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir. Müşteri daha sonra bu adresler arasından seçim yapabilir. Müşteri Ayrıca yeni bir adres ekleyebilir. Sevkiyat adresi, Sevkiyat gerektiren siparişteki tüm maddeler için kullanılır. Özel satır maddeleri için özelleştirilemez. Sevkiyat Adresi formatları her ülke veya bölge için tanımlanır ve ülkeye/bölgeye özel kurallar bu modül tarafından zorlanır. Bu modül adres doğrulaması sağlamasa da, adres doğrulama Özelliştirme yoluyla gerçekleştirilebilir. Siparişte yalnızca mağazada çekilecek maddeler varsa, bu modül otomatik olarak gizlenir.

    Aşağıdaki resimde ödeme sayfasında kullanılan bir teslimat adresi modülü örneği gösterilmektedir.

    ![Teslimat Adresi modülü örneği](./media/ecommerce-shippingaddress.PNG)

- **Teslimat seçenekleri** – bu modül bir müşteriye sipariş için teslimat seçeneği seçmesini sağlar. Teslimat seçenekleri sevkiyat adresine göre yapılır. Sevkiyat Adresi değiştirilirse, teslimat seçenekleri tekrar alınmalıdır. Siparişte yalnızca mağazada çekilecek maddeler varsa, bu modül otomatik olarak gizlenir.

    Aşağıdaki resimde ödeme sayfasında kullanılan bir teslimat seçenekleri modülü örneği gösterilmektedir.

    ![Teslim seçenekleri modülü örneği](./media/ecommerce-deliveryoptions.PNG)

- **Ödeme bölümü konteyneri** – bu modül, ödeme akışında bir bölüm oluşturmak üzere birden fazla modül koyacağınız bir konteynerdir. Örneğin, bu konteynerdeki ödemeyle ilgili tüm modülleri tek bir bölüm olarak görünmelerini sağlamak için yerleştirebilirsiniz. Bu modül yalnızca akışın düzenini etkiler.
- **Hediye kartı** – bu modül, bir hediye kartı kullanarak müşteriye sipariş ödemesine olanak tanır. Yalnızca Microsoft Dynamics 365 Commerce hediye kartlarını destekler. Bir siparişe bir veya daha fazla hediye kartı uygulanabilir. Hediye kartının bakiyesi sepetteki tutarı kapsamıyorsa, hediye kartı başka bir ödeme yöntemiyle birleştirilebilir. Hediye kartları ancak müşteri oturum açtığında kullanılabilir.
- **Bağlılık programı puanları** – Bu modül, bağlılık programı puanları kullanarak bir müşteriye sipariş ödemesine olanak tanır. Mevcut puan ve süresi dolan noktaların özetini verir ve müşterinin kullanılacak puan sayısını seçmesini sağlar. Müşteri oturum açmamış veya bir bağlılık programı üyesi değilse veya alışveriş sepetindeki toplam tutar 0 (sıfır) ise, bu modül otomatik olarak gizlenir.
- **Ödeme** – bu modül, bir kredi kartı kullanarak müşteriye sipariş ödemesine olanak tanır. Sepetteki toplam miktar bağlılık puanları veya hediye kartı tarafından kapsanıyorsa ya da 0 (sıfır) ise bu modül otomatik olarak gizlenir. Bu modül için kredi kartı tümleştirmesi, Adyen ödeme Bağlayıcısı tarafından sağlanır. Bu bağlayıcının nasıl kullanılacağı hakkında daha fazla bilgi için, bkz: [Adyen için Dynamics 365 Connector](dev-itpro/adyen-connector.md).
- **Fatura adresi** – bu modül müşterinin faturalama bilgileri sağlamasına olanak tanır. Bu bilgiler, Adyen tarafından kredi kartı bilgileriyle birlikte işlenir. Bu modül, müşterilerinin sevkiyat adresi olarak kendi faturalama adreslerini kullanmasına olanak tanıyan bir seçenek içerir.

    Aşağıdaki resimde, kullanıma alma sayfasında hediye kartı, bağlılık programı puanları, ödeme ve faturalama adresi modülleri gösterilmektedir.

    ![Hediye kartı, bağlılık programı puanları, ödeme ve faturalama adres modülleri örneği](./media/ecommerce-payments.PNG)

- **İlgili kişi bilgileri** – bu modül müşterinin bir sipariş için iletişim bilgilerini (e-posta adresi) eklemesine veya değiştirmesine olanak tanır.

- **Metin bloku** – bu modül, içerik yönetimi sistemi (CMS) tarafından yönlendirilen tüm iletileri içerir. Örneğin, "Siparişiniz ile ilgili sorunlar için 1-800-Fabrikam ile bağlantı kurun" iletisini içeren bir ileti bulunabilir. 

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Sevkiyat adresi ve sevkiyat yöntemi gibi, ödeme bilgilerinin çoğu sepette depolanır ve siparişin bir parçası olarak işlenir. Tek özel durum kredi kartı bilgisi içindir. Bu bilgiler, adyen ödeme bağlayıcısı kullanılarak doğrudan işlenir. Ödeme yetkilendirildi, ancak ücretlendirilmemiştir.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Bir sayfaya ödeme modülü ekleyin ve gerekli özellikleri ayarlayın

Bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Sayfa Parçaları**'na gidin ve yeni parçası oluşturmak için **Yeni**'yi seçin.
1. **Yeni Sayfa Parçası** iletişim kutusunda, **Ödeme** modülünü seçin.
1. **Sayfa parçası adı** altında, **Ödeme parça** için bir ad girin ve **Tamam** 'ı seçin.
1. **Ödeme modülü** yuvasını seçin.
1. Sağdaki Özellikler bölmesinde, Kurşun Kalem sembolünü seçin, alana başlık metnini girin ve onay işareti simgesini seçin.
1. **Ödeme bilgileri** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül ekle** iletişim kutusunda **Sevkiyat Adresi**, **teslim seçenekleri**, **kullanıma alma bölümü konteyneri** ve **ilgili kişi bilgileri** modüllerini seçin ve **Tamam** seçin.
1. **Ödeme bölümü konteyneri** modülü için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Hediye kartı**, **Sadakat** ve **Ödeme** modüller'i seçin, ve **Tamam**'ı seçin. Bu şekilde, tüm ödeme yöntemlerinin bir bölümde birlikte göründüğünden emin olabilirsiniz.
1. **Kaydet**'i seçin ve ardından parçayı önizlemek için **Önizleme**'yi seçin. Bazı modüller sepet bağlamına sahip değildir ve önizlemede işlenemeyebilir.
1. Parçayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.
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
