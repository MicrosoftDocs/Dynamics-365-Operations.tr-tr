---
title: "Perakende çevre genel bakış"
description: "Bu konu, perakende çevre birimlerine ilgili kavramları açıklar. Bu çevre birimleri (POS) satış noktasına bağlanabilir ve POS ile bağlantı yönetiminden sorumlu olan bileşenleri çeşitli yolları açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Perakende çevre genel bakış

Bu konu, perakende çevre birimlerine ilgili kavramları açıklar. Bu çevre birimleri (POS) satış noktasına bağlanabilir ve POS ile bağlantı yönetiminden sorumlu olan bileşenleri çeşitli yolları açıklanmaktadır.

<a name="concepts"></a>Kavramlar
--------

### <a name="pos-registers"></a>POS kayıtları

Gezinti:'ı **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**kayıtları**. Noktası (POS) satış kasa POS belirli bir örneğinin özelliklerini tanımlamak için kullanılan bir varlıktır. Donanım profili veya Kurulum kasa, kasa eşlenen mağaza ve görsel deneyim o kasaya oturumu açtığında kullanıcı için kullanılacak perakende çevre birimleri için bu özellikleri içerir.

### <a name="devices"></a>Aygıtlar

Gezinti:'ı **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**aygıtları**. Cihaz, POS kaydının eşlendiği bir cihazın fiziksel örneğini gösteren bir varlıktır. Bir aygıt oluşturulduğunda bir POS için eşleştirilir kaydı. Cihaz varlığı, bir POS kaydı etkinleştirildiğinde kullanılan istemci türü ve belirli bir cihaza dağıtılan uygulama paketi hakkındaki bilgileri izler. Aygıtları aşağıdaki uygulama türlerine eşlenen: Modern POS perakende, bulut POS perakende, perakende Modern POS – Windows Phone, Modern POS perakende – Android ve Modern POS perakende – IOS.

### <a name="retail-modern-pos"></a>Perakende Modern POS

Modern POS, Microsoft Windows için POS programıdır. 10 Windows işletim sistemlerinde (OSs) dağıtılabilir.

### <a name="cloud-pos"></a>Bulut POS

Bulut POS bir web tarayıcısında erişilebilir Modern POS programı, tarayıcı tabanlı bir sürümüdür.

### <a name="modern-pos-for-ios"></a>IOS için modern POS

Modern POS IOS için IOS aygıtlara dağıtılabilir Modern POS programı IOS tabanlı bir sürümü var.

### <a name="modern-pos-for-android"></a>Android için modern POS

Modern POS Android için Android aygıtlar üzerinde dağıtılabilir Modern POS programı Android tabanlı bir sürümü var.

### <a name="pos-peripherals"></a>POS çevre birimleri

POS çevre birimleri için POS işlevleri açıkça desteklenen aygıtlardır. Bu tür çevresel aygıtlar, genellikle belirli sınıflara ayrılmıştır. Bu sınıflar hakkında daha fazla bilgi için bu konudaki "Aygıt sınıfları" bölümüne bakın.

### <a name="hardware-station"></a>Donanım istasyonu

Gezinti:'ı **perakende ve ticaret**&gt;**kanallar**&gt;**perakende mağazalar**&gt;**tüm perakende mağazalar**. Bir mağaza seçin ve sonra **Donanım istasyonları** FastTab'a tıklayın. **Donanım istasyon** burada perakende çevresel mantık dağıtılan örneklerini tanımlamak için kullanılan bir kanal düzeyindeki ayar ayardır. Bu ayar kanal düzeyinde donanım istasyon özelliklerini belirlemek için kullanılır. Belirli bir mağazanın Modern POS örneğinde kullanılabilir liste donanım istasyonları için de kullanılır. Donanım istasyon Modern POS programa Windows için yerleşik olarak bulunur. Donanım istasyon da bağımsız olarak tek başına bir Microsoft Internet Information Services (IIS) programı olarak dağıtılabilir. Bu durumda, ağ üzerinden erişilebilir.

### <a name="hardware-profile"></a>Donanım profili

Gezinti:'ı **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profilleri**. Donanım profili, POS kaydı veya donanım istasyon için yapılandırılan aygıtlar listesidir. Donanım profili, POS kaydı veya donanım istasyon doğrudan eşlenebilir.

## <a name="devices-classes"></a>Aygıt sınıfları
POS çevre genellikle sınıflara ayrılmıştır. Bu bölümde açıklanmış ve Modern POS destekleyen aygıtlar için genel bir bakış sağlar.

### <a name="printer"></a>Yazıcı

Yazıcılar, geleneksel POS Makbuz Yazıcılar ve tam sayfa yazıcıları içerir. Yazıcı, nesne bağlama ve katıştırma Retail POS (OPOS) ve Microsoft Windows Sürücü arabirimler aracılığıyla desteklenir. Aynı anda en fazla iki yazıcı kullanılabilir. Daha fazla bilgi taşıyan, müşteri siparişleri, tam sayfa bir yazıcıda yazdırılan ise bu yeteneği nerede cash-and-carry müşteri giriş giriş yazıcılarda yazdırılır senaryolarını desteklemektedir. Makbuz yazıcılar, Ethernet aracılığıyla bir ağa bağlanan veya Bluetooth bağlı doğrudan bir bilgisayara USB üzerinden bağlı.

### <a name="scanner"></a>Tarayıcı

En çok iki barkod tarayıcılar aynı anda kullanılabilir. Bu özellik, sabit bir katıştırılmış tarayıcı çoğu Standart boyutta maddeler için kullanıma alma işlemlerini hızlandırmak için kullanılırken daha taşınabilir bir tarayıcı büyük ya da ağır maddeleri taramak için gerekli olduğu senaryolar destekler. Tarayıcılar OPOS, Evrensel Windows Platformu (UWP) veya klavye Golf Sopası arabirimler desteklenebilir. USB veya Bluetooth, bir tarayıcı bir bilgisayara bağlanmak için kullanılabilir.

### <a name="msr"></a>MSR

Bir USB Manyetik Bant Okuyucu (MSR) OPOS sürücülerini kullanarak ayarlanabilir. Tek başına bir MSR elektronik fon transferi (EFT) ödeme hareketleri için kullanmak istiyorsanız, MSR ödeme Bağlayıcısı tarafından yönetiliyor olması gerekir. Tek başına MSRs müşteri bağlılık girişi, çalışan oturum aç ve ödeme bağlayıcı bağımsız olarak Hediye kartı girişi için kullanılabilir.

### <a name="cash-drawer"></a>Nakit Çekmecesi

Nakit Çekmecesi iki donanım profili desteklenebilir. Kaydı aynı anda kullanılabilir olması için her iki etkin vardiyası bu yeteneği sağlar. Paylaşılan bir shift veya aynı anda birden çok mobil POS aygıt tarafından kullanılan bir para çekmecesini söz konusu olduğunda, yalnızca bir para çekmecesini donanım profili izin verilir. Nakit Çekmecesi, ağa bağlı veya bir makbuz yazıcısı RJ12 arabirimi üzerinden bağlı doğrudan bir bilgisayara USB üzerinden bağlı. Bazı durumlarda, Nakit Çekmecesi Bluetooth bağlanabilir.

### <a name="line-display"></a>Satır görüntüleme

Satırını görüntüler, ürünler, hareket bakiyeleri ve diğer yararlı bilgileri müşteriye bir hareket sırasında göstermek için kullanılır. Bir satır görüntüleme OPOS sürücülerini kullanarak USB ile bilgisayara bağlanabilir.

### <a name="signature-capture"></a>İmza alma

İmza yakalama aygıtları doğrudan bilgisayara USB üzerinden OPOS sürücülerini kullanarak bağlanabilir. İmza yakalama yapılandırıldığında, müşteri aygıtta oturum açmanız istenir. İmza sağlanan sonra kabul Kasiyerin gösterilir.

### <a name="scale"></a>Ölçek

Ölçekler USP aracılığıyla bilgisayara OPOS sürücülerini kullanarak bağlanabilir. "Weighed" ürün olarak işaretlenmiş bir ürün için bir hareket eklendiğinde, POS ağırlık ölçeğindeki okuyan, ürün harekete ekler ve ölçek sağlanan miktarı kullanır.

### <a name="pin-pad"></a>PIN pad

Kişisel kimlik numarası (PIN) PAD'ler OPOS desteklenir, ancak ödeme bağlayıcı yönetilmelidir.

### <a name="secondary-display"></a>İkincil görüntü

İkincil görüntü yapılandırıldığında, sayı 2 Windows görüntü temel bilgileri göstermek için kullanılır. İkincil görüntü amacı kutudan çıktığında, ikincil görüntü yapılandırılabilir değildir ve sınırlı içerik gösterilir çünkü bağımsız yazılım satıcısı (ISV) uzantısı desteklemektir.

### <a name="payment-device"></a>Ödeme cihazı

Ödeme bağlayıcı üzerinden ödeme aygıt desteği uygulanır. Ödeme aygıtları, bir veya diğer aygıt sınıfları sağlar işlevlerin çoğunu gerçekleştirebilirsiniz. Örneğin, bir ödeme aygıtı, bir MSR/kart okuyucu, satır görüntüleme, imza yakalama aygıtı veya PIN pad işlev görebilir. Ödeme aygıtları uygulanır bağımsız donanım profilinde bulunan diğer aygıtları için sağlanan tek başına aygıt destek desteği.

## <a name="supported-interfaces"></a>Desteklenen arabirimleri
### <a name="opos"></a>OPOS

Microsoft Dynamics 365 ile - işlemlerinde kullanılabilir aygıtlar en büyük aralığı sağlanmasına yardımcı olmak için perakende, POS endüstri standardı için OLE işlemleri - perakende Microsoft Dynamics 365 desteklenmeyen birincil perakende çevre aygıtı platformudur. POS standardı için OLE tarafından Ulusal perakende federasyon (Perakende çevre aygıtları için endüstri standardında bir iletişim protokollerini oluşturan NRF), üretilmiştir. OPOS POS standardı için OLE yaygın olarak benimsenen bir uygulamasıdır. 1990'ların ortalarında içinde geliştirilmiştir ve daha sonra bu yana birkaç kez güncelleştirildi. OPOS POS donanım POS Windows tabanlı sistemleri ile kolay tümleştirme sağlayan bir aygıt sürücüsü mimarisi sağlar. OPOS tanıtıcı uyumlu donanım ve yazılım POS arasındaki iletişimi denetler. OPOS denetimi iki bölümden oluşur:

-   **Denetim nesnesi** – denetim nesnesi (örneğin, satır görüntüler) aygıt sınıfı için yazılım programı için arabirim sağlar. Monroe Danışmanlık Hizmetleri ([www.monroecs.com](http://www.monroecs.com/)) standartlaştırılmış genel kontrol nesneleri (CCOs) olarak bilinen OPOS denetim nesneleri kümesi sağlar. CCOs POS bileşeni olan Microsoft Dynamics 365 işlemleri - perakende için test etmek için kullanılır. Üretici OPOS için yerleşik bir hizmet nesnesi sağlar Microsoft Dynamics 365 işlemleri - perakende destekleyen bir aygıt sınıfı OPOS, birçok aygıt türü ile desteklenen için sağlanan bu nedenle, sınama, garanti yardımcı olur. Her aygıt türü açıkça test gerekmez.
-   **Servis nesnesi** – hizmet nesnesinin denetim nesnesi (CCO) aygıt arasındaki iletişimi sağlar. Genellikle, hizmet nesnesinin bir aygıt için aygıt üreticisi tarafından sağlanır. Ancak, bazı durumlarda, hizmet nesnesinin üreticisinin Web sitesinden yüklemek olabilir. Örneğin, daha yeni bir hizmet nesnesi kullanılabilir olabilir. Üreticinin Web sitesi adresini bulmak için donanım belgelerinize bakın.

[![Denetim nesnesi ve servis nesnesi](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) destek OLE OPOS uygulanması için aygıt üreticileri ve POS yayımcılar standart doğru uygularsanız, POS sistemleri ve desteklenen aygıtlar birlikte çalışabilir, bunlar daha önce birlikte test uygulamasında olsa bile garanti POS yardımcı olur. **Not:** OPOS destek OPOS sürücülere sahip tüm aygıtları için destek garanti etmez. İşlemleri - 365 Microsoft Dynamics Retail ilk o aygıt türü veya sýnýfa OPOS desteklemesi gerekir. Ayrıca, Servis nesneleri her zaman en son sürümünü CCOs ile güncel olmayabilir. Genel olarak, hizmet nesnelerini kalitesi değişir, farkında olmalıdır.

### <a name="windows"></a>Windows

POS Makbuz yazdırması OPOS için optimize edilmiştir. OPOS Windows yazdırma daha hızlı olma eğilimindedir. Bu nedenle, OPOS, burada 40 sütun giriş yazdırılır ve işlem süreleri hızlı özellikle perakende ortamlarda iyi fikirdir. Çoğu aygıtlar için OPOS denetimleri kullanacaksınız. Ancak, bazı OPOS makbuz yazıcılar Windows sürücüleri de destekler. Windows sürücüsünü kullanarak, son yazı tipleri ve birden çok kasalar için bir yazıcı ağ erişebilirsiniz. Ancak, Windows sürücüleri kullanarak dezavantajları vardır. Bu dezavantajı bazı örnekler şunlardır:

-   Windows sürücüleri kullanıldığında, görüntüleri yazdırma oluşmadan önce işlenir. Bu nedenle, yazdırma OPOS denetimleri kullanan yazıcılarda daha yavaş olma eğilimindedir.
-   Yazıcı ("zincirleme") bağlanan aygıtların Windows sürücüleri kullanıldığında düzgün çalışmayabilir. Örneğin, para çekmecesini açılamayabilir veya beklediğiniz gibi SLIP yazıcı word değil.
-   OPOS daha geniş bir kağıt kesme veya notu yazdırma gibi perakende makbuz yazıcılar özgü değişkenler kümesini de destekler.

Kullanmakta olduğunuz Windows yazıcı OPOS denetimleri varsa, yazıcı hala doğru işlemleri - perakende Microsoft Dynamics 365 ile çalışması gerekir.

### <a name="universal-windows-platform"></a>Evrensel Windows platformu

UWP, perakende çevre söz konusu olduğunda, ilgili Windows Tak ve Kullan aygıtları için destek. Bu tür bir aygıtı destekleyen bir Windows işletim sistemi sürümü Tak ve Kullan aygıt bağlıysa, aygıt gerektiği gibi kullanılacak sürücü yok gereklidir. Windows Bluetooth hoparlör aygıtı algılarsa, örneğin, işletim Sisteminin aygıt olduğunu bilir **hoparlör** sınıf türü. Bu nedenle, ve bu aygıtın bir Konuşmacı kabul eder. Hiçbir ek kurulum gereklidir. POS aygıtları, pek çok USB aygıtı takılı, ve Windows İnsan arayüz aygıtları (HIDs) tanıyacaktır. Ancak, bu aygıt sınıfı veya aygıt türünü belirtmek değildir çünkü sağlayan aygıt yeteneklerini saptamak mümkün olmayabilir. Barkod tarayıcılar ve MSRs için aygıt sınıflarını Windows 10'da eklenmiştir. Aygıt kendisini Windows 10 için bu sınıfların bir aygıt olarak bildirirse, bu nedenle, Windows aygıtı üzerindeki olaylara yönelik uygun zamanlarda dinleyecektir. Modern POS UWP MSRs ve tarayıcıları destekler. Bu nedenle, bu aygıtlardan birini girişten hazırdır ve bu sınıfların birine ait bir aygıt bağlıysa, aygıt kullanılabilir. Örneğin, bar kod tarayıcı bir UWP bir Windows 10 bilgisayara takılı olduğundan ve barkod sign-in Modern POS için yapılandırılır, barkod tarayıcı oturum açma ekranı üzerinde etkin hale gelir. Hiçbir ek kurulum gereklidir. Ek sınıflar noktasının hizmet UWP aygıtların Windows için eklenir. Bu sınıflar, nakit çekmece ve makbuz yazıcılar için sınıfları içerir. Bu yeni Modern POS aygıt sınıfları için destek bekliyor.

### <a name="keyboard-wedge"></a>Klavye Golf Sopası

Sanki bu verileri bir klavye üzerinde yazılan klavye Golf Sopası aygıtları bilgisayara veri göndermek. Bu nedenle, varsayılan olarak, POS'a etkin olduğu alan taranmış veya geçirilen veriyi alır. Bazı durumlarda, bu davranış yanlış alanına taranacak veri yanlış türde neden olabilir. Örneğin, bir barkod kredi kartı veri girişi için tasarlanmış bir alana taraması. Çoğu durumda, taranmış veya geçirilen verileri bir barkod ya da manyetik kartı olup olmadığını belirleyen POS'a mantığı yoktur. Bu nedenle, verileri doğru şekilde ele alınır. Ancak, aygıt OPOS yerine klavye Golf Sopası aygıtları ayarlanırken, daha fazla "bilinir çünkü" nasıl bu aygıtlardan veri, veri kaynaklandığı aygıtla ilgili tüketilebilir üzerinde daha fazla denetim yok. Örneğin, bir barkod tarayıcı verileri otomatik olarak bir barkod tanınan ve daha kolay ve daha hızlı genel dize arama, klavye Golf Sopası aygıtları durumunda olduğu gibi kullanılan, ilişkili kayıt veritabanında bulunamadı.

### <a name="native-printer"></a>Yerel yazıcı

Yerel (veya donanım profilinde "Aygıt" türü olarak adlandırılır) yazıcılar bilgisayar için yapılandırılmış bir yazıcı seçmek için kullanıcıdan şekilde yapılandırılabilir. Bir yazıcı, **aygıt** türü yapılandırılmış, Modern POS print komutunun karşılaşırsa kullanıcıdan bir listeden bir yazıcı seçin istenir. Bu davranış Windows sürücüleri için davranış çünkü farklı **Windows** yazıcı türü donanım profili olmayan yazıcıların listesini göster. Bunun yerine, adlandırılmış bir yazıcı sağlanmasını gerektirir **aygıt adı** alan.

### <a name="windows"></a>Windows

**Windows** yazıcılar için kullanılan aygıt türü. Windows yazıcı donanım profilinde yapılandırıldığında, belirli bir yazıcı adı sağlanmalıdır. Windows yazıcı yapılandırılmışsa, Modern POS yazdırma olayları karşılaştığında, olay belirtilen Windows yazıcıya gönderilir. Kullanıcı, bir yazıcı seçmek için istenmez.

### <a name="network"></a>Ağ

Ağ adreslenebilir Nakit Çekmecesi, makbuz Yazıcılar ve ödeme terminalleri, doğrudan Windows için Modern POS uygulaması içinde kurulan Ara işlem iletişimlerini (IPC) donanım istasyon veya diğer Modern POS istemciler için IIS donanım istasyon üzerinden bir ağ üzerinden kullanılabilir.

## <a name="hardware-station-deployment-options"></a>Donanım istasyonu dağıtım seçenekleri
### <a name="ipc-built-in"></a>IPC (yerleşik)

Ara işlem iletişimlerini (IPC) donanım istasyon için Modern POS Windows uygulamasına yerleşik olarak bulunur. IPC donanım istasyon kullanmak için Windows için Modern POS uygulaması kullanan bir kayıt için bir donanım profili atayın. Sonra bir donanım istasyonu oluşturmak **adanmış** burada kasa kullanılacak mağaza türü. Modern POS başlattığınızda, IPC donanım istasyon etkin olması ve konfigüre edilmiş POS çevre kullanıma hazır olacaktır. Herhangi bir nedenle geçici olarak yerel donanım gerektirmeyen, kullanın **donanım istasyonlarını yönetme** işlem donanım istasyon özellikleri devre dışı bırakmak için. Modern POS IPC donanım istasyon ağ çevre ile doğrudan iletişim kurmak için de kullanabilirsiniz.

### <a name="iis"></a>IIS

IIS veya donanım istasyon iki yolla tek başına bir sürümünü kullanabilirsiniz. Tanımlayıcısı "IIS" POS uygulaması Microsoft Internet Information Services aracılığıyla donanım istasyonu bağlanır anlamına gelir. POS uygulaması burada aygıtlar bağlı IIS donanım istasyona bir bilgisayarda çalışan web servisleri üzerinden bağlanır. IIS kullanıldığında, bir donanım istasyonuna bağlı perakende çevre kullanılan IIS donanım istasyon aynı ağ üzerindeki tüm POS kaydı tarafından. Yalnızca Modern POS için Windows Perakende çevre birimleri için yerleşik destek bulunması nedeniyle, tüm Modern POS uygulamaları donanım profilinde yapılandırılmış POS çevre birimleri ile iletişim kurmak için IIS donanım istasyon kullanmanız gerekir. Bu nedenle, IIS donanım istasyonun her örnek bir web hizmetinin çalıştığı bilgisayar ve aygıtlarla iletişim kuran uygulama gerektirir. IIS donanım istasyonu tüm olmayan - Windows Modern POS uygulamaları için gereklidir.

#### <a name="dedicated"></a>Ayrılmış

Modern POS kullanan donanım istasyonları, **adanmış** çevre app nerede kullanılıyor bilgisayara doğrudan bağlı olan algılamak için yazın. Ancak, **adanmış** türü IIS donanım istasyonları için de kullanılabilir. Bulut POS POS uygulaması olarak kullanan bir senaryoda Geleneksel, sabit POS **adanmış** donanım istasyon türü bulut POS çalışan aynı bilgisayara dağıtılan IIS donanım istasyonları için kullanılır. Perakende çevre açısından bakıldığında, IIS adanmış donanım istasyonu daha iyi Geleneksel, sabit POS senaryoları için çevre desteği perakende. Adanmış donanım istasyonları donanım profilinde desteklenen tüm çevre birimlerini destekler.

#### <a name="shared"></a>Paylaştırılmış

Paylaşılan donanım istasyonları kurs günün üzerinden birden çok POS aygıtları tarafından kullanılmak üzere tasarlanmıştır. Paylaşılan donanım istasyonları desteği yalnızca Nakit Çekmecesi, makbuz Yazıcılar ve ödeme terminalleri için en iyi duruma getirilir. Tek başına barkod tarayıcılar, MSRs, satırı görüntüler, Ölçek veya diğer aygıtlar doğrudan bağlanamazsınız. Aksi halde, POS aygıtlar birden fazla aynı anda bu çevre talep etmeye çalıştığınızda çakışmaları ortaya çıkar. İşte çakışmalar için desteklenen aygıtlar nasıl yönetilir:

-   **Nakit Çekmecesi** – para çekmecesini aygıta gönderilen bir olay ile açılır. Nakit Çekmecesi çağrıldığında oluşabilecek tek sorun para çekmecesini zaten açıksa oluşur. Nakit Çekmecesi ayarlanması gerektiğini paylaşılan donanım istasyonları söz konusu olduğunda, **Shared** donanım profilinde. Bu ayar, POS Aç komutlarını gönderdiğinde para çekmecesini zaten açık olup olmadığını denetlemesini önler.
-   **Makbuz yazıcısı** – iki giriş yazdırma komutlarını donanım istasyona aynı zamanda bir komut gönderilir, aygıta bağlı olarak kaybolabilir. Bazı aygıtlar dahili belleğe sahip veya havuzu bu sorunu önleyebilirsiniz. Yazdırma komutu başarılı değilse, kasiyer bir hata iletisi alır ve POS Yazdır komutunu yeniden deneyebilirsiniz.
-   **Ödeme terminal** – kasiyer çalışır zaten kullanılmakta olan bir harekette terminal ödeme ödeme için bir ileti bildirirse kasiyer terminal kullanılıyor ve daha sonra yeniden deneyin kasiyere sorar. Genellikle, bir terminal zaten kullanılıyor ve ödeme yeniden denemeden önce diğer işlem tamamlanana kadar bekler kasiyerler görebilirsiniz.

Doğrulama desteklenmeyen aygıtlar için paylaşılan donanım istasyona eşlenen bir donanım profili ayarlanmış olup olmadığını algılamak için gelecekteki bir sürümde planlanmaktadır. Desteklenmeyen herhangi bir aygıtı algıladıysa, kullanıcı aygıtları için paylaşılan donanım istasyonları desteklenmez bildiren bir ileti alırsınız. Paylaşılan donanım istasyonları, söz konusu olduğunda **tendering üzerine seçin** seçeneği ayarlanmış **Evet** kayıt düzeyinde. POS kullanıcı sonra POS bir hareket için bir ödeme seçildiğinde donanım istasyon arasında seçim yapması istenir. Donanım istasyonu yalnızca anında ödeme seçildiğinde, donanım istasyon seçimi doğrudan mobil senaryoları için POS akışına eklenir. Ek bir avantaj olarak, terminal ödeme satır görünümünde Paylaşılan senaryoları için kullanýlmaz. Terminal ödeme satırı görüntü biçimi kullanılırsa, işlem tamamlanıncaya kadar bu terminal kullanarak diğer kullanıcıların engellenebilir. Mobil senaryolarda, bir hareket uzun bir süre için satırlar eklenebilir. Bu nedenle, **tendering üzerine seçin** seçenek en uygun aygıt kullanılabilir olmasını sağlamak için gereklidir.

### <a name="network-peripherals"></a>Ağ çevre birimleri

Nakit Çekmecesi, makbuz Yazıcılar ve ağ bağlantısı ödeme terminalleri donanım profilinde aygıtlar için ağ atamasını sağlar.

#### <a name="modern-pos-for-windows"></a>Windows için modern POS

İki ayrı yerde çevre ağı için IP adresleri belirtebilirsiniz. Modern POS Windows İstemcisi tek bir ağ çevre birimleri kümesi kullanıyorsanız, bu aygıtların IP adreslerini kullanarak ayarlamanız gerekir **IP yapılandırmasını** kayıt için eylem bölmesi seçeneğini. Paylaşılacaktır ağ aygıtlarını durumunda POS kayıtları arasında paylaşılan donanım istasyona doğrudan ağ aygıtlarını atanmış olan bir donanım profili eşlenebilir. IP adreslerini atamak için bu donanım istasyonu seçin **perakende mağazalar** sayfa ve sonra **IP yapılandırmasını** seçeneğini **donanım istasyonları** bu donanım istasyonu atanan ağ aygıtlarını belirtmek için bölüm. Yalnızca ağ aygıtlarına sahip donanım istasyonları, donanım istasyon dağıtmak zorunda değilsiniz. Bu durumda, donanım istasyonu yalnızca kavramsal olarak adreslenebilir ağ aygıtları perakende depolama konumlarına göre gruplandırmak için gereklidir.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>POS ve Modern POS için IOS Android için Modern POS bulut

Fiziksel olarak bağlı ve ağ adreslenebilir çevre sürücüler mantığı donanım istasyonu yer alıyor. Bu nedenle, Modern POS için Windows dışındaki tüm POS istemcileri için bir IIS donanım istasyonu dağıtılan ve çevre, ne olursa olsun bu çevre birimleri fiziksel donanım istasyonuna bağlı mı yoksa ağ üzerinden gönderilen ile iletişim kurmak POS etkinleştirmek için etkin olması gerekir.

## <a name="setup-and-configuration"></a>Kurulum ve yapılandırma
### <a name="hardware-station-installation"></a>Donanım istasyon yükleme

Bilgi için bkz: [perakende donanım istasyonu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS Windows için Kurulum ve yapılandırma

Bilgi için bkz: [Modern POS perakende yapılandırma ve yükleme](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS aygıt kurulum ve yapılandırma

OPOS bileşenleri hakkında daha fazla bilgi için bu belgenin "desteklenen arabirimleri" bölümüne bakın. Genellikle, OPOS sürücüler aygıt üreticisi tarafından sağlanır. Bir OPOS aygıt sürücüsü yüklendiğinde, Windows kayıt defterinde aşağıdaki konumlardan birinde bir anahtar ekler:

-   **32-bit sistem:** HKEY\_yerel\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bit sistem:** HKEY\_yerel\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

ServiceOPOS kayıt defteri konumu içinde yapılandırılan aygıtları OPOS aygıt sınıfına göre düzenlenir. Birden fazla aygıt sürücüsü kaydedilir.

## <a name="supported-scenarios-by-hardware-station-type"></a>Senaryolar donanım istasyon türü tarafından desteklenen
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>İstemci desteği – IPC donanım istasyon IIS donanım istasyon karşılaştırması

Topoloji ve desteklenen dağıtım senaryoları aşağıdaki tabloda gösterilmektedir.

| İstemci      | IPC donanım istasyonu | IIS donanım istasyonu |
|-------------|----------------------|----------------------|
| Windows uygulaması | Evet                  | Evet                  |
| Bulut POS   | Hayır                   | Evet                  |
| Android     | Hayır                   | Evet                  |
| IOS         | Hayır                   | Evet                  |

### <a name="network-peripherals"></a>Ağ çevre birimleri

Çevre ağ üzerinden doğrudan Windows için Modern POS uygulaması içinde kurulan donanım istasyon desteklenebilir. Diğer istemciler için bir IIS donanım istasyonu dağıtmanız gerekir.

| İstemci      | IPC donanım istasyonu | IIS donanım istasyonu |
|-------------|----------------------|----------------------|
| Windows uygulaması | Evet                  | Evet                  |
| Bulut POS   | Hayır                   | Evet                  |
| Android     | Hayır                   | Evet                  |
| IOS         | Hayır                   | Evet                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Aygıt türleri donanım istasyon türü tarafından desteklenen
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS için Windows ile bir IPC (yerleşik) donanım istasyonu

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Desteklenen aygıt sınıfı</th>
<th>Desteklenen arabirimleri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yazıcı</td>
<td><ul>
<li>OPOS</li>
<li>Windows sürücüsü</li>
<li>Aygıt</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="even">
<td>Yazıcı 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows sürücüsü</li>
<li>Aygıt</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Satır görüntüleme</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Çift ekran</td>
<td>Windows sürücüsü</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>OPOS</li>
<li>UWP (hiçbir Kurulum gereklidir.)</li>
<li>Klavye üçgen (hiçbir Kurulum gereklidir.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Keşideci</td>
<td><ul>
<li>OPOS</li>
<li>Ağ <strong>Not:</strong> sadece bir çekmece if ayarlanabilir <strong>kullanım shift paylaşılan</strong> çekmece üzerinde yapılandırılır.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Çekmece 2</td>
<td><ul>
<li>OPOS</li>
<li>Ağ <strong>Not:</strong> sadece bir çekmece if ayarlanabilir <strong>kullanım shift paylaşılan</strong> çekmece üzerinde yapılandırılır.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tarayıcı</td>
<td><ul>
<li>OPOS</li>
<li>UWP (hiçbir Kurulum gereklidir.)</li>
<li>Klavye üçgen (hiçbir Kurulum gereklidir.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tarayıcı 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (hiçbir Kurulum gereklidir.)</li>
<li>Klavye üçgen (hiçbir Kurulum gereklidir.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Ölçek</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN pad</td>
<td>OPOS (Destek özelleştirme ödeme bağlayıcısı aracılığıyla sağlanır.)</td>
</tr>
<tr class="even">
<td>İmza alma</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Ödeme terminali </td>
<td><ul>
<li>Özel aygıtları için destek</li>
<li>Ağ (daha fazla bilgi için ödeme bağlayıcı belgelerine bakın.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Adanmış bir IIS donanım istasyon olan tüm Modern POS istemcileri

**Not:** IIS donanım istasyonu adanmış"," POS istemci donanım istasyon arasında bire bir ilişki yoktur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Desteklenen aygıt sınıfı</th>
<th>Desteklenen arabirimleri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yazıcı</td>
<td><ul>
<li>OPOS</li>
<li>Windows Sürücü <strong>Not:</strong> Windows için ağ üzerinde yazıcıları paylaşma, donanım istasyonun kullanıcı yazıcıya erişim izni olmalıdır.</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="even">
<td>Yazıcı 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows sürücüsü</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Satır görüntüleme</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Keşideci</td>
<td><ul>
<li>OPOS</li>
<li>Ağ <strong>Not:</strong> if donanım profili başına yalnızca bir çekmece ayarlanabilir <strong>kullanım shift paylaşılan</strong> çekmece üzerinde yapılandırılır.</li>
</ul></td>
</tr>
<tr class="even">
<td>Çekmece 2</td>
<td><ul>
<li>OPOS</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tarayıcı</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Tarayıcı 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Ölçek</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN pad</td>
<td>OPOS (Destek özelleştirme ödeme bağlayıcısı aracılığıyla sağlanır.)</td>
</tr>
<tr class="odd">
<td>Sig. Yakalama</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Ödeme terminali </td>
<td><ul>
<li>Özel aygıtları için destek</li>
<li>Ağ (daha fazla bilgi için ödeme bağlayıcı belgelerine bakın.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Paylaşılan IIS donanım istasyonu olan tüm Modern POS istemcileri

**Not:** IIS donanım istasyon "paylaşıldığında," aynı anda birden çok aygıt donanım istasyonu kullanabilirsiniz. Bu senaryoda, aşağıdaki tabloda listelenen aygıtlar kullanmanız gerekir. Barkod tarayıcılar ve MSRs, gibi burada listelenmeyen aygıtları paylaşmaya çalışırsanız, birden çok aygıt aynı çevre talep etmeye çalıştığınızda hatalar ortaya çıkar. Gelecekte bu tür bir yapılandırma açıkça engellenir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Desteklenen aygıt sınıfı</th>
<th>Desteklenen arabirimleri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yazıcı</td>
<td><ul>
<li>OPOS</li>
<li>Windows Sürücü <strong>Not:</strong> Windows için ağ üzerinde yazıcıları paylaşma, donanım istasyonun kullanıcı yazıcıya erişim izni olmalıdır.</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="even">
<td>Yazıcı 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows sürücüsü</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Keşideci</td>
<td><ul>
<li>OPOS</li>
<li>Ağ <strong>Not:</strong> if donanım profili başına yalnızca bir çekmece ayarlanabilir <strong>kullanım shift paylaşılan</strong> çekmece üzerinde yapılandırılır.</li>
</ul></td>
</tr>
<tr class="even">
<td>Çekmece 2</td>
<td><ul>
<li>OPOS</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ödeme terminali </td>
<td><ul>
<li>Özel aygıtları için destek</li>
<li>Ağ (daha fazla bilgi için ödeme bağlayıcı belgelerine bakın.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Desteklenen senaryolar için yapılandırma
Donanım profilleri oluşturma hakkında daha fazla bilgi için bkz: [tanımlayın ve kanal istemcileri kayıtlarını ve donanım istasyonları da dahil olmak üzere, koruma](define-maintain-channel-clients-registers-hw-stations.md). **Not:** 1611 işlemleri sürümü için Microsoft Dynamics 365 için donanım istasyonu profili artık kullanılmamaktadır. İstasyon donanım profilini önceden ayarlanmış öznitelikler şimdi donanım istasyon bir parçasıdır.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS için Windows ile bir IPC (yerleşik) donanım istasyonu

Bu yapılandırma Geleneksel, sabit POS kasalar için en genel bir yapılandırmadır. Bu senaryo için donanım profili bilgilerini kayıt kendisini doğrudan eşleştirilir. EFT terminal numarası kayıt üzerinde de ayarlamanız gerekir. Bu yapılandırmayı kurmak için aşağıdaki adımları izleyin.

1.  Tüm gerekli çevrebirimleri yapılandırıldığı bir donanım profili oluşturun.
2.  Donanım profili için POS kasada eşleyin.
3.  Bir donanım istasyonunu oluşturmak **adanmış** türü perakende mağaza POS kasa nerede kullanılır. Açıklama isteğe bağlıdır. **Not:** donanım istasyonu diğer özelliklerini ayarlamanız gerekmez. Kayıt defterindeki tüm diğer gerekli bilgileri, donanım profili gibi gelecektir.
4.  ' I **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**.
5.  Seçin **1090** deposuna yeni donanım profili eşitlemek için dağıtım zamanlaması. ' I **şimdi çalıştırmak** POS değişiklikler eşitleme.
6.  Seçin **1040** deposuna yeni donanım istasyon eşitlemek için dağıtım zamanlaması. ' I **şimdi çalıştırmak** POS değişiklikler eşitleme.
7.  Yükleyin ve Windows için Modern POS etkinleştirin.
8.  Modern POS için Windows'u başlatın ve bağlı çevrebirim aygıtlar kullanmaya başlar.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Adanmış bir IIS donanım istasyon olan tüm Modern POS istemcileri

Bu yapılandırma yalnızca bir POS tarafından kullanılan donanım istasyonu olan tüm Modern POS istemcileri için kullanılabilir kaydedin. Bu yapılandırmayı kurmak için aşağıdaki adımları izleyin.

1.  Tüm gerekli çevrebirimleri yapılandırıldığı bir donanım profili oluşturun.
2.  Bir donanım istasyonunu oluşturmak **adanmış** türü perakende mağaza POS kasa nerede kullanılır.
3.  Adanmış donanım istasyonda aşağıdaki özellikleri ayarlayın:
    -   **Ana bilgisayar adı** – donanım istasyon nerede çalışacak ana bilgisayar adı. **Not:** bulut POS giderebilir **localhost** bulut POS çalıştığı yerel bilgisayarda belirlemek için. Ancak, donanım istasyonla bulut POS yerleştirin için gerekli sertifika bilgisayar adı olarak da "Localhost" olmalıdır. Sorunları önlemek için her mağazanın gerektiği gibi adanmış donanım istasyon örneği liste öneririz. Her donanım istasyon için ana bilgisayar adı, donanım istasyon nereye dağıtılacağı belirli bir bilgisayar adı olmalıdır.
    -   **Bağlantı noktası** – Modern POS istemcisiyle iletişim kurmak için donanım istasyon için kullanılacak bağlantı noktası.
    -   **Donanım profili** – donanım istasyonu kendisi, kasaya atanan donanım profili kullanılacaktır sağlanan donanım profili değil.
    -   **EFT POS numarası** – EFT EFT yetkilerini gönderilirken kullanılacak terminal kimliği. Bu kimlik kredi kartı işlemcisi tarafından sağlanır.
    -   **Paket adı** – donanım istasyon dağıtıldığında kullanmak için donanım istasyon paketi.

4.  ' I **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**.
5.  Seçin **1090** deposuna yeni donanım profili eşitlemek için dağıtım zamanlaması. ' I **şimdi çalıştırmak** POS değişiklikler eşitleme.
6.  Seçin **1040** deposuna yeni donanım istasyon eşitlemek için dağıtım zamanlaması. ' I **şimdi çalıştırmak** POS değişiklikler eşitleme.
7.  Donanım istasyon yükleyin. Donanım istasyon yükleme hakkında daha fazla bilgi için bkz: [perakende donanım istasyonu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).
8.  Yükleyin ve Modern POS etkinleştirin. Modern POS yükleme hakkında daha fazla bilgi için bkz: [Modern POS perakende yapılandırma ve yükleme](retail-modern-pos-device-activation.md).
9.  Modern POS için oturum açın ve Seç **çekmece işlemleri**.
10. Başlat **donanım istasyonlarını yönetme** işlemi.
11. ' I **yönetmek**.
12. Donanım İstasyon Yönetimi sayfasında, donanım istasyonu Kapat seçeneğine ayarlayın.
13. Kullanın ve donanım istasyonu seçin **çift**.
14. Donanım istasyon eşleştirdikten sonra ' ı **Kapat**.
15. Donanım istasyon Seçimi sayfasında, son seçilen donanım istasyon etkin hale getirmek için tıklatın.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Paylaşılan IIS donanım istasyonu olan tüm Modern POS istemcileri

Bu yapılandırma, donanım istasyonlar diğer aygıtlarla paylaştığınız tüm Modern POS istemciler için kullanılabilir. Bu yapılandırmayı kurmak için aşağıdaki adımları izleyin.

1.  Gerekli çevrebirimleri yapılandırıldığı bir donanım profili oluşturun.
2.  Bir donanım istasyonunu oluşturmak **Shared** türü perakende mağaza POS kasa nerede kullanılır.
3.  Paylaşılan donanım istasyonda aşağıdaki özellikleri ayarlayın:
    -   **Ana bilgisayar adı** – donanım istasyon nerede çalışacak ana bilgisayar adı.
    -   **Açıklama** – yardımcı olacak metni tanımlamak donanım istasyonu gibi **verir** veya **deposunun ön**.
    -   **Bağlantı noktası** – Modern POS istemcisiyle iletişim kurmak için donanım istasyon için kullanılacak bağlantı noktası.
    -   **Donanım profili** – bir donanım profili için paylaşılan donanım istasyonları, her donanım istasyon olması gerekir. Donanım profilleri donanım istasyonlar arasında paylaşılabilir, ancak her donanım istasyona eşlenmelidir. Ayrıca, birden çok aygıt aynı paylaşılan donanım istasyonunu kullandığınızda, paylaşılan kaymaları kullanmanızı öneririz. Paylaşılan bir vardiya ayarlarken ayarlamak için **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profilleri**. Her bir paylaşılan bir donanım profili için para çekmecesini seçin ve set **Shared shift çekmece** için seçenek **Evet**.
    -   **EFT POS numarası** – EFT EFT yetkilerini gönderilirken kullanılacak terminal kimliği. Bu kimlik kredi kartı işlemcisi tarafından sağlanır.
    -   **Paket adı** – donanım istasyon dağıtıldığında kullanmak için donanım istasyon paketi.

4.  Depodaki gerekli her ek donanım istasyon için 2 ve 3 numaralı adımları yineleyin.
5.  ' I **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**.
6.  Seçin **1090** deposuna yeni donanım profili eşitlemek için dağıtım zamanlaması. ' I **şimdi çalıştırmak** POS değişiklikler eşitleme.
7.  Seçin **1040** deposuna yeni donanım istasyon eşitlemek için dağıtım zamanlaması. ' I **şimdi çalıştırmak** POS değişiklikler eşitleme.
8.  Donanım İstasyon 2 ve 3 numaralı adımları ayarlamak her ana bilgisayara yükleyin. Donanım istasyon yükleme hakkında daha fazla bilgi için bkz: [perakende donanım istasyonu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).
9.  Yükleyin ve Modern POS etkinleştirin. Modern POS yükleme hakkında daha fazla bilgi için bkz: [Modern POS perakende yapılandırma ve yükleme](retail-modern-pos-device-activation.md).
10. Modern POS için oturum açın ve Seç **çekmece işlemleri**.
11. Başlat **donanım istasyonlarını yönetme** işlemi.

12. ' I **yönetmek**.
13. Donanım İstasyon Yönetimi sayfasında, donanım istasyonu Kapat seçeneğine ayarlayın.
14. Kullanın ve donanım istasyonu seçin **çift**.
15. 14 Modern POS kullanan her donanım istasyon için tekrarlayın.
16. Gerekli donanım istasyonları eşleştirdikten sonra ' ı **Kapat**.
17. Donanım istasyon Seçimi sayfasında, son seçilen donanım istasyon etkin hale getirmek için tıklatın. **Not:** aygıtlar farklı donanım istasyonları sık kullanıyorsanız, Modern donanım istasyon bunlar ödeme işlemine başladığınızda seçmek için kasiyerlere sorulacak POS yapılandırmanızı öneririz. ' I **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**kayıtları**. Kaydı seçin ve ardından set **ödeme seçin** için seçenek **Evet**. Kullanım **1090** kanal veritabanındaki değişiklikleri eşitlemek için dağıtım zamanlaması.

## <a name="extensibility"></a>Genişletilebilirlik
Donanım istasyon için genişletilebilirlik senaryolar hakkında daha fazla bilgi için bkz: [donanım istasyon genişletilebilirlik](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Güvenlik
Geçerli güvenlik standartlarına göre aşağıdaki ayarlardan bir üretim ortamında kullanılmalıdır: **Not:** donanım istasyon yükleyici otomatik olarak Self-Servisi üzerinden yüklemesinin bir parçası olarak bu kayıt defteri düzenlemeleri yapacaktır.

-   Güvenli Yuva Katmanı (SSL) devre dışı bırakılmalıdır.
-   Yalnızca Aktarım Katmanı Güvenliği (TLS) sürüm 1.2 (veya geçerli en yüksek sürüm) etkin kullanılan ve. **Not:** varsayılan olarak, SSL ve TLS TLS 1.2 dışındaki tüm sürümü devre dışı bırakılır. Düzenlemek veya bu değerleri etkinleştirmek için şu adımları izleyin:
    1.  Windows amblemi tuşuna basın açmak için anahtar + R bir **çalıştırmak** penceresi.
    2.  İçinde **açık** alanında, yazın **Regedit**ı **Tamam**.
    3.  Yoksa bir **kullanıcı hesabı denetimi** ileti kutusu görüntülenirse,'ı **Evet**.
    4.  İçinde **Kayıt Defteri Düzenleyicisi'ni** penceresinde, gidin **HKEY\_yerel\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Aşağıdaki anahtarları yalnızca TLS 1.2 için izin vermek için otomatik olarak girildiğinde:
        -   TLS 1.2Server: etkin = 1
        -   TLS 1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: etkin = 1
        -   TLS 1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: Etkin = 0
        -   TLS 1.1Client: Etkin = 0
        -   TLS 1.0Server: Etkin = 0
        -   TLS 1.0Client: Etkin = 0
        -   SSL 3.0Server: Etkin = 0
        -   SSL 3.0Client: Etkin = 0
        -   SSL 2.0Server: Etkin = 0
        -   SSL 2.0Client: Etkin = 0
-   Bilinen, belirtilen nedenlerden dolayı gerekli olmadıkça hiçbir ek ağ bağlantı noktaları açık olmalıdır.
-   Çapraz kaynağı kaynak paylaşımını devre dışı bırakılması gerekir ve kabul edilen izin verilen kaynakları belirtmeniz gerekir.
-   Yalnızca güvenilen sertifika yetkilileri, donanım istasyon çalışan bilgisayarlarda kullanılacak sertifikaları almak için kullanılmalıdır.

**Not:** çok önemli IIS ve ödeme kartı endüstri (PCI) gereksinimleri için güvenlik yönergeleri gözden geçirin.

## <a name="peripheral-simulator"></a>Çevre birimi benzeticisi
Bilgi için bkz: [perakende çevresel simulator](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested çevre aygıtları
### <a name="ipc-built-in-hardware-station"></a>IPC (yerleşik) donanım istasyonu

Aşağıdaki çevre Modern POS için Windows'da yerleşik IPC donanım istasyonu kullanılarak sınanmıştır.

#### <a name="printer"></a>Yazıcı

| Üretici | Model    | Arabirim | Yorumlar                |
|--------------|----------|-----------|-------------------------|
| Epson        | TM-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Yıldız         | TSP650II | OPOS      |                         |
| Yıldız         | TSP650II | Özel    | Ağ bağlı   |
| Yıldız         | mPOP     | OPOS      | Bluetooth bağlı |
| HP           | F7M67AA  | OPOS      | USB güç kaynağı             |

#### <a name="bar-code-scanner"></a>Barkod tarayıcı

| Üretici  | Model         | Arabirim | Yorumlar |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Simge        | LS2208        | OPOS      |          |
| Tümleşik HP | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN pad

| Üretici | Model  | Arabirim | Yorumlar                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Özelleştirme ödeme Bağlayıcısı gerektirir |

#### <a name="payment-terminal"></a>Ödeme terminali 

| Üretici | Model | Arabirim | Yorumlar                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir                                |
| VeriFone     | MX925 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir; Ağ ve USB bağlı |
| VeriFone     | MX915 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir; Ağ ve USB bağlı |

#### <a name="cash-drawer"></a>Nakit Çekmecesi

| Üretici | Model     | Arabirim | Yorumlar                |
|--------------|-----------|-----------|-------------------------|
| Yıldız         | mPOP      | OPOS      | Bluetooth bağlı |
| APG          | Atwood    | Özel    | Ağ bağlı   |
| Yıldız         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Satır görüntüleme

| Üretici  | Model   | Arabirim | Yorumlar |
|---------------|---------|-----------|----------|
| Tümleşik HP | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>İmza alma

| Üretici | Model  | Arabirim | Yorumlar |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Ölçek

| Üretici | Model         | Arabirim | Yorumlar |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Üretici | Model       | Arabirim | Yorumlar |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Adanmış IIS donanım istasyonu

Windows için Modern POS ve bulut POS adanmış (paylaştırılmamış) IIS donanım istasyonu kullanarak aşağıdaki çevre sınanmıştır.

#### <a name="printer"></a>Yazıcı

| Üretici | Model    | Arabirim | Yorumlar                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Yıldız         | TSP650II | OPOS      |                           |
| Yıldız         | TSP650II | Özel    | Ağ bağlı     |
| Yıldız         | TSP100   | OPOS      | TSP650II sürücüleri gerektirir |
| HP           | F7M67AA  | OPOS      | USB güç kaynağı               |

#### <a name="bar-code-scanner"></a>Barkod tarayıcı

| Üretici  | Model   | Arabirim | Yorumlar |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Simge        | LS2208  | OPOS      |          |
| Tümleşik HP | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN pad

| Üretici | Model  | Arabirim | Yorumlar                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Özelleştirme ödeme Bağlayıcısı gerektirir |

#### <a name="payment-terminal"></a>Ödeme terminali 

| Üretici | Model | Arabirim | Yorumlar                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir                                |
| VeriFone     | MX925 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir; Ağ ve USB bağlı |
| VeriFone     | MX915 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir; Ağ ve USB bağlı |

#### <a name="cash-drawer"></a>Nakit Çekmecesi

| Üretici | Model     | Arabirim | Yorumlar              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Özel    | Ağ bağlı |
| Yıldız         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Satır görüntüleme

| Üretici  | Model   | Arabirim | Yorumlar |
|---------------|---------|-----------|----------|
| Tümleşik HP | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>İmza alma

| Üretici | Model  | Arabirim | Yorumlar |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Ölçek

| Üretici | Model         | Arabirim | Yorumlar |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Üretici | Model       | Arabirim | Yorumlar |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Paylaşılan IIS donanım istasyonu

Windows için Modern POS ve bulut POS paylaşılan IIS donanım istasyonu kullanarak aşağıdaki çevre sınanmıştır. **Not:** sadece bir yazıcı, ödeme Terminali ve para çekmecesini desteklenir.

#### <a name="printer"></a>Yazıcı

| Üretici | Model    | Arabirim | Yorumlar                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Yıldız         | TSP650II | OPOS      |                           |
| Yıldız         | TSP650II | Özel    | Ağ bağlı     |
| Yıldız         | TSP100   | OPOS      | TSP650II sürücüleri gerektirir |
| HP           | F7M67AA  | OPOS      | USB güç kaynağı               |

#### <a name="payment-terminal"></a>Ödeme terminali 

| Üretici | Model | Arabirim | Yorumlar                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir; Ağ ve USB bağlı |
| VeriFone     | MX915 | Özel    | Özelleştirme ödeme Bağlayıcısı gerektirir; Ağ ve USB bağlı |

#### <a name="cash-drawer"></a>Nakit Çekmecesi

| Üretici | Model     | Arabirim | Yorumlar              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Özel    | Ağ bağlı |
| Yıldız         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Sorun Giderme
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS donanım istasyon seçim listesinde algılayabilir, ancak eşleştirme tamamlanamıyor

**Çözüm:** aşağıdaki olası hata noktalarını listesini doğrulayın:

-   Modern POS çalıştıran bilgisayar donanım istasyonu çalıştıran bilgisayarda kullanılan sertifikaya güvendiğini.
    -   Bir web tarayıcısında bu kurulum doğrulamak için aşağıdaki URL'ye Git: https://&lt;bilgisayar adı&gt;:&lt;bağlantı noktası numarası&gt;/HardwareStation/ping.
    -   Bu URL bir ping bilgisayar erişilebilir ve tarayıcı sertifikanın güvenilir olup olmadığını gösterir doğrulamak için kullanır. (Örneğin, Internet Explorer uygulamasında kilit simgesi adres çubuğunda görünür. Bu simgeyi tıklattığınızda, Internet Explorer sertifikanın güvenilir olup olmadığını doğrular. Sertifika yerel bilgisayarda gösterilen sertifikanın ayrıntılarını görüntüleyerek yükleyebilirsiniz.)
-   Donanım istasyonu çalıştıran bilgisayarda Güvenlik Duvarı'nda donanım istasyonu tarafından kullanılan bağlantı noktası açıldı.
-   Donanım istasyon donanım istasyon yükleyici sonunda çalışan yükleme ticari bilgi aracı ile ticari hesap bilgileri doğru bir şekilde yükledi.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS donanım istasyon seçim listesinde algılayamıyor

**Çözüm:** birini aşağıdaki Etkenler bu soruna neden olabilir:

-   Donanım istasyonu doğru merkezinde ayarlanmadı. İstasyon donanımı ve donanım istasyonu doğru girdiğinizden emin olmak için bu konudaki adımları kullanın.
-   Kanal yapılandırmasını güncelleştirmek için işleri çalıştırılmış henüz. Bu durumda, kanal konfigürasyonu için 1070 işini çalıştırın.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS yeni Nakit Çekmecesi ayarlarını yansıtmaz.

**Çözüm:** geçerli toplu kapatın. Cari toplu işlemin kapanıncaya kadar para çekmecesini değişiklikler için Modern POS güncelleştirilmez.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modern POS bir perakende çevre ile ilgili bir sorun raporlama

**Çözüm:** Bu sorun tipik bazı nedenleri şunlardır:

-   Diğer aygıt sürücüsü yapılandırma programları kapalı olduğundan emin olun. Bu yardımcı programlar açık varsa, bunlar Modern POS veya donanım istasyon aygıtı olduğunu iddia eden engelleyebilir.
-   Perakende çevre birden fazla POS aygıtları ile paylaşılıyorsa, aşağıdaki kategorilerden birini ait olduğundan emin olun:
    -   Nakit Çekmecesi
    -   Makbuz yazıcısı
    -   Ödeme terminali 

    Çevre aşağıdaki kategorilerden birine ait değilse, donanım istasyon birden fazla POS aygıtları arasında paylaşılması çevre sağlamak için tasarlanmış değildir.
-   Bazen, aygıt sürücülerini, genel kontrol nesneleri (CCOs) düzgün çalışmayı durdurmasına neden olabilir. Bir aygıt son yüklendi, ancak düzgün çalışmıyor veya diğer sorunları fark varsa, genellikle CCOs yeniden yükleyerek sorunu çözebilirsiniz. CCOs karşıdan yüklemek için ziyaret <http://monroecs.com/oposccos_current.htm>.
-   Sınama ve sorun giderme sırasında sık sık çevre değişiklik yaparsanız, önbellek kendisini yenilemek beklemek yerine IIS Sıfırlaması gerekebilir. IIS'yi sıfırlamak için şu adımları izleyin:
    1.  Gelen **Start** menüsü, türü **CMD**.
    2.  Arama sonuçlarında, sağ **komut istemi**ı **yönetici olarak çalıştır**.
    3.  İçinde **komut istemi** penceresinde, türü **iisreset/restart** yazıp Enter tuşuna basın.
    4.  IIS yeniden başlatıldıktan sonra Modern POS yeniden başlatın.
-   Çevre aygıtları için sık sık değişiklik yaparken de sık sık başlatır ve POS istemci çıkmak dllhost işleminin bir önceki oturum geçerli oturumla etkileyebilir. Bu durumda, aygıt önceki oturum yönetme dinamik bağlantı kitaplığı (DLL) ana bilgisayar kapatılıncaya kadar kullanılamayabilir. DLL ana bilgisayarı kapatmak için şu adımları izleyin:
    1.  Gelen **Start** menüsü, türü **Görev Yöneticisi**.
    2.  Tıklatın arama sonuçlarında **Görev Yöneticisi**.
    3.  Görev Yöneticisi'nde, üzerinde **ayrıntıları** sekmesinde, etiketli sütun başlığını tıklatıp **adı** tablo adına göre alfabetik olarak sıralamak için.
    4.  Dllhost.exe bulana kadar aşağı kaydırın.
    5.  Her DLL ana seçin ve ardından **son görev**.
    6.  Modern POS DLL ana bilgisayarı kapattıktan sonra yeniden başlatın.


<a name="see-also"></a>Ayrıca bkz.
--------

[Perakende çevresel simülatörü](retail-peripheral-simulator.md)


