---
title: PayPal için hızlı ödemeleri yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te daha hızlı ödeme özelliklerini etkinleştirmek üzere PayPal için hızlı ödemeleri yapılandırma yöntemi açıklanmıştır.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905294"
---
# <a name="configure-express-payments-for-paypal"></a>PayPal için hızlı ödemeleri yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te daha hızlı ödeme özelliklerini etkinleştirmek üzere PayPal için hızlı ödemeleri yapılandırma yöntemi açıklanmıştır.

## <a name="key-terms"></a>Önemli terimler

| Vade | Açıklama |
|---|---|
| PayPal Cüzdanı | PayPal bağlayıcısı tarafından desteklenen müşteri deneyimi ve tümleştirme. PayPal düğmesi olarak da bilinir. |
| Cüzdan | Kredi ve ATM kartı tiplerini ayırt etmek için kullanılan banka kimlik numarası (BIN) aralığı ve son kullanma tarihi gibi geleneksel ödeme özellikleri içermeyen bir ödeme türü. |
| Hızlı ödeme | Desteklenen ödeme yöntemleri kullanıldığında daha hızlı ödeme davranışını destekleyen bir Commerce modülü. Bu makale, PayPal ile ödeme hızlı modülü kullanımını kapsamaktadır. |

Dynamics 365 Commerce, PayPal Cüzdanı için kullanıma hazır bir tümleştirme sunar. PayPal için Dynamics 365 Ödeme Bağlayıcısı yapılandırıldığında, bir çevrimiçi sipariş ödemesi sırasında PayPal düğmesi seçilebilir bir ödeme yöntemi olarak görünür. Kullanıcılar PayPal'ı seçtiklerinde, doğrudan PayPal aracılığıyla ödemeyi tamamlamaya yönlendirilir ve daha sonra siparişlerini tamamlamak için çevrimiçi mağazaya geri gönderilir. PayPal sepeti ödemesi, müşterilerin ödeme işlemini daha çabuk tamamlayabilmeleri için ödeme hesabı bilgilerini kullanarak ödeme formunu önceden doldurmalarını sağlar.

Commerce, hızlı ödeme işlemlerini kolaylaştırmak için bir hızlı ödeme modülü ekledi. Hızlı ödeme modülü, bir ödeme veya sepet sayfasına dahil edilebilecek bir parça içinde kullanılabilir. PayPal yapılandırıldığında PayPal bağlayıcı referansına yönelik aynı Dynamics 365 Ödeme Bağlayıcısı, hem hızlı ödeme seçeneği hem de normal ödeme seçeneği için kullanılır.

## <a name="paypal-checkout-in-commerce"></a>Commerce'te PayPal ödemesi

### <a name="prerequisites"></a>Önkoşullar

[PayPal için Dynamics 365 Ödeme Bağlayıcısı](../paypal.md) bölümünde açıklandığı gibi ortamınız için PayPal Cüzdanı ayarlayın.

PayPal'ı normal ödeme akışında bir seçenek olarak kullanıyorsanız (kullanıcıların hızlı ödeme önceden doldurma eylemlerini kullanmadan hesap bilgilerini el ile girebileceği durumlarda), [Ödeme modülündeki](../payment-module.md) kurulum yönergelerini uygulayın.

### <a name="payment-express-module-with-paypal"></a>PayPal ile hızlı ödeme modülü

Hızlı ödeme modülü, site müşterilerine ödeme işlemi sırasında ödeme hizmeti hesap bilgilerini önceden doldurarak daha hızlı ödeme yapma seçeneği sunmak için destekleyici ödeme yöntemleriyle çalışır. Hızlı ödeme modülü, ödeme formunu, adres, ilgili kişi bilgileri ve seçilen ödeme yöntemi gibi kullanıcı hesabı ayrıntılarıyla doldurmak için yapılandırılmış ödeme bağlayıcısını kullanır.

PayPal hızlı ödeme kullanıldığında ve kullanıcı, ödeme sayfasının hızlı ödeme bölümünde PayPal düğmesini seçtiğinde, bir PayPal ödemesi iFrame penceresi açılır. Daha sonra kullanıcı, işlem için ödeme yapmak üzere hesabın sevkiyat adresini, faturalama adresini, e-posta adresini ve PayPal ödeme yöntemini kullanmak için kendi PayPal hesabında oturum açar.

Kullanıcı, eylemi PayPal penceresinde tamamladığında, ödeme formunun seçili ayrıntılarla önceden doldurulduğu Commerce sitesi ödeme sayfasına yönlendirilir. Hızlı ödeme akışında, döndürülen sevkiyat adresi için kullanılabilen ilk teslimat seçeneği kullanıcı için önceden doldurulur. Daha sonra kullanıcının siparişi tamamlamak üzere **Sipariş ver**'i seçmeden önce siparişi gözden geçirme ve ödeme siparişi ayrıntılarını değiştirme seçeneği olur.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>PayPal ile hızlı ödeme modülünü bir parçaya ekleme

Commerce site oluşturucuda PayPal ile hızlı ödeme modülünü bir parçaya eklemek için aşağıdaki adımları izleyin.

1. Sitenize gidin.
1. Sol gezinti bölmesinde, **Parçalar**'ı seçin ve sonra **Yeni**'yi seçin.
1. **Yeni Parça** iletişim kutusunda, **Hızlı ödeme** modülünü bulup seçin ve sonra **Parça adı** altında parça için bir ad girin (örneğin, **Hızlı ödeme**).
1. Parçayı oluşturmak için **Tamam**'ı seçin.
1. Ana hat görünümünde, oluşturduğunuz ödeme hızlı modülü yuvasını seçin.
1. Özellikler bölmesinde **Başlık**'ı seçin.
1. **Başlık** iletişim kutusunda, **Başlık metni** alanına sitenizin hızlı ödeme bölümü için göstermek istediğiniz başlık metnini (örneğin, **Hızlı ödeme**) girin.
1. **Başlık düzeyi** altında başlık düzeyini (örneğin, **H2**) seçin.
1. **Tamam**'ı seçin.
1. Özellikler bölmesinde, **iFrame yüksekliği** alanında iFrame öğesinin yüksekliğini girin veya ayarlayın (örneğin, **60**).
1. **Desteklenen ödeme tipleri** alanında **PayPal** girin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Hızlı ödeme parçasını ödeme sayfasına ekleme

Site oluşturucuda ödeme sayfasına hızlı ödeme parçası eklemek için aşağıdaki adımları izleyin.

1. Sitenize gidin.
1. Sol gezinti bölmesinde, **Sayfalar**'ı seçin ve sonra da sitenizin ödeme sayfasını seçin.
1. Sayfayı düzenlemek için **Düzenle**'yi seçin.
1. **Ana** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.

    > [!NOTE]
    > Ödeme parçası içeren bir konteyner modülü zaten varsa, hızlı ödeme bölümünü **Ana** yuvada varolan ödeme kapsayıcısının üzerinde görünecek şekilde taşıyın. Daha sonra hızlı ödeme bölümü, normal ödeme kapsayıcısının üzerinde oluşturulur. Bir konteyner modülünü yukarı veya aşağı taşımak için üç noktayı (**...**) seçin ve **Yukarı taşı** veya **Aşağı taşı**'yı seçin.

1. **Kapsayıcı** özellikleri bölmesinde, özellik ayarlarını aşağıdaki şekilde yapılandırmanızı öneririz:

    - **Konteyner Düzeni** – **Yığılmış**'ı seçin.
    - **Genişlik** – **Konteyneri doldur**'u seçin.
    - **Gösterilen Alt Öğeler** – **Üç**'ü seçin.

1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Parça Ekle**'yi seçin.
1. **Parça seç** iletişim kutusunda daha önce oluşturduğunuz hızlı ödeme parçasını bulup seçin ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Hızlı ödeme parçasını sepet sayfasına ekleme

Site oluşturucuda sepet sayfasına hızlı ödeme parçası eklemek için aşağıdaki adımları izleyin.

1. Sitenize gidin.
1. Sol gezinti bölmesinde, **Sayfalar**'ı seçin ve sonra da sitenizin sepet sayfasını seçin.
1. Sayfayı düzenlemek için **Düzenle**'yi seçin.
1. **Ana** yuvasında, **Sepet** modülünü içeren kapsayıcıyı bulun. **Sepet** modülü bir **Hızlı ödeme** yuvası içerecektir.
1. **Hızlı Ödeme** yuvasını seçin, üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Hızlı ödeme** modülünü seçin ve **Tamam**'ı seçin.
1. Özellikler bölmesinde, **Desteklenen ödeme tipleri** alanında **Paypal** girin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="modes-of-delivery"></a>Teslimat şekilleri

Hızlı ödeme modülü PayPal'ı kullanacak şekilde yapılandırıldığında, PayPal hesabı için seçilen sevkiyat adresi için döndürülen ilk teslimat seçeneği önceden doldurulur. Kullanıcılar, teslimat adresini istedikleri gibi değiştirebilecektir.

Teslimat şeklinin sırası, Commerce Headquarters'daki kanalın **Teslimat şekilleri** bölümünde yapılandırılır. Daha fazla bilgi için bkz. [Teslimat koşullarını ayarlama](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Ödeme sırasında teslimat şekilleri işlendiğinde ödeme modülü de teslim seçenekleri modülünü kullanacaktır. Daha fazla bilgi için bkz. [Teslimat seçenekleri modülü](../delivery-options-module.md).

Teslimat şekilleri Commerce Headquarters'da bulunan çevrimiçi mağazanın listesine eklenir. **Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin ve mağazanızın kanal kimliğini seçin. Ardından **Kurulum \> Teslimat şekilleri**'ni seçin. Yapılandırmada gösterilen teslimat şekilleri modülü sitede benzer şekilde görünür. Perakende kanalı veya ürünü için teslimat şekilleri eklemek veya kaldırmak için, eylem bölmesinde **Teslimat şekillerini yönet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Ödemeler ile ilgili SSS](payments-retail.md)

[Ödeme yapma modülü](../add-checkout-module.md)

[Ödeme modülü](../payment-module.md)

[Teslimat şekillerini ayarla](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Teslimat seçenekleri modülü](../delivery-options-module.md)
