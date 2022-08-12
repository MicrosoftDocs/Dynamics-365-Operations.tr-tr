---
title: Google Pay'i Adyen ile yapılandırma
description: Bu makalede, Google Pay'i Microsoft Dynamics 365 Commerce'te Adyen ile yapılandırma açıklanmaktadır.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115039"
---
# <a name="configure-google-pay-with-adyen"></a>Google Pay'i Adyen ile yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, Google Pay'i Microsoft Dynamics 365 Commerce'te Adyen ile yapılandırma açıklanmaktadır.

Dynamics 365 Commerce Adyen ödeme ağ geçidi hizmeti kullanılırken Google Pay için kullanıma hazır bir tümleştirme sunar. Google Pay Adyen ödeme hizmetiyle birlikte Google Pay Tüccar hesabı kullanan dijital cüzdan ödeme yöntemidir. Yapılandırıldığında Google Pay düğmesi çevrimiçi sipariş ödemesi sırasında bir ödeme yöntemi olarak seçilebilir. Kullanıcılar desteklenen bir tarayıcıda ya da cihazda **Google Pay**'i seçtiklerinde, ödemelerini doğrudan Google Pay hizmetiyle tamamlamaya yönlendirilirler. Daha sonra, siparişi tamamlama üzere çevrimiçi mağazaya dönerler.

Google Pay, Commerce'te hızlı ödeme modülü ile birlikte kullanıldığında kullanıcının ödeme sürecini daha hızlı tamamlamalarına yardımcı olması için, ödeme hesabı bilgileri ödeme formunda otomatik olarak doldurulur. Commerce hızlı ödeme davranışını etkinleştiren bir hızlı ödeme modülü içerir. Hızlı ödeme modülü, bir ödeme veya sepet sayfasına dahil olan bir parça içinde kullanılabilir. PayPal yapılandırıldığında hızlı ödemeyi ve normal ödeme seçeneklerini etkinleştirmek için Adyen için Dynamics 365 Ödeme Bağlayıcısı'na ek olarak Google Pay bağlayıcısı başvurusu için Dynamics 365 Ödeme Bağlayıcısı da kullanılır. Google Pay Adyen ödeme terminalleri ve mağaza içi kullanım için Commerce satış noktası (POS) ile de yapılandırılabilir.

## <a name="key-terms"></a>Önemli terimler

| Vade | Açıklama |
|---|---|
| Google Pay | Google Pay "düğmesi" olarak da bilinen Google Pay Adyen bağlayıcısı üzerinden desteklenen bir cüzdan ödeme seçeneğidir. Dynamics Google Pay Bağlayıcısı tarafından desteklenen müşteri deneyimi ve tümleştirmeyi etkinleştirir. |
| Cüzdan | Kredi ve ATM kartı tiplerini ayırt etmek için kullanılan banka kimlik numarası (BIN) aralığı ve son kullanma tarihi gibi geleneksel ödeme özellikleri içermeyen bir ödeme türü. |
| Hızlı ödeme modülü | Desteklenen ödeme yöntemleriyle daha hızlı ödeme davranışını destekleyen bir Dynamics 365 Commerce modülü. |

## <a name="prerequisites"></a>Ön Koşullar

Google Pay'i Commerce'te Adyen ile kullanmak için Google Tüccar hesabı gereklidir. Google Tüccar hesabının nasıl ayarlanacağı hakkında bilgi için [Google Pay için Adyen belgeleri](https://docs.adyen.com/payment-methods/google-pay/) ve Google'ın [Tümleştirme denetim listesi](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist) bölümlerine bakın.

Google Pay ödeme yöntemi Adyen hesabınızla da tümleştirilmelidir. Tümleştirme bağlantısı yönergeleri için bkz. [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Dynamics 365 Commerce headquarters'da gelişmiş cüzdan özelliğini de etkinleştirilmelisiniz. **Çalışma Alanları \> Özellik yönetimi**'ne gidin, **Gelişmiş cüzdan desteği ve ödeme iyileştirmeleri** özelliğini arayın, özelliği seçin ve ardından **Etkinleştir**'i seçin. Özellik etkinleştirildikten sonra, değişikliğin tüm kanallarda kullanılabilmesini sağlamak için **1110** dağıtım zamanlamasını çalıştırın.

## <a name="map-the-google-pay-payment-method"></a>Google Pay ödeme yöntemini eşleme

Google Pay bir dijital cüzdan ödeme yöntemidir. Google Pay için ödeme eşlemesini ayarlama hakkında bilgi için [Cüzdan ödemesi desteği](../wallets.md) bölümüne bakın.

POS ve çevrimiçi kanallarda Google Pay ödeme yöntemini kart ödeme türlerine eşlemek için aşağıdaki adımları izleyin.

1. Commerce headquarters'ta, **Perakende ve Ticaret \> Kanal ayarı \> Ödeme yöntemleri \> Kart türleri**'ne gidin.
1. Google Pay'e yeni bir satır eklemek için **Yeni**'yi seçin.
1. **Kimlik** alanına, **GooglePay** yazın.
1. **Elektronik ödeme adı** alanına **Google Pay** yazın.
1. **Tür** alanına, **Cüzdan** yazın.
1. **Veren** alanına, **Google** yazın.
1. Eylem Bölmesinde, **İşlemci eşleme** seçeneğini belirleyerek **İşlemci ödeme eşleme yöntemleri** iletişim kutusunu açın.
1. **Eşlenmemiş İşlemci Ödeme Yöntemleri** altında, eşlenmemiş işlemci ödeme yöntemlerinin listesini her yöntem uygun bağlayıcıyla eşleştirilmiş olarak görürsünüz. Eşlenmemiş Google Pay işlemci ödeme yöntemlerini kart ödeme türleriyle eşlemek için her kart ödeme türü için aşağıdaki adımları izleyin:

    1. **Kart ödeme türleri** altından bir kart ödeme türü seçin.
    1. **Eşlenmemiş İşlemci Ödeme Yöntemleri** sütununda, POS'ta kullanım için **Adyen için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısı ve çevrimiçi kanallarda kullanım için **Google Pay için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısını seçin.
    1. **Ekle**'yi seçin. Seçimler **Eşlenmiş İşlemci Ödeme Yöntemleri** sütununa eklenir.

1. Ödeme yöntemlerini eşlemeyi tamamladığınızda **Kaydet**'i seçin.
1. **Kart türleri** sayfasında, **Kaydet**'i seçin.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Google Pay için Commerce çevrimiçi mağazası yapılandırma

Google Pay kullanmak üzere bir Commerce çevrimiçi mağazası yapılandırmak için aşağıdaki adımları izleyin.

1. Commerce headquarters'ta, **Perakende ve Ticaret \> Kanallar \> Çevrimiçi mağazalar**'a gidin.
1. Kanalın **Perakende Kanal Kimliği** değerini seçerek sitenizin çevrimiçi mağaza kanalını seçin.
1. **Ödeme hesapları** hızlı sekmesinde, **Bağlayıcı** altında, **Adyen için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısının listelendiğini doğrulayın. Bağlayıcı listelenmemişse, eklemek için [Adyen için Dynamics 365 Ödeme Bağlayıcısını Ayarlama](adyen-connector-setup.md) bölümündeki yönergeleri izleyin.

    > [!NOTE]
    > Çoğu durumda, **Adyen için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısının kanalınızın ilk bağlayıcısı olarak listelenmesi gerekir (ilk bağlayıcı birincil bağlayıcı olarak da bilinir). **PayPal için Dynamics 365 Ödeme Bağlayıcısı** ve **GooglePay için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcıları gibi kullanılacak diğer bağlayıcılar gelmelidir.

1. **Adyen için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısı eklendikten sonra, **GooglePay için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısını eklemek üzere **Ekle**'yi seçin. Ardından, bağlayıcı için aşağıdaki özellikleri ayarlayın.

    | Alan                  | Açıklama | Gerekli | Otomatik olarak ayarla | Örnek değer |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Derleme Adı          | GooglePay için Dynamics 365 Ödeme Bağlayıcısı için derlemenin adı. | Evet | Evet | *İkili ad* |
    | Hizmet hesabı kodu     | Tüccar özellikleri kurulumu için benzersiz tanıtıcı. Bu tanıtıcı ödeme hareketlerine damgalanır ve faturalama gibi aşağı akış süreçlerinin kullanması gereken tüccar özelliklerini tanımlar. | Evet | Evet | *GUID* |
    | Google tüccar kimliği     | Google Tüccar hesabınıza atanan Google Tüccar Kimliğini girin. Bu özellik üretim ortamları için gereklidir ancak test ortamları için isteğe bağlıdır. Daha fazla bilgi için <https://pay.google.com/> adresini ziyaret edin. | Evet | No. | *Sayısal tanımlayıcı* |
    | Tüccar hesabı kodu    | Benzersiz Adyen tüccar tanıtıcısını girin. Bu değer, [Adyen'e kaydolma](adyen-connector-setup.md#sign-up-with-adyen) bölümünde açıklandığı gibi, Adyen'e kaydolduğunuzda sağlanır. | Evet | No. | *Tüccar Tanımlayıcısı* |
    | Bulut API Anahtarı          | Adyen bulut API anahtarını girin. Bu anahtarı edinmek için [API anahtarı edinme](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) bölümündeki yönergeleri izleyin. | Evet | No. | "abcdefg" |
    | Ağ geçidi ortamı    | Eşlenecek Adyen ağ geçici ortamı. Olası değerler **Test** ve **Canlı**'dır. Bu alanı yalnızca üretim cihazları ve işlemler için **Canlı** olarak ayarlamalısınız. | Evet | Evet | "Canlı" |
    | Desteklenen Para Birimleri   | Bağlayıcının işlemesi gereken para birimleri. Kart mevcut senaryolarda, işlem isteği ödeme terminaline gönderildikten sonra Adyen [Dinamik Para Birimi Dönüşümü](https://www.adyen.com/pos-payments/dynamic-currency-conversion) ile diğer para birimlerini destekleyebilir. Desteklenen para birimlerinin listesini almak için Adyen desteğine başvurun. | Evet | Evet | "USD;EUR" |
    | Desteklenen Ödeme Türleri | Bağlayıcının işlemesi gereken ödeme türleri. | Evet | Evet | "GooglePay" |

1. Bağlayıcı özelliklerini ayarlamayı bitirdikten sonra, **1070 (Kanal yapılandırma**) dağıtım zamanlaması işini çalıştırın.

## <a name="configure-commerce-pos-for-google-pay"></a>Google Pay için Commerce POS yapılandırma

POS yapılandırması Adyen için Dynamics 365 Ödeme Bağlayıcısı'na donanım profilinin **EFT hizmeti** alanındaki ayarı kullanır. Commerce headquarters'ta Adyen için Dynamics 365 Ödeme Bağlayıcısı'na elektronik fon transferi (EFT) hizmetini yapılandırma hakkında bilgi için [Dynamics 365 POS donanım profili bölümü ayarlama](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile) bölümüne bakın.

Adyen bağlayıcısı için işlemci eşlemesi Google Pay'in POS terminalinde kullandığı cüzdan kartı türlerini yakalar.

### <a name="use-the-payment-express-module-with-google-pay"></a>Google Pay ile hızlı ödeme modülünü kullanma

Commerce hızlı ödeme modülü, site müşterilerine ödeme işlemi sırasında ödeme hizmeti hesap bilgilerini kullanarak daha hızlı ödeme yapma seçeneği sunmak için destekleyici ödeme yöntemleriyle çalışır. Hızlı ödeme modülü yapılandırılmış bağlayıcı düğmesine başvurur ve ödeme formunu doldurmak için kullanıcının seçtiği sipariş ayrıntılarını (adres, iletişim bilgileri ve ödeme yöntemi) getirir.

Google Pay ile hızlı ödeme modülü kullanırken, müşteriler **Hızlı Ödeme** bölümünde Google Pay düğmesini seçtiğinde Google Pay iFrame penceresi açılır. Daha sonra kullanıcılar, işlem için ödeme yapmak üzere hesabın sevkiyat adresini, faturalama adresini, e-posta adresini ve Google Pay ödeme yöntemini kullanmak için kendi Google Pay hesabında oturum açar.

Kullanıcılar, eylemi Google Pay penceresinde tamamladığında, ödeme formunun Google Pay hesap ayrıntılarıyla önceden doldurulduğu Commerce sitesi ödeme sayfasına yönlendirilir. Kullanıcılar Google Pay penceresinden ödeme sayfasına döndükten sonra aşağıdaki ayrıntıları görürler:

- Hızlı ödeme akışında, döndürülen sevkiyat adresi için kullanılabilen ilk teslimat seçeneği müşteri için önceden seçilidir.
- Google Pay kullanıldığında ilgili kişi e-posta adresi döndürülmez. Konuk olarak ödeme yapan kullanıcıların ödeme sayfasının iletişim bilgisi bölümüne bir e-posta adresi girmeleri gerekir. Oturum açan kullanıcıların iletişim bilgileri Dynamics müşteri hesaplarından (kimlik doğrulama için kullandıkları birincil e-posta adresi) otomatik olarak doldurulur.

Müşterilerin siparişi tamamlamak üzere **Sipariş ver**'i seçmeden önce siparişleri gözden geçirme ve ödeme siparişi ayrıntılarını değiştirme seçeneği olur.

### <a name="configure-google-pay-in-site-builder"></a>Site oluşturucusunda Google Pay'i yapılandırma 

Parçalarınızı ya da sayfalarınızı Google Pay ile yapılandırabilmek için sitenizin içerik güvenliği ilkelerinin Commerce site oluşturucusunda ayarlandığından emin olmanız gerekir.

İçerik güvenliği ilkelerinizin site oluşturucusunda ayarlandığından emin olmak için aşağıdaki adımları izleyin.

1. Sitenizde **Site ayarları \> Uzantılar**'a gidin.
1. **İçerik güvenliği ilkesi** sekmesinde, **child-src**, **connect-src**, **frame-ancestors**, **frame-src**, **img-src**, **script-src** ve **style-src** yönergelerine `*.google.com` için bir satır ekleyin.
1. Tamamladıktan sonra **Kaydet ve yayımla**'yı seçin.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Hızlı ödeme parçasını site oluşturucusunda Google Pay ile yapılandırma

Çevrimiçi mağaza için hızlı ödeme parçasını Google Pay'e ayarlamak için aşağıdaki adımları izleyin.

1. Site oluşturucusunda **Parçalar**'a gidin.
1. **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda **Kapsayıcı** modülünü seçin, parça adını girin (örneğin **Hızlı Ödeme**) ve sonra **Tamam**'ı seçin. 
1. Yeni parçanın **Varsayılan Kapsayıcı** yuvasını seçin.
1. Sağdaki özellikler bölmesinde kapsayıcı modülünün özelliklerini ayarlayın:

    - **Başlık** – Sitenizin hızlı ödeme bölümünde görüntülenmek üzere bir başlık girin (örneğin **Hızlı Ödeme**).
    - **Konteyner düzeni** – **Akış**'ı seçin.
    - **Genişlik** – **Konteyneri doldur**'u seçin.
    - **Gösterilen alt öğeler** – Ödeme sayfasının hızlı ödeme bölümünün bir satırına sığacak alt öğe sayısını belirtmek için **Üç**'ü seçin (örneğin metin kutusu, PayPal için hızlı ödeme ve Google Pay için hızlı ödeme).
    - **CSS sınıfı adı** – **msc-express-payment-container** yazın (gerekli).

    > [!IMPORTANT]
    > - **CSS sınıfı adı** değeri, ödeme sırasında kapsayıcı davranışını denetlemesi için **msc-express-payment-container** olarak ayarlanmalıdır. Bu davranış gizleme, daraltma ve ödeme akışı sırasında hızlı ödeme bölümünde geçerli olacak diğer eylemleri içerir. **msc-express-payment-container** sınıfı modül kitaplığı ödeme modülüyle serbest bırakılan varsayılan işlemlerle çalışır.
    > - **CSS sınıfı adı**'na başka stiller de eklenebilir. Modülün davranışını özelleştirdiğinizde, hızlı ödeme davranışı için ödeme modülünde aynı modül kitaplığında kodlanmış davranışı kullanıyorsanız stil denetimlerini karşılıklı olarak kontrol edin.

1. **Varsayılan konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Hızlı ödeme** modülünü seçin ve **Tamam**'ı seçin.
1. **Hızlı ödeme** modülü özellikler bölmesinde, **iFrame yüksekliği** değerini piksel olarak ayarlayın ya da düzenleyin (örneğin **60**).
1. **Desteklenen ödeme türleri** alanında **Google Pal** girin. Bu değer kanal için ayarlanmış bağlayıcının **Desteklenen Ödeme Türleri** dizesiyle eşleşmelidir (bu makalenin [Google Pay için Commerce çevrimiçi mağazası yapılandırma](#configure-a-commerce-online-store-for-google-pay) bölümünde açıklanmıştır).

    > [!NOTE]
    > Diğer ödeme yöntemlerine **Hızlı ödeme** modülleri eklemek için 6'dan 9'a kadar olan adımları tekrarlayabilirsiniz. **Desteklenen ödeme türleri** değerini eklenen yapılandırılmış ödeme türleriyle (örneğin **Paypal**) uyumlu hale getirin.

1. İsteğe bağlı: Yönergeleri ya da açıklamaları dahil etmek için varsayılan kapsayıcı modülüne bir metin bloğu modülü ekleyebilirsiniz. Modülü ekledikten sonra, özellikler bölmesindeki **Zengin metin** alanına istediğiniz metni girin. **Metin bloğu** yuvasındaki üç nokta (**...**) düğmesini seçip **Yukarı taşı** ya da **Aşağı taşı** seçeneklerini kullanarak metni hızlı ödeme modüllerinin üstüne veya altına yerleştirebilirsiniz.
1. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i, ardından **Düzenlemeyi bitir**'i seçin.
1. Parçayı yayımlamak için **Yayımla**'yı seçin.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Hızlı ödeme parçasını ödeme sayfasına ekleme

Ödeme sayfasına hızlı ödeme parçası eklemek için aşağıdaki adımları izleyin.

1. Site oluşturucusunda, **Sayfalar**'a gidin ve sonra da sitenizin ödeme sayfasını seçin.
1. **Düzenle** öğesini seçin.
1. **Ana yuva** alanında üç nokta (**...**) düğmesini, ardından **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. Sağdaki özellikler bölmesinde kapsayıcı modülünün özelliklerini ayarlayın:

    - **Konteyner Düzeni** – **Yığılmış**'ı seçin.
    - **Genişlik** – **Konteyneri doldur**'u seçin.
    - **Gösterilen Alt Öğeler** – Ödeme sayfasının hızlı ödeme bölümünün bir satırına sığacak alt öğe sayısını belirtmek için **Üç**'ü seçin (örneğin metin kutusu, PayPal için hızlı ödeme ve Google Pay için hızlı ödeme).

1. **Kapsayıcı** modül yuvasında, üç nokta (**...**) düğmesini seçin ve **Parça ekle**'yi seçin.
1. **Parça seç** iletişim kutusunda daha önce oluşturduğunuz hızlı ödeme parçasını seçin ve sonra **Tamam**'ı seçin.
1. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i, ardından **Düzenlemeyi bitir**'i seçin.
1. Sayfayı yayımlamak için **Yayımla**'yı seçin.

> [!NOTE]
> Ödeme sayfasında ödeme parçası olan bir kapsayıcı zaten varsa ve hızlı ödeme modülünün normal ödeme kapsayıcısının üzerinde işlenmesini istiyorsanız, **Ana yuva**'daki üç nokta (**...**) düğmesini seçip **Yukarı taşı** ya da **Aşağı taşı** seçeneklerini kullanarak bu modülü mevcut ödemenin üstüne ya da altına yerleştirebilirsiniz.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Hızlı ödeme parçasını sepet sayfasına ekleme

Sepet sayfasına hızlı ödeme parçası eklemek için aşağıdaki adımları izleyin.

1. Site oluşturucusunda, **Sayfalar**'a gidin ve sonra da sitenizin sepet sayfasını seçin.
2. **Düzenle** öğesini seçin.
3. Ana hat görünümündeyken, ağaç görünümündeki **Ana yuva**'yı genişletip **Sepet** modülünü içeren kapsayıcıyı bulun.
4. **Sepet** modülünde, **Hızlı Ödeme** yuvasını seçin, önce üç nokta (**...**) düğmesini, ardından **Modül ekle**'yi seçin.
5. **Modül seç** iletişim kutusunda **Hızlı ödeme** modülünü seçin ve **Tamam**'ı seçin.
6. **Hızlı ödeme** modülü yuvasını seçin. Ardından, sağdaki özellikler bölmesinde, **Desteklenen ödeme türleri** altında **GooglePay** girin. Bu değer kanal için ayarlanmış bağlayıcının **Desteklenen Ödeme Türleri** dizesiyle eşleşmelidir (bu makalenin [Google Pay için Commerce çevrimiçi mağazası yapılandırma](#configure-a-commerce-online-store-for-google-pay) bölümünde açıklanmıştır).
1. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i, ardından **Düzenlemeyi bitir**'i seçin.
1. Sayfayı yayımlamak için **Yayımla**'yı seçin.

Kullanıcılar sepetin **Hızlı Ödeme** yuvasına en fazla üç adet desteklenen **Hızlı Ödeme** modülü (diğer bir deyişle, üç adet kullanılabilir desteklenen ödeme seçeneği) ekleyebilirler.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Ödeme bölümünde Google Pay'i bir seçenek olarak ayarlama

Yalnızca ödemeye yönelik, hızlı olmayan işlevler için ödeme bölümünde Google Pay'i bir seçenek olarak ayarlayabilirsiniz. Ödeme formu kullanıcı tarafından doldurulur ve Google Pay ödeme sayfası yalnızca Google Pay üzerinden ödeme için kullanılabilir. Herhangi bir Google hesabı bilgisi doldurulmuş ödeme ayrıntılarının üzerine yazılmaz.

> [!NOTE]
> Aşağıdaki yordamda sitenizin teslimat bilgileri, sevkiyat adresi, teslimat seçenekleri, iletişim bilgileri, isteğe bağlı hüküm ve koşullar ile ödeme unsurları için bölme ile yapılandırılmış bir ödeme parçası kullandığı varsayılır. Varsayılan modül kitaplığı ödeme modülü metin bloğu, bağlılık programı puanları, hediye kartı ve ödeme modülleri olan bir ödeme bölümü kapsayıcısıyla birlikte yayımlanmıştır. Daha fazla bilgi için [Ödeme modülü](../payment-module.md) bölümüne bakın.

Google Pay'i ödeme sayfasının **Ödeme Yöntemi** bölümündeki düzenli ödeme seçeneği olarak ayarlamak için aşağıdaki adımları izleyin.

1. Site oluşturucusunda, **Parçalar**'a gidin ve sonra da sitenizin ödeme parçasını seçin.
1. **Düzenle** öğesini seçin.
1. **Ödeme bilgileri** bölümünde üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Ödeme** modülünü seçin ve **Tamam**'ı seçin.
1. **Ödeme** modülünün sağdaki özellikler bölmesinde, kapsayıcı modülünün özelliklerini ayarlayın:

    - **Başlık** – Sitenizin hızlı ödeme bölümünde görüntülenmek üzere bir başlık girin (örneğin **Google Pay**).
    - **iFrame Yüksekliği** – Değeri piksel cinsinden istediğiniz tasarım yüksekliğiyle değiştirin (örneğin **75**). 
    - **Desteklenen ödeme türleri** – Commerce headquarters'da bulunan Google Pay bağlayıcısı yapılandırmasıyla eşlemek için **Google Pay** yazın.
    - **Birincil ödemedir** – Onay kutusunun işaretini kaldırın. (Bu özellik Adyen ödeme modülü için genellikle etkindir.)
    - **Ödeme stilini geçersiz kılma** – Bu özellik Google Pay yapılandırmasında desteklenmez.
    - **Bağlayıcı kimliğini kullan** – Sayfada birden fazla ödeme bağlayıcısı kullanılıyorsa bu özellik seçilmelidir.

1. **Ödeme** yuvasındaki üç nokta (**...**) düğmesini seçip **Yukarı taşı** ya da **Aşağı taşı** seçeneklerini kullanarak modülü diğer ödeme modüllerinin üstüne veya altına yerleştirin.
1. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i, ardından **Düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

### <a name="modes-of-delivery"></a>Teslimat şekilleri

Google Pay kullanan hızlı ödeme modülünde, Google Pay hesabından gelen seçili sevkiyat adresi için döndürülen ilk teslimat seçeneği önceden seçilidir. Kullanıcılar istedikleri zaman sevkiyat adresini başka bir seçenekle değiştirebilirler.

Teslimat yöntemlerinin hızlı ödeme modülünde görüntülenme sırası Commerce headquarters'da kanalın **Teslimat şekilleri** sayfasında yapılandırılır. Commerce headquarters'da **Perakende ve Ticaret \> Kanallar \> Çevrimiçi mağazalar**'a gidin ve mağazanızın **Perakende Kanalı Kodu** değerini seçin. Eylem Bölmesi'ndeki **Ayar** sekmesinde, **Teslimat şekilleri**'ni seçin. Listelenen teslimat şekilleri hızlı ödeme modülündeki sırayla görüntülenir. Eylem Bölmesi'ndeki **Teslimat şekillerini yönet** seçeneğini kullanarak perakende kanal ya da ürün için teslimat şekilleri ekleyebilir veya kaldırabilirsiniz. Teslimat şekillerini ayarlama hakkında daha fazla bilgi için [Teslimat şekillerini ayarlama](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) bölümüne bakın.

Ödeme sırasında teslimat şekilleri işlendiğinde ödeme modülü de teslimat seçenekleri modülünü kullanır. Daha fazla bilgi için bkz. [Teslimat seçenekleri modülü](../delivery-options-module.md).

Teslimat şekilleri çevrimiçi mağazadaki **Teslimat şekilleri** listesine eklendiklerinde görüntülenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ödemeler ile ilgili SSS](payments-retail.md)

[Ödeme yapma modülü](../add-checkout-module.md)

[Ödeme modülü](../payment-module.md)
