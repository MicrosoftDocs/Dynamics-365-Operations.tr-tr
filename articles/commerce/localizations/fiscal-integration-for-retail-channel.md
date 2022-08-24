---
title: Commerce kanalları için mali tümleştirmeye genel bakış
description: Bu makale, Dynamics 365 Commerce içinde kullanılabilen mali tümleştirme yeterliliklerine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 0a56df2a463153c6c3986ce84907e25ea7d965b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286512"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Commerce kanalları için mali tümleştirmeye genel bakış

[!include [banner](../includes/banner.md)]

Bu makale, Dynamics 365 Commerce içinde kullanılabilen mali tümleştirme yeterliliklerine bir genel bakıştır. 

Mali tümleştirme, satışların yerel mali yasalar ile mali kaydını etkinleştiren ve perakende sektöründe veri kaçakçılığını önlemeyi amaçlayan çeşitli mali cihazlar ve servisler ile tümleştirmedir. Mali tümleştirme ile kapsanabilecek bazı tipik senaryolar şunlardır:

- Satış noktası (POS) ile bağlantılı bir mali cihazda bir satışı kaydetmek, örneğin mali yazıcı gibi ve müşteriye bir mali giriş yazdırmak.
- Retail POS içinde tamamlanan satışlar ve iadeler için veri dairesi tarafından işletilen harici bir web hizmetine güvenli bir biçimde bilgi göndermek.
- Dijital imzalar kullanarak satış hareketlerini değiştirilememesini garanti etmek.

Mali tümleştirme işlevi, Retail POS ve mali cihazlar ve servisler arasındaki tümleştirmeyi daha da geliştirmek ve özelleştirmek için ortak çözüm sağlayan bir çerçevedir. Bu işlev, belirli ülkeler ve bölgeler için temel senaryolarını destekleyen mali tümleştirme örnekleri de içerir ve belirli mali cihazlar ve servisler ile çalışır. Mali tümleştirme örneği, Commerce bileşenlerinin çeşitli eklentilerinden oluşur ve yazılım geliştirme paketine (SDK) dahildir. Mali tümleştirme örnekleri hakkında daha fazla bilgi için bkz. [Commerce SDK'sinde mali tümleştirme örnekleri](#fiscal-integration-samples-in-the-commerce-sdk). Commerce SDK'sini yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Mali tümleştirme örneği tarafından desteklenmeyen diğer senaryoları desteklemek için, Retail POS'u diğer mali cihazlar ve hizmetlerle tümleştirmek veya diğer ülke ve bölgelerin gereksinimlerini karşılamak için mevcut mali tümleştirme örneğini genişletmeniz veya mevcut bir örneği örnek olarak kullanarak yeni bir örnek oluşturmanız gerekir.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Mali kayıt işlemi ve mali cihazlar ile cihazmar için mali tümleştirme örnekleri

Retail POS mali kayıt işleminde bir veya birden çok adımdan oluşur. Her adım belirli hareketlerin veya etkinliklerin bir mali cihaz veya serviste mali kaydını içerir. Aşağıdaki çözüm bileşenleri, bir mali cihaz veya hizmetteki mali kayıtta yer alır:

- **Mali belge sağlayıcısı** - Bu bileşen, hareket/etkinlik verisini mali cihaz veya hizmet ile etkileşimde de kullanılan biçimde serileştirir, mali cihaz veya hizmetten gelen yanıtları ayrıştırır ve yanıtları kanal veritabanına kaydeder. Uzantı, kaydedilmesi gereken belirli hareketleri ve etkinlikleri de tanımlar.
- **Mali bağlayıcı** - Bu bileşen, mali cihaz veya hizmet ile iletişimi başlatır, talepleri ve doğrudan komutları mali cihaz veya hizmete, mali belgeden çıkartılan hareket/etkinlik verisine dayanarak gönderir ve mali cihazdan gelen yanıtları alır.

Mali tümleştirme örneği, bir mali belge sağlayıcısı ve bir mali bağlayıcı için Commerce Runtime (CRT), Donanım istasyonu ve POS uzantıları içerir. Ayrıca aşağıdaki yapılandırma bileşeni içerir:

- **Mali belge sağlayıcı yapılandırması** - Bu yapılandırma, bir çıkış yöntemini ve mali belgeler için bir biçimi tanımlar. Ayrıca, veriler ve ödeme yöntemleri için bir veri eşleme de içerir, böylece Retail POS'tan gelen veriyi mali cihaz veya hizmet yazılımında önceden belirlenmiş değerler ile uyumlu hale getirir.
- **Mali bağlayıcı yapılandırması** - Bu yapılandırma, belirli bir mali cihaz veya hizmet ile fiziksel iletişimi tanımlar.

Belirli bir POS kaydı için bir mali kayıt işlemi, POS işlev profilindeki karşılık gelen ayar ile tanımlanır. Mali kayıt işlemi hakkında daha fazla ayrıntı için, mali belge sağlayıcısını ve mali bağlayıcı yapılandırmalarını karşıya yükleyin ve yapılandırma parametrelerini değiştirin bkz. [Mali kayıt işlemi ayarlamak](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Ürün katalog araması, müşteri araması veya hareket taslak oluşumu gibi mali olmayan işlemler için cihazlara ihtiyaç duyuyorsanız bunları, mali işlem kısıtlamaları olan kasalar olarak seçebilirsiniz. Daha fazla bilgi için bkz. [Mali kasa kısıtlamaları olan kasalar kurma](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Aşağıdaki tipik mali kayıt akışı POS'taki bir olayla başlar (örneğin, bir satış hareketinin sonlandırılması) ve diğer Commerce bileşenlerini (CRT ve Donanım istasyonu gibi) içeren önceden tanımlanmış bir adım dizisi uygular.

1. POS, mali tümleştirme çerçevesinden (FIF) bir mali belge talep eder.
1. FIF, geçerli etkinliğin mali kayıt gerektirip gerektirmediğini belirler.
1. Mali kayıt işlemi ayarlarına dayalı olarak, FIF bir mali bağlayıcıyı ve mali kayıt için kullanılacak karşılık gelen mali belge sağlayıcısını belirler.
1. FIF, bir hareket veya etkinliği temsil eden bir mali belge oluşturan mali belge sağlayıcısını çalıştırır (ör. bir XML belgesi).
1. FIF, oluşturulan mali belgeyi POS'a iade eder.
1. POS, FIF'nin mali belgeyi mali cihaza veya hizmete göndermesini ister.
1. FIF, mali belgeyi işleyen mali bağlayıcıyı çalıştırır ve bunu mali cihaz veya hizmete gönderir.
1. FIF, mali yanıtı (mali cihazın veya hizmetin yanıtı) POS'a iade eder.
1. POS, mali yanıtı analiz ederek mali kaydın başarılı olup olmadığını anlar. POS, gerektiğinde, FIF'nin oluşan hataları işlemesini ister. 
1. POS, FIF işleminin mali yanıtı işlemesini ve kaydetmesini ister.
1. Mali belge sağlayıcısı mali yanıtı işler. Bu işlemenin bir parçası olarak, mali belge sağlayıcısı yanıtı ayrıştırır ve genişletilmiş verileri bu dosyadan ayıklar.
1. FIF, yanıtı ve genişletilmiş verileri kanal veritabanına kaydeder.
1. POS, gerektiğinde donanım istasyonuna bağlı olan sıradan bir makbuz yazıcısıyla bir makbuz yazdırır. Makbuz, mali yanıttan gerekli verileri içerebilir.
 
Aşağıdaki örnek, tipik mali cihaz veya hizmetler için mali kayıt yürütme akışları mali bir cihazı gösterir.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Mali kayıt, donanım istasyonuna bağlı bir cihaz aracılığıyla yapılır

Bu yapılandırma, mali yazıcı gibi bir fiziksel mali aygıt donanım istasyonuna bağlandığında kullanılır. Ayrıca, bir mali aygıtla veya hizmetle yüklü yazılımlar aracılığıyla iletişim kurulduğunda, donanım istasyonunda da geçerlidir. Bu durumda, mali belge sağlayıcısı CRT üzerinde bulunur ve mali bağlayıcı donanım istasyonunda bulunur.

![Mali kayıt, donanım istasyonuna bağlı bir cihaz aracılığıyla yapılır.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Mali kayıt bir harici hizmet aracılığıyla yapılır

Bu yapılandırma, mali kayıt vergi dairesi tarafından sağlanan bir web hizmeti gibi bir harici hizmet aracılığıyla yapıldığında kullanılır. Bu durumda, mali belge sağlayıcısı ve mali bağlayıcı, CRT üzerinde bulunur.

![Mali kayıt bir harici hizmet aracılığıyla yapılır.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Mali kayıt, CRT üzerinde dahili olarak yapılır

Mali kayıt için harici bir mali aygıt veya hizmet gerekli olmadığında bu yapılandırma kullanılır. Örneğin, mali kayıt satış hareketlerinin dijital imzaları aracılığıyla yapıldığında kullanılır. Bu durumda, mali belge sağlayıcısı ve mali bağlayıcı, CRT üzerinde bulunur.

![Mali kayıt, CRT üzerinde dahili olarak yapılır.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Mali kayıt yerel ağdaki bir aygıt veya hizmet yoluyla yapılır

Bu yapılandırma, deponun yerel ağında bir fiziksel mali aygıt veya mali servis olduğunda kullanılır ve bir HTTPS uygulama programlama arabirimi (API) sağlar. Bu durumda, mali belge sağlayıcısı CRT üzerinde bulunur ve mali bağlayıcı POS'ta bulunur.

![Mali kayıt yerel ağdaki bir aygıt veya hizmet yoluyla yapılır.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Hata işleme

Mali tümleştirme çerçevesi, mali kayıt sırasındaki başarısızlıkları ele almak için aşağıdaki seçenekleri sunar:

- **Yeniden deneme** – Operatörler, bu seçeneği başarısızlık hızlıca çözümlenebildiğinde kullanırlar ve mali kayıt yeniden yürütülebilir. Örneğin, bu seçenek mali cihaz bağlı olmadığında, mali yazıcının kağıdı bittiğinde veya mali yazıcıda bir kağıt sıkışması olduğunda kullanılabilir.
- **İptal** – Bu seçenek, operatörlerin, geçerli mali hareket veya etkinlik başarısız olduğunda ertelemesine izin verir. Kayıt ertelendikten sonra, operatör POS üzerinde çalışmaya devam edebilir ve mali kaydın gerekli olmadığı herhangi bir operasyonu tamamlayabilir. Mali kayıt gerektiren herhangi bir etkinlik POS içinde gerçekleştiğinde (ör. yeni bir kayıt açıldığında), hata işleme iletişim kutusu operatörü önceki hareketin doğru biçimde kaydedilmediğini uyarmak ve hata işleme seçeneklerini sunmak için açılır.
- **Atla** - Operatörler bu seçeneği mali kayıt belirli koşullarda atlanabileceği durumlarda ve operasyonların POS üzerinde devam edebileceği durumlarda kullanabilirler. Örneğin, bu seçenek mali kaydın başarısız olduğu bir satış işlemi için kullanılabilir ve özel bir kağıt günlükte kaydedilebilir.
- **Kaydedildi olarak işaretle** - Operatörler bu seçeneği hareket gerçekten de mali cihazda kaydedilmişse (örneğin, bir mali giriş yazdırılmışsa), ancak mali yanıt kanal veritabanına kaydedildiğinde bir hata oluşmuşsa kullanabilirler.
- **Ertele** – Operatörler, kayıt servisi kullanılamadığı için kayıtlı olmadığında bu seçeneği kullanabilir. 

> [!NOTE]
> **Atla**, **Kaydedildi olarak işaretle** ve **Ertele** seçeneklerinin kullanılmadan önce mali kayıt işleminde etkinleştirilmeleri gerekir. Ek olarak, karşılık gelen izinlerin de operatörlere verilmesi gerekir.

**Atla**, **Kaydedildi olarak işaretle** ve **Ertele** seçenekleri, bilgi kodlarının başarısızlık hakkında bazı belirli bilgileri yakalamasına olanak sağlar, başarısızlık hata sebebi ve mali kaydı atlama nedeni veya hareketin kaydedildi olarak işaretlenmesi gibi. Hata el alma parametreleri hakkında daha fazla bilgi için bkz. [Hata ele alma ayarları ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>İsteğe bağlı mali kayıt

Mali kayıt, bazı işlemler için isteğe bağlı ancak bazı diğerleri için zorunlu olabilir. Örneğin, normal satışların ve iadelerin mali kaydı zorunlu olabilir ancak, müşteri mevduatıyla ilişkili operasyonların mali kaydı isteğe bağlı olabilir. Bu durumda, bir satışın mali kaydını tamamlama başarısızlığı, sonraki satışları engellemelidir, ancak bir müşteri mevduatının mali kaydını tamamlama başarısızlığı, sonraki satışları engellememelidir. Zorunlu ve isteğe bağlı operasyonlar arasında ayırt edebilmek için bunları farklı belge sağlayıcıları üzerinden gerçekleştirmenizi ve bu sağlayıcılar için mali kayıt işleminde farklı adımlar ayarlamanızı öneririz. **Hatada devam et** parametresi, isteğe bağlı mali kayıt ile ilişkili her adım için etkin olmalıdır. Hata el alma parametreleri hakkında daha fazla bilgi için bkz. [Hata ele alma ayarları ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Mali kaydı el ile yeniden çalıştırma

Bir hareket veya etkinliğin mali kaydı bir arızadan sonra ertelenirse (örneğin operatör hata işleme iletişim kutsunda **İptal** seçtiyse), mali kaydı karşılık gelen bir eylemi çağırarak el ile yeniden yürütebilirsiniz. Daha fazla bilgi için bkz. [Ertelenen mali kaydın el ile yürütülmesini etkinleştir](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Ertele seçeneği

**Ertele** seçeneği, geçerli adım başarısız olduğunda mali kayıt işlemine devam etmenize olanak sağlar. Bir mali kayıt yedekleme seçeneği olduğunda kullanılabilir.

### <a name="fiscal-registration-health-check"></a>Mali kayıt sağlık denetimi

Mali kayıt için sağlık denetimi prosedürü, mali cihaz veya servisin belirli etkinlikler ortaya çıktığında kullanılabilirliğini doğrular. Mali kayıt şu anda tamamlanamıyor, operatör önceden uyarıldı.

POS, aşağıdaki etkinlikler gerçekleştiğinde sağlık denetimini çalıştırır:

- Yeni bir hareket açılır.
- Askıya alınmış bir hareket geri çağırılır.
- Satış veya iade hareketi sonlandırılır.

Sağlık denetimi başarısız olursa, POS, sağlık denetimi iletişim kutusunu gösterir. Bu iletişim kutusu, aşağıdaki düğmeleri sağlar:

- **Tamam** - Bu düğme, operatörün bir sağlık denetimi hatasını göz ardı etmesini ve işlemi sürdürmey devam etmesine izin verir. Operatörler, bu düğmeyi yalnızca **Sağlık denetimi hatasını atlamaya izin ver** izni bunlar için etkinse seçebilirler.
- **İptal** - Operatör bu düğmeyi seçerse, POS son eylemi iptal eder (örneğin, bir madde yeni bir harekete eklenmemişse).

> [!NOTE]
> Sağlık denetimi yalnızca güncel işlem mali kayıt gerektiriyorsa ve **Hatada devam et** parametresi mali kayı işleminin şu anki adımı için iptal edilmiştir. Daha fazla ayrıntı için bkz. [Hata işleme ayarlarını düzenle](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Mali hareket içinde mali yanıtları depolamak

Bir hareketin veya etkinliğin mali kaydı başarılı olursa, bir mali hareket kanal veritabanında oluşturulur ve orijinal hareket veya etkinliğe bağlanır. Benzer şekilde, **Atla** veya **Kaydedildi olarak işaretle** seçeneği başarısız bir mali kayıt için seçilirse, bu bilgi mali kayıt içinde depolanır. Bir mali kayıt, mali cihaz veya hizmetin mali yanıtını bulundurur. Mali kayıt işlemi çok sayıda adımdan oluşuyorsa, başarılı veya başarısız kayıt ile sonuçlanan mali kayıt işlemin her bir adımı için oluşturulur.

Mali hareketler *P-job* tarafından, hareketlerle birlikte Human Resources'a aktarılır. **Mağaza hareketleri** sayfasındaki **Mali hareketler** hızlı sekmesinde, hareketlerle bağlantılı mali hareketleri görüntüleyebilirsiniz.

Bir mali hareket aşağıdaki ayrıntıları saklar:

- Mali kayıt işlemi ayrıntıları (işlem, bağlantı grubu, bağlayıcı ve benzeri). Ayrıca, mali cihazın seri numarasını da **Kayıt numarası** alanında depolar, şayet bu bilgi mali yanıt içinde dahil edilmişse.
- Mali kaydın durumu: **Tamamlandı**, başarılı kayıt için, **Atlandı** eğer operatör **Atla** seçeneğini başarısız bir kayıt için seçtiyse veya **Kaydedildi olarak işaretlendi** eğer operatör **Kaydedildi olarak işaretle** seçeneğini seçtiyse ya da operatör **Ertele** seçeneğini seçtiyse **Ertelendi**.
- Seçilen bir mali hareket ile ilgili bilgi kodu hareketleri. Bilgi kodu hareketlerini görüntülemek için **Mali hareketler** hızlı sekmesinde, **Atlandı**, **Kaydedildi olarak işaretlendi** veya **Ertelendi** durumunda bir mali hareketi seçin ve sonra **Bilgi kodu hareketleri**'ni seçin.

**Genişletilmiş veri**'yi seçerek mali hareketin bazı özelliklerini de görüntüleyebilirsiniz. Görüntülenebilen özelliklerin listesi, mali hareketi oluşturan mali kayıt işlemine özgüdür. Örneğin, Fransa'da geçerli olan dijital imzalama işlevi için dijital imza, sıra numarası, sertifika parmak izi, karma algoritma tanımlaması ve diğer mali hareket özelliklerini görüntüleyebilirsiniz.

## <a name="fiscal-texts-for-discounts"></a>İskontolar için mali metinler

Bazı ülkeler ve bölgeler, farklı türde iskontolar uygulandığında mali girişler üzerinde yazdırılması gereken ek metinler için gereksinimlere sahiptir. Mali tümleştirme işlevi, bir mali girişteki bir iskonto satırından sonra iskonto için bir özel metin ayarlamanıza olanak sağlar. El ile iskontolar için bir mali metni POS işlevselliği profilindeki **Ürün iskontosu** bilgi kodu olarak belirtilen bir mali metin için yapılandırabilirsiniz. İskontolar için mali metinleri ayarlama hakkında daha fazla bilgi için bkz. [İskontolar için mali metinler ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>X ve Z mali raporları yazdırma

Mali tümleştirme işlevselliği, tümleştirilmiş mali cihaz veya hizmete ilişkin gün sonu bildirimleri oluşturulmasını destekler:

- Karşılık gelen eylemleri çalıştıran yeni düğmelerin POS ekranı düzenine eklenmesi gerekir. Daha fazla bilgi için bkz. [POS'tan mali X/Z raporlarını ayarla](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Mali tümleştirme örneğinde, bu operasyonların mali cihazda karşılık gelen operasyonlarla eşleşmesi gerekir.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Commerce SDK'sindeki mali tümleştirme örnekleri

Aşağıdaki mali tümleştirme örnekleri Commerce SDK'si içerisinde şu anda kullanılabilir:

- [İtalya için yazarkasa tümleştirme örneği](./emea-ita-fpi-sample.md)
- [Polonya için yazar kasa tümleştirme örneği](./emea-pol-fpi-sample.md)
- [Avusturya için mali kayıt hizmeti tümleştirme örneği](./emea-aut-fi-sample.md)
- [Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği](./emea-cze-fi-sample.md)
- [İsveç için kontrol birimi tümleştirmesi örneği](./emea-swe-fi-sample.md)
- [Almanya için mali kayıt hizmeti tümleştirme örneği](./emea-deu-fi-sample.md)
- [Rusya için yazar kasa tümleştirme örneği](./rus-fpi-sample.md)

Aşağıdaki mali tümleştirme işlevi, mali tümleştirme çerçevesi kullanılarak da uygulanır ancak kullanıma hazır olarak sunulur ve Commerce SDK'sine dahil değildir:

- [Brezilya için mali kayıt](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Fransa için dijital imza](./emea-fra-cash-registers.md)

Aşağıdaki mali tümleştirme işlevi de ayrıca Commerce SDK'si içinde kullanılabilir ancak mali tümleştirme çerçevesinin avantajlarından faydalanmaz. Bu işlevin mali tümleştirme çerçevesine geçirilmesi daha sonraki güncelleştirmeler için planlanmıştır.

- [Norveç için dijital imza](./emea-nor-cash-registers.md)

Commerce SDK'sinde kullanılabilen aşağıdaki eski mali tümleştirme işlevi mali tümleştirme çerçevesini kullanmaz ve sonraki güncelleştirmelerde kullanım dışı bırakılacaktır:

- [İsveç için kontrol birimi tümleştirmesi örneği (eski)](./retail-sdk-control-unit-sample.md)
- [Fransa için dijital imza (eski)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
