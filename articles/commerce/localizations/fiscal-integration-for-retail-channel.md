---
title: Commerce kanalları için mali tümleştirmeye genel bakış
description: Bu konu, Dynamics 365 Commerce içinde kullanılabilen mali tümleştirme yeterliliklerine genel bakış sağlar.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 45677681ebae40210d6e2d896323f7e691b765e2
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057568"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Commerce kanalları için mali tümleştirmeye genel bakış

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Giriş

Bu konu, Dynamics 365 Commerce içinde kullanılabilen mali tümleştirme yeterliliklerine bir genel bakıştır. Mali tümleştirme, satışların yerel mali yasalar ile mali kaydını etkinleştiren ve perakende sektöründe veri kaçakçılığını önlemeyi amaçlayan çeşitli mali cihazlar ve servisler ile tümleştirmedir. Mali tümleştirme ile kapsanabilecek bazı tipik senaryolar şunlardır:

- Satış noktası (POS) ile bağlantılı bir mali cihazda bir satışı kaydetmek, örneğin mali yazıcı gibi ve müşteriye bir mali giriş yazdırmak.
- Retail POS içinde tamamlanan satışlar ve iadeler için veri dairesi tarafından işletilen harici bir web hizmetine güvenli bir biçimde bilgi göndermek.
- Dijital imzalar kullanarak satış hareketlerini değiştirilememesini garanti etmek.

Mali tümleştirme işlevi, Retail POS ve mali cihazlar ve servisler arasındaki tümleştirmeyi daha da geliştirmek ve özelleştirmek için ortak çözüm sağlayan bir çerçevedir. Bu işlev, belirli ülkeler ve bölgeler için temel senaryolarını destekleyen mali tümleştirme örnekleri de içerir ve belirli mali cihazlar ve servisler ile çalışır. Mali tümleştirme örneği, Commerce bileşenlerinin çeşitli eklentilerinden oluşur ve yazılım geliştirme paketine (SDK) dahildir. Mali tümleştirme örnekleri hakkında daha fazla bilgi için bkz. [Retail SDK'da mali tümleştirme örnekleri](#fiscal-integration-samples-in-the-retail-sdk). Retail SDK'yi yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Mali tümleştirme örneği tarafından desteklenmeyen diğer senaryoları desteklemek için, Retail POS'u diğer mali cihazlar ve hizmetlerle tümleştirmek veya diğer ülke ve bölgelerin gereksinimlerini karşılamak için mevcut mali tümleştirme örneğini genişletmeniz veya mevcut bir örneği örnek olarak kullanarak yeni bir örnek oluşturmanız gerekir.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Mali kayıt işlemi ve mali aygıtları için mali tümleştirme örnekleri

Retail POS mali kayıt işleminde bir veya birden çok adımdan oluşur. Her adım belirli hareketlerin veya etkinliklerin bir mali cihaz veya serviste mali kaydını içerir. Aşağıdaki çözüm bileşenleri, bir Donanım istasyonuna bağlı olan bir mali cihazdaki mali kayıtta yer alır:

- **Commerce Runtime (CRT) uzantısı** – Bu bileşen, hareket/etkinlik verisini mali cihaz ile etkileşimde de kullanılan biçimde serileştirir, mali cihazdan gelen yanıtları ayrıştırır ve yanıtları kanal veritabanına kaydeder. Uzantı, kaydedilmesi gereken belirli hareketleri ve etkinlikleri de tanımlar. Bu bileşen genellikle *mali belge sağlayıcısı* olarak adlandırılır.
- **Donanım istasyonu uzantısı** - Bu bileşen, mali cihaz ile iletişimi başlatır, talepleri ve doğrudan komutları mali cihaza, mali belgeden çıkartılan hareket/etkinlik verisine dayanarak gönderir ve mali cihazdan gelen yanıtları alır. Bu bileşen genellikle *mali bağlayıcı* olarak adlandırılır.

Bir mali cihaz için mali tümleştirme örneği, bir mali belge sağlayıcısı ve bir mali bağlayıcı ile sırasıyla CRT ve Donanım istasyonlarının uzantılarını içerir. Ayrıca aşağıdaki yapılandırma bileşeni içerir:

- **Mali belge sağlayıcı yapılandırması** - Bu yapılandırma, bir çıkış yöntemini ve mali belgeler için bir biçimi tanımlar. Ayrıca, veriler ve ödeme yöntemleri için bir veri eşleme de içerir, böylece Retail POS'tan gelen veriyi mali cihaz yazılımında önceden belirlenmiş değerler ile uyumlu hale getirir.
- **Mali bağlayıcı yapılandırması** - Bu yapılandırma, belirli bir mali cihaz ile fiziksel iletişimi tanımlar.

Belirli bir POS kaydı için bir mali kayıt işlemi, POS işlev profilindeki karşılık gelen ayar ile tanımlanır. Mali kayıt işlemi hakkında daha fazla ayrıntı için, mali belge sağlayıcısını ve mali bağlayıcı yapılandırmalarını karşıya yükleyin ve parametrelerini değiştirin bkz. [Mali kayıt işlemi ayarlamak](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Aşağıdaki örnek tipik mali kayıt yürütme akışı mali bir aygıtı gösterir. Akışı POS içindeki (örneğin, bir satış hareketi sonlandırma) bir etkinlik ile başlar ve aşağıdaki sıralı adımları uygular:

1. POS, CRT'den bir mali belge talep eder.
2. CRT, geçerli etkinliğin mali kayıt gerektirip gerektirmediğini belirler.
3. Mali kayıt işlemi ayarlarına dayalı olarak, CRT bir mali bağlayıcıyı ve mali kayıt için kullanılacak karşılık gelen mali belge sağlayıcısını belirler.
4. CRT, bir hareket veya etkinliği temsil eden bir mali belge oluşturan mali belge sağlayıcısını çalıştırır (örneğin bir XML belgesi).
5. POS, CRT'nin hazırladığı belgeyi Donanım istasyonuna gönderir.
6. Donanım istasyonu, mali belgeyi işleyen mali bağlayıcıyı çalıştırır ve bunu mali cihaz veya hizmete iletişim kurar.
7. POS, mali cihaz veya servisten gelen yanıtı analiz ederek mali kaydın başarılı olup olmadığını anlar.
8. CRT, yanıtı kanal veritabanına kaydeder.

![Çözüm şeması](media/emea-fiscal-integration-solution.png "Çözüm şeması")

## <a name="error-handling"></a>Hata işleme

Mali tümleştirme çerçevesi, mali kayıt sırasındaki başarısızlıkları ele almak için aşağıdaki seçenekleri sunar:

- **Yeniden deneme** – Operatörler, bu seçeneği başarısızlık hızlıca çözümlenebildiğinde kullanırlar ve mali kayıt yeniden yürütülebilir. Örneğin, bu seçenek mali cihaz bağlı olmadığında, mali yazıcının kağıdı bittiğinde veya mali yazıcıda bir kağıt sıkışması olduğunda kullanılabilir.
- **İptal** – Bu seçenek, operatörlerin, geçerli mali hareket veya etkinlik başarısız olduğunda ertelemesine izin verir. Kayıt ertelendikten sonra, operatör POS üzerinde çalışmaya devam edebilir ve mali kaydın gerekli olmadığı herhangi bir operasyonu tamamlayabilir. Mali kayıt gerektiren herhangi bir etkinlik POS içinde gerçekleştiğinde (ör. yeni bir kayıt açıldığında), hata işleme iletişim kutusu operatörü önceki hareketin doğru biçimde kaydedilmediğini uyarmak ve hata işleme seçeneklerini sunmak için açılır.
- **Atla** - Operatörler bu seçeneği mali kayıt belirli koşullarda atlanabileceği durumlarda ve operasyonların POS üzerinde devam edebileceği durumlarda kullanabilirler. Örneğin, bu seçenek mali kaydın başarısız olduğu bir satış işlemi için kullanılabilir ve özel bir kağıt günlükte kaydedilebilir.
- **Kaydedildi olarak işaretle** - Operatörler bu seçeneği hareket gerçekten de mali cihazda kaydedilmişse (örneğin, bir mali giriş yazdırılmışsa), ancak mali yanıt kanal veritabanına kaydedildiğinde bir hata oluşmuşsa kullanabilirler.

> [!NOTE]
> **Atla** ve **Kaydedildi olarak işaretle** seçeneklerinin kullanılmadan önce mali kayıt işleminde etkinleştirilmeleri gerekir. Ek olarak, karşılık gelen izinlerin de operatörlere verilmesi gerekir.

**Atla** ve **Kaydedildi olarak işaretle** seçenekleri, bilgi kodlarının başarısızlık hakkında bazı belirli bilgileri yakalamasına olanak sağlar, başarısızlık hata sebebi ve mali kaydı atlama nedeni veya hareketin kaydedildi olarak işaretlenmesi gibi. Hata el alma parametreleri hakkında daha fazla bilgi için bkz. [Hata ele alma ayarları ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>İsteğe bağlı mali kayıt

Mali kayıt, bazı işlemler için isteğe bağlı ancak bazı diğerleri için zorunlu olabilir. Örneğin, normal satışların ve iadelerin mali kaydı zorunlu olabilir ancak, müşteri mevduatıyla ilişkili operasyonların mali kaydı isteğe bağlı olabilir. Bu durumda, bir satışın mali kaydını tamamlama başarısızlığı, sonraki satışları engellemelidir, ancak bir müşteri mevduatının mali kaydını tamamlama başarısızlığı, sonraki satışları engellememelidir. Zorunlu ve isteğe bağlı operasyonlar arasında ayırt edebilmek için bunları farklı belge sağlayıcıları üzerinden gerçekleştirmenizi ve bu sağlayıcılar için mali kayıt işleminde farklı adımlar ayarlamanızı öneririz. **Hatada devam et** parametresi, isteğe bağlı mali kayıt ile ilişkili her adım için etkin olmalıdır. Hata el alma parametreleri hakkında daha fazla bilgi için bkz. [Hata ele alma ayarları ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-running-fiscal-registration"></a>Mali kaydı el ile çalıştırmak

Bir hareket veya etkinliğin mali kaydı bir arızadan sonra ertelenirse (örneğin operatör hata işleme iletişim kutsunda **İptal** seçtiyse), mali kaydı karşılık gelen bir eylemi çağırarak el ile yeniden yürütebilirsiniz. Daha fazla bilgi için bkz. [Ertelenen mali kaydın el ile yürütülmesini etkinleştir](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

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
- Mali kaydın durumu: **Tamamlandı**, başarılı kayıt için, **Atlandı** eğer operatör **Atlama** seçeneğini başarısız bir kayıt için seçtiyse veya **Kaydedildi olarak işaretle** eğer operatör **Kaydedildi olarak işaretle** seçeneğini seçtiyse.
- Seçilen bir mali hareket ile ilgili bilgi kodu hareketleri. Bilgi kodu hareketlerini görüntülemek için **Mali hareketler** hızlı sekmesinde, **Atlanmış** veya **Kaydedildi olarak işaretlenmiş** bir mali hareketi seçin ve sonra **Bilgi kodu hareketleri**'ni seçin.

## <a name="fiscal-texts-for-discounts"></a>İskontolar için mali metinler

Bazı ülkeler ve bölgeler, farklı türde iskontolar uygulandığında mali girişler üzerinde yazdırılması gereken ek metinler için gereksinimlere sahiptir. Mali tümleştirme işlevi, bir mali girişteki bir iskonto satırından sonra iskonto için bir özel metin ayarlamanıza olanak sağlar. El ile iskontolar için bir mali metni POS işlevselliği profilindeki **Ürün iskontosu** bilgi kodu olarak belirtilen bir mali metin için yapılandırabilirsiniz. İskontolar için mali metinleri ayarlama hakkında daha fazla bilgi için bkz. [İskontolar için mali metinler ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>X ve Z mali raporları yazdırma

Mali tümleştirme işlevselliği, tümleştirilmiş mali cihaz veya hizmete ilişkin gün sonu bildirimleri oluşturulmasını destekler:

- Karşılık gelen eylemleri çalıştıran yeni düğmelerin POS ekranı düzenine eklenmesi gerekir. Daha fazla bilgi için bkz. [POS'tan mali X/Z raporlarını ayarla](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Mali tümleştirme örneğinde, bu operasyonların mali cihazda karşılık gelen operasyonlarla eşleşmesi gerekir.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Retail SDK'daki mali tümleştirme örnekleri

Aşağıdaki mali tümleştirme örnekleri Retail SDK içerisinde şu anda kullanılabilir:

- [İtalya için yazar kasa tümleştirme örneği](emea-ita-fpi-sample.md)
- [Polonya için yazar kasa tümleştirme örneği](emea-pol-fpi-sample.md)
- [Avusturya için mali kayıt hizmeti tümleştirme örneği](emea-aut-fi-sample.md)
- [Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği](emea-cze-fi-sample.md)
- [İsveç için kontrol birimi tümleştirmesi örneği](./emea-swe-fi-sample.md)

Aşağıdaki mali tümleştirme işlevi de ayrıca Retail SDK içinde kullanılabilir ancak mali tümleştirme çerçevesinin avantajlarından faydalanmaz. Bu işlevin mali tümleştirme çerçevesine geçirilmesi daha sonraki güncelleştirmeler için planlanmıştır.


- [Fransa için dijital imza](emea-fra-cash-registers.md)
- [Norveç için dijital imza](emea-nor-cash-registers.md)

Retail SDK'da kullanılabilen aşağıdaki eski mali tümleştirme işlevi mali tümleştirme çerçevesini kullanmaz ve sonraki güncelleştirmelerde kullanım dışı bırakılacaktır:

- [İsveç için kontrol birimi tümleştirmesi örneği (eski)](./retail-sdk-control-unit-sample.md)
