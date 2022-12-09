---
title: Mobil platformlar için Store Commerce uygulaması
description: Bu makalede Android ve iOS için Microsoft Dynamics 365 Commerce Store Commerce uygulamasının nasıl kullanılacağı anlatılmaktadır.
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815796"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Mobil platformlar için Store Commerce uygulaması

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makalede Android ve iOS için Microsoft Dynamics 365 Commerce Store Commerce uygulamalarının nasıl kullanılacağı anlatılmaktadır.

Android için iOS Dynamics 365 Commerce mobil uygulamaları, tam özellikli mobil satış noktası (POS) cihazlarını perakende ortamınız için daha kolay ve basit bir şekilde dağıtmanızı sağlar. Store Commerce mobil uygulamaları neredeyse [Windows için Store Commerce](store-commerce.md)'in tüm yetenek ve avantajlarını sunar ve çok çeşitli iOS ve Android telefon ve tablette düzgün çalışır. Store Commerce mobil uygulamaları, Apple ve Google Play uygulama mağazalarından doğrudan indirilebilir; geliştiricilerin dağıtım veya güncelleştirme için yeni bir uygulama paketi oluşturması gerekmez. 

Store Commerce mobil uygulamaları, geçerli Retail karma uygulamalarıyla işlevsel olarak tamamıyla eşittir. Ek olarak, iOS için Store Commerce uygulamasında donanım istasyonu desteği bulunur. Böylece iOS cihazları, paylaşımlı donanım istasyonu dağıtımına ihtiyaç duymaksızın ağa bağlı ödeme terminalleri, makbuz yazıcıları ve kasa çekmeceleri ile iletişim kurabilir. 

> [!IMPORTANT]
> Windows, Android ve iOS için Store Commerce uygulamaları, Dynamics 365 Commerce için yeni nesil POS uygulamalarıdır. Store Commerce uygulamaları, öncellerine göre çok sayıda geliştirme sunmasının yanı sıra tüm işlevlere ve özellik eşliğine sahiptir. Microsoft, 2023 yılının ilerleyen bölümünde MPOS ile Android ve iOS Retail POS karma uygulamalarını kullanım dışı bırakacaktır ve tüm yeni POS dağıtımlarınız için Store Commerce veya Cloud POS (CPOS) kullanmanızı önerir. Varolan müşteriler, Retail karma uygulamalarından Store Commerce'e geçme planı yapmalıdır. Daha fazla bilgi için bkz. [Modern POS'u Store Commerce'a geçirme](pos-extension/migrate-mpos-store-commerce.md). 

## <a name="app-architecture"></a>Uygulama mimarisi

Store Commerce mobil uygulamaları, karma modda dağıtıldığında Windows için Store Commerce uygulaması ile aynı topolojiyi kullanır. Store Commerce mobil uygulamaları, CPOS'u doğrudan Commerce Scale Unit'ten (CSU) işleyen ve CSU kullanarak Gözetimsiz Commerce ve Commerce headquarters'a bağlayan kabuk uygulamalarıdır. Kabuk uygulama modeli, Store Commerce uygulamalarının ödeme terminali, yazıcı, para çekmecesi ve diğer çevre birimleri ile doğrudan tümleştirme için adanmış bir donanım istasyonunu desteklemesine olanak sağlar. Donanım aygıtlarını kullanmak için paylaşılan bir donanım istasyonu kurmanız gerekmez. 

Store Commerce mobil uygulamasını güncelleştirmek için CSU'yu güncelleştirmeniz yeterlidir. Uygulama, tüm yeni POS işlev ve özelliklerini otomatik olarak alır. CSU'nun nasıl güncelleştirileceğine ilişkin daha fazla bilgi için bkz. [Güncelleştirme ve uzantıları Commerce Scale Unit'e (bulut) uygulama](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Kabuk uygulamaları, uygulama mağazası güncelleştirmeleri aracılığıyla hizmet verir. Alt sürüm genel kullanıma eriştiğinde Microsoft bunu uygulama mağazalarına yayımlar. Microsoft, yüksek öncelikli hata düzeltmelerini serbest bırakmak üzere alt sürüm güncelleştirmeleri arasında yama da yayımlayabilir.

## <a name="prerequisites"></a>Ön Koşullar

Store Commerce mobil uygulamaları için başta Commerce headquarters ve CSU bileşenleri olmak üzere Dynamics 365 Commerce gereklidir. Aşağıdaki tabloda Android ve iOS mobil uygulamaları için gereken en düşük işletim sistemi ve CSU sürümleri listelenmiştir. 

| Önkoşul | Android      | iOS  |
| ------------ | ------------ | ---- |
| İşletim sistemi sürümü   | 7.0          | 15.0 |
| CSU sürümü  | 9.38.22266.8 | Hesaplanacak  |

## <a name="install-the-app"></a>Uygulamayı yükleme

Store Commerce mobil uygulamalarını doğrudan Google Play mağazasından veya Apple App Store'dan yükleyebilirsiniz. 

- [Android için Store Commerce uygulaması](https://aka.ms/storecommerceandroid)
- [iOS için Store Commerce uygulaması](https://aka.ms/storecommerceios)

Android uygulama (.apk) veya Apple uygulama (.ipa) paketleri, Microsoft Dynamics Lifecycle Services'te bulunan Paylaşılan varlık kitaplığından da indirilebilir. 

## <a name="device-and-register-setup"></a>Cihaz ve kayıt kurulumu

Kayıt, Store Commerce mobil uygulamalarında etkinleştirilmeden önce Commerce headquarters'da cihaz ve kayıt kurmanız gerekir. Daha fazla bilgi için bkz. [Cihaz ve kayıtlar](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Cihaz kurulumu

Yeni bir cihaz oluşturmak ve ayarlamak için aşağıdaki adımları izleyin.

1. Commerce headquarters'da **Retail ve Commerce \> Kanal ayarı \> POS kurulumu \> Cihazlar** adımlarını izleyin. 
1. Yeni bir cihaz seçin ve dağıtımını yaptığınız mobil uygulamaya bağlı olarak uygulama türünü **Modern POS - Android** veya **Modern POS - iOS** olarak seçin. 

    > [!NOTE] 
    > **Modern POS - Android** ve **Modern POS - iOS** uygulama türleri, Android ve iOS için mevcut karma uygulamaları dağıtmak için de kullanılır. MPOS kullanımdan kaldırıldıktan sonra bu uygulama türlerinin etiketleri **Store Commerce - Android** ve **Modern POS - iOS** olarak güncelleştirilecektir. 

### <a name="register-setup"></a>Kayıt kurulumu

Yeni bir kayıt oluşturabilir ve bunu oluşturduğunuz cihazla ilişkilendirebilir veya varolan bir kaydı yeni aygıtınızla ilişkilendirebilirsiniz. Kayıtlar hakkında daha fazla bilgi için bkz. [Kayıt oluşturma ve ilişkilendirme](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Ekran düzeni kurulumu

Dynamics 365 Commerce lisansınızla birlikte gelen demo verilerinde bulunan bir ekran düzenini başka bir amaçla kullanıyorsanız Store Commerce uygulaması, cihazınızın ekran çözünürlüğü dikey yönlendirmede 480 &times; 853 pikselden küçükse ekli kompakt düzeni otomatik olarak seçer. Ancak, ekran düzenini sıfırdan oluşturuyorsanız veya mobil cihazınızın çözünürlüğü kompakt düzenin desteklediğinden büyükse dağıtmayı planladığınız telefon veya tablet için uygun bir çözünürlük ve ilişkili düğme grupları oluşturun. Ekran düzeyi yapılandırmaları hakkında daha fazla bilgi içi bkz. [POS kullanıcı arabirimi görsel yapılandırmaları](../pos-screen-layouts.md). 

Cihaz ve kayıtları yapılandırdıktan sonra Commerce headquarters'da **Retail ve Commerce \> Retail ve Commerce Kimliği \> Dağıtım Planları**'na gidin ve kayıtlar işini çalıştırın.

## <a name="activate-a-device"></a>Cihaz etkinleştir

Store Commerce mobil uygulamasında cihaz etkinleştirmek için aşağıdaki adımları izleyin.

1. Mobil cihazınızda uygulamayı açın.
1. Lifecycle Services'in ortam ayrıntıları sayfasında veya Commerce headquarters'ın **Kanal profilleri** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Kanal profilleri**) görebileceğiniz CPOS URL'sini girin.
1. Cihaz yönetim izni olan çalışanın kimlik bilgilerini kullanarak oturum açın.
1. Commerce headquarters'da oluşturduğunuz veya yeniden kullandığınız kayıt ile ilişkili mağazayı seçin.
1. Commerce headquarters'da oluşturduğunuz cihaz ile ilişkili kaydı seçin.
1. Cihazınız etkinleştirilmelidir. Seçtiğiniz mağaza ile ilişkili çalışanın operatör kimliği ve parolasını kullanarak kayıtta oturum açabilirsiniz. 

Cihaz etkinleştirme ile ilgili daha fazla bilgi için bkz. [Satış noktası (POS) cihazı etkinleştirme](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Windows için Store Commerce ile özellik eşliği

Aşağıdaki tabloda Store Commerce uygulamasının Windows, Android ve iOS platformlarındaki özellikleri karşılaştırılmıştır.

| Özellik                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Adanmış donanım istasyonu                                                            | Evet     | Evet     | Evet |
| Paylaşımlı donanım istasyonu                                                               | Evet     | Evet     | Evet |
| Ağa bağlı çevre birimleri ile iletişim (ödeme terminali, yazıcı ve nakit çekmecesi) | Evet     | Evet     | Evet |
| Yerel donanım istasyonu aracılığıyla Satış Noktası için OLE (OPOS) çevre birimleri             | Evet     | No.      | No.  |
| Çevrimdışı mod                                                                          | Evet     | No.      | No.  |

## <a name="additional-resources"></a>Ek kaynaklar

[Store Commerce uygulaması](store-commerce.md)

[Store Commerce ve Cloud POS arasında seçim yapma](../mpos-or-cpos.md)

[Store Commerce kurulum ve yükleme sorunlarını giderme](../troubleshoot/store-commerce-setup-installation.md)
