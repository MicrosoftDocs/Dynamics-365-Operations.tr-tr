---
title: Adanmış ödeme terminalleri ve yazıcı ve nakit çekmecesini sorar
description: Bu konu, bir adanmış ödeme terminali alma ve kullanıcıdan bir para çekmecesini ve bir makbuz yazıcısı seçmesini sağlayan bilgiler içerir.
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 41b0faa7ef24bdae229f7e6760d22357cb87eb0d
ms.sourcegitcommit: 7b7cc93c0f78c6bfc7a3ea66a74a29ba0f218553
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/04/2020
ms.locfileid: "3658370"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Adanmış ödeme terminalleri ve yazıcı ve nakit çekmecesini sorar

[!include [banner](includes/banner.md)]

Bu konu, bir adanmış ödeme terminali alma ve kullanıcıdan bir para çekmecesini ve bir makbuz yazıcısı seçmesini sağlayan bilgiler içerir.

## <a name="overview"></a>Özet

Modern satıcılar, mağaza içi kullanıma alma deneyimini verimli hale getirmek için yollar arıyor. Elektronik ödemelerden daha az kullanıma yönelik en son eğilimler yalnızca satın alma deneyimini daha iyi hale getirmek için değil, ayrıca tüm mağaza ilişkilendirmelerinde kullanılabilen Çevresel aygıtların eksiksiz olması gereksinimini de azaltır.

Microsoft Dynamics 365 Commerce, bu eğilimleri, bir satış noktası (POS) aygıtında her zaman atanmış bir adanmış ödeme terminali bulunan bir senaryoyu etkinleştirerek destekler, ancak kendi giriş yazıcısı veya para çekmecesini içermez. Yetkililerin, bir teslim alma veya nakit ödemesi alacak durumlarda, bu aygıtların konfigüre edildiği bir donanım İstasyonu seçmesi istenir.

## <a name="key-terms"></a>Önemli terimler

| Vade | Tanım |
|---|---|
| Kaydol | Bir POS kaydının örneğini konfigüre etmek için kullanılan varlık. |
| Aygıt | Bir POS kaydının fiziksel örneğinin ve kendisine atanan Modern POS uygulamasının temsili. |
| Adanmış donanım istasyonu | Donanım istasyonu iş mantığı Modern POS for Windows ve Modern POS for Android uygulamasına yerleşiktir. |
| Çekmece açılış (d/k) bağlantı noktası | Bir makbuz girişine nakit çekmecesini bağlamak için geleneksel yöntem. |
| Ağ çevre birimleri | Ağ etkin ödeme terminalleri, makbuz yazıcıları ve nakit çekmecesi için yerleşik destek. |

## <a name="supported-pos-clients-and-devices"></a>Desteklenen POS istemcileri ve aygıtları

Bu konuda açıklanan işlevsellik Windows için Modern POS ve Android POS istemcileri için Modern POS tarafından desteklenmektedir.

Bu işlevsellik, ağ etkin ödeme terminalleri ve makbuz yazıcılarını destekler. Nakit çekmecesini, d/k bağlantı noktası üzerinden ağ etkin giriş yazıcısına bağlayarak nakit çekmecesi desteği sağlayabilirsiniz.

Bu işlev için yerleşik destek, bir [Adyen için Dynamics 365 Ödeme Konnektörü](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3) tarafından sağlanır. Ancak, diğer ödeme bağlayıcıları, ödemeler için Commerce Software Development Kit (SDK) ile desteklenebilir. Desteklenen makbuz yazıcılar, Star Micronics ve Epson kaynaklı ağ etkin giriş yazıcılarını içerir.

Star Micronics giriş yazıcılarını ayarlamak için, aygıtı ağ üzerinden kullanılacak şekilde yapılandırmak üzere yıldız Micronics yazıcı yardımcı programını kullanın. Bu yardımcı program ayrıca, aygıtın IP adresini de sağlar.

Epson makbuz yazıcılarını ayarlamak için, bu aygıtı ağ iletişim kurallarını kullanacak şekilde ayarlamak üzere Epson ePOS-Print yardımcı programını kullanın.

Ağ çevre birimlerinin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz [Ağ çevre desteği genel bakış](https://go.microsoft.com/fwlink/?linkid=2129965).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Adanmış ödeme terminalleri ve yazıcı ve nakit çekmecesi komutu ayarlayın

### <a name="set-up-hardware-profiles"></a>Donanım profillerini ayarlama

İki tür donanım profiliniz olmalıdır. İlki kayda atanır. İkincisi depolama düzeyindeki bir donanım istasyonuna atanır ve ağ girişi yazıcılarını ve nakit çekmelükisini mantıksal olarak gruplamak için kullanılır.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Kasa için bir donanım profili ayarla

Kasaya atanan donanım profilini ayarlamak için aşağıdaki adımları izleyin.

1. Dynamics 365 Commerce İçinde , **donanım profilini** arayın.
2. **Yeni**'yi seçin.
3. Bir donanım profili numarası atayın ve sonra bir açıklama girin. Bu donanım profili, kasanın kendisine atanacak. Bu nedenle, **geri dönüş ile adanmış** olarak bir açıklama yeterli olacaktır.
4. Farklı aygıt türleri için hızlı sekmelerde aşağıdaki aygıt türlerini ayarlayın.

    | Aygıt | Türü | Aygıt adı | Ek ayrıntılar |
    |---|---|---|---|
    | Yazıcı | Geri dönüş | **Epson** veya **Star** | Aygıt adı büyük/küçük harf duyarlıdır. **Makbuz profılı kodu,**, Kanal düzeyinde donanım istasyonuna atanan donanım profilinde kurulmuş olan ağ yazıcısıyla eşlenen **makbuz profili kimliğiyle** aynı olmalıdır. |
    | Kasa çekmecesi | Geri dönüş | **Epson** veya **Star** | Aygıt adı büyük/küçük harf duyarlıdır. **Paylaşılan mesaiyi kullan** seçeneğinde **Evet**'i işaretleyin. |
    | EFT hizmeti | Adyen | Geçerli değil | Kullanıma hazır Adyen ödeme bağlayıcısını kurma hakkında bilgi için, bkz: [Adyen için Dynamics 365 ödeme konnektörü](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Diğer ödeme bağlayıcıları, ödemeler için [Commerce Software Development Kit (SDK) ile desteklenebilir](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension). |
    | PIN pad | Ağ | **MicrosoftAdyenDeviceV001** | Hiçbiri. |

5. Dynamics 365 Commerce İçinde , **kayıtlar** 'ı arayın.
6. Kasa numarasını seçerek bir kayıt seçin ve **Düzenle** seçeneğini belirleyin.
7. Henüz oluşturduğunuz donanım profilini, adanmış bir ödeme terminali kullanması gereken kasaya atayın. Bu kayıt defteri ile eşlenen aygıtın, Windows için modern POS veya Android için Modern POS uygulaması kullanması gerekir.
8. **Kaydet**'i seçin.
9. Eylem Bölmesi'ndeki **Kayıtlar** sekmesinde, **IP adreslerini yapılandıra**'ni seçin.
10. **PIN pad** hızlı sekmesinde, ödeme terminalinin IP adresini girin. Adyen bağlayıcısını kullanarak ödeme terminali IP adresinin nasıl alınacağı hakkında bilgi için, bkz: [adyen için Dynamics 365 ödeme konnektörü](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).
11. **Kaydet**'i seçin.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Makbuz Yazıcısı ve nakit çekmecesi için donanım profili ayarla

Ağ girişi yazıcısını ve nakit çekmecesini gruplamak için kullanılan donanım profilini ayarlamak için, aşağıdaki adımları izleyin.

1. Dynamics 365 Commerce İçinde , **donanım profilini** arayın.
2. **Yeni**'yi seçin.
3. Bir donanım profili numarası atayın ve sonra bir açıklama girin. Bu donanım profili, giriş yazıcısını ve nakit çekmecesini gruplamak için kullanılacak. Bu nedenle, **ağ yazıcısı ve nakit çekmecesi** gibi bir açıklama yeterli olacaktır.
4. Farklı aygıt türleri için hızlı sekmelerde aşağıdaki aygıt türlerini ayarlayın.

    | Aygıt | Türü | Tanım | Ek ayrıntılar |
    |---|---|---|---|
    | Yazıcı | Ağ | **Epson** veya **Star** | Aygıt adı büyük/küçük harf duyarlıdır. **Makbuz profılı kodu,**, kayda atanan donanım profilinde kurulmuş olan yazıcısıyla eşlenen **makbuz profili kimliğiyle** aynı olmalıdır. |
    | Kasa çekmecesi | Geri dönüş | **Epson** veya **Star** | Aygıt adı büyük/küçük harf duyarlıdır. **Paylaşılan mesaiyi kullan** seçeneğinde **Evet**'i işaretleyin. |

5. **Kaydet**'i seçin.

### <a name="set-up-hardware-stations"></a>Donanım istasyonu ayarlama

İki donanım istasyona sahip olmalısınız. İlki kasaya eşlenelecektir. İkincisi, gerektiğinde, bir girişin yazdırılması gerektiğinde veya bir nakit çekmecesinin açık olması halinde seçildiğinde seçilir.

#### <a name="register-a-hardware-station"></a>Donanım istasyonu kaydetme

1. Dynamics 365 Commerce İçinde , **tüm mağazalar** için arama yapın.
2. **Perakende Kanal kimlik** değerlerini seçerek bir mağaza seçin ve sonra **Düzenle** 'ı seçin.
3. **Donanım istasyonları** hızlı sekmesinde **Ekle**'yi seçin.
4. **Donanım istasyon türü** alanını **adanmış** olarak ayarlayın.
5. Bir açıklama girin, ancak bu donanım İstasyonu için başka değer ayarlamayın. Bu donanım İstasyonu, kayıt için her zaman kullanılacak. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Makbuz Yazıcısı ve nakit çekmecesi için donanım istasyonu ayarla

1. Dynamics 365 Commerce İçinde , **tüm mağazalar** için arama yapın.
2. **Perakende Kanal kimlik** değerlerini seçerek bir mağaza seçin ve sonra **Düzenle** 'ı seçin.
3. **Donanım istasyonları** hızlı sekmesinde **Ekle**'yi seçin.
4. **Donanım istasyon türü** alanını **adanmış** olarak ayarlayın.
5. Açıklama girin. Bu donanım istasyonu, giriş yazıcısını ve nakit çekmecesini gruplamak için kullanılacak.
6. **Donanım profili** alanında, giriş yazıcısı ve nakit çekmecesi için daha önce oluşturduğunuz donanım profilini seçin.
7. **Kaydet**'i seçin.
8. Makbuz Yazıcısı ve nakit çekmecesi için donanım İstasyonu hala seçiliyken, **IP adreslerini Yapılandır**'ı seçin.
9. Yazıcının IP adresini alın ve hem Makbuz Yazıcısı hem de nakit çekmecesini IP adresi olarak girin.
10. **Kaydet**'i seçin
11. **Dağıtım zamanlamalarını** arayın.
12. **1090** dağıtım zamanlamasını seçin ve **şimdi Çalıştır**'ı seçin.
13. **1070** dağıtım zamanlamasını seçin ve **şimdi Çalıştır**'ı seçin.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Sistemi, gerektiğinde giriş yazıcısı ve nakit çekmecesi seçimini isteyecek şekilde ayarlar

1. Desteklenen bir POS istemcisinde, bir vardiya açıksa, geçerli vardiyayı kapatın.
2. Oturum açın ve **çekmece olmyan çekmece operasyonları** seçin.
3. Donanım istasyonunu açmak için **donanım istasyonlarını Yönet** işlemini kullanın.
4. Kaydın etkin hale getirmek üzere kayıt için oluşturduğunuz donanım istasyonunu seçin.
5. POS oturumunu kapatın ve vardiya açın.

Donanım profiline atanan ödeme terminali şimdi etkin olacak ve bir makbuz yazıcısı veya nakit çekmecesi gerektiğinde sizden istemde bulunulacaktır.

Bu özelliği isteyen birçok tüccarlar, e-posta alındıları ve elektronik ödemeleri teşvik ederek atık azaltmakla ilgileniyor. POS konfigürasyonuna bağlı olarak, yalnızca bir müşteri fiziksel bir giriş istediğinde veya nakit ödeme yapmak istediğinde, mağaza yetkililer tarafından bir makbuz yazıcısı veya nakit çekmecesi seçmesi istenir.

Mağaza ile ilgili bir girişin yazdırılması ve ödeme için nakit kullanılması gerekse, ancak başlangıçta seçilen donanım profilinde her iki aygıtı dahil etmek için mağaza çalışanlarının bir donanım istasyonunu yalnızca bir kez seçmesi istenir. Bu durumda, mağaza ilişkilendirme işlemi, hareketi tamamlamak için kullanılabilecek bir donanım istasyonunu seçmek amacıyla yeniden size bildirilir.

## <a name="related-articles"></a>İlgili makaleler

- [Android ve iOS'ta POS Hybrid uygulamasını ayarlama](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [Adyen için Dynamics 365 Ödeme Bağlayıcısı](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [Ağ çevrebirim desteğine genel bakış](https://go.microsoft.com/fwlink/?linkid=2129965)
