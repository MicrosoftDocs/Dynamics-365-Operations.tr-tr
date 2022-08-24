---
title: Adyen için Dynamics 365 Commerce Payment Connector ile bağlantılı olmayan geri ödemeleri işleme
description: Bu makalede, Adyen için Microsoft Dynamics 365 ödeme konnektörü kullanıldığında bağlantısız para iadelerini nasıl çalıştığı açıklanmaktadır.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 2b2bee7ad45bbff82c8b7de2741925fde29d8583
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284324"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Adyen için Dynamics 365 Commerce Payment Connector ile bağlantılı olmayan geri ödemeleri işleme

[!include [banner](../includes/banner.md)]

Bu makalede, [Adyen için Microsoft Dynamics 365 ödeme konnektörü](adyen-connector.md) kullanıldığında bağlantısız para iadelerini nasıl çalıştığı açıklanmaktadır. Ayrıca, satış noktasında (POS) veya çağrı merkezinde yeni bir ödeme yöntemiyle para iadesi işleme yeteneğini de gözden geçirir.

Adyen için Dynamics 365 ödeme konnektörü, orijinal hareket için kullanılandan farklı bir ödeme yöntemi kullanarak para iadelerini işleme yeteneğini destekler. Sağlanan kaynak ödeme yöntemine karşı para iadesini işlemek için [bağlantılı para iadelerini](linked-refunds.md) kullanmanızı öneririz, ancak bazı senaryolarda farklı bir yönteme yapılan para iadesi gereklidir. Örneğin, orijinal ödeme için kullanılan kartın artık süresi geçmiş veya kaybolmuş olabilir veya Kullanıcı tarafından iptal edilmiş olabilir.

## <a name="prerequisites"></a>Önkoşullar

Aşağıdaki önkoşulların, Adyen için Dynamics 365 ödeme bağlayıcısının bağlantısız para iadelerini işleyebilmesi için tamamlanması gerekir:

- [Ödeme yöntemlerini](../payment-methods.md) ayarlayın.
- [Çok yönlü kanal ödemeleri](../omni-channel-payments.md) ayarlayın.

## <a name="additional-configuration"></a>Ek yapılandırma

Dynamics 365 Payment Connector for Adyen, sonraki bölümde tanımlanan her desteklenen geri ödeme için kullanıma hazır uygulama sağlar. Adyen için Dynamics 365 ödeme bağlayıcısının kutulu uygulamasını kullanmayan müşterilerin, kredi kartlarının simgeleştirme şeklini destekleyen bağlayıcıyı kurmanız gerekir.

## <a name="supported-refund-scenarios"></a>Desteklenen geri ödeme senaryoları

Dynamics 365 Commerce, önceden onaylanmış ve doğrulanmış hareketlerin geri ödemelerini destekler. Geri ödemeler, hareketin tam iadesi ya da kısmi geri ödeme bilgisinden oluşabilir. Geri ödemeler, orijinal ödeme yetkilendirmesi tam tutarını aşamaz. Bağlantısız para iadeleri yalnızca POS ve çağrı merkezi 'nde desteklenir.

## <a name="enable-unlinked-refunds-functionality"></a>Bağlantısız para iadesi işlevini etkinleştir

Commerce genel merkezinde bağlantısı kaldırılmış geri ödemeler işlevini etkinleştirmek için şu adımları izleyin.

1. **Retail ve Commerce \> Headquarters ayarı \> Parametreler \> Paylaşılan Commerce parametreleri**'ne gidin.
1. **Çoklu kanal ödemeleri** sekmesinde, **Çoklu kanal ödemeleri kullan** seçeneğini **Evet** olarak ayarlayın.

### <a name="supported-payment-method-variants"></a>Desteklenen ödeme yöntemi çeşitleri

Aşağıdaki ödeme yöntemi türevleri kutunun dışında bağlantısız para iadelerini destekler:

- Kartlar
- Cüzdan

Tüm ödeme yöntemi çeşitleri bağlantısız para iadelerini desteklemez. Aşağıdaki tabloda, genel ödeme yöntemlerinin listesi yer almaktadır ve her yöntemin, bağlı ve bağlantısız para iadelerini sağlayan destek yetenekleri gösterilmiştir.

| Ödeme yöntemi        | Bağlantılı geri ödeme | Bağlantılı olmayan geri ödeme |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Evet           | Evet             |
| amexconsumer          | Evet           | Evet             |
| amexcorporate         | Evet           | Evet             |
| amexdebit             | Evet           | Evet             |
| amexprepaid           | Evet           | Evet             |
| amexprepaidreloadable | Evet           | Evet             |
| amexsmallbusiness     | Evet           | Evet             |
| discover              | Evet           | Evet             |
| maestro               | Evet           | Evet             |
| maestrouk             | Evet           | Evet             |
| mc                    | Evet           | Evet             |
| mcalphabankbonus      | Evet           | Evet             |
| mcprepaidanonymous    | Evet           | Evet             |
| visa                  | Evet           | Evet             |
| visaalphabankbonus    | Evet           | Evet             |
| visacheckout          | Evet           | Evet             |
| visadankort           | Evet           | Evet             |
| visahipotecario       | Evet           | Evet             |
| visasaraivacard       | Evet           | Evet             |
| vpay                  | Evet           | Evet             |
| givex                 | **Hayır**        | Evet             |
| svs                   | **Hayır**        | Evet             |
| cup                   | Evet           | Evet             |
| diners                | Evet           | Evet             |
| interac               | **Hayır**        | Evet             |
| jcb                   | Evet           | Evet             |
| jcb_applepay          | Evet           | Evet             |
| unionpay              | Evet           | Evet             |

### <a name="process-an-unlinked-refund-in-pos"></a>POS'ta bağlantısız para iadesini işle

Bir müşteri bir maddeyi iadeler için izin verilen dönem içinde bir POS kasiyerini iade edin ve geçerli bir girişi vardır. İade için işlem sırasında **Ödemeyi iade et** iletişim kutusu bir **ödeme yöntemi Seç** seçeneği içerir. Böylece kasiyer, para iadesi (kartlar ve cüzdan) için desteklenen ödeme yöntemleri arasında bir ödeme yöntemi seçebilir.

### <a name="process-an-unlinked-refund-in-call-center"></a>Çağrı merkezinde bağlantısız para iadesini işle

Bağlantısız geri ödeme, çağrı merkezindeki bir siparişle ilgili olarak işlendiyse, Çağrı Merkezi çalışanı kaynak yöntemden farklı bir ödeme yöntemi seçer. Bundan sonra çalışana bir yönetici geçersiz kılma kişisel kimlik numarası (PIN) elde etmek istenir. Ödeme için farklı ödeme yönteminin işlenmesiyle önce PIN gereklidir.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Arama Merkezi için yönetici geçersiz kılma PIN'i ayarla

Commerce Headquarters'da arama merkezi için bir yönetici geçersiz kılma PIN'i ayarlamak için aşağıdaki adımları izleyin.

1. **Perakende ve Ticaret \> Kanal kurulum \> Çağrı Merkezi kurulumu**'na gidin veya "izinleri geçersiz kıl" arayın.
1. Bağlantısız olarak yapılan geri ödeme izinleri için rol seçin.
1. **Geri ödemeler** hızlı sekmesinde, **Alternatif ödemeye izin izin ver** seçeneğini **Evet** olarak ayarlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Adyen için Dynamics 365 Payment Connector](adyen-connector.md)

[Önceden onaylanmış ve doğrulanmış hareketlerin bağlı iadesi](linked-refunds.md)
