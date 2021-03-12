---
title: Ödeme modülü
description: Bu konuda, bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak açıklanır.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb32b014ac35e33db28d3dee03b01dfa43f5d6a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980518"
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

| Özellik adı | Değerler | Tanım |
|----------------|--------|-------------|
| Ödeme başlığı | Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Ödeme modülü için başlık. |
| Sipariş özeti başlığı | Başlık metni | Modülün sipariş özeti bölümü için başlık. |
| Sepet satır maddeleri başlığı | Başlık metni | Ödeme modülünde gösterilen sepet satırı maddeleri için başlık. |
| Satır maddesinde sevkiyat masraflarını göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, satır maddeleri için geçerli olan sevkiyat giderleri sepet satırlarında gösterilir. Commerce Headquarters'da **Eşit dağıtım olmadan masraf başlığı** özelliği açıksa, sevkiyat masrafı satır düzeyinde değil, başlık düzeyinde uygulanır. Bu özellik, Commerce sürüm 10.0.13'te eklenmiştir. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Ödeme modülünde kullanılabilen modüller

- **Sevkiyat adresi** – Bu modül, müşteriye bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir. Bu modülle ilgili daha fazla bilgi için bkz. [Sevkiyat adresi modülü](ship-address-module.md).

    Aşağıdaki resimde ödeme sayfasında kullanılan bir teslimat adresi modülü örneği gösterilmektedir.

    ![Teslimat Adresi modülü örneği](./media/ecommerce-shippingaddress.PNG)

- **Teslimat seçenekleri** – Bu modül bir müşteriye sipariş için teslimat şekli seçme olanağı sağlar. Bu modülle ilgili daha fazla bilgi için bkz. [Teslimat seçenekleri modülü](delivery-options-module.md).

    Aşağıdaki resimde ödeme sayfasında kullanılan bir teslimat seçenekleri modülü örneği gösterilmektedir.
 
    ![Teslim seçenekleri modülü örneği](./media/ecommerce-deliveryoptions.PNG)

- **Ödeme bölümü konteyneri** – bu modül, ödeme akışında bir bölüm oluşturmak üzere birden fazla modül koyacağınız bir konteynerdir. Örneğin, bu konteynerdeki ödemeyle ilgili tüm modülleri tek bir bölüm olarak görünmelerini sağlamak için yerleştirebilirsiniz. Bu modül yalnızca akışın düzenini etkiler.

- **Hediye kartı** – bu modül, bir hediye kartı kullanarak müşteriye sipariş ödemesine olanak tanır. Bu modülle ilgili daha fazla bilgi için bkz. [Hediye kartı modülü](add-giftcard.md).

- **Bağlılık programı puanları** – Bu modül, bağlılık programı puanları kullanarak bir müşteriye sipariş ödemesine olanak tanır. Mevcut puan ve süresi dolan noktaların özetini verir ve müşterinin kullanılacak puan sayısını seçmesini sağlar. Müşteri oturum açmamış veya bir bağlılık programı üyesi değilse veya alışveriş sepetindeki toplam tutar 0 (sıfır) ise, bu modül otomatik olarak gizlenir.

- **Ödeme**: Bu modül, müşteriye bir kredi kartı veya banka kartı kullanarak sipariş ödemesi yapma olanağı tanır. Müşteriler, seçtikleri ödeme seçeneği için fatura adresi de sağlayabilir. Bu modülle ilgili daha fazla bilgi için bkz. [Ödeme modülü](payment-module.md).

    Aşağıdaki resimde, ödeme sayfasındaki hediye kartı, bağlılık programı puanları ve ödeme modülleri gösterilmektedir.

    ![Ödeme sayfasındaki hediye kartı, bağlılık programı puanları ve ödeme modüllerini gösteren örnek](./media/ecommerce-payments.PNG)

- **İlgili kişi bilgileri** – bu modül müşterinin bir sipariş için iletişim bilgilerini (e-posta adresi) eklemesine veya değiştirmesine olanak tanır.

- **Metin bloku** – bu modül, içerik yönetimi sistemi (CMS) tarafından yönlendirilen tüm iletileri içerir. Örneğin, "Siparişiniz ile ilgili sorunlar için 1-800-Fabrikam ile bağlantı kurun" iletisini içeren bir ileti bulunabilir. 

- **Ödeme hükümleri ve koşulları**: Bu modül hüküm ve koşulları içeren zengin metni ve müşteri girişi için bir onay kutusunu gösterir. Onay kutusu isteğe bağlıdır ve yapılandırılabilir. Giriş, modül tarafından yakalanır ve sipariş verme tetiklenmeden önce denetim olarak kullanılabilir, ancak sipariş özet bilgilerinde bulunmaz. Bu modül, iş gereksinimlerine göre ödeme kapsayıcısına, ödeme bölümü kapsayıcısına veya hüküm ve koşullar yuvasına eklenebilir. Ödeme kapsayıcısına veya ödeme bölümü kapsayıcısına eklenirse, ödeme sürecinde bir adım olarak gösterilir. Hüküm ve koşullar yuvasına eklenirse, siparişi verme düğmesinin yakınında görünür.

    Aşağıdaki resimde ödeme sayfasındaki hüküm ve koşullar örneği gösterilmektedir.

    ![Ödeme sayfasındaki hüküm ve koşullar örneği](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Sevkiyat adresi ve sevkiyat yöntemi gibi, ödeme bilgilerinin çoğu sepette depolanır ve siparişin bir parçası olarak işlenir. Tek özel durum kredi kartı bilgisi içindir. Bu bilgiler, adyen ödeme bağlayıcısı kullanılarak doğrudan işlenir. Ödeme yetkilendirilir ancak sipariş karşılanana kadar ücretlendirilmez.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Bir sayfaya ödeme modülü ekleyin ve gerekli özellikleri ayarlayın

Bir yeni sayfaya ödeme modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda, **Ödeme** modülünü seçin.
1. **Parça adı** altında, **Ödeme parçası** için bir ad girin ve **Tamam**'ı seçin.
1. **Ödeme modülü** yuvasını seçin.
1. Sağdaki Özellikler bölmesinde, Kurşun Kalem sembolünü seçin, alana başlık metnini girin ve onay işareti simgesini seçin.
1. **Ödeme bilgileri** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül ekle** iletişim kutusunda **Sevkiyat Adresi**, **teslim seçenekleri**, **kullanıma alma bölümü konteyneri** ve **ilgili kişi bilgileri** modüllerini seçin ve **Tamam** seçin.
1. **Ödeme bölümü konteyneri** modülü için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Hediye kartı**, **Sadakat** ve **Ödeme** modüller'i seçin, ve **Tamam**'ı seçin. Bu şekilde, tüm ödeme yöntemlerinin bir bölümde birlikte göründüğünden emin olabilirsiniz.
1. **Hüküm ve koşullar** yuvasında, gerekiyorsa, bir **Ödeme hükümleri ve koşulları** modülü ekleyin. Modülün özellikler bölmesinde hüküm ve koşul metnini uygun şekilde yapılandırın.
1. **Kaydet**'i seçin ve ardından parçayı önizlemek için **Önizleme**'yi seçin. Bazı modüller sepet bağlamına sahip değildir ve önizlemede işlenemeyebilir.
1. Parçayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.
1. Yeni ödeme parçasını kullanan bir şablon oluşturun.
1. Yeni şablon kullanan bir ödeme sayfası oluşturun.

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)
