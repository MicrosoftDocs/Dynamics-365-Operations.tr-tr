---
title: Dynamics 365 Commerce'te Adyen ile Apple Pay'i ayarlama
description: Bu makalede, Apple Pay'i Microsoft Dynamics 365 Commerce'te Adyen ile yapılandırma açıklanmaktadır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 896847cee696e221b2114f7f28a0b56e73fc911b
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838242"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'te Adyen ile Apple Pay'i ayarlama

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makalede, Apple Pay'i Microsoft Dynamics 365 Commerce'te Adyen ile yapılandırma açıklanmaktadır.

## <a name="key-terms"></a>Önemli terimler

| Vade | Açıklama |
|---|---|
| Apple Pay | Apple Pay "düğmesi" olarak da bilinen Apple Pay, Adyen bağlayıcısı üzerinden desteklenen bir cüzdan ödeme seçeneğidir. Microsoft Dynamics 365 Apple Pay Bağlayıcısı tarafından desteklenen müşteri deneyimi ve tümleştirmeyi etkinleştirir. |
| Cüzdan | Kredi ve ATM kartı tiplerini ayırt etmek için kullanılan Banka Kimlik Numarası (BIN) aralığı ve son kullanma tarihi gibi geleneksel ödeme özellikleri içermeyen bir ödeme türü. |

Dynamics 365 Commerce Adyen ödeme ağ geçidi hizmeti kullanılırken Apple Pay için kullanıma hazır bir tümleştirme sunar. Apple Pay Adyen ödeme hizmetiyle birlikte Apple Pay satıcı hesabı kullanan dijital cüzdan ödeme yöntemidir. Yapılandırıldığında Apple Pay düğmesi çevrimiçi mağazanın sipariş ödeme sayfasının bir parçası olan bir ödeme yöntemi olarak seçilebilir. Apple Pay düğmesi yalnızca desteklenen Apple Pay cihazları için bir ödeme seçeneği olarak sunulur. Kullanıcılar desteklenen bir tarayıcıda ya da cihazda **Apple Pay**'i seçtiklerinde, ödemelerini doğrudan Apple Pay hizmetiyle tamamlamaya yönlendirilirler. Daha sonra, siparişi tamamlamak üzere çevrimiçi mağazaya dönerler.

sitede Apple Pay ve kredi kartı ödeme seçeneklerini etkinleştirmek için Adyen için Dynamics 365 Ödeme Bağlayıcısı'na ek olarak Apple Pay bağlayıcısı başvurusu için Dynamics 365 Ödeme Bağlayıcısı da kullanılır. Apple Pay, Commerce satış noktası (POS) ile Adyen için Dynamics 365 Ödeme Bağlayıcısını kullanan Adyen ödeme terminallerinde sahip mağazalarda kullanılmak üzere de yapılandırılabilir. Bu durumda, Adyen için Dynamics 365 Ödeme Bağlayıcısı, Apple Ödeme cihazı dokunuşunu terminal aracılığıyla işler.

## <a name="prerequisites"></a>Ön Koşullar

Commerce'ta Adyen ile Apple Pay kullanmak için bir Apple satıcı hesabı gereklidir. Apple Pay'i test müşteri alanında ayarlama hakkında bilgi için bkz. [Apple Pay Ziyaret tümleştirmesi](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Üretim ortamınızda canlı yayınlamaya hazır olduğunuzda ne yapmanız gerektiğini öğrenmek için bkz. [Servise alma](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Apple Pay ödeme yöntemi Adyen hesabınızla da tümleştirilmelidir. Adyen, ödeme yöntemi ayarlamanıza ve sertifikayı kullanacağınız etki alanlarının sertifikayla kullanılmak üzere atanmasını sağlamaya da yardımcı olabilir.

Commerce Headquarters'ta gelişmiş cüzdan özelliği bayrağını etkinleştirmek için **Çalışma alanları \> Özellik yönetimi**'ne gidin ve **Gelişmiş cüzdan desteği ve ödeme iyileştirmeleri** özelliğine gidin. Özelliği ve **Etkinleştir** düğmesini seçin. Özellik etkinleştirildikten sonra, değişikliğin tüm kanallarda kullanılabilmesini sağlamak için **1110** dağıtım zamanlamasını çalıştırın.

## <a name="map-the-apple-pay-payment-method"></a>Apple Pay ödeme yöntemini eşleme

Apple Pay bir dijital cüzdan ödeme yöntemidir. Apple Pay için ödeme eşlemesini ayarlama hakkında bilgi için [Cüzdan ödemesi desteği](../wallets.md) bölümüne bakın.

Commerce Headquarters'da Apple Pay ödeme yöntemini eşlemek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Ödeme yöntemleri \> Kart türleri**'ne gidin.
1. **Yeni**'yi seçerek Apple Pay için bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Kimlik:** ApplePay
    - **Elektronik ödeme adı:** Apple Pay
    - **Tür:** Cüzdan
    - **Veren:** Apple

1. **İşlemci eşleme** seçeneğini belirleyerek **İşlemci ödeme eşleme yöntemleri** iletişim kutusunu açın. **Eşlenmemiş İşlemci Ödeme Yöntemleri** sütunu, kullanılabilir her bağlayıcı için desteklenen ödeme yöntemlerini listeler (Adyen, PayPal ve Apple).
1. **Adyen için Dynamics 365 Payment Bağlayıcısı** (POS'ta kullanmak için) ve **Apple Pay için Dynamics 365 Payment Bağlayıcısı** bağlayıcısı (çevrimiçi kanal) için istediğiniz desteklenen ödeme yöntemlerini eşleyin.
1. Her bir eşleme satırı için **Eşlenmemiş İşlemci Ödeme Yöntemleri** sütununda desteklenecek satırı seçin ve ardından seçimleri  **Eşlenmiş İşlemci Ödeme Yöntemleri** sütununa taşımak için **Ekle**'yi seçin.
1. **Tamam**'ı ve ardından **Kart Türleri** sayfasında **Kaydet**'i seçin.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Siteniz için Apple Pay sertifikasını ayarlama

Her site için etki alanı ilişkilendirme dosyasını (Apple Pay sertifikası olarak da bilinir) [Adyen Apple Pay belgelerinde](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) açıklandığı şekilde yüklemeniz gerekir. Etki alanı ilişkilendirme dosyasını sitenizin Medya Kitaplığına yüklemek için Commerce site oluşturucusunu kullanabilirsiniz.

Site oluşturucuda Apple Pay sertifikasını ayarlamak için şu adımları izleyin.

1. Sertifikayı (etki alanı ilişkilendirme dosyası) [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live)'den indirin.
1. Etki alanı ilişkilendirme dosyasına .txt uzantısını ekleyin.
1. Site oluşturucuda etki alanı ilişkilendirme dosyasını sitenizin ortam kitaplığına [yükleyin](../upload-serve-static-files.md).
1. **URL'ler**'e gidin.
1. **Yeni \> Yeni URL**'yi seçin.
1. **Yeni URL** iletişim kutusunda **Medya Kitaplığı varlığı** seçeneğini belirleyin.
1. **URL yolu** alanında, URL yolunu girin (daha önce girilmediyse). Etki alanı temel URL'sinin ardından, aşağıdaki gerekli Apple dizesini girin: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. **Sonraki**'yi seçin. Ortam Kitaplığı **belge** (.txt) türündeki tüm yüklenmiş medya varlıklarını gösterir.
1. Daha önce tanımladığınız URL'ye yönelik istekler için sunulması gereken etki alanı ilişkilendirme dosyasını seçin.
1. **Oluştur**'u seçin.

Bu noktada, oluşturduğunuz URL Taslak durumundadır. İşlemi tamamlamak için URL'yi yayımlayın. URL'nin gösterdiği dosya, siz URL'yi yayınlana kadar döndürülmez.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Apple Pay için Commerce çevrimiçi mağazası yapılandırma

Apple Pay için Commerce çevrimiçi mağazası yapılandırmak üzere aşağıdaki adımları izleyin.

1. Commerce headquarters'ta, **Perakende ve Ticaret \> Kanallar \> Çevrimiçi mağazalar**'a gidin.
1. Sitenizin çevrimiçi mağaza kanalının **Perakende Kanalı Kimliği** değerini seçin.
1. Daha önce ayarlanmadıysa [Adyen için Dynamics 365 Ödeme Bağlayıcısını Ayarlama](adyen-connector-setup.md) bölümündeki yönergeleri izleyerek **Ödeme hesapları** hızlı sekmesinde **Adyen için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısını seçin.
1. Adyen bağlayıcısı yapılandırıldıktan sonra **Apple Pay için Dynamics 365 Ödeme Bağlayıcısı** bağlayıcısını eklemek için **Ekle**'yi seçin.
1. Bağlayıcı satıcı özellikleri için değerleri girin.

    | Özellik               | Açıklama | Gerekli | Otomatik olarak ayarla | Örnek değer |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Derleme Adı          | Apple Pay için Dynamics 365 Ödeme Bağlayıcısı için derlemenin adı. | Evet | Evet | İkili ad |
    | Hizmet Hesabı Kimliği     | Satıcı özellikleri kurulumunun benzersiz tanımlayıcısı. Bu tanıtıcı ödeme hareketlerine damgalanır ve faturalama gibi aşağı akış süreçlerinin kullanması gereken tüccar özelliklerini tanımlar. | Evet | Evet | Guid |
    | Satıcı Hesabı Kimliği    | Benzersiz Adyen tüccar tanıtıcısını girin. Bu değer, [Adyen'e kaydolma](adyen-connector-setup.md#sign-up-with-adyen) bölümünde açıklandığı gibi, Adyen'e kaydolduğunuzda sağlanır. | Evet | No. | MerchantIdentifier |
    | Bulut API Anahtarı          | Adyen bulut API anahtarını girin. Bu anahtarı edinmek için [API anahtarı edinme](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) bölümündeki yönergeleri izleyin. | Evet | No. | abcdefg |
    | Ağ Geçidi Ortamı    | Eşlenecek Adyen ağ geçici ortamını girin. Olası değerler **Test** ve **Canlı**'dır. Bu alanı yalnızca üretim cihazları ve işlemler için **Canlı** olarak ayarlamalısınız. | Evet | Evet | Canlı |
    | Desteklenen Para Birimleri   | Bağlayıcının işlemesi gereken para birimlerini girin. Kart mevcut senaryolarda, işlem isteği ödeme terminaline gönderildikten sonra Adyen [dinamik para birimi dönüştürme](https://www.adyen.com/pos-payments/dynamic-currency-conversion) ile diğer para birimlerini destekleyebilir. Desteklenen para birimlerinin listesini almak için Adyen desteğine başvurun. | Evet | Evet | USD;EUR |
    | Desteklenen Ödeme Türleri | Bağlayıcının işlemesi gereken ödeme türlerini girin. | Evet | Evet | ApplePay |

1. Satıcı bilgileri girildikten sonra, **1070** kanal yapılandırması dağıtım zamanlaması işini çalıştırın.


### <a name="configure-content-security-policies-in-site-builder"></a>Site oluşturucuda içerik güvenlik ilkelerini yapılandırma

Parçalarınızı ya da sayfalarınızı Apple Pay kullanmak üzere yapılandırabilmek için içerik güvenliği ilkelerinin (CSP'ler) siteniz için Commerce site oluşturucusunda yapılandırıldığından emin olmanız gerekir.

İçerik güvenliği ilkelerinizi site oluşturucusunda yapılandırmak için aşağıdaki adımları izleyin.

1. **Site Ayarları \> Uzantılar**'a gidin.
1. **İçerik güvenliği ilkesi** sekmesinde `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` içeren bir satırı **child-src**, **connect-src**, **frame-src**, **img-src**, **script-src**, ve **style-src** bölümlerine eklemek için **Ekle**'yi seçin.
1. Tamamladığınızda değişikliklerin işlenmesi için **Kaydet ve yayımla**'yı seçin.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Ödeme seçeneği olarak Apple Pay'i ayarlama

Apple Pay'i sitenizin (hızlı olmayan) ödeme sayfasında bir ödeme seçeneği olarak ayarlamak için bu adımları izleyin.

1. Site oluşturucusunda, **Parçalar**'a gidin ve sonra da sitenizin ödeme parçasını seçin.
1. **Düzenle** öğesini seçin.
1. **Ödeme bölümü konteyneri** yuvasında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Apple Pay** modülünü ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin.
1. Parçayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

**Apple Pay** modülü ayarları modülde yerleşik olarak bulunur ve Commerce headquarters'ta çevrimiçi kanal için ayarlanan yapılandırılmış Apple Pay için Dynamics 365 Ödeme Bağlayıcısı'a bağlanır.

### <a name="apple-pay-payment-behavior"></a>Apple Pay ödeme davranışı

**Apple Pay** ödeme düğmesi, yalnızca desteklenen Apple Pay cihazlarında (iPhones, iPads ve Apple Pay'i destekleyen Safari tarayıcılarda) desteklenir. Kullanıcı bu cihazlardan birini kullanmıyorsa **Apple Pay** ödeme düğmesi görünümden gizlenir.

Kullanıcı **Apple Pay** ödeme düğmesini seçtiğinde **Apple Pay** iletişim kutusu görüntülenir. Kullanıcı bu iletişim kutusunda Apple Pay cihazı veya tarayıcısı ile kimlik doğrulaması yapabilir. **Apple Pay** iletişim kutusunda sipairş tutarı ve kullanıcının Apple Wallet için yapılandırdığı ödeme yöntemi gösterilir. Kullanıcı bu ayrıntıları inceleyip ödemeye devam etmek için **Öde**'yi seçebilir. Ödeme tamamlandıktan sonra, kullanıcı tamamlanan işleme ilişkin ayrıntılı sipariş özetini gösteren **Sipariş Tamamlandı** sayfasına yönlendirilir.

## <a name="configure-commerce-pos-for-apple-pay"></a>Apple Pay için Commerce POS yapılandırma

POS yapılandırması Adyen için Dynamics 365 Ödeme Bağlayıcısı'na donanım profilinin **EFT hizmeti** alanındaki yapılandırmayı kullanır. Commerce headquarters'ta Adyen için Dynamics 365 Ödeme Bağlayıcısı EFT hizmetini [Dynamics 365 POS donanım profili ayarlama](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile) bölümünde açıklandığı şekilde yapılandırın.

**Desteklenen ödeme tüleri** alanındaki ödeme türleri listesine **ApplePay** eklediğinizden emin olun. Listedeki ödeme türlerini ayırmak için noktalı virgül (;) kullanın.

Adyen bağlayıcısı için işlemci eşlemesi Apple Pay'in POS terminalinde kullandığı cüzdan kartı türlerini yakalar.

## <a name="additional-resources"></a>Ek kaynaklar

[Ödemeler ile ilgili SSS](payments-retail.md)

[Ödeme yapma modülü](../add-checkout-module.md)

[Ödeme modülü](../payment-module.md)
