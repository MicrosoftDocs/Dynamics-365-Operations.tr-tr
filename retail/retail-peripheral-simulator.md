---
title: "Perakende çevresel simülatörü"
description: "Bu konu Microsoft Dynamics 365 işlemleri - perakende ile sağlanan çevresel simulator aracı açıklanır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Perakende çevresel simülatörü

Bu konu Microsoft Dynamics 365 işlemleri - perakende ile sağlanan çevresel simulator aracı açıklanır.

<a name="overview"></a>Özet
--------

Microsoft Dynamics 365 - operasyonlar için perakende çevresel simulator ayarlamak, test ve perakende ortamlarda kullanılan çevre aygıtları ile ilgili sorun giderme yardımcı olan bir araçtır. Çevre simulator sınama perakende çevre birimlerinin daha verimli ve hatalı Kurulum veya hatalı çalışan aygıt sürücüleri tarafından neden olduğu sorunları yalıtmak için kullanabilirsiniz. Çevre simulator işlemleri için o Dynamics 365 aygıtların sanal sürümleri özellikleri bir masaüstü programı içerir - perakende destekler. Bir bölümün her bir sanal aygıt için aygıt ve perakende noktası (POS) satış arasındaki etkileşimi gösterir. Çeşitli POS senaryoları için geçerli olan giriş sağlamak için de kullanabilirsiniz. Çevre simulator POS aşağıdaki sanal aygıtlar arasındaki etkileşimi destekler:

-   **Yazıcı** – çevre simulator POS Yazıcı için yapılandırılmış olan girişler gösterebilirsiniz.
-   **Satır ekran** – faaliyet fiziksel çizgi ekranda göstermek için bir sanal satır görüntüleme yapılandırabilirsiniz.
-   **Manyetik Bant Okuyucu (MSR)** – çevre simulator POS Benzetilen Manyetik Şerit olayları gönderebilir.
-   **Çekmece** – fiziksel para çekmecesini benzetimini yapabilirsiniz.
-   **Çekmece 2** – çevre simulator içinde ikinci bir para çekmecesini ayarlayarak, iki etkin vardiyası olan tek bir POS kaydı ilgili senaryolar simüle edebilirsiniz.
-   **Tarayıcı** – çevre simulator destekleyen sanal barkod tarayıcı barkod tarama olaylarını kesebilirsiniz.
-   **Ölçek** – sanal bir ölçek POS tartılan öğeleri etkileşim benzetimini sağlar.
-   **Kişisel kimlik numarası (PIN) pad** – PIN pad işlemlerinin benzetimini yapabilirsiniz. **Not:** ödeme bağlayıcısı aracılığıyla fiziksel bir PIN pad destek sağlamanız gerekir.
-   **İmza yakalama** – müşteri hesabının ödeme gibi bazı ödemeler için gerekli imzaları isteyecek şekilde ayarlayabilirsiniz bir sanal imza yakalama aygıtı çevresel simulator içerir.

Çevre simulator kaynaklanan bir barkod tarayıcı ve MSR Golf Sopası olaylar klavye benzetimi yapmak için de kullanabilirsiniz. Sanal çevre simulator nesne bağlama ve katıştırma özellikle perakende POS (OPOS) aygıtlar için destekler.

## <a name="key-scenarios"></a>Senaryoları
### <a name="troubleshooting"></a>Sorun Giderme

Çevre simulator, aygıt kurulum sorunlarını gidermek için kullanabilirsiniz. Çevre simulator veya aynı sınıfın ikinci bir aygıtı yoksa, burada kaynaklanan sorunları belirlemek zor olabilir. Ancak, çevre simulator varsa, sanal aygıtlarını kurabileceğiniz ve aynı kod yollarını ve fiziksel aygıtlar için kullanılan iş mantığı çalıştırın. Çevre simulator açısından bakıldığında, sanal ve fiziksel aygıtlar arasındaki temel fark hizmet nesnesinin veya aygıt sürücüsü var. Servis nesnesi, fiziksel aygıtlar için aygıt üreticisi tarafından sağlanır. Bunun tersine, çevre simülatörü Servis nesneleri çevresel simulator bir parçası olarak sağlanır. Gerçek bir aygıt adına donanım profilinde aygıt adı değiştirildikten sonra bir aygıt düzgün çalışmazsa, çevresel simulator düzgün çalışırken, üreticinin sağladığı hizmet nesnesi ile ilgili bir sorun olduğunu kabul edilebilir.

### <a name="training"></a>Eğitim

Çevre simulator, fiziksel donanım Kurulumu kullanılamaz olduğunda eğitimi kasiyer için gerçekçi bir katman eklemek için kullanabilirsiniz. Çevre simulator eğitimi senaryolarda dahil olduğunda, kasiyer daha etkili POS ile ürün kodu tarar ve hediye çubuk gibi giriş kartı swipes sağlayarak ve makbuzları belirli bir işlem için yazdırılan gözleme etkileşim kurabilirsiniz.

### <a name="testing"></a>Test etme

Çevresel simulator ürün barkodları, makbuz biçimleri ve benzerleri, fiziksel donanım sanal bir ortamda dağıtmak zorunda kalmadan test etmek için kullanabilirsiniz. Fiziksel donanım gerekli deðildir ve POS istemci donanım istasyon veya fiziksel bir bilgisayarda dağıtmak zorunda değilsiniz çünkü arka ofis içinde yapılan değişiklikleri daha hızlı bir şekilde sınayabilirsiniz.

## <a name="set-up-the-peripheral-simulator"></a>Çevre simulator Ayarla
### <a name="set-up-a-hardware-profile"></a>Bir donanım profili kurmak

1.  Çevre simulator ayarlamak için Git **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profilleri**.
2.  Yeni bir profil oluşturmak için tıklatın **yeni**.
3.  Değerleri girin **Profil numarası** ve **açıklama** alanlar.
4.  Test edilmesi gereken sanal aygıtları için aşağıdaki tabloyu kullanın. Bir tablodaki sütunların açıklaması aşağıdadır:
    -   **Aygıt** – bu sütun aygıtı ayarlamak için genişletin hızlı adını verir.
    -   **Aygıt türü** – bu sütun aygıt adıyla etiketlenir alanında seçtiğiniz değeri verir.
    -   **Aygıt adı** – bu sütun için aygıt adı girin tam değer verir. **Önemli:** donanım istasyon aygıtlara yönelik olarak bu özel adlar kullanır çünkü burada verilen aygıt adları gereklidir. Bu özel adlar kullanmıyorsanız, aygıt kullanılamaz.

    | Aygıt            | Aygıt türü | Aygıt adı              |
    |-------------------|-------------|--------------------------|
    | Yazıcı           | OPOS        | MockOPOSPrinter          |
    | Satır görüntüleme      | OPOS        | MockOPOSLineDisplay      |
    | MSR               | OPOS        | MockOPOSMSR              |
    | Keşideci            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Tarayıcı           | OPOS        | MockOPOSScanner          |
    | Ölçek             | OPOS        | MockOPOSScale            |
    | PIN Pad           | OPOS        | MockOPOSPinPad           |
    | İmza alma | OPOS        | MockOPOSSignatureCapture |

**Not:** barkod tarayıcı ve MSR Golf Sopası olaylar klavye benzetimi yapmak için hiçbir donanım profilinde özel kurulum gereklidir.

### <a name="assign-the-hardware-profile-to-a-register"></a>Donanım profili için bir kayıt atama

1.  Donanım profili oluşturduktan sonra Git **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**kayıtları**.
2.  İçinde **POS kayıtları** bağlantıyı tıklatın **kayıt numarası** çevre simulator kullanması gereken kasa için alan.
3.  **Düzenle**'yi tıklatın.
4.  İçinde **profil** bölümünde **donanım profili** alanında, oluşturduğunuz sanal çevre birimleri için donanım profilini seçin.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Kanal veritabanındaki değişiklikleri Eşitle

1.  Git **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**.
2.  Seçin **1090** dağıtım zamanlaması.
3.  ' I **şimdi çalıştırmak** POS değişiklikleri eşitlemek için.

Veriler eşitlenir sonra yeni donanım profilinde ve kayıt üzerinde değişiklik kanal veritabanında kullanılabilir.

## <a name="install-the-peripheral-simulator"></a>Çevre simulator yükleyin
1.  Git **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profilleri**.
2.  ' I **karşıdan**ı **PeripheralSimulator**. **Not:** çevre simulator karşıdan yüklemeden önce açılır pencere engelleyicilerini devre dışı bırakmanız gerekir.
3.  Karşıdan yükleme tamamlandıktan sonra açık **Downloads** klasörü çift tıklatın ve **VirtualPeripherals.msi** yükleyiciyi başlatmak için.
4.  Çevre simulator, varsayılan ayarları kullanarak yükleyin.

Çevre simulator yanı sıra, genel kontrol nesneleri Monroe danışmanlık hizmetleri yüklemeniz gerekir. Aksi halde, çevresel simulator düzgün çalışmaz. Ortak denetim nesneleri karşıdan yüklemek için şu adrese gidin <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Çevre simulator kullanma
Çevre simulator başlatmak için tıklatın **Başlat**, bilgisayarınızda yazın **perakende çevresel simulator**ve arama sonuçlarında göründüğünde app seçin. Çevre simulator başlattıktan sonra desteklenen aygıtları görmek için bir aygıt adını tıklatın. Bu aygıtlar, pencerenin sol tarafındaki sekmeleri olarak listelenir. Belirli bir aygıt görüntülemek için bu aygıta sekmesini tıklatın.

### <a name="line-display-capabilities"></a>Satır görüntüleme yetenekleri

Çevre simulator içinde listelenen ilk aygıt satır görüntülenir. Sanal satır görüntüleme yapılandırıldığında, POS harekete taranıp gibi kalemleri gösterir. Satır öğeleri yanı sıra, bir ödeme POS'a seçildiğinde gelmiş olan toplam görüntü gösterilir. Ayrıca, vadesi gelen bakiye gösterilir bir ödeme girildiğinde, ancak hala bir denge olduğu hareketin vade. POS kullanılmadığından, kasa kapalı olduğunu göstermek için bir ileti görüntülenebilir. İletiyi yapılandırmak gerekir **çizgi ekran** hızlı donanım profilinde.

### <a name="cash-drawer-capabilities"></a>Nakit Çekmecesi yetenekleri

Nakit Çekmecesi çevresel simulator içinde listelenen ikinci bir aygıttır. Donanım profili sanal Nakit Çekmecesi kullanmak üzere yapılandırıldığında, POS ödeme bildirimi gibi işlemler çekmece karşılık para çekmecesini etkin vardiya için açar ve böylece kasiyer yapabilirsiniz değiştirmek veya standart cash-and-carry hareketler sırasında Nakit havale. Etiketleri sanal Nakit Çekmecesi olan **ana çekmece** ve **ikinci çekmece**. Bu etiketler çekmece ve Çekmecesi 2 donanım profilinde sırasıyla temsil eder. Bir çekmece kapalı, kapalı para çekmecesini görüntüsü gösterilir ve kapalı para çekmecesini düğmesinde etiketli **çekmeceyi Aç**. Bu düğmeyi tıklatırsanız, resim çekmeceyi Aç olduğunu belirtmek için bir açık para çekmecesini görüntüsü ile değiştirilir. Açık para çekmecesini düğmesinde etiketli **çekmeceyi Kapat**. POS, birden fazla operasyon para çekmecesini açmak neden olabilir. Nakit Çekmecesi açıkken çoğu işlemi devam edemiyor. Özel durumlar, bazı son günün yordamlardır. POS kullanıcı para çekmecesini açık iken bir işlem gerçekleştirilemiyor bildiren bir hata iletisi alırsa, kullanıcı devam etmek için fiziksel veya sanal para çekmecesini kapatmanız gerekir. Nakit Çekmecesi olarak işaretlenmişse, **Shared** donanım profilinde sistem çekmece bir operasyondan önce kapalı olduğundan emin olun değildir. Para çekmecesini açık olsa bile, her zaman olduğu gibi işlem devam eder. Nakit Çekmecesi satış associates arasında paylaşılır ve bir yerlerde desteklediği senaryoları ilişkilendirmek Bu davranış başka bir ilişkilendirme kendi POS aygıt ilgisiz görevleri gerçekleştirirken para çekmecesini kullanır. Nakit Çekmecesi için yapılan değişiklikler geçerli shift kapatılır ve yeni bir vardiya açıldığında kadar açık değildir.

### <a name="msr-capabilities"></a>MSR yetenekleri

Çevre simulator OPOS modu veya klavye Golf Sopası modu çalışarak, sanal MSR işlemleri için güçlü destek sağlar. OPOS modu MSR donanım profilinde bir OPOS aygıtı olarak çalışması için yapılandırılmasını gerektirir. Klavye Golf Sopası modu, yalnızca Microsoft Windows klavye Golf Sopası veri olaylar gönderir. Kur farkları yanı sıra, Golf Sopası modları OPOS ve klavye aşağıdaki şekillerde farklıdır:

-   POS istemci OPOS MSR aygıtlarını manyetik bant veri bağlılık veya Hediye kartı giriş için izin senaryoları gibi belirli senaryolar için sağlar.
-   Klavye Golf Sopası modunda, çevresel simulator verileri gönderildiğinde etkin olan alana klavye Golf Sopası verileri gönderir. Bu davranış, bir klavye kullanarak veri girilmesi durumunda ortaya çıkan davranış benzer. MSR bir klavye üçgen kullanmak için kullanıcı için perakende Modern POS (doğru alanında alınan veri emin olmak için MPOS) geçmelidir. Bu nedenle, bir gecikme saat verileri doğru alana gönderdiğinden emin olmak için kullanıcının sahip şekilde yapılandırabilirsiniz.

#### <a name="testing-gift-and-payment-card-swipes"></a>Hediye ve ödeme kartı swipes sınama

Ayrıca çevre simulator sağlayan sanal MSR senaryoları için hediye ve ödeme kartı swipes test etmek için belirli bir MSR veri yapılandırmanızı sağlar. Bir kart oluşturmak için artı işaretini tıklatın (**+**) düğmesini tıklatın ve kart türünü seçin. Daha sonra kart numarası belirtin veya sona erdiği ay ve yıl tanýmladýðýnýz kartının POS gönderilmesi gereken verileri izlemek. Seçtiğiniz değer **kart türüne** bir kart için eşlenen bir etiket bir alandır. Bu etiket, bunlar çevre simulator geçirilen kartları belirlemek kolaylaştırır. Sol ok tuşunu kullanarak çevre simulator içinde yapılandırılmış olan kartları seçebilirsiniz (**&lt;**) ve sağ ok (**&gt;**) görüntü kartı üzerindeki düğmelere. Düzenleyebilir ve kartları kullanarak silmek **düzenleme** ve **Sil** düğmelerinin yanında artı işareti (**+**) düğmesi.

### <a name="pin-pad"></a>PIN pad

PIN pad simulator OPOS PIN pad benzetimini yapmak için yapılandırabilirsiniz. Bir elektronik fon transferi (EFT) hareket POS'a gerçekleştirilir ve PIN girişi gerektirir, PIN girişi için PIN iste aygıta donanım istasyonu çağırır. Çalışmak için PIN pad çevresel simulator içinde EFT ödeme bağlayıcı desteği gerektirir.

### <a name="printer"></a>Yazıcı

POS'tan yazdırılacağı gibi sanal çevre yazıcı yalnızca girişler gösterilir. Yazdırma işlemi birden çok giriş oluşturursa, giriş gezinebilirsiniz.

#### <a name="configure-receipt-printing"></a>Makbuz yazdırması yapılandırmak

1.  Git **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profilleri**.
2.  Oluşturduğunuz sanal çevre birimleri için donanım profilini seçin.
3.  Üzerinde **yazıcı** hızlı,'ı **düzenleme**.
4.  İçinde **giriş Profil Kimliği** alan, alış irsaliyesi profili seçin.
5.  Click **Save**.

### <a name="scale"></a>Ölçek

POS harekete ölçekli ürün eklenir ve yapılandırılmış bir ölçek, POS ölçeğindeki ağırlık alır. Ürün harekete eklenmeden önce iki sanal ve fiziksel ölçek için ürün veya ağırlık belirtilmelidir. Ölçekli ürün harekete eklemeden önce çevresel simulator ölçeklemek için gidin ve artı işaretini kullanın (**+**) ve eksi işareti (**-**) ölçeği raporlamalıdır ağırlık ayarlamak için düğmeler. Ayrıca, istediğiniz kalınlık doğrudan girebilirsiniz **geçerli değer** alan. Ölçek için ağırlık birimlerinin artı işareti kullanarak ayarlayabilirsiniz (**+**), **düzenleme**, ve **Sil** düğmeleri. Bu şekilde, ağırlıklı ürünler veya ölçek kullanıldığı yerel temel birimler belirtilebilir.

#### <a name="configure-a-scale-product"></a>Ölçekli ürün yapılandırma

1.  Git **perakende ve****ticaret**&gt;**ürün ve kategori**&gt;**ürünleri kategoriye göre serbest**.
2.  Ürün kaydı açın.
3.  Küçük yazılara ürünü seçin.
4.  Üzerinde **perakende** hızlı, set **ölçekli ürün** gelen seçenek **No** için **Evet**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Kanal veritabanındaki değişiklikleri Eşitle

1.  Git **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**.
2.  Seçin **1040** dağıtım zamanlaması.
3.  ' I **şimdi çalıştırmak** POS değişiklikleri eşitlemek için.

POS harekete ölçekli ürün eklendiğinde, veri senkronize sonra POS ağırlık için ölçek denetler.

### <a name="signature-capture"></a>İmza alma

Sanal imza yakalama aygıtı kullanılan ödeme imza gerektirdiğinde imza sanal imza yakalama altlığında girmesini ister. Kullanıcı imza POS'a göstermek için kabul edebilirsiniz. Kasiyerin ardından imza kabul edebilirsiniz. İmza sonra ödeme ile birlikte kaydedilir ve arka ofis diğer hareket verilerini birlikte eşitlenir.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Bir imza gerektirecek şekilde bir ödeme ayarlama

1.  Git **perakende ve ticaret**&gt;**kanallar**&gt;**perakende mağazalar**&gt;**tüm perakende mağazalar**.
2.  Perakende Mağaza seçin.
3.  **Düzenle**'yi tıklatın.
4.  ' I **ayarlamak**, daha sonra **ayarlamak** bölümünde,'ı **ödeme yöntemleri**.
5.  **Düzenle**'yi tıklatın.
6.  İmza gerektiren bir ödeme yöntemi seçin.
7.  İçinde **genel** altında bölümünde **imza yakalama**ayarlayın **imza yakalama aygıtını kullan** için seçenek **Evet**.
8.  İçinde **imza yakalama minimum tutar** alanında, imza yakalama tetiklemesi gereken minimum tutarı girin.

#### <a name="synchronize-changes-to-the-channel-database"></a>Kanal veritabanındaki değişiklikleri Eşitle

1.  Git **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım zamanlamasını**.
2.  Seçin **1070** dağıtım zamanlaması.
3.  ' I **şimdi çalıştırmak** POS değişiklikleri eşitlemek için.

Bir ödeme gerektiren bir imza kullanıldığında ve tutar imza eşik karşılayan veriler eşitlenir sonra sanal imza yakalama aygıtında bir imza için POS ister.

## <a name="additional-configuration"></a>Ek yapılandırma
Sınamakta senaryolar için daha uygun bir şekilde çevre simulator's yapılandırma dosyasını düzenleyebilirsiniz. C: yapılandırma dosyasından bulabilirsiniz\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Ölçek, test için hazır kart tipleri ve barkod türleri üzerinde test etmek için kullanılabilir birimleri yapılandırma dosyasını tanımlar. Örneğin, metin değerleri yapılandırma dosyasında değişiklik yaparak, yeni kart tipi veya çalışma zamanında Seçili ölçü birimi ekleyebilirsiniz. Uygulamayı yeniden başlatıldıktan sonra yeni değerleri görüntülenir.

## <a name="troubleshooting"></a>Sorun Giderme
Çevre simulator için Aktiviteler içinde çevre simulator günlüğe kaydedilir. Günlük C: bulabilirsiniz\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Çevre simulator sorunları da at erişebileceğiniz Windows olay günlüğüne bildirir **uygulama ve hizmet günlükleri**&gt;**Microsoft**&gt;**DynamicsAX**. Donanım profili veya diğer alanlarında yapılan değişiklikler açık değilse, MPOS veya çevresel simulator kullandığınızda kanal veritabanına veri eşitlemek için kullanılan dağıtım Zamanlayıcısı işleri denetleyin. Değişikliklerin eşitlenmesi ama hala POS'a açık olmayan, POS istemciyi yeniden başlatın. Yapılandırılmış Nakit Çekmecesi değişiklikleri yeni bir vardiya oluşturulana kadar etkili değildir. Nakit Çekmecesi için değişiklik yaparsanız, bu nedenle, her zaman yeni Nakit Çekmecesi kurulumunu test etme varolan shift kapatmak emin olun. Bazen, Monroe danışmanlık hizmetleri ortak denetim nesnelerden sonra üreticinin sürücüsü yüklüyse, sürücü ortak denetim nesneleri düzgün çalışmayı durdurmasına neden olabilir. Bu durumda, ortak denetim nesneleri yeniden yüklemeniz gerekir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Retail peripherals overview](retail-peripherals-overview.md)


