---
title: "Tanımlamak ve kanal istemcileri, kasalar ve donanım istasyonlarını korumak"
description: "Bu wiki&quot;de çevre birimlerinin Perakende POS&quot;unuza nasıl bağlanacağı açıklanır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Tanımlamak ve kanal istemcileri, kasalar ve donanım istasyonlarını korumak

Bu wiki'de çevre birimlerinin Perakende POS'unuza nasıl bağlanacağı açıklanır.

**Not:** Belirli yükleme yönergeleri için bkz. [Perakende donanım istasyonunu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md) ve [Retail Modern POS self servis indirme/yükleme ve Modern POS ve Bulut POS'ta cihazı etkinleştirme](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Anahtar bileşenler
Mağaza arası ilişkileri, mağazadaki satış noktası (POS) kasalarını veya kanallarını ve bu kasaların veya kanalların işlemleri gerçekleştirmek için kullandıkları perakende çevre birimlerini tanımlamak için çeşitli bileşenler kullanılır. Bu bölümde her bileşen tanımlanır ve bir perakende mağaza dağıtımında nasıl kullanılması gerektiği açıklanır.

### <a name="pos-registers"></a>POS kayıtları

Gezinti:'ı **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**kayıtları**. POS kasa POS belirli bir örneğinin özelliklerini tanımlamak için kullanılan bir varlıktır. Donanım profili veya Kurulum kaydetmek, oturum açtığında kullanıcı için kullanılacak kayıt, kayıt eşlenen mağaza ve görsel deneyimi perakende çevre birimleri için bu özellikleri içerir.

### <a name="devices"></a>Aygıtlar

Gezinti:'ı **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**aygıtları**. Cihaz, POS kaydının eşlendiği bir cihazın fiziksel örneğini gösteren bir varlıktır. Cihaz oluşturulduğunda bir POS kaydına eşlenir. Cihaz varlığı, bir POS kaydı etkinleştirildiğinde kullanılan istemci türü ve belirli bir cihaza dağıtılan uygulama paketi hakkındaki bilgileri izler. Cihazlar iki tür olabilir: **Retail modern POS** (MPOS) veya **Retail Cloud POS** (Bulut POS).

#### <a name="mpos"></a>MPOS

MPOS, Windows 8.1 veya sonraki bir sürümün çalıştırıldığı PC tabanlı işletim sistemine yüklenen POS istemci uygulamasıdır. **Retail modern POS** uygulama türü bir cihazla eşleniyorsa indirme paketi belirli bir cihaz için belirtilebilir. İndirme paketi, kurulum paketinin farklı sürümlerini içerecek biçimde özelleştirilebilir. Farklı paketleri dağıtma becerisi farklı POS kayıtlarının farklı tümleştirmelere ihtiyaç duyduğu hallerde esneklik sağlar. MPOS yerleşik bir donanım istasyonu ile birlikte dağıtılır.

#### <a name="cloud-pos"></a>Bulut POS

Tarayıcı tabanlı bir POS POS bulut olur. Tarayıcıda çalışır çünkü bulut POS Windows 8.1 veya daha yeni bir PC tabanlı işletim sistemi gerektirmez. I**Retail Cloud POS** uygulama türü arka ofiste belirli bir cihazla eşleniyorsa bu cihaz bir paketin indirilmesi veya kurulmasına gerek kalmadan tarayıcı aracılığıyla kullanılabilir. Bulut POS, barkod tarama tabanlı klavye emülasyonu dışında donanım kullanmak için bir donanım istasyonu gerektirir.

### <a name="hardware-profile"></a>Donanım profili

Gezinti:'ı **ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profilleri**. Donanım profili bir POS kaydına veya bir donanım istasyonuna bağlı donanımı tanımlar. Donanım profili, ödeme yazılım geliştirme seti (SDK) ile iletişim sırasında kullanılması gereken ödeme işlemcisi parametrelerini belirlemek için de kullanılır. (Ödeme SDK, donanım istasyonunun bir parçası olarak dağıtılır.)

### <a name="hardware-station"></a>Donanım istasyonu

Gezinti:'ı **perakende ve ticaret**&gt;**kanallar**&gt;**perakende mağazalar**&gt;**tüm perakende mağazalar**. Bir mağaza seçin ve sonra **Donanım istasyonları** FastTab'a tıklayın. Donanım istasyonu, POS çevre birimlerini destekleyen bir iş mantığı örneğidir. Yazılım istasyonu MPOS ile birlikte otomatik olarak yüklenir. Alternatif olarak, yazılım istasyonu bağımsız bir bileşen olarak yüklenebilir ve bir web hizmeti üzerinden MPOS veya Bulut POS'la erişilebilir. Donanım istasyonu kanal düzeyinde tanımlanmalıdır.

### <a name="hardware-station-profile"></a>Donanım istasyonu profili

Gezinti:'ı **ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım istasyon profilleri**. Kanal düzeyinde belirtilen donanım istasyonunun kendisi donanım istasyonu URL'si gibi örneğe özgü bilgileri içerirken, donanım istasyonu profili statik veya birden fazla donanım istasyonu arasında paylaşılan bilgileri içerir. Statik bilgiler kullanılması gereken bağlantı noktasını, donanım istasyonu paketini ve donanım profilini içerir. Statik bilgiler, örneğin her bir donanım istasyonu için gereken donanıma bağlı olarak **Ödeme **veya **İadeler** gibi, dağıtılan donanım istasyonu türünün tanımını da içerir.

## <a name="scenarios"></a>Senaryolar
### <a name="mpos-with-connected-peripheral-devices"></a>Çevre birimi cihazlarına bağlı MPOS

[![Geleneksel sabit satış noktası,](./media/traditional-300x279.png)](./media/traditional.png) MPOS POS çevre Geleneksel, sabit POS senaryoda bağlanmak için ilk kayıt için gidin ve bir donanım profili atayabilirsiniz. POS kasalarda bulabilirsiniz **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**kayıtları**. Donanım profilini atadıktan sonra "Kayıtlar" dağıtım planını kullanarak değişiklikleri kanal veritabanıyla eşitleyin. Adresindeki Dağıtım tabloları bulabilirsiniz **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**. Daha sonra kanalda "yerel" bir donanım istasyonu kurun. ' I **perakende ve ticaret**&gt;**kanallar**&gt;**perakende mağazalar**&gt;**tüm perakende mağazalar**ve bir mağaza seçin. Ardından bir donanım istasyonu eklemek için **Donanım istasyonları** FastTab üzerinden **Ekle**'ye tıklayın. Bir açıklama girin, ana bilgisayar adı olarak **localhost** yazın ve "Kanal konfigürasyonu" dağıtım planını kullanarak değişiklikleri kanalla eşitleyin. Adresindeki Dağıtım tabloları bulabilirsiniz **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**. Son olarak, MPOS'ta **localhost** donanım istasyonunu seçmek için **Donanım istasyonu seç** işlemini kullanın. Donanım istasyonunu **Etkin** olarak ayarlayın. Bu senaryoda kullanılan donanım profili POS kaydının kendisinden gelmelidir. Bu senaryo için bir donanım istasyonu profili gerekmez. **Not:** Kasa çekmeceleri gibi bazı donanım profili değişiklikleri kanalla eşitlendikten sonra yeni bir vardiyanın açılmasını gerektirir. **Not:** Bulut POS'ta perakende çevre birimleriyle iletişim kurmak için bağımsız donanım istasyonu kullanılmalıdır.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>Bağımsız donanım istasyonlu MPOS veya Bulut POS

\[Başlık kimliği = "ek\_340041" align = "alignleft" width = "300" =\][![çevre paylaşılan](./media/shared-300x254.png)](./media/shared.png) çevre paylaşılan\[/altyazı\] Bu senaryoda, bir bağımsız donanım istasyon MPOS ve bulut POS istemcileri arasında paylaşılır. Bu senaryoda donanım istasyonunun kullandığı indirme paketi, bağlantı noktası ve donanım profilini belirtmek için bir donanım istasyonu profili oluşturmanız gerekir. İstasyon donanım profilinde bulabilirsiniz **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım istasyon profilleri**. İstasyon donanım profili oluşturduktan sonra belirli perakende kanalına gidin (**perakende ve ticaret**&gt;**kanallar**&gt;**perakende mağazalar**&gt;**tüm perakende mağazalar**) ve yeni bir donanım istasyon ekleyin. Bu yeni donanım istasyonunu daha önce oluşturulan donanım istasyonu profiliyle eşleyin. Ardından, kasiyerin donanım istasyonunu tanımlamasına yardımcı olacak bir açıklama girin. İçinde **ana bilgisayar adı** alan, ana makine URL'yi aşağıdaki biçimde girin: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Yerine **&lt;MachineName:Port&gt;** donanım istasyon ve donanım istasyon profilde belirtilen bağlantı noktası gerçek makine adıyla.) Bir tek başına donanım istasyon için de terminal kimliği (EFT) elektronik fon transferi belirtmeniz Bu değer, ödeme bağlayıcısı ödeme sağlayıcı ile iletişim kurduğunda donanım istasyonuna bağlanan EFT terminalini tanımlar. Daha sonra asıl donanım istasyonu makinesinden kanala gidin ve donanım istasyonunu seçin. Ardından, **İndir**'e tıklayın ve donanım istasyonunu yükleyin. Daha sonra MPOS veya Bulut POS'tan önceden yüklenmiş donanım istasyonunu seçmek için **Donanım istasyonu seç** işlemini kullanın. POS ile donanım istasyonu arasında güvenli bir ilişki kurmak için **Eşleştir** 'i seçin. Bu adım bir POS ve bir donanım istasyonunun her birleşimi için bir kez tamamlanmalıdır. Donanım istasyonu eşleştirildikten sonra, aynı işlem donanım istasyonunu kullanılırken etkinleştirmek için kullanılır. Bu senaryo için donanım profili Kaydet yerine donanım istasyonu profili atanmalıdır. Herhangi bir nedenden dolayı donanım istasyon doğrudan atanmış bir donanım profili yoksa, daha sonra kaydetmesi için atanan donanım profili kullanılır

## <a name="client-maintenance"></a>İstemci bakımı
### <a name="registers"></a>Kayıtlar

POS kayıtları öncelikle kendi kayıtları ve kayıtlara atanan profiller aracılığıyla yönetilir. Ayrı bir kayda özgü öznitelikler kayıt düzeyinde yönetilir. Bu öznitelikler kaydın kullanıldığı mağazayı, kayıt numarasını, açıklamayı ve kaydın kendisine özgü EFT terminali kodunu içerir.

### <a name="pos-profiles"></a>POS profilleri

POS profilleri adresinde bulabilirsiniz **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**. Profiller aracılığıyla bir kaydın çeşitli özelliklerini yönetmek yararlıdır, çünkü profiller birçok kayıt arasında paylaşılabilir. Profiller ayrı bir kayıtla eşlenebileceği gibi profil mağaza kapsamında geçerliyse perakende mağazayla da eşlenebilir. Aşağıdaki bölümlerde, POS profilleri ve bunların nasıl kullanıldıkları açıklanır.

#### <a name="offline-profile"></a>Çevrimdışı profil

Çevrimdışı profil mağaza düzeyinde ayarlanır. Kayıt, kanal veritabanına bağlı değilken bir POS kaydı üzerinde gerçekleştirilen işlemler için yükleme ayarlarını belirtmek amacıyla kullanılır.

#### <a name="functionality-profile"></a>İşlevsellik profili

İşlevsellik profili mağaza düzeyinde ayarlanır. POS gerçekleştirilebilecek işlevleri hakkında mağaza çapında ayarları belirtmek için kullanılır. Aşağıdaki yetenekleri işlevsellik profili yönetilir. Bu yetenekler FastTab'a göre düzenlenir.

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
    -   Bilgi kodları POS'a nasıl yönetildiğini tüm yönleri. Ayrıntılar için bkz: [bilgi kodları](info-codes-retail.md).
-   **Makbuz numaralandırma** FastTab'i:
    -   Mağaza numarası, terminal numarası, sabitler ve satışların, iadelerin, satış siparişlerinin ve tekliflerin ayrı seriler halinde mi yazdırıldığı yoksa tümünün aynı seriyi mi takip ettiği gibi parçaları içerebilecek makbuz numaralandırma maskelerini belirtin.

#### <a name="receipt-profiles"></a>Makbuz profilleri

Giriş profilleri donanım profili içinden yazıcılara atanır. Bunlar belirli bir yazıcıda yazdırılmış giriş türlerini belirtmek için kullanılır. Profiller giriş biçimleri için ayarları ve makbuzun her zaman yazdırılıp yazdırılmadığını veya kasiyerden makbuzun yazdırılması gerekip gerekmediğine karar vermesinin istenip istenmediğini belirleyen ayarları içerir. Farklı yazıcılar farklı giriş profillerini de kullanabilir. Örneğin, yazıcı 1 standart termal makbuz yazıcısıdır ve bu nedenle daha küçük giriş biçimlerine sahiptir. Ancak yazıcı 2 yalnızca müşteri sipariş girişlerini yazdırmak için kullanılan tam boyutlu bir makbuz yazıcısı olup daha fazla alan gerektirir.

#### <a name="hardware-profiles"></a>Donanım profilleri

Donanım profilleri bu makalenin önceki bölümlerinde istemci kurulumu bileşeni olarak açıklanmıştır. Donanım profilleri doğrudan POS kaydına veya donanım istasyonu profiline atanır. Bunlar belirli bir POS kaydı veya donanım istasyonunun kullandığı cihazların türlerini belirtmek için kullanılır. Donanım profilleri, ödeme SDK ile iletişim kurmak için kullanılan EFT ayarlarını belirtmek için de kullanılır.

#### <a name="visual-profiles"></a>Görsel profiller

Görsel profiller kayıt düzeyinde atanır. Belirli bir kayıt için temayı belirtmek amacıyla kullanılırlar. Profiller kullanılan uygulamanın türü (MPOS veya Bulut POS), vurgu rengi ve tema, yazı tipi düzeni, oturum açma ve POS arka planları için ayarları içerir.

### <a name="custom-fields"></a>Özel alanlar

Sistemde bulunmayan POS sağlanmayan alanları eklemek için özel alanlar oluşturabilirsiniz. Özel alanlar kullanma hakkında daha fazla bilgi için bkz: [özel alanlar Web günlüğü postası ile çalışan](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

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

Cihazın etkinleştirme durumundaki değişiklikler hariç POS istemcisindeki tüm değişikliklerin etkinleştirilmesi için kanal veritabanıyla eşitlenmesi gerekir. Kanal veritabanındaki değişiklikleri eşitlemek için gitmek **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**, ve gerekli dağıtım zamanlamasını çalıştırın. İstemci değişiklikleri için "Kayıtlar" ve "Kanal konfigürasyonu" dağıtım planlarını çalıştırmalısınız.


