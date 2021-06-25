---
title: Çevre birimleri
description: Bu konu, Commerce çevre birimleriyle ilgili kavramları açıklar.
author: rubencdelgado
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 833eb271b15dd6d32501049ce9154022a388f1d4
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189587"
---
# <a name="peripherals"></a>Çevre birimleri

[!include[banner](includes/banner.md)]

Bu konu, mağaza çevre birimleriyle ilgili kavramları açıklar. Bu çevre birimlerinin satış noktasına (POS) bağlanmasıyla ilgili çeşitli yollar ve POS ile bağlantı yönetiminden sorumlu olan bileşenler açıklanmaktadır.

## <a name="concepts"></a>Kavramlar

### <a name="pos-registers"></a>POS kayıtları

Gezinti:**Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kayıtlar**'a tıklayın. Satış noktası (POS) kasası, POS'un belirli bir kurulumunun özelliklerini tanımlamak için kullanılan bir varlıktır. Bu özelliklere kasada kullanılacak donanım profili veya çevre birimleri kurulumu, kasanın eşleştiği mağaza ve bu kasada oturum açan kullanıcının görsel deneyimi dahildir.

### <a name="devices"></a>Aygıtlar

Gezinti: **Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Cihazlar**'a tıklayın. Cihaz, POS kaydının eşlendiği bir cihazın fiziksel örneğini gösteren bir varlıktır. Cihaz oluşturulduğunda bir POS kaydına eşlenir. Cihaz varlığı, bir POS kaydı etkinleştirildiğinde kullanılan istemci türü ve belirli bir cihaza dağıtılan uygulama paketi hakkındaki bilgileri izler. 

Cihazlar aşağıdaki uygulama türlerine eşlenebilir: Retail Modern POS, Retail Cloud POS, Retail Modern POS - Windows Phone, Retail Modern POS - Android ve Retail Modern POS -iOS.

### <a name="modern-pos"></a>Modern POS

Modern POS, Microsoft Windows için POS programıdır. Windows 10 işletim sistemlerinde (OSs) dağıtılabilir.

### <a name="cloud-pos"></a>Bulut POS

Bulut POS Modern POS programının bir web tarayıcısından erişilebilen tarayıcı tabanlı sürümüdür.

### <a name="modern-pos-for-ios"></a>iOS için Modern POS

iOS için Modern POS, Modern POS programının iOS aygıtlarda dağıtılabilen iOS tabanlı bir sürümüdür.

### <a name="modern-pos-for-android"></a>Modern POS for Android

Modern POS for Android, Modern POS programının Android cihazlara dağıtılabilir bir Android tabanlı sürümüdür.

### <a name="pos-peripherals"></a>POS çevre birimleri

POS çevre birimleri, POS işlevleri için açıkça desteklenen cihazlardır. Bu çevre birimleri, genellikle belirli sınıflara ayrılmıştır. Bu sınıflar hakkında daha fazla bilgi için bu konudaki "Cihaz sınıfları" bölümüne bakın.

### <a name="hardware-station"></a>Hardware Station

Gezinti: **Retail and Commerce** &gt; **Kanallar** &gt; **Mağazalar** &gt; **Tüm perakende mağazaları**'na tıklayın. Bir mağaza seçin ve sonra **Donanım istasyonları** FastTab'a tıklayın. **Donanım istasyonu** ayarı çevresel çevre birimi mantığının dağıtıldığı kurulumları tanımlamak için kullanılan kanal düzeyindeki bir ayardır. Kanal düzeyindeki bu ayar donanım istasyonu özelliklerini belirlemek için kullanılır. Ayrıca, belirli bir mağazanın Modern POS kurulumunda kullanılabilen donanım istasyonlarını listelemek için kullanılır. Donanım istasyonu Windows ve Android için Modern POS programlarına yerleşik olarak bulunur. Donanım istasyonu bağımsız olarak tek başına bir Microsoft Internet Information Services (IIS) programı olarak dağıtılabilir. Bu durumda, ağ üzerinden erişilebilir.

### <a name="hardware-profile"></a>Donanım profili

Gezinti: **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım istasyonu profilleri**'ne tıklayın. Donanım profili bir POS kasası veya bir donanım istasyonu için yapılandırılmış cihazların listesidir. Donanım profili doğrudan POS kasasıyla veya donanım istasyonuyla eşlenebilir.

## <a name="devices-classes"></a>Cihaz sınıfları
POS çevre birimleri, genellikle sınıflara ayrılmıştır. Bu bölümde Modern POS'un desteklediği cihazlar açıklanmakta ve bunlar için genel bir bakış sunulmaktadır.

### <a name="printer"></a>Yazıcı

Yazıcılar, geleneksel POS makbuz yazıcıları ve tam sayfa yazıcıları içerir. Yazıcılar Retail POS için Nesne Bağlama ve Katıştırma (OPOS) ve Microsoft Windows sürücü arabirimleri aracılığıyla desteklenir. Aynı anda en fazla iki yazıcı kullanılabilir. Bu özellik peşin müşteri girişlerinin makbuz yazıcısından yazdırıldığı, ancak daha fazla bilgi içeren müşteri siparişlerinin tam sayfa yazıcısından yazdırıldığı senaryoları destekler. Makbuz yazıcılar, USB aracılığıyla doğrudan bilgisayara, Ethernet aracılığıyla bir ağa veya Bluetooth aracılığıyla bağlanabilir.

### <a name="scanner"></a>Tarayıcı

Aynı anda en fazla iki barkod tarayıcı kullanılabilir. Bu özellik, büyük veya ağır maddeleri taramak için daha mobil bir tarayıcının gerekli olduğu ancak kullanıma alma süresini hızlandırmak amacıyla çoğu standart boyutlu madde için sabit katıştırılmış bir tarayıcının kullanıldığı senaryoları destekler. Tarayıcılar OPOS, Evrensel Windows Platformu (UWP) veya klavye emülasyonu arabirimleri ile desteklenebilir. USB veya Bluetooth, bir tarayıcıyı bir bilgisayara bağlanmak için kullanılabilir.

### <a name="msr"></a>MSR

Bir USB manyetik bant okuyucu (MSR) OPOS sürücüleri kullanılarak ayarlanabilir. Elektronik fon transferi (EFT) ödeme hareketleri için bağımsız MSR kullanmak istiyorsanız, MSR'nin bir ödeme bağlayıcısı tarafından yönetiliyor olması gerekir. Bağımsız MSR'ler müşteri bağlılık programları girişi, personel oturum açma ve hediye kartı girişi için ödeme bağlayıcısından bağımsız olarak kullanılabilir.

### <a name="cash-drawer"></a>Kasa çekmecesi

Her donanım profili için iki kasa çekmecesi desteklenebilir. Bu özellik her kasa için aynı anda iki etkin vardiyanın kullanılabilmesini sağlar. Paylaşılan bir vardiya veya aynı anda birden çok mobil POS cihazı tarafından kullanılan bir kasa çekmecesi söz konusu olduğunda, her donanım profili için yalnızca bir kasa çekmecesine izin verilir. Kasa çekmeceleri, USB aracılığıyla doğrudan bilgisayara, Ethernet aracılığıyla bir ağa veya RJ12 arabirimi aracılığıyla bir makbuz yazıcıya bağlanabilir. Bazı durumlarda, kasa çekmecesi Bluetooth ile de bağlanabilir.

### <a name="line-display"></a>Satır görüntüleme

Satır görüntülemeler, bir hareket sırasında müşteriye ürünleri, hareket bakiyelerini ve diğer yararlı bilgileri göstermek için kullanılır. Bir satır görüntüleme cihazı OPOS sürücüleri kullanılarak USB ile bilgisayara bağlanabilir.

### <a name="signature-capture"></a>İmza alma

İmza yakalama cihazları doğrudan bilgisayara USB üzerinden OPOS sürücülerini kullanarak bağlanabilir. İmza yakalama yapılandırıldığında, müşteriden aygıtta oturum açması istenir. İmza sağlandıktan sonra kabul için kasiyere gösterilir.

### <a name="scale"></a>Ölçek

Teraziler OPOS sürücüleri kullanılarak USB ile bilgisayara bağlanabilir. Bir ürün "Tartıldı" olarak işaretlendiğinde harekete eklenir, POS ağırlığı teraziden okur, ürünü harekete ekler ve terazinin sağladığı miktarı kullanır.

### <a name="pin-pad"></a>PIN pad

Kişisel kimlik numarası (PIN) pad'ler OPOS ile desteklenir, ancak bir ödeme bağlayıcı aracılığıyla yönetilmeleri gerekir.

### <a name="secondary-display"></a>İkincil ekran

İkincil bir ekran yapılandırıldığında, temel bilgileri görüntülemek için 2 numaralı Windows ekranı kullanılır. İkincil ekranın amacı, bağımsız yazılım satıcısı (ISV) uzantısını desteklemektir, çünkü hazır durumda, ikincil ekran yapılandırılmaz ve sınırlı içerik gösterir.

### <a name="payment-device"></a>Ödeme cihazı

Ödeme bağlayıcı üzerinden ödeme cihazı desteği uygulanır. Ödeme cihazları, diğer cihaz sınıflarının sağladığı bir veya daha fazla işlevi gerçekleştirebilir. Örneğin, bir ödeme cihazı, bir MSR/kart okuyucu, satır görüntüleme cihazı, imza yakalama cihazı veya PIN pad gibi işlev görebilir. Ödeme cihazlarına yönelik destek, donanım profiline dahil edilmiş olan diğer cihazlar için sağlanan bağımsız cihaz desteğinden bağımsız olarak uygulanır.

## <a name="supported-interfaces"></a>Desteklenen arabirimler
### <a name="opos"></a>OPOS

Commerce ile en geniş cihaz yelpazesinin kullanılabilmesini sağlamaya yardımcı olmak amacıyla, POS endüstri standardı için OLE, desteklenen birincil çevre birim cihazı platformudur. POS standardı için OLE, çevre birim cihazları için endüstri standardı iletişim protokollerini belirleyen Ulusal Perakende Federasyonu (NFR) tarafından üretilmiştir. OPOS, POS standardı için OLE'nin yaygın olarak benimsenen bir uygulamasıdır. 1990'ların ortalarında geliştirilmiştir ve o günden bu yana birkaç kez güncelleştirilmiştir. OPOS, POS donanımının Windows tabanlı POS sistemleri ile kolay tümleştirilmesini sağlayan bir aygıt sürücüsü mimarisi sağlar. OPOS uyumlu donanım ile POS yazılımı arasındaki iletişimi denetler. OPOS denetimi iki bölümden oluşur:

-   **Denetim nesnesi** – Bir cihaz sınıfı için denetim nesnesi (satır görüntülemeler gibi) yazılım programı için arabirim sağlar. Monroe Danışmanlık Hizmetleri ([www.monroecs.com](http://www.monroecs.com/)) genel denetim nesneleri (CCOs) olarak bilinen standartlaştırılmış OPOS denetim nesneleri kümesi sağlar. CCO'lar, Commerce'in POS bileşenlerini test etmekte kullanılır. Bu nedenle, Commerce bir cihaz sınıfını OPOS aracılığıyla destekliyorsa, üreticinin OPOS için oluşturulmuş bir hizmet nesnesi sağlaması durumunda, test birçok cihaz türünün desteklenebilmesini garanti etmeye yardımcı olur. Her cihaz türünü açıkça test etmeniz gerekmez.
-   **Hizmet nesnesi** – Hizmet nesnesi denetim nesnesi (CCO) ile cihaz arasındaki iletişimi sağlar. Genellikle, bir cihaz için hizmet nesnesi cihaz üreticisi tarafından sağlanır. Ancak, bazı durumlarda, hizmet nesnesini üreticisinin web sitesinden indirmeniz gerekebilir. Örneğin, daha yeni bir hizmet nesnesi mevcut olabilir. Üreticinin web sitesi adresini bulmak için donanım belgelerinize bakın.

[![Denetim nesnesi ve hizmet nesnesi](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) POS için OLE'nin OPOS uygulanması için destek, cihaz üreticileri ve POS yayımcıların standardı doğru uygulaması durumunda, POS sistemleri ve desteklenen cihazların, daha önce birlikte test edilmemiş olsalar bile, birlikte çalışabileceklerini garanti etmeye yardımcı olur. 

> [!NOTE]
> OPOS desteği OPOS sürücülerine sahip tüm cihazlar için destek garanti etmez. Commerce önce OPOS aracılığıyla cihaz türünü veya sınıfını desteklemelidir. Ayrıca, hizmet nesneleri CCO'ların en son sürümü ile daima güncel olmayabilir. Ayrıca, genel olarak, hizmet nesnelerinin kalitesinin farklılık gösterdiğini de unutmamanız gerekir.

### <a name="windows&quot;></a>Windows

POS'ta makbuz yazdırm OPOS için optimize edilmiştir. OPOS Windows ile yazdırmaya göre daha hızlı olma eğilimindedir. Bu nedenle, özellikle 40 sütunlu makbuzların yazdırıldığı ve hareket sürelerinin hızlı olduğu ortamlarında OPOS kullanmak iyi bir fikirdir. Çoğu cihaz için OPOS denetimleri kullanacaksınız. Ancak, bazı OPOS makbuz yazıcılar Windows sürücüleri de destekler. Windows sürücüsü kullanarak, son yazı tiplerine ve birden çok kasa için bir ağ yazıcısına erişebilirsiniz. Ancak, Windows sürücüleri kullanmanın dezavantajları vardır. Aşağıda bazı dezavantaj örnekleri verilmiştir:

-   Windows sürücüleri kullanıldığında, görüntüler yazdırma oluşmadan önce işlenir. Bu nedenle, yazdırma OPOS denetimleri kullanan yazıcılara göre daha yavaş olma eğilimindedir.
-   Yazıcı aracılığıyla bağlanan cihazlar (&quot;papatya zinciri") Windows sürücüleri kullanıldığında düzgün çalışmayabilir. Örneğin, kasa çekmecesi açılamayabilir veya slip yazıcısı beklediğiniz gibi çalışmayabilir.
-   Ayrıca OPOS kağıt kesme veya slip yazdırma gibi makbuz yazıcılara özgü daha geniş bir değişkenler kümesini destekler.
-   Windows yazıcıları, IIS donanım istasyonu aracılığıyla desteklenmez. 

Kullanmakta olduğunuz Windows yazıcı için OPOS denetimleri varsa, yazıcı yine de Commerce ile düzgün şekilde çalışmalıdır.

### <a name="universal-windows-platform"></a>Evrensel Windows Platformu

UWP, çevre birimleri söz konusu olduğunda, Tak ve Kullan cihazlar için Windows desteğiyle ilgilidir. Bu tür bir aygıtı destekleyen bir Windows işletim sistemi sürümüne bir Tak ve Kullan cihaz bağlandığında, cihazın gerektiği gibi kullanılması için sürücü gerekli değildir. Örneğin, Windows Bluetooth hoparlör cihazı algılarsa, İşletim Sistemi cihazın **Hoparlör** sınıf türünde olduğunu bilir. Bu nedenle, ve bu cihazı bir hoparlör olarak kabul eder. Ek kurulum gerekli değildir. POS cihazları durumunda, pek çok USB cihazı takılabilir ve Windows bunları İnsan Arabirim Aygıtları (HID) olarak tanıyacaktır. Ancak, cihaz sınıf veya cihaz türü belirtmediğinden, cihazın sağladığı özelliklerin belirlenmesi mümkün olmayabilir. Windows 10'da, barkod tarayıcılar ve MSR'ler için cihaz sınıfları eklenmiştir. Bu nedenle, cihaz kendisini Windows 10'a bu sınıflardan birine ait bir cihaz olarak bildirirse, Windows cihazdan gelen olayları uygun zamanlarda dinleyecektir. Modern POS UWP MSR'leri ve tarayıcıları destekler. Bu nedenle, bu cihazların birinden gelen bir giriş için hazır olduğunda ve bu sınıfların birine ait bir cihaz bağlandığında, cihaz kullanılabilir. Örneğin, bir UWP barkod tarayıcı Windows 10 bilgisayara takılırsa ve barkod oturum açma Modern POS için yapılandırılırsa, barkod tarayıcı oturum açma ekranı üzerinde etkin hale gelir. Ek kurulum gerekli değildir. Hizmet noktası UWP cihazlarının ek sınıfları Windows'a eklenir. Bu sınıflar, nakit çekmecesi ve makbuz yazıcıları sınıflarıdır. Modern POS'ta bu yeni sınıflar için destek beklemededir.

### <a name="keyboard-wedge"></a>Klavye emülasyonu

Klavye emülasyon cihazları, verileri bilgisayara sanki veriler klavyeden yazılmış gibi gönderir. Bu nedenle, varsayılan olarak, POS'ta etkin olan alan taranan veya veya geçirilen veriyi alır. Bazı durumlarda, bu davranış yanlış türde verinin yanlış alana taranmasına neden olabilir. Örneğin, bir barkod kredi kartı veri girişi için tasarlanmış bir alana taranabilir. Çoğu durumda, POS'ta taranan veya geçirilen verinin barkod mu yoksa manyetik kart mı olduğunu belirleyen bir mantık bulunur. Bu nedenle, veriler doğru şekilde ele alınır. Ancak, cihazlar klavye emülasyon cihazları yerine OPOS olarak kurulduğunda, cihazlardan gelen verilerin nasıl kullanılacağı konusunda daha fazla denetim olanağı vardır çünkü verinin geldiği cihazla ilgili daha fazla "bilgi" vardır. Örneğin, bir barkod tarayıcıdan gelen veriler otomatik olarak bir barkod olarak tanınır ve veri tabanındaki ilişkili kayıt, klavye emülasyon cihazları kullanılması durumda gerçekleşen jenerik dizin aramasına göre daha kolay ve daha hızlı bulunur.

> [!NOTE]
> POS'ta klavye emülasyonu tarayıcıları kullanıldığında, bu tarayıcıların son taranan karakterden sonra satır başı göndermek veya olay **Girmek** üzere programlanması gerekir. Bu yapılandırma yapılmazsa, klavye emülasyonlu tarayıcılar doğru çalışmayacaktır. Satır sonu olayının nasıl ekleneceği hakkında bilgi için cihaz üreticinizin sağladığı belgelere başvurun.  

### <a name="native-printer"></a>Yerel yazıcı

Yerel (veya donanım profilinde türü "Cihaz" olarak adlandırılır) yazıcılar kullanıcıdan bilgisayar için yapılandırılmış bir yazıcı seçmelerini istemek üzere yapılandırılabilir. **Cihaz** türü bir yazıcı yapılandırıldığında, Modern POS bir yazdırma komutuyla karşılaşırsa, kullanıcıdan listeden bir yazıcı seçmesi istenir. Bu davranış Windows sürücülerinin davranışından farklıdır çünkü donanım profilindeki **Windows** yazıcı türü yazıcı listesi göstermez. Bunun yerine, **Cihaz adı** alanında adlandırılmış bir yazıcı sağlanmasını gerektirir.

### <a name="network"></a>Ağ

Ağa adreslenebilir kasa çekmeceleri, makbuz yazıcıları ve ödeme terminalleri, doğrudan Windows için Modern POS uygulaması içinde kurulan İşlemler Arası İletişim (IPC) donanım istasyonu veya diğer Modern POS istemcileri için IIS donanım istasyonu aracılığıyla bir ağ üzerinden kullanılabilir.

## <a name="hardware-station-deployment-options"></a>Donanım istasyonu dağıtma seçenekleri

### <a name="dedicated"></a>Özel

Windows ve Android için Modern POS istemcileri ve **adanmış** veya yerleşik donanım istasyonları vardır. Bu istemciler, uygulamalara yerleşik iş mantığını kullanan çevre birimleri ile doğrudan iletişim kurabilir. Android uygulama yalnızca ağ aygıtlarını destekliyor. Android için Çevre birimi desteği hakkında daha fazla bilgi için [Android ve iOS'da POS hybrid uygulaması kurma](./dev-itpro/hybridapp.md) makalesini ziyaret edin.

Adanmış donanım istasyonunu kullanmak için, Windows ve Android için Modern POS uygulamasını kullanacak bir kasaya bir donanım profili atayın. Sonra kasanın kullanılacağı mağaza için **Adanmış** türde bir donanım istasyonu oluşturun. Modern POS 'u çekmece dışı modda başlatıp donanım istasyon yeteneklerini açmak için **donanım istasyonlarını yönetimi** işlemini kullanın, adanmış donanım istasyonu varsayılan olarak etkin olur. Daha sonra, Modern POS oturumunu kapatın, sonra yeniden oturum açın ve donanım profilinde yapılandırılan çevre birimleri kullanılabilir. 

### <a name="shared"></a>Paylaştırılmış 

Ayrıca bazen, POS uygulamasının Microsoft Internet Information Services aracılığıyla donanım istasyonuna bağlandığı "IIS" donanım istasyonu, "IIS" olduğu da denir. POS uygulaması IIS donanım istasyonuna cihazların bağlandığı bilgisayarda çalışan web hizmetleri aracılığıyla bağlanır. Paylaşılan donanım istasyonu kullanıldığında, donanım istasyonuna bağlanan çevrebirimleri IIS donanım istasyonuyla aynı ağda olan herhangi bir POS kasası tarafından kullanılabilir. Yalnızca Windows ve Android için Modern POS çevre birimleri için yerleşik destek içerdiğinden, diğer tüm Modern POS uygulamalarının donanım profilinde yapılandırılmış POS çevre birimleri ile iletişim kurmak için IIS donanım istasyonunu kullanması gerekir. Bu nedenle, IIS donanım istasyonun her kurulumu web hizmetini çalıştıran bir bilgisayar ve cihazlarla iletişim kuran uygulama gerektirir. 

Paylaşılan donanım istasyonu, çevre birimlerinin birden çok satış noktası tarafından paylaşılmasını sağlamak için veya tek bir satış noktası için taahhüt edilen küme veya çevrebirimleri yönetmek için kullanılabilir. 

Çoklu POS istemcileri arasındaki çevre birimlerinin paylaşımını desteklemek için bir donanım istasyonu kullanıldığında, yalnızca nakit çekmecesi, makbuz yazıcıları ve ödeme terminalleri kullanılmalıdır. Bağımsız barkod tarayıcıları, MSR'leri, satır görüntüleme cihazlarını, terazileri veya diğer cihazları doğrudan bağlayamazsınız. Aksi halde, birden fazla POS cihazı aynı anda çevre birimlerinden talepte bulunmaya çalıştığında çakışmalar oluşur. Desteklenen aygıtlar için çakışmalar şu şekilde yönetilir:

-   **Kasa çekmecesi** – Kasa çekmecesi cihaza gönderilen bir olay ile açılır. Kasa çekmecesi çağrıldığında oluşabilecek tek sorun kasa çekmecesinin zaten açık olması durumunda oluşur. Paylaşılan donanım istasyonları durumunda, kasa çekmecesi donanım profilinde **Paylaşılan** olarak ayarlanmalıdır. Bu ayar, POS'un açma komutları gönderdiğinde kasa çekmecesinin zaten açık olup olmadığını denetlemesini önler.
-   **Makbuz yazıcısı** – İki makbuz yazdırma komutu donanım istasyona aynı ayna gönderilirse, aygıta bağlı olarak komutlardan biri kaybolabilir. Bazı cihazlar bu sorunu önleyebilecek dahili belleğe veya havuza sahiptir. Yazdırma komutu başarılı olmazsa, kasiyer bir hata iletisi alır ve yazdır komutunu POS'tan yeniden deneyebilir.
-   **Ödeme terminali** – Kasiyer bir hareketi zaten kullanılmakta olan ödeme terminalinden ödemeye çalışırsa, terminalin kullanılmakta olduğu kasiyere bir mesajla bildirilir ve daha sonra tekrar denemesi istenir. Genellikle, kasiyerler bir terminalin zaten kullanılmakta olduğunu görebilir ve ödemeyi yeniden denemeden önce diğer hareketin tamamlanmasını bekleyecektir.

Doğrulama, desteklenmeyen cihazların paylaşılan bir donanım istasyonuyla eşlenen bir donanım profili için ayarlanığ ayarlanmadığını algılamak için gelecekteki bir sürümde planlanmaktadır. Desteklenmeyen herhangi bir cihaz algılanırsa, kullanıcı cihazların paylaşılan donanım istasyonları için desteklenmediğini bildiren bir ileti alır. Paylaşılan donanım istasyonları söz konusu olduğunda **Ödeme sırasında seç** seçeneği kasa düzeyinde **Evet** olarak ayarlanır. POS kullanıcısından POS'taki bir hareket için bir ödeme seçildiğinde bir donanım istasyonu seçmesi istenir. Donanım istasyonu yalnızca ödeme anında seçildiğinde, donanım istasyon seçimi doğrudan mobil senaryoları için POS akışına eklenir. Ek bir avantaj olarak, ödeme terminalindeki satır görünümü paylaşılan senaryolar için kullanılmaz. Ödeme terminali satırı görüntüleme olarak kullanılırsa, hareket tamamlanıncaya kadar diğer kullanıcıların bu terminali kullanması engellenebilir. Mobil senaryolarda, satırlar bir harekete daha uzun bir süre içinde eklenebilir. Bu nedenle, **Ödeme sırasında seç** seçeneği, en uygun aygıt kullanılabilirliğini sağlamak için gereklidir.

### <a name="network-peripherals"></a>Ağ çevre birimleri

Donanım profilindeki cihazlar için ağ tanımlaması kasa çekmecelerinin, makbuz yazıcıların ve ödeme terminallerinin ağ bağlantısı üzerinden bağlanmasını sağlar.

#### <a name="modern-pos-for-windows"></a>Windows için Modern POS

Ağ çevre birimleri için IP adreslerini iki yerde belirtebilirsiniz. Modern POS Windows istemcisi tek bir ağ çevre birimleri kümesi kullanıyorsa, bu cihazların IP adreslerini kasanın kendi Eylem Bölmesinde **IP yapılandırması** seçeneğini kullanarak ayarlamanız gerekir. Ağ cihazlarının POS kasaları arasında paylaştırılacak olması durumunda, kendisine atanmış ağ cihazları olan bir donanım profili doğrudan paylaşılan donanım istasyonuyla eşlenebilir. IP adreslerini atamak için, **Mağazalar** sayfasında bu donanım istasyonunu seçin ve sonra **Donanım istasyonları** bölümündeki **IP yapılandırması** seçeneğini seçerek bu donanım istasyonuna atanan ağ cihazlarını belirtin. Yalnızca ağ cihazlarına sahip donanım istasyonları için, donanım istasyonunun kendisini dağıtmak zorunda değilsiniz. Bu durumda, donanım istasyonu yalnızca ağa adreslenebilir cihazları mağazadaki konumlarına göre kavramsal olarak gruplamak için gereklidir.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>İOS için Bulut ve Modern POS

Fiziksel olarak bağlı olan ve ağa adreslenebilir çevre birimleri yöneten mantık donanım istasyonunda yer alır. Bu nedenle, Modern POS için Windows ve Android dışındaki tüm POS istemcileri için bir IIS donanım istasyonunun dağıtılmış ve POS'un çevre birimlerle, bu çevre birimlerin fiziksel olarak donanım istasyonuna bağlı olmasına veya ağ üzerinden adreslenmiş olmasına bakılmaksızın, iletişim kurmasını sağlamak üzere etkinleştirilmiş olması gerekir.

## <a name="setup-and-configuration"></a>Kurulum ve yapılandırma
### <a name="hardware-station-installation"></a>Donanım istasyonu yükleme

Bilgi için bkz. [Donanım istasyonunu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Windows için Modern POS kurulumu ve yapılandırması

Daha fazla bilgi için bkz. [Modern POS'u (MPOS) yapılandırma, yükleme ve etkinleştirme](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Android ve iOS için Modern POS kurulumu ve yapılandırması

Bilgi için bkz. [Android ve iOS'ta POS hybrid uygulamasını ayarlama](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS cihazı kurma ve yapılandırma

OPOS bileşenleri hakkında daha fazla bilgi için bu belgenin "Desteklenen arabirimler" bölümüne bakın. Genellikle, OPOS sürücüler cihaz üreticisi tarafından sağlanır. Bir OPOS aygıt sürücüsü yüklendiğinde, Windows kayıt defterinde aşağıdaki konumlardan birine bir anahtar ekler:

-   **32 bit sistem:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64 bit sistem:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

ServiceOPOS kayıt defteri konumu içinde, yapılandırılan cihazlar OPOS cihaz sınıfına göre düzenlenir. Birden fazla cihaz sürücüsü kaydedilir.

## <a name="supported-scenarios-by-hardware-station-type"></a>Donanım istasyon türü tarafından desteklenen senaryolar
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>İstemci desteği – IPC donanım istasyonu ile IIS donanım istasyon karşılaştırması

Aşağıdaki tabloda desteklenen topolojiler ve dağıtım senaryoları gösterilmektedir.

| İstemci      | IPC donanım istasyonu | IIS donanım istasyonu |
|-------------|----------------------|----------------------|
| Windows uygulaması | Evet                  | Evet                  |
| Bulut POS   | Hayır                   | Evet                  |
| Android     | Evet                  | Evet                  |
| iOS         | Hayır                   | Evet                  |

### <a name="network-peripherals"></a>Ağ çevre birimleri

Ağ çevre birimleri doğrudan Windows ve Android uygulamaları için Modern POS uygulamasına yerleşik olan donanım istasyonu aracılığıyla desteklenebilir. Diğer tüm istemciler için bir IIS donanım istasyonu dağıtmanız gerekir.

| İstemci      | IPC donanım istasyonu | IIS donanım istasyonu |
|-------------|----------------------|----------------------|
| Windows uygulaması | Evet                  | Evet                  |
| Bulut POS   | Hayır                   | Evet                  |
| Android     | Evet                  | Evet                  |
| iOS         | Hayır                   | Evet                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Donanım istasyon türü tarafından desteklenen cihaz türleri
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Windows için Modern POS, IPC (yerleşik) donanım istasyonu ile

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Desteklenen cihaz sınıfı</th>
<th>Desteklenen arabirimler</th>
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
<li>UWP (Kurulum gerekli değildir.)</li>
<li>Klavye emülsayonu (Kurulum gerekli değildir.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Keşideci</td>
<td><ul>
<li>OPOS</li>
<li>Ağ </br><strong>Not:</strong> Çekmecede <strong>Paylaşılan vardiya kullan</strong> yapılandırılırsa yalnızca bir çekmece ayarlanabilir.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Çekmece 2</td>
<td><ul>
<li>OPOS</li>
<li>Ağ </br><strong>Not:</strong> Çekmecede <strong>Paylaşılan vardiya kullan</strong> yapılandırılırsa yalnızca bir çekmece ayarlanabilir.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tarayıcı</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Kurulum gerekli değildir.)</li>
<li>Klavye emülsayonu (Kurulum gerekli değildir.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tarayıcı 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Kurulum gerekli değildir.)</li>
<li>Klavye emülsayonu (Kurulum gerekli değildir.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Ölçek</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN pad</td>
<td>OPOS (Destek ödeme bağlayıcısı özelleştirmesi aracılığıyla sağlanır.)</td>
</tr>
<tr class="even">
<td>İmza alma</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Ödeme terminali</td>
<td><ul>
<li>Özel cihaz desteği</li>
<li>Ağ (Daha fazla bilgi için, ödeme bağlayıcısı belgelerine bakın.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>"Paylaşılan" bir IIS donanım istasyonu olan tüm Modern POS istemcileri

> [!NOTE]
> IIS donanım istasyonu "adanmış" olduğunda, POS istemcisi ile donanım istasyonu arasında bire bir ilişki bulunur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Desteklenen cihaz sınıfı</th>
<th>Desteklenen arabirimler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yazıcı</td>
<td><ul>
<li>OPOS</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="even">
<td>Yazıcı 2</td>
<td><ul>
<li>OPOS</li>
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
<li>Ağ </br><strong>Not:</strong> Çekmecede <strong>Paylaşılan vardiya kullan</strong> yapılandırılırsa donanım profili başına yalnızca bir çekmece ayarlanabilir.</li>
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
<td>OPOS (Destek ödeme bağlayıcısı özelleştirmesi aracılığıyla sağlanır.)</td>
</tr>
<tr class="odd">
<td>İmza yakalama</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Ödeme terminali</td>
<td><ul>
<li>Özel cihaz desteği</li>
<li>Ağ (Daha fazla bilgi için, ödeme bağlayıcısı belgelerine bakın.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-shared-an-iis-hardware-station"></a>Paylaşılan bir IIS donanım istasyonu olan tüm Modern POS istemcileri

> [!NOTE]
> IIS donanım istasyonu "paylaşıldığında", aynı anda birden çok cihaz donanım istasyonunu kullanabilir. Bu senaryoda, yalnızca aşağıdaki tabloda listelenen cihazları kullanmanız gerekir. Barkod tarayıcılar ve MSR'ler gibi burada listelenmeyen cihazları paylaştırmayı denerseniz, birden fazla cihaz aynı çevre birimden talepte bulunmaya çalıştığında hatalar oluşacaktır. Gelecekte bu tür bir yapılandırma açıkça engellenecektir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Desteklenen cihaz sınıfı</th>
<th>Desteklenen arabirimler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yazıcı</td>
<td><ul>
<li>OPOS</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="even">
<td>Yazıcı 2</td>
<td><ul>
<li>OPOS</li>
<li>Ağ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Keşideci</td>
<td><ul>
<li>OPOS</li>
<li>Ağ </br><strong>Not:</strong> Çekmecede <strong>Paylaşılan vardiya kullan</strong> yapılandırılırsa donanım profili başına yalnızca bir çekmece ayarlanabilir.</li>
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
<td>Ödeme terminali</td>
<td><ul>
<li>Özel cihaz desteği</li>
<li>Ağ (Daha fazla bilgi için, ödeme bağlayıcısı belgelerine bakın.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Desteklenen senaryolar için yapılandırma
Donanım profilleri oluşturma hakkında daha fazla bilgi için bkz. [Kasalar ve donanım istasyonları dahil olmak üzere kanal istemcilerini tanımlama ve koruma](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Windows için Modern POS, IPC (yerleşik) donanım istasyonu ile

Bu yapılandırma geleneksel, sabit POS kasalar için en genel yapılandırmadır. Bu senaryo için, donanım profili bilgileri doğrudan kasanın kendisiyle eşleştirilir. EFT terminal numarasının da kasa üzerinde ayarlanması gerekir. Bu yapılandırmayı kurmak için aşağıdaki adımları izleyin.

1.  Tüm gerekli çevrebirimlerin yapılandırıldığı bir donanım profili oluşturun.
2.  Donanım profilini POS kasayla eşleyin.
3.  POS kasanın kullanılacağı mağaza için **Adanmış** türde bir donanım istasyonu oluşturun. Açıklama isteğe bağlıdır. 

    > [!NOTE]
    > Donanım istasyonunda diğer özellikleri ayarlamanız gerekmez. Donanım profili gibi gerekli tüm diğer bilgiler, kasanın kendisinden gelecektir.

4.  **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım planı**'na gidin.
5.  Yeni donanım profilini mağazayla eşitlemek için **1090** dağıtım planını seçin. Değişiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a tıklayın.
6.  Yeni donanım istasyonunu mağazayla eşitlemek için **1040** dağıtım planını seçin. Değişiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a tıklayın.
7.  Windows için Modern POS'u yükleyin ve etkinleştirin.
8.  Windows için Modern POS'u başlatın ve bağlı çevrebirim cihazlarını kullanmaya başlayın.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Android için Modern POS, IPC (yerleşik) donanım istasyonu ile

**10.0.8 için yeni** - Epson ağ yazıcıları ve bu yazıcılara, DK bağlantı noktasıyla bağlı nakit çekmeenlerin şimdi Modern POS fo Android uygulaması için desteklenmektedir. Ayrıntılar için [Android ve iOS için POS hybrid uygulama kurulumu](./dev-itpro/hybridapp.md) makalesini ziyaret edin.

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Paylaşılan bir IIS donanım istasyonu olan tüm Modern POS istemcileri

Bu yapılandırma, özellikle bir POS kasası tarafından kullanılan donanım istasyonu bulunan tüm Modern POS istemcileri için kullanılabilir. Bu yapılandırmayı kurmak için aşağıdaki adımları izleyin.

1.  Tüm gerekli çevrebirimlerin yapılandırıldığı bir donanım profili oluşturun.
2.  POS kasanın kullanılacağı mağaza için **Adanmış** türde bir donanım istasyonu oluşturun.
3.  Adanmış donanım istasyonunda aşağıdaki özellikleri ayarlayın:
    -   **Ana bilgisayar adı** – Donanım istasyonunun çalışacağı ana bilgisayarın adı. 
    
        > [!NOTE]
        > Bulut POS Bulut POS'un çalıştığı yerel bilgisayarı belirlemek için **localhost**'u çözebilir. Ancak, Bulut POS'u donanım istasyonuyla eşleştirmek için gerekli olan sertfikada bilgisayar adı olarak "Localhost" bulunmalıdır. Sorunları önlemek için, gerektiğinde, mağaza için her adanmış donanım istasyonu kurulumunu listelemenizi öneririz. Her donanım istasyonu için ana bilgisayar adı, donanım istasyonunun dağıtılacağı belirli bilgisayarın adı olmalıdır.
    
    -   **Bağlantı noktası** – Modern POS istemcisiyle iletişim kurmak için donanım istasyonunun kullandığı bağlantı noktası.
    -   **Donanım profili** – Donanım profili donanım istasyonunun kendisinde sağlanmadıysa, kasaya atanan donanım profili kullanılır.
    -   **EFT POS numarası** – EFT kimlik doğrulamaları gönderildiğinde kullanılan EFT terminali kimliği. Bu kimlik kredi kartı işlemcisi tarafından sağlanır.
    -   **Paket adı** – Donanım istasyonu dağıtıldığında kullanılan donanım istasyonu paketi.

4.  **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım planı**'na gidin.
5.  Yeni donanım profilini mağazayla eşitlemek için **1090** dağıtım planını seçin. Değişiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a tıklayın.
6.  Yeni donanım istasyonunu mağazayla eşitlemek için **1040** dağıtım planını seçin. Değişiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a tıklayın.
7.  Donanım istasyonunu yükleyin. Donanım istasyonu yükleme hakkında daha fazla bilgi için bkz. [Retail hardware station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).
8.  Modern POS'u yükleyin ve etkinleştirin. Modern POS yükleme hakkında daha fazla bilgi için bkz. [Modern POS (MPOS) yapılandırma, yükleme ve etkinleştirme](retail-modern-pos-device-activation.md).
9.  Modern POS için oturum açın ve **Çekmece işlemi olmayan işlem gerçekleştir**'i seçin.
10. **Donanım istasyonlarını yönet** işlemini başlatın.
11. **Yönet**'e tıklayın.
12. Donanım istasyonu yönetimi sayfasında, donanım istasyonunu açma seçeneğini ayarlayın.
13. Kullanılacak donanım istasyonunu seçin ve **Eşleştir**'e tıklayın.
14. Donanım istasyonu eşleştirildikten sonra **Kapat**'a tıklayın.
15. Donanım istasyonu seçimi sayfasında, son seçilen donanım istasyonunu etkin hale getirmek için tıklayın.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Paylaşılan bir IIS donanım istasyonu olan tüm Modern POS istemcileri

Bu yapılandırma, donanım istasyonlarını diğer aygıtlarla paylaşan tüm Modern POS istemcileri için kullanılabilir. Bu yapılandırmayı kurmak için aşağıdaki adımları izleyin.

1.  Gerekli çevrebirimlerin yapılandırıldığı bir donanım profili oluşturun.
2.  POS kasanın kullanılacağı mağaza için **Paylaşılan** türde bir donanım istasyonu oluşturun.
3.  Paylaştırılmış donanım istasyonunda aşağıdaki özellikleri ayarlayın:
    -   **Ana bilgisayar adı** – Donanım istasyonunun çalışacağı ana bilgisayarın adı.
    -   **Açıklama** – Donanım istasyonunu tanımlamaya yardımcı olan **İadeler** veya **Ön mağaza** gibi bir metin.
    -   **Bağlantı noktası** – Modern POS istemcisiyle iletişim kurmak için donanım istasyonunun kullandığı bağlantı noktası.
    -   **Donanım profili** – Paylaşılan donanım istasyonları için her donanım istasyonunun bir donanım profili olması gerekir. Donanım profilleri donanım istasyonları arasında paylaşılabilir, ancak her donanım istasyonuyla eşlenmeleri gerekir. Ayrıca, birden çok aygıt aynı paylaşılan donanım istasyonunu kullandığında, paylaşılan vardiyalar kullanmanızı öneririz. Paylaşılan vardiya kurmak için **Perakende ve Ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri**'ne tıklayın. Her bir paylaşılan donanım profili için kasa çekmecesini seçin ve **Paylaşılan vardiya çekmecesi** için seçeneği **Evet** olarak ayarlayın.
    -   **EFT POS numarası** – EFT kimlik doğrulamaları gönderildiğinde kullanılan EFT terminali kimliği. Bu kimlik kredi kartı işlemcisi tarafından sağlanır.
    -   **Paket adı** – Donanım istasyonu dağıtıldığında kullanılan donanım istasyonu paketi.

4.  Mağazadaki gerekli her ek donanım istasyon için 2 ve 3 numaralı adımları yineleyin.
5.  **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım planı**'na gidin.
6.  Yeni donanım profilini mağazayla eşitlemek için **1090** dağıtım planını seçin. Değişiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a tıklayın.
7.  Yeni donanım istasyonunu mağazayla eşitlemek için **1040** dağıtım planını seçin. Değişiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a tıklayın.
8.  2 ve 3 numaralı adımlarda kurduğunuz her ana bilgisayara donanım istasyonunu yükleyin. Donanım istasyonu yükleme hakkında daha fazla bilgi için bkz. [Retail hardware station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).
9.  Modern POS'u yükleyin ve etkinleştirin. Modern POS yükleme hakkında daha fazla bilgi için bkz. [Modern POS (MPOS) yapılandırma, yükleme ve etkinleştirme](retail-modern-pos-device-activation.md).
10. Modern POS için oturum açın ve **Çekmece işlemi olmayan işlem gerçekleştir**'i seçin.
11. **Donanım istasyonlarını yönet** işlemini başlatın.

12. **Yönet**'e tıklayın.
13. Donanım istasyonu yönetimi sayfasında, donanım istasyonunu açma seçeneğini ayarlayın.
14. Kullanılacak donanım istasyonunu seçin ve **Eşleştir**'e tıklayın.
15. Modern POS'un kullanacağı her donanım istasyonu için 14. adımı tekrarlayın.
16. Gerekli donanım istasyonları eşleştirdikten sonra **Kapat**'a tıklayın.
17. Donanım istasyonu seçimi sayfasında, son seçilen donanım istasyonunu etkin hale getirmek için tıklayın. 

> [!NOTE]
> Cihazlar genellikle farklı donanım istasyonları kullanıyorsa, Modern POS'u kasiyerlerden ödeme işlemini başlatırken bir donanım istasyonu seçmelerini isteyecek şekilde yapılandırmanızı öneririz. **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Yazar kasalar** öğesine tıklayın. Kasayı seçin ve ardından **Ödeme sırasında seç** seçeneğini **Evet** olarak ayarlayın. Değişiklikleri kanal veritabanıyla eşitlemek için **1090** dağıtım planını kullanın.

## <a name="extensibility"></a>Genişletilebilirlik
Donanım istasyonu için genişletilebilirlik senaryoları hakkında daha fazla bilgi için bkz. [Donanım İstasyonu genişletilebilirliği](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Güvenlik
Geçerli güvenlik standartlarına göre aşağıdaki ayarları üretim ortamında kullanılmalıdır: 

### <a name="hardware-station-installer"></a>Donanım istasyonu yükleyici
Donanım istasyonu yükleyicisi bu kayıt defteri düzenlemelerini Self Servis hizmeti üzerinden yüklemenin bir parçası olarak otomatik olarak yapar.
 
-   Güvenli Yuva Katmanı (SSL) devre dışı bırakılmalıdır.
-   Yalnızca Aktarım Katmanı Güvenliği (TLS) sürüm 1.2 (veya geçerli en yüksek sürüm) etkinleştirilmeli ve kullanılmalıdır. 

### <a name="ssl-and-tls"></a>SSL ve TLS
Varsayılan olarak, SSL ve TLS 1.2 dışındaki tüm TLS sürümleri devre dışı bırakılır. Bu değerleri düzenlemek veya etkinleştirmek için şu adımları izleyin:
    1.  **Çalıştır** penceresini açmak için Windows logı tuşuyla birlikte R'ye basın.
    2.  **Aç** alanına, **Regedit** yazıp **Tamam**'a tıklayın.
    3.  Bir **Kullanıcı Hesabı Denetimi** ileti kutusu görüntülenirse, **Evet**'e tıklayın.
    4.  **Kayıt Defteri Düzenleyicisi** penceresinde, **HKEY\_yerel\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**'a gidin. Aşağıdaki anahtarlar yalnızca TLS 1.2 için izin vermek üzere otomatik olarak girilmiştir:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Bilinen, belirtilen nedenlerden dolayı gerekli olmadıkça hiçbir ek ağ bağlantı noktası açık olmamalıdır.
-   Çapraz kaynaklı kaynak paylaşımını devre dışı bırakılmalı ve kabul edilen izin verilen kaynaklar belirtilmelidir.
-   Yalnızca güvenilen sertifika yetkilileri, donanım istasyonu çalıştıran bilgisayarlarda kullanılacak sertifikaları almak için kullanılmalıdır.

> [!NOTE]
> IIS için güvenlik yönergelerini ve Ödeme Kartı Endüstrisi (PCI) gereksinimlerini gözden geçirmeniz çok önemlidir.

## <a name="peripheral-simulator"></a>Çevre birimi benzeticisi
Bilgi için bkz. [Commerce için çevre birimi benzeticisi](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Microsoft tarafından test edilmiş çevre birim cihazları
### <a name="ipc-built-in-hardware-station"></a>IPC (yerleşik) donanım istasyonu

Aşağıdaki çevre birimler Windows için Modern POS içine yerleşik olan IPC donanım istasyonu kullanılarak sınanmıştır.

#### <a name="printer"></a>Yazıcı

| Üretici | Model    | Arabirim | Yorumlar                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88   | Özel    | Ağ üzerinden bağlı   |
| Star         | TSP650II | Özel    | Ağ üzerinden bağlı   |
| Star         | mPOP     | OPOS      | Bluetooth ile bağlı |
| HP           | F7M67AA  | OPOS      | Güç beslemeli USB             |

> [!NOTE]
> Star TSP 100 yazıcısı, yerleşik donanım istasyonu için desteklenmez. Yerleşik donanım istasyonu, mevcut Star TP 100 sürücüleriyle uyumlu olmayan 64-bit işlem kullanır. 

#### <a name="bar-code-scanner"></a>Barkod tarayıcısı

| Üretici  | Model         | Arabirim | Yorumlar |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Simge        | LS2208        | OPOS      |          |
| HP Tümleşik | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN pad

| Üretici | Model  | Arabirim | Yorumlar                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Ödeme bağlayıcısı için özelleştirme gerektirir |

#### <a name="payment-terminal"></a>Ödeme terminali

| Üretici | Model | Arabirim | Yorumlar                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir                                |
| VeriFone     | MX925 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir; Ağ üzerinden ve USB ile bağlı |
| VeriFone     | MX915 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir; Ağ üzerinden ve USB ile bağlı |

#### <a name="cash-drawer"></a>Kasa çekmecesi

| Üretici | Model     | Arabirim | Yorumlar                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Bluetooth ile bağlı |
| APG          | Atwood    | Özel    | Ağ üzerinden bağlı   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Özel    | DK bağlantı noktasıyla ağ Epson yazıcısına bağlanıldı |

#### <a name="line-display"></a>Satır görüntüleme

| Üretici  | Model   | Arabirim | Yorumlar |
|---------------|---------|-----------|----------|
| HP tümleşik | G6U79AA | OPOS      |          |
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

Aşağıdaki çevre birimler Windows için Modern POS ve Bulut POS ile adanmış (paylaştırılmamış) IIS donanım istasyonu kullanılarak sınanmıştır.

#### <a name="printer"></a>Yazıcı

| Üretici | Model    | Arabirim | Yorumlar                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Epson        | TM-T88V  | Özel    | Ağ üzerinden bağlı     |
| Star         | TSP650II | Özel    | Ağ üzerinden bağlı     |
| HP           | F7M67AA  | OPOS      | Güç beslemeli USB               |

#### <a name="bar-code-scanner"></a>Barkod tarayıcısı

| Üretici  | Model   | Arabirim | Yorumlar |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Simge        | LS2208  | OPOS      |          |
| HP Tümleşik | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN pad

| Üretici | Model  | Arabirim | Yorumlar                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Ödeme bağlayıcısı için özelleştirme gerektirir |

#### <a name="payment-terminal"></a>Ödeme terminali

| Üretici | Model | Arabirim | Yorumlar                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir                                |
| VeriFone     | MX925 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir; Ağ üzerinden ve USB ile bağlı |
| VeriFone     | MX915 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir; Ağ üzerinden ve USB ile bağlı |

#### <a name="cash-drawer"></a>Kasa çekmecesi

| Üretici | Model     | Arabirim | Yorumlar              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Özel    | Ağ üzerinden bağlı |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Özel    | DK bağlantı noktasıyla ağ Epson yazıcısına bağlanıldı |

#### <a name="line-display"></a>Satır görüntüleme

| Üretici  | Model   | Arabirim | Yorumlar |
|---------------|---------|-----------|----------|
| HP tümleşik | G6U79AA | OPOS      |          |
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

### <a name="shared-iis-hardware-station"></a>Paylaştırılmış IIS donanım istasyonu

Aşağıdaki çevre birimler Windows için Modern POS ve Bulut POS ile paylaştırılmış IIS donanım istasyonu kullanılarak sınanmıştır. 

> [!NOTE]
> Sadece bir yazıcı, ödeme terminali ve kasa çekmecesi desteklenir.

#### <a name="printer"></a>Yazıcı

| Üretici | Model    | Arabirim | Yorumlar                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Epson        | TM-T88   | Özel    | Ağ üzerinden bağlı     |
| Star         | TSP650II | Özel    | Ağ üzerinden bağlı     |
| HP           | F7M67AA  | OPOS      | Güç beslemeli USB               |

#### <a name="payment-terminal"></a>Ödeme terminali

| Üretici | Model | Arabirim | Yorumlar                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir; Ağ üzerinden ve USB ile bağlı |
| VeriFone     | MX915 | Özel    | Ödeme bağlayıcısı için özelleştirme gerektirir; Ağ üzerinden ve USB ile bağlı |

#### <a name="cash-drawer"></a>Kasa çekmecesi

| Üretici | Model     | Arabirim | Yorumlar              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Özel    | Ağ üzerinden bağlı |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Özel    | DK bağlantı noktasıyla ağ Epson yazıcısına bağlanıldı |


## <a name="troubleshooting"></a>Sorun Giderme
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS donanım istasyonunun seçim listesinde olduğunu algılayabiliyor, ancak eşleştirmeyi tamamlayamıyor

**Çözüm:** Aşağıdaki olası hata noktaları listesini kontrol edin:

-   Modern POS çalıştıran bilgisayar donanım istasyonu çalıştıran bilgisayarda kullanılan sertifikaya güveniyor.
    -   Bu kurulumu doğrulamak için, bir web tarayıcısında, şu URL'ye gidin: https://&lt;Bilgisayar Adı&gt;:&lt;Bağlantı Noktası Numarası&gt;/HardwareStation/ping.
    -   Bu URL bilgisayara erişilebildiğini doğrulamak için bir ping kullanır ve tarayıcı sertifikanın güvenilir olup olmadığını gösterir. (Örneğin, Internet Explorer uygulamasında kilit simgesi adres çubuğunda görünür. Bu simgeyi tıklattığınızda, Internet Explorer sertifikanın güvenilir olup olmadığını doğrular. Sertifikayı yerel bilgisayarda gösterilen sertifikanın ayrıntılarını görüntüleyerek yükleyebilirsiniz.)
-   Donanım istasyonu çalıştıran bilgisayarda, donanım istasyonu tarafından kullanılan bağlantı noktası güvenlik duvarında açılır.
-   Donanım istasyonu, donanım istasyon yükleyici sonunda çalışan Satıcı bilgilerini yükleme aracı ile ticari hesap bilgilerini doğru bir şekilde yükledi.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS, seçim listesinde bulunan donanım istasyonunu algılayamıyor

**Çözüm:** Aşağıdaki etkenlerden biri bu soruna neden olabilir:

-   Donanım istasyonu genel merkezden doğru şekilde ayarlanmamıştır. Donanım istasyonu profilinin ve donanım istasyonunun doğru şekilde girildiğinden emin olmak için bu konunun önceki bölümlerinde açıklanan adımları kullanın.
-   İşler kanal yapılandırmasını güncelleştirmek için çalıştırılmamış. Bu durumda, kanal konfigürasyonu için 1070 işini çalıştırın.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS yeni kasa çekmecesi ayarlarını yansıtmıyor.

**Çözüm:** Geçerli toplu işi kapatın. Geçerli toplu işlem kapanıncaya kadar kasa çekmecesindeki değişiklikler Modern POS'da güncelleştirilmez.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS bir çevre birimiyle ilgili bir sorun raporluyor

**Çözüm:** Bu sorunun tipik bazı nedenleri şunlardır:

-   Diğer aygıt sürücüsü yapılandırma yardımcı programlarının kapalı olduğundan emin olun. Bu yardımcı programlar açıksa, Modern POS veya donanım istasyonunun cihazdan talepte bulunmasını engelleyebilir.
-   Çevre birimi birden fazla POS cihazıyla paylaşılıyorsa, aşağıdaki kategorilerden birine ait olduğundan emin olun:
    -   Kasa çekmecesi
    -   Makbuz yazıcısı
    -   Ödeme terminali

    Çevre birim aşağıdaki kategorilerden birine ait değilse, donanım istasyonu çevre birimin birden fazla POS cihazı arasında paylaşılmasına olanak tanımak için tasarlanmamıştır.
-   Bazen, cihaz sürücüleri, genel denetim nesnelerinin (CCOs) düzgün çalışmayı durdurmasına neden olabilir. Son zamanlarda bir cihaz yüklendiyse, ancak düzgün çalışmıyorsa veya başka sorunlar fark ediyorsanız, genellikle sorunu CCO'ları yeniden yükleyerek çözebilirsiniz. CCO'ları indirmek için şu adrese gidin: <http://monroecs.com/oposccos_current.htm>.
-   Sınama ve sorun giderme sırasında sık sık çevre birim değişikliği yaparsanız, önbelleğin kendisini yenilemesini beklemek yerine IIS'yi sıfırlamanız gerekebilir. IIS'yi sıfırlamak için şu adımları izleyin:
    1.  **Başlat** menüsüde **CMD** yazın.
    2.  Arama sonuçlarında, **Komut istemi**'ne sağ tıklayın ve **Yönetici olarak çalıştır**'a tıklayın.
    3.  **Komut istemi** penceresinde, **iisreset/Restart** yazıp Enter tuşuna basın.
    4.  IIS yeniden başlatıldıktan sonra Modern POS'u yeniden başlatın.
-   Çevre birimi cihazlarında için sık sık değişiklik yaptığınızda, POS istemcisini de sık sık başlatıp çıkıyorsanız, bir önceki POS oturumundaki dllhost işlemi geçerli oturumla etkileşime girebilir. Bu durumda, önceki oturumu yöneten dinamik bağlantı kitaplığı (DLL) ana bilgisayarı kapatılıncaya kadar cihaz kullanılamayabilir. DLL ana bilgisayarını kapatmak için şu adımları izleyin:
    1.  **Başlat** menüsüde **Görev yöneticisi** yazın.
    2.  Arama sonuçlarında **Görev yöneticisi**'ne tıklayın.
    3.  Görev yöneticisinde, **Ayrıntılar** sekmesinde, **Ad** etiketli sütun başlığına tıklayıp tabloyu ada göre alfabetik olarak sıralayın.
    4.  dllhost.exe'yi bulana kadar aşağı kaydırın.
    5.  Her DLL ana bilgisayarını seçin ve ardından **Görevi sonlandır**'a tıklayın.
    6.  DLL ana bilgisayarları kapandıktan sonra Modern POS'u yeniden başlatın.


## <a name="additional-resources"></a>Ek kaynaklar

[Commerce için çevre birimi benzeticisi](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]