---
title: "Kanal istemcilerini, kasaları ve donanım istasyonlarını tanımlama ve koruma"
description: "Bu konu, çevre birimlerinin Perakende POS&quot;unuza nasıl bağlanacağı açıklanır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 800e5c139b54541a179a336c8247eaa6017201d8
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Kanal istemcilerini, kasaları ve donanım istasyonlarını tanımlama ve koruma

[!include[banner](includes/banner.md)]


Bu konu, çevre birimlerinin Perakende POS'unuza nasıl bağlanacağı açıklanır.

**Not:** Belirli yükleme yönergeleri için bkz. [Perakende donanım istasyonunu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md) ve [Retail Modern POS self servis indirme/yükleme ve Modern POS ve Bulut POS'ta cihazı etkinleştirme](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Anahtar bileşenler
Mağaza arası ilişkileri, mağazadaki satış noktası (POS) kasalarını veya kanallarını ve bu kasaların veya kanalların işlemleri gerçekleştirmek için kullandıkları perakende çevre birimlerini tanımlamak için çeşitli bileşenler kullanılır. Bu bölümde her bileşen tanımlanır ve bir perakende mağaza dağıtımında nasıl kullanılması gerektiği açıklanır.

### <a name="pos-registers"></a>POS kayıtları

Gezinme: **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kasalar**'a tıklayın. POS kasası, POS'un belirli bir örneğinin özelliklerini tanımlamak için kullanılan bir varlıktır. Bu özelliklere kasada kullanılacak donanım profili veya perakende çevri birimleri, kasanın eşleştiği mağaza ve kasaya oturum açan kullanıcının görsel deneyimi dahildir.

### <a name="devices"></a>Aygıtlar

Gezinme: **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Cihazlar**'a tıklayın. Cihaz, POS kaydının eşlendiği bir cihazın fiziksel örneğini gösteren bir varlıktır. Cihaz oluşturulduğunda bir POS kaydına eşlenir. Cihaz varlığı, bir POS kaydı etkinleştirildiğinde kullanılan istemci türü ve belirli bir cihaza dağıtılan uygulama paketi hakkındaki bilgileri izler. Cihazlar iki tür olabilir: **Retail modern POS** (MPOS) veya **Retail Cloud POS** (Bulut POS).

#### <a name="mpos"></a>MPOS

MPOS, Windows 8.1 veya sonraki bir sürümün çalıştırıldığı PC tabanlı işletim sistemine yüklenen POS istemci uygulamasıdır. **Retail modern POS** uygulama türü bir cihazla eşleniyorsa indirme paketi belirli bir cihaz için belirtilebilir. İndirme paketi, kurulum paketinin farklı sürümlerini içerecek biçimde özelleştirilebilir. Farklı paketleri dağıtma becerisi farklı POS kayıtlarının farklı tümleştirmelere ihtiyaç duyduğu hallerde esneklik sağlar. MPOS yerleşik bir donanım istasyonu ile birlikte dağıtılır.

#### <a name="cloud-pos"></a>Bulut POS

Bulut POS, tarayıcı tabanlı bir POS'tur. Tarayıcıda çalıştığı için Bulut POS Windows 8.1 veya sonraki bir PC tabanlı işletim sistemi gerektirmez. I**Retail Cloud POS** uygulama türü arka ofiste belirli bir cihazla eşleniyorsa bu cihaz bir paketin indirilmesi veya kurulmasına gerek kalmadan tarayıcı aracılığıyla kullanılabilir. Bulut POS, barkod tarama tabanlı klavye emülasyonu dışında donanım kullanmak için bir donanım istasyonu gerektirir.

### <a name="hardware-profile"></a>Donanım profili

Gezinti: **Ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri**'ne tıklayın. Donanım profili bir POS kaydına veya bir donanım istasyonuna bağlı donanımı tanımlar. Donanım profili, ödeme yazılım geliştirme seti (SDK) ile iletişim sırasında kullanılması gereken ödeme işlemcisi parametrelerini belirlemek için de kullanılır. (Ödeme SDK, donanım istasyonunun bir parçası olarak dağıtılır.)

### <a name="hardware-station"></a>Donanım istasyonu

Gezinme: **Perakende ve ticaret** &gt; **Kanallar** &gt; **Perakende mağazaları** &gt; **Tüm perakende mağazaları**'na tıklayın. Bir mağaza seçin ve sonra **Donanım istasyonları** FastTab'a tıklayın. Donanım istasyonu, POS çevre birimlerini destekleyen bir iş mantığı örneğidir. Yazılım istasyonu MPOS ile birlikte otomatik olarak yüklenir. Alternatif olarak, yazılım istasyonu bağımsız bir bileşen olarak yüklenebilir ve bir web hizmeti üzerinden MPOS veya Bulut POS'la erişilebilir. Donanım istasyonu kanal düzeyinde tanımlanmalıdır.

### <a name="hardware-station-profile"></a>Donanım istasyonu profili

Gezinti: **Ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım istasyonu profilleri**'ne tıklayın. Kanal düzeyinde belirtilen donanım istasyonunun kendisi donanım istasyonu URL'si gibi örneğe özgü bilgileri içerirken, donanım istasyonu profili statik veya birden fazla donanım istasyonu arasında paylaşılan bilgileri içerir. Statik bilgiler kullanılması gereken bağlantı noktasını, donanım istasyonu paketini ve donanım profilini içerir. Statik bilgiler, örneğin her bir donanım istasyonu için gereken donanıma bağlı olarak **Ödeme**veya **İadeler** gibi, dağıtılan donanım istasyonu türünün tanımını da içerir.

## <a name="scenarios"></a>Senaryolar
### <a name="mpos-with-connected-peripheral-devices"></a>Çevre birimi cihazlarına bağlı MPOS

[![Geleneksel, sabit satış noktası](./media/traditional-300x279.png)](./media/traditional.png) 

Geleneksel, sabit POS senaryosunda MPOS'u POS çevre birimlerine bağlamak için önce kaydın kendisine gidin ve bir donanım profili atayın. POS kayıtlarını, **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kasalar** altında bulabilirsiniz. Donanım profilini atadıktan sonra "Kayıtlar" dağıtım planını kullanarak değişiklikleri kanal veritabanıyla eşitleyin. Dağıtım planlarını **Perakende ve ticaret** &gt; **Perakende BT'si** &gt; **Dağıtım planı** altında bulabilirsiniz. Daha sonra kanalda "yerel" bir donanım istasyonu kurun. **Perakende ve ticaret** &gt; **Kanallar** &gt; **Perakende mağazaları** &gt; **Tüm perakende mağazaları**'na tıklayın ve bir mağaza seçin. Ardından bir donanım istasyonu eklemek için **Donanım istasyonları** FastTab üzerinden **Ekle**'ye tıklayın. Bir açıklama girin, ana bilgisayar adı olarak **localhost** yazın ve "Kanal konfigürasyonu" dağıtım planını kullanarak değişiklikleri kanalla eşitleyin. Dağıtım planlarını **Perakende ve ticaret** &gt; **Perakende BT'si** &gt; **Dağıtım planı** altında bulabilirsiniz. Son olarak, MPOS'ta **localhost** donanım istasyonunu seçmek için **Donanım istasyonu seç** işlemini kullanın. Donanım istasyonunu **Etkin** olarak ayarlayın. Bu senaryoda kullanılan donanım profili POS kaydının kendisinden gelmelidir. Bu senaryo için bir donanım istasyonu profili gerekmez. **Not:** Kasa çekmeceleri gibi bazı donanım profili değişiklikleri kanalla eşitlendikten sonra yeni bir vardiyanın açılmasını gerektirir. **Not:** Bulut POS'ta perakende çevre birimleriyle iletişim kurmak için bağımsız donanım istasyonu kullanılmalıdır.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>Bağımsız donanım istasyonlu MPOS veya Bulut POS
[![Paylaşılan çevre birimleri](./media/shared-300x254.png)](./media/shared.png)

Bu senaryoda bağımsız donanım istasyonu MPOS ve Bulut POS istemcileri arasında paylaşılır. Bu senaryoda donanım istasyonunun kullandığı indirme paketi, bağlantı noktası ve donanım profilini belirtmek için bir donanım istasyonu profili oluşturmanız gerekir. Donanım istasyonu profilini **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım istasyonu profilleri** altında bulabilirsiniz. Donanım istasyonu profilini oluşturduktan sonra ilgili perakende kanalına gidin (**Perakende ve ticaret** &gt; **Kanallar** &gt; **Perakende mağazaları** &gt; **Tüm perakende mağazaları**) ve yeni bir donanım istasyonu ekleyin. Bu yeni donanım istasyonunu daha önce oluşturulan donanım istasyonu profiliyle eşleyin. Ardından, kasiyerin donanım istasyonunu tanımlamasına yardımcı olacak bir açıklama girin. **Ana bilgisayar adı** alanına, ana makine URL'sini **https://&lt;MakineAdı:BağlantıNoktası&gt;/Donanımİstasyonu biçiminde girin**. (**&lt;MakineAdı:BağlantıNoktası&gt;**'nı, donanım istasyonu profilinde belirtilen donanım istasyonu gerçek makine adıyla değiştirin.) Bağımsız bir donanım istasyonu için, elektronik fon transferi (EFT) terminal kimliğini de belirtmelisiniz. Bu değer, ödeme bağlayıcısı ödeme sağlayıcı ile iletişim kurduğunda donanım istasyonuna bağlanan EFT terminalini tanımlar. Daha sonra asıl donanım istasyonu makinesinden kanala gidin ve donanım istasyonunu seçin. Ardından, **İndir**'e tıklayın ve donanım istasyonunu yükleyin. Daha sonra MPOS veya Bulut POS'tan önceden yüklenmiş donanım istasyonunu seçmek için **Donanım istasyonu seç** işlemini kullanın. POS ile donanım istasyonu arasında güvenli bir ilişki kurmak için **Eşleştir** 'i seçin. Bu adım bir POS ve bir donanım istasyonunun her birleşimi için bir kez tamamlanmalıdır. Donanım istasyonu eşleştirildikten sonra, aynı işlem donanım istasyonunu kullanılırken etkinleştirmek için kullanılır. Bu senaryoda, donanım profili, kasanın kendisinden ziyade donanım istasyonu profiline atanmalıdır. Herhangi bir nedenden dolayı donanım istasyonu doğrudan atanmış bir donanım profiline sahip değilse, kasaya atanmış donanım profili kullanılır

## <a name="client-maintenance"></a>İstemci bakımı
### <a name="registers"></a>Kayıtlar

POS kayıtları öncelikle kendi kayıtları ve kayıtlara atanan profiller aracılığıyla yönetilir. Ayrı bir kayda özgü öznitelikler kayıt düzeyinde yönetilir. Bu öznitelikler kaydın kullanıldığı mağazayı, kayıt numarasını, açıklamayı ve kaydın kendisine özgü EFT terminali kodunu içerir.

### <a name="pos-profiles"></a>POS profilleri

POS profillerini, **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** altında bulabilirsiniz. Profiller aracılığıyla bir kaydın çeşitli özelliklerini yönetmek yararlıdır, çünkü profiller birçok kayıt arasında paylaşılabilir. Profiller ayrı bir kayıtla eşlenebileceği gibi profil mağaza kapsamında geçerliyse perakende mağazayla da eşlenebilir. Aşağıdaki bölümlerde, POS profilleri ve bunların nasıl kullanıldıkları açıklanır.

#### <a name="offline-profile"></a>Çevrimdışı profil

Çevrimdışı profil mağaza düzeyinde ayarlanır. Kayıt, kanal veritabanına bağlı değilken bir POS kaydı üzerinde gerçekleştirilen işlemler için yükleme ayarlarını belirtmek amacıyla kullanılır.

#### <a name="functionality-profile"></a>İşlevsellik profili

İşlevsellik profili mağaza düzeyinde ayarlanır. POS'ta gerçekleştirilebilecek işlemler hakkında mağaza çapındaki ayarları belirtmek için kullanılır. Aşağıdaki yetenekler işlevsellik profili aracılığıyla yönetilir. Bu yetenekler FastTab'a göre düzenlenir.

-   **Genel** FastTab'i:
    -   Uluslararası Standartlar Kuruluşu (ISO).
    -   Çevrimdışı modda müşteri oluşturun.
    -   E-posta girişi profili.
    -   Merkezi personel oturum doğrulaması.
-   **İşlevler** FastTab'i:
    -   Oturum açma ve genişletilmiş oturum açma yönetimi.
    -   Fiyatları girme becerisi ve küçük para birimleri için ondalıkların gerekli olup olmadığı gibi, POS'un mali ve para birimiyle ilgili özellikleri.
    -   Zaman kaydını POS aracılığıyla etkinleştirme.
    -   Ürünlerin ve ödemelerin POS'ta ve makbuzlar üzerinde nasıl göründüğü.
    -   Gün sonu yönetimi.
    -   Kanal veritabanı hareket tutma parametreleri.
    -   Müşterilerin POS'tan nasıl arandığı ve oluşturulduğu.
    -   İskontoların nasıl hesaplandığı.
-   **Tutar** FastTab'i:
    -   İzin verilen maksimum ve minimum fiyatlar.
    -   İskonto uygulaması ve hesaplaması.
-   **Bilgi kodları** FastTab'i:
    -   Bilgi kodlarının POS'ta yönetilmesinin tüm yönleri. Ayrıntılar için bkz: [Bilgi kodları](info-codes-retail.md).
-   **Makbuz numaralandırma** FastTab'i:
    -   Mağaza numarası, terminal numarası, sabitler ve satışların, iadelerin, satış siparişlerinin ve tekliflerin ayrı seriler halinde mi yazdırıldığı yoksa tümünün aynı seriyi mi takip ettiği gibi parçaları içerebilecek makbuz numaralandırma maskelerini belirtin.

#### <a name="receipt-profiles"></a>Makbuz profilleri

Giriş profilleri donanım profili içinden yazıcılara atanır. Bunlar belirli bir yazıcıda yazdırılmış giriş türlerini belirtmek için kullanılır. Profiller giriş biçimleri için ayarları ve makbuzun her zaman yazdırılıp yazdırılmadığını veya kasiyerden makbuzun yazdırılması gerekip gerekmediğine karar vermesinin istenip istenmediğini belirleyen ayarları içerir. Farklı yazıcılar farklı giriş profillerini de kullanabilir. Örneğin, yazıcı 1 standart termal makbuz yazıcısıdır ve bu nedenle daha küçük giriş biçimlerine sahiptir. Ancak yazıcı 2 yalnızca müşteri sipariş girişlerini yazdırmak için kullanılan tam boyutlu bir makbuz yazıcısı olup daha fazla alan gerektirir.

#### <a name="hardware-profiles"></a>Donanım profilleri

Donanım profilleri bu makalenin önceki bölümlerinde istemci kurulumu bileşeni olarak açıklanmıştır. Donanım profilleri doğrudan POS kaydına veya donanım istasyonu profiline atanır. Bunlar belirli bir POS kaydı veya donanım istasyonunun kullandığı cihazların türlerini belirtmek için kullanılır. Donanım profilleri, ödeme SDK ile iletişim kurmak için kullanılan EFT ayarlarını belirtmek için de kullanılır.

#### <a name="visual-profiles"></a>Görsel profiller

Görsel profiller kayıt düzeyinde atanır. Belirli bir kayıt için temayı belirtmek amacıyla kullanılırlar. Profiller kullanılan uygulamanın türü (MPOS veya Bulut POS), vurgu rengi ve tema, yazı tipi düzeni, oturum açma ve POS arka planları için ayarları içerir.

### <a name="custom-fields"></a>Özel alanlar

POS'ta kullanıma hazır olarak sunulmayan alanlar eklemek için özel alanlar oluşturabilirsiniz. Özel alanları kullanmak hakkında daha fazla bilgi için bkz. [Özel alanlarla çalışma blog gönderisi](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Dil metni

Dil metni girişlerini kullanarak POS'ta varsayılan dizeleri geçersiz kılabilirsiniz. POS'ta dizeyi geçersiz kılmak için yeni bir dil metni satırı ekleyin. Daha sonra kimliği, geçersiz kılınmasını gereken varsayılan dizeyi ve POS'ta varsayılan dize yerine gösterilmesi gereken metni belirtin.

### <a name="hardware-station-profiles"></a>Donanım istasyonu profilleri

Donanım istasyonu profilleri, bu makalenin önceki bölümlerinde açıklanmıştır. Donanım istasyonlarına örneğe özgü olmayan bilgileri atamak için kullanılır.

### <a name="channel-reports-configuration"></a>Kanal raporları konfigürasyonu

**Perakende kanal raporları konfigürasyonu** sayfasındaki perakende kanalında mevcut raporları ayarlayın. Raporun XML tanımını sağlayarak ve raporu POS'taki belirli bir izin grubuna atayarak yeni raporlar oluşturabilirsiniz.

### <a name="devices"></a>Cihazlar

Cihazlar bu makalenin önceki bölümlerinde açıklanmıştır. Belirli bir POS kaydının etkinleştirilmesini yönetmek için kullanılırlar. Cihazlar belirli bir kayıt için kullanılan uygulamayı ve MPOS istemcisinin yüklenmesi için kullanılması gereken yükleme paketini belirtmek için de kullanılır. Cihaz etkinleştirme durumları şunlardır:

-   **Beklemede**: Cihaz etkinleştirilmeye hazırdır.
-   **Etkinleştirildi**: Cihaz etkinleştirilmiştir.
-   **Devre dışı bırakıldı**: Cihaz arka ofiste veya POS aracılığıyla devre dışı bırakılmıştır.
-   **Devre dışı**: Cihaz devre dışı bırakılmıştır.

Etkinleştirmeyle ilgili ek bilgiler cihazın etkinleştirme durumunu değiştiren çalışanı, etkinleştirmenin zaman damgasını ve cihaz konfigürasyonunun doğrulanıp doğrulanmadığını içerir.

### <a name="client-data-synchronization"></a>İstemci verilerini eşitleme

Cihazın etkinleştirme durumundaki değişiklikler hariç POS istemcisindeki tüm değişikliklerin etkinleştirilmesi için kanal veritabanıyla eşitlenmesi gerekir. Kanal veritabanındaki değişiklikleri eşitlemek için **Perakende ve ticaret** &gt; **Perakende BT'si** &gt; **Dağıtım planı**'na gidin ve gerekli dağıtım planını çalıştırın. İstemci değişiklikleri için "Kayıtlar" ve "Kanal konfigürasyonu" dağıtım planlarını çalıştırmalısınız.




