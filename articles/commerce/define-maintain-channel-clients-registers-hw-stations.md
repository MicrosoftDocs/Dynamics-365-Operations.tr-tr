---
title: Çevre birimlerini satış noktasına (POS) bağlama
description: Bu konu, çevre birimlerinin Perakende POS'unuza nasıl bağlanacağı açıklanır.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1c53c7215d3a5a182f345d5e040274ae06f9b12
ms.sourcegitcommit: 116898def829c0f78bda8a117242aa308793465d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370963"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Çevre birimlerini satış noktasına (POS) bağlama

[!include [banner](includes/banner.md)]

Bu konu, çevre birimlerinin Perakende POS'unuza nasıl bağlanacağı açıklanır.

> [!NOTE]
> Belirli yükleme yönergeleri için bkz. [Retail hardware station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md) ve [Modern POS'u (MPOS) yapılandırma, yükleme ve etkinleştirme](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Anahtar bileşenler

Mağaza arası ilişkileri, mağazadaki satış noktası (POS) kasalarını veya kanallarını ve bu kasaların veya kanalların işlemleri gerçekleştirmek için kullandıkları çevre birimlerini tanımlamak için çeşitli bileşenler kullanılır. Bu bölümde her bileşen tanımlanır ve bir mağaza dağıtımında nasıl kullanılması gerektiği açıklanır.

### <a name="pos-registers"></a>POS kayıtları

Gezinti:**Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kayıtlar**'a tıklayın.

POS kasası, POS'un belirli bir örneğinin özelliklerini tanımlamak için kullanılan bir varlıktır. Bu özelliklere kasada kullanılacak donanım profili veya çevre birimleri kurulumu, kasanın eşleştiği mağaza ve bu kasada oturum açan kullanıcının görsel deneyimi dahildir.

### <a name="devices"></a>Aygıtlar

Gezinti: **Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Cihazlar**'a tıklayın.

Cihaz, POS kaydının eşlendiği bir cihazın fiziksel örneğini gösteren bir varlıktır. Cihaz oluşturulduğunda bir POS kaydına eşlenir. Cihaz varlığı, bir POS kaydı etkinleştirildiğinde kullanılan istemci türü ve belirli bir cihaza dağıtılan uygulama paketi hakkındaki bilgileri izler. Cihazlar iki tür olabilir: **Retail modern POS** (MPOS) veya **Retail Cloud POS** (Bulut POS).

#### <a name="mpos"></a>MPOS

MPOS, Windows 8.1 veya sonraki bir sürümün çalıştırıldığı PC tabanlı işletim sistemine yüklenen POS istemci uygulamasıdır. **Retail modern POS** uygulama türü bir cihazla eşleniyorsa indirme paketi belirli bir cihaz için belirtilebilir. İndirme paketi, kurulum paketinin farklı sürümlerini içerecek biçimde özelleştirilebilir. Farklı paketleri dağıtma becerisi farklı POS kayıtlarının farklı tümleştirmelere ihtiyaç duyduğu hallerde esneklik sağlar. MPOS yerleşik bir donanım istasyonu ile birlikte dağıtılır.

#### <a name="cloud-pos"></a>Bulut POS

Bulut POS, tarayıcı tabanlı bir POS'tur. Tarayıcıda çalıştığı için Bulut POS Windows 8.1 veya sonraki bir PC tabanlı işletim sistemi gerektirmez. **Retail Cloud POS** uygulama türü Headquarters'ta belirli bir cihazla eşleniyorsa bu cihaz bir paketin indirilmesi veya kurulmasına gerek kalmadan tarayıcı aracılığıyla kullanılabilir. Bulut POS, barkod tarama tabanlı klavye emülasyonu dışında donanım kullanmak için bir donanım istasyonu gerektirir.

### <a name="hardware-profile"></a>Donanım profili

Gezinme: **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**'ne gidin.

Donanım profili bir POS kaydına veya bir entegre ya da paylaşılan donanım istasyonuna bağlı donanımı tanımlar. Donanım profili, ödeme yazılım geliştirme seti (SDK) ile iletişim sırasında kullanılması gereken ödeme işlemcisi parametrelerini belirlemek için de kullanılır. Ödeme SDK, donanım istasyonunun bir parçası olarak dağıtılır.

### <a name="hardware-station"></a>Hardware station

Gezinti: **Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin, bir mağaza seçin ve ardından **Donanım istasyonları** hızlı sekmesini seçin.

Donanım istasyonu, POS çevre birimlerini destekleyen bir iş mantığı örneğidir. Yazılım istasyonu MPOS ile birlikte otomatik olarak yüklenir. Alternatif olarak, yazılım istasyonu bağımsız bir bileşen olarak yüklenebilir ve bir web hizmeti üzerinden MPOS veya Bulut POS'la erişilebilir. Donanım istasyonu kanal düzeyinde tanımlanmalıdır.

## <a name="scenarios"></a>Senaryolar

### <a name="mpos-with-connected-peripheral-devices"></a>Çevre birimi cihazlarına bağlı MPOS

[![Geleneksel, sabit satış noktası.](./media/traditional-300x279.png)](./media/traditional.png)

Geleneksel, sabit POS senaryosunda MPOS'u POS çevre birimlerine bağlamak için önce kaydın kendisine gidin ve bir donanım profili atayın. POS kayıtlarını **Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kayıtlar** altında bulabilirsiniz. 

Donanım profilini atadıktan sonra **Kayıtlar** dağıtım planını kullanarak değişiklikleri kanal veritabanıyla eşitleyin. Dağıtım planlarını **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Dağıtım planı** altında bulabilirsiniz. 

Daha sonra kanalda özel bir donanım istasyonu kurun. **Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin ve bir mağaza seçin. 

Ardından bir donanım istasyonu eklemek için **Donanım istasyonları** FastTab üzerinden **Ekle**'yi seçin. Donanım istasyonu türü olarak **Özel**'i seçin ve sonra bir açıklama girin. Bu senaryoda kullanılan donanım profili POS kaydının kendisinden geldiği için, **Donanım profili** alanı boş bırakılabilir. Ardından **Kanal yapılandırması** dağıtım zamanlamasını kullanarak değişiklikleri kanala eşitleyin. Dağıtım planlarını **Retail ve Commerce \> Retail ve Commerce IT \> Dağıtım planı** altında bulabilirsiniz. 

Son olarak MPOS'da, açıklama için daha önce girdiğiniz değerle eşleşen donanım istasyonunu seçmek üzere **Donanım istasyonu seç** işlemini kullanın ve donanım istasyonunu **Etkin** olarak ayarlayın. 

> [!NOTE]
> - Kasa çekmeceleri gibi bazı donanım profili değişiklikleri kanalla eşitlendikten sonra yeni bir vardiyanın açılmasını gerektirir.
> - Bulut POS'ta çevre birimleriyle iletişim kurmak için bağımsız donanım istasyonu kullanılmalıdır.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>Bağımsız donanım istasyonlu MPOS veya Bulut POS

[![Paylaşılan çevre birimleri.](./media/shared-300x254.png)](./media/shared.png)

Bu senaryoda bağımsız donanım istasyonu MPOS ve Bulut POS istemcileri arasında paylaşılır. Bu senaryoda donanım istasyonunun kullandığı indirme paketi, bağlantı noktası ve donanım profilini belirtmek için paylaşılan bir donanım istasyonu oluşturmanız gerekir. Belirli bir kanaldaki **Donanım istasyonları** hızlı sekmesini (**Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**) seçerek ve **Paylaşılan** türe yeni bir donanım istasyonu ekleyerek yeni bir donanım istasyonu tanımlarsınız. 

Ardından, kasiyerin donanım istasyonunu tanımlamasına yardımcı olacak bir açıklama girin. **Ana bilgisayar adı** alanına, ana makine URL'sini `https://<MachineName:Port>/HardwareStation` biçiminde girin. (**&lt;MachineName:Port&gt;** öğesini, donanım istasyonu gerçek makine adıyla değiştirin.) Bağımsız bir donanım istasyonu için, elektronik fon transferi (EFT) terminal kimliğini de belirtmelisiniz. Bu değer, ödeme bağlayıcısı ödeme sağlayıcı ile iletişim kurduğunda donanım istasyonuna bağlanan EFT terminalini tanımlar. 

Ardından, donanım istasyonunun barındırılacağı makineden Genel merkezde kanala gidin ve donanım istasyonunu seçin. Donanım istasyonu yükleyicisini karşıdan yüklemek ve donanım istasyonunu yüklemek için **İndir**'i seçin. Donanım istasyonu yükleme hakkında daha fazla bilgi için bkz. [Retail hardware station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md). 

Daha sonra MPOS veya Bulut POS'tan önceden yüklenmiş donanım istasyonunu seçmek için **Donanım istasyonu seç** işlemini kullanın. POS ile donanım istasyonu arasında güvenli bir ilişki kurmak için **Eşleştir** 'i seçin. Bu adım bir POS ve bir donanım istasyonunun her birleşimi için bir kez tamamlanmalıdır. 

Donanım istasyonu eşleştirildikten sonra, aynı işlem donanım istasyonunu kullanılırken etkinleştirmek için kullanılır. Bu senaryoda, donanım profili, kasanın kendisine değil de paylaşılan bir donanım istasyonuna atanmalıdır. Herhangi bir nedenden dolayı donanım istasyonuna doğrudan bir donanım profili atanmazsa, kasaya atanan donanım profili kullanılır.

## <a name="client-maintenance"></a>İstemci bakımı

### <a name="registers"></a>Kayıtlar

POS kayıtları öncelikle kendi kayıtları ve kayıtlara atanan profiller aracılığıyla yönetilir. Ayrı bir kayda özgü öznitelikler kayıt düzeyinde yönetilir. Bu öznitelikler kaydın kullanıldığı mağazayı, kayıt numarasını, açıklamayı ve kaydın kendisine özgü EFT terminali kodunu içerir.

### <a name="pos-profiles"></a>POS profilleri

POS profillerini, **Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** altında bulabilirsiniz. Profiller aracılığıyla bir kaydın çeşitli özelliklerini yönetmek yararlıdır, çünkü profiller birçok kayıt arasında paylaşılabilir. Profiller ayrı bir kayıtla eşlenebileceği gibi profil mağaza kapsamında geçerliyse mağazayla da eşlenebilir. Aşağıdaki bölümlerde, POS profilleri ve bunların nasıl kullanıldıkları açıklanır.

#### <a name="offline-profile"></a>Çevrimdışı profil

Çevrimdışı profil mağaza düzeyinde ayarlanır. Kayıt, kanal veritabanına bağlı değilken bir POS kaydı üzerinde gerçekleştirilen işlemler için yükleme ayarlarını belirtmek amacıyla kullanılır.

#### <a name="functionality-profile"></a>İşlevsellik profili

İşlevsellik profili mağaza düzeyinde ayarlanır. POS'ta gerçekleştirilebilecek işlemler hakkında mağaza çapındaki ayarları belirtmek için kullanılır. Aşağıdaki yetenekler işlevsellik profili aracılığıyla yönetilir. Bu yetenekler FastTab'a göre düzenlenir.

- **Genel** FastTab'i:

    - Uluslararası Standartlar Kuruluşu (ISO).
    - Çevrimdışı modda müşteri oluşturun.
    - E-posta girişi profili.
    - Merkezi personel oturum doğrulaması.

- **İşlevler** FastTab'i:

    - Oturum açma ve genişletilmiş oturum açma yönetimi.
    - Fiyatları girme becerisi ve küçük para birimleri için ondalıkların gerekli olup olmadığı gibi, POS'un mali ve para birimiyle ilgili özellikleri.
    - Zaman kaydını POS aracılığıyla etkinleştirme.
    - Ürünlerin ve ödemelerin POS'ta ve makbuzlar üzerinde nasıl göründüğü.
    - Gün sonu yönetimi.
    - Kanal veritabanı hareket tutma parametreleri.
    - Müşterilerin POS'tan nasıl arandığı ve oluşturulduğu.
    - İskontoların nasıl hesaplandığı.

- **Tutar** FastTab'i:

    - İzin verilen maksimum ve minimum fiyatlar.
    - İskonto uygulaması ve hesaplaması.

- **Bilgi kodları** FastTab'i:

    - Bilgi kodlarının POS'ta yönetilmesinin tüm yönleri. Ayrıntılar için bkz. [Bilgi kodları ve bilgi kodu grupları](info-codes-retail.md).

- **Makbuz numaralandırma** FastTab'i:

    - Mağaza numarası, terminal numarası, sabitler ve satışların, iadelerin, satış siparişlerinin ve tekliflerin ayrı seriler halinde mi yazdırıldığı yoksa tümünün aynı seriyi mi takip ettiği gibi parçaları içerebilecek makbuz numaralandırma maskelerini belirtin.

#### <a name="receipt-profiles"></a>Makbuz profilleri

Giriş profilleri donanım profili içinden yazıcılara atanır. Bunlar belirli bir yazıcıda yazdırılmış giriş türlerini belirtmek için kullanılır. Profiller giriş biçimleri için ayarları ve makbuzun her zaman yazdırılıp yazdırılmadığını veya kasiyerden makbuzun yazdırılması gerekip gerekmediğine karar vermesinin istenip istenmediğini belirleyen ayarları içerir. Farklı yazıcılar farklı giriş profillerini de kullanabilir. Örneğin, yazıcı 1 standart termal makbuz yazıcısıdır ve bu nedenle daha küçük giriş biçimlerine sahiptir. Ancak yazıcı 2 yalnızca müşteri sipariş girişlerini yazdırmak için kullanılan tam boyutlu bir makbuz yazıcısı olup daha fazla alan gerektirir. Daha fazla bilgi için bkz. [Giriş profili yapılandırma](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Donanım profilleri

Donanım profilleri bu konunun önceki bölümlerinde istemci kurulumu bileşeni olarak açıklanmıştır. Donanım profilleri, doğrudan POS kasasına veya paylaşılan bir donanım istasyonuna atanır ve belirli bir POS'un veya donanım istasyonunun kullandığı aygıt türlerini belirtmek için kullanılır. Donanım profilleri, ödeme SDK ile iletişim kurmak için kullanılan EFT ayarlarını belirtmek için de kullanılır.

#### <a name="visual-profiles"></a>Görsel profiller

Görsel profiller, belirli bir kasanın temasını belirlemek için kullanılır ve kasa düzeyinde atanır. Profiller kullanılan uygulamanın türü (MPOS veya Bulut POS), vurgu rengi ve tema, yazı tipi düzeni, oturum açma sayfası arka planı ve POS arka planları için ayarları içerir. Daha fazla bilgi için bkz. [Satış noktası (POS) görsel profil oluşturma](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Özel alanlar

POS'ta kullanıma hazır olarak sunulmayan alanlar eklemek için özel alanlar oluşturabilirsiniz. Özel alanları kullanmak hakkında daha fazla bilgi için bkz. [Özel alanlarla çalışma blog gönderisi](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Dil metni

Dil metni girişlerini kullanarak POS'ta varsayılan dizeleri geçersiz kılabilirsiniz. POS'ta dizeyi geçersiz kılmak için yeni bir dil metni satırı ekleyin. Daha sonra kimliği, geçersiz kılınmasını gereken varsayılan dizeyi ve POS'ta varsayılan dize yerine gösterilmesi gereken metni belirtin.

### <a name="channel-reports-configuration"></a>Kanal raporları konfigürasyonu

**Kanal raporları yapılandırması** sayfasındaki kanaldaki mevcut raporları ayarlayın. Raporun XML tanımını sağlayarak ve raporu POS'taki belirli bir izin grubuna atayarak yeni raporlar oluşturabilirsiniz.

### <a name="devices"></a>Cihazlar

Cihazlar bu makalenin önceki bölümlerinde açıklanmıştır. Belirli bir POS kaydının etkinleştirilmesini yönetmek için kullanılırlar. Cihazlar belirli bir kayıt için kullanılan uygulamayı ve MPOS istemcisinin yüklenmesi için kullanılması gereken yükleme paketini belirtmek için de kullanılır. Cihaz etkinleştirme durumları şunlardır:

- **Beklemede**: Cihaz etkinleştirilmeye hazırdır.
- **Etkinleştirildi**: Cihaz etkinleştirilmiştir.
- **Devre dışı bırakıldı**: Cihaz Headquarters veya POS aracılığıyla devre dışı bırakılmıştır.
- **Devre dışı**: Cihaz devre dışı bırakılmıştır.

Etkinleştirmeyle ilgili ek bilgiler cihazın etkinleştirme durumunu değiştiren çalışanı, etkinleştirmenin zaman damgasını ve cihaz konfigürasyonunun doğrulanıp doğrulanmadığını içerir.

### <a name="client-data-synchronization"></a>İstemci verilerini eşitleme

Cihazın etkinleştirme durumundaki değişiklikler hariç POS istemcisindeki tüm değişikliklerin etkinleştirilmesi için kanal veritabanıyla eşitlenmesi gerekir. Kanal veritabanındaki değişiklikleri eşitlemek için **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Dağıtım planı**'na gidin ve gerekli dağıtım planını çalıştırın. İstemci değişiklikleri için **Kayıtlar** ve **Kanal yapılandırması** dağıtım planlarını çalıştırmalısınız.

## <a name="additional-resources"></a>Ek kaynaklar

[Retail Hardware Station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
