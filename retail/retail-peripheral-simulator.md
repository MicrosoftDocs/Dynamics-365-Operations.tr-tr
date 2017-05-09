---
title: "Perakende çevre birimi benzeticisi"
description: "Bu konuda Microsoft Dynamics 365 for Operations - Perakende ile sağlanan çevre birim benzetim aracı açıklanır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
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

# <a name="retail-peripheral-simulator"></a>Perakende çevre birimi benzeticisi

[!include[banner](includes/banner.md)]


Bu konuda Microsoft Dynamics 365 for Operations - Perakende ile sağlanan çevre birim benzetim aracı açıklanır.

<a name="overview"></a>Özet
--------

Microsoft Dynamics 365 for Operations - Perakende çevre birim benzeticisi, perakende ortamlarda kullanılan çevre birim cihazlarını kurmanıza, test etmenize ve sorunları gidermenize yardımcı olan bir araçtır. Çevre birim benzeticiyi perakende çevre birimlerinin test işlemini verimli hale getirmek ve hatalı kurulum ya da arızalı cihaz sürücülerinin neden olduğu sorunları izole etmek için kullanabilirsiniz. Çevre birim benzeticide Microsoft Dynamics 365 for Operations - Perakende'nini desteklediği cihazların sanal sürümlerine sahip bir masaüstü programı bulunur. Her sanal cihaz için bir bölüm cihaz ile perakende satış noktası (POS) arasındaki etkileşimi gösterir. Bunu ayrıca çeşitli POS senaryoları için geçerli olan giriş sağlamak için de kullanabilirsiniz. Çevre birim benzeticisi POS ile aşağıdaki sanal cihazlar arasındaki etkileşimi destekler:

-   **Yazıcı** – Çevre birim benzetici POS yazıcı için yapılandırılmış olan girişleri gösterebilir.
-   **Satır görüntüsü** – Fiziki satır görüntüsündeki bir etkinliği gösteren bir sanal satır görüntüsü yapılandırabilirsiniz.
-   **Manyetik bant okuyucu (MSR)** – Çevre birim benzeticisinden POS'a manyetik bant okuyucu olayları benzetimi gönderebilirsiniz.
-   **Çekmece** – Fiziksel kasa çekmecesi benzetimi yapabilirsiniz.
-   **Çekmece 2** – Çevre birim benzeticide ikinci bir kasa çekmecesini ayarlayarak, iki etkin vardiyası olan tek bir POS kaydıyla ilgili senaryolar için benzetim yapabilirsiniz.
-   **Tarayıcı** – Çevre birim benzeticinin desteklediği sanal barkod tarayıcı barkod tarama olayları düzenleyebilir.
-   **Terazi** – Sanal bir terazi POS ile tartılan öğeler arasındaki etkileşimin benzetimini yapmanızı sağlar.
-   **Kişisel kimlik numarası (PIN) pad** – PIN pad işlemlerinin benzetimini yapabilirsiniz. **Not:** Ödeme bağlayıcısı aracılığıyla fiziksel bir PIN pad için destek sağlamanız gerekir.
-   **İmza yakalama** – Çevre birim benzetici, müşteri hesabı ödemeleri gibi bazı ödemeler için gerekli imzalar için bir istem ayarlayabileceğiniz bir sanal imza yakalama cihazı içerir.

Çevre birim benzeticisini, bir barkod tarayıcı ve MSR'den kaynaklanan klavye emülasyon olaylarının benzetimini yapmak için de kullanabilirsiniz. Sanal çevre birim benzeticisi özellikle Retail POS (OPOS) cihazları için Nesne Bağlama ve Katıştırma özelliğini destekler.

## <a name="key-scenarios"></a>Temel senaryolar
### <a name="troubleshooting"></a>Sorun Giderme

Çevre birim benzeticiyi cihaz kurulum sorunlarını gidermek için kullanabilirsiniz. Çevre birim benzeticiniz veya aynı sınıftan ikinci bir cihazınız yoksa, sorunun nereden kaynaklandığını belirlemek zor olabilir. Ancak, çevre birim benzeticiniz varsa, sanal cihazlar kurabilir ve fiziksel cihazlar için kullanılan aynı kod yollarını ve iş mantığını çalıştırabilirsiniz. Çevre birim benzetici açısından bakıldığında, sanal cihazlar ile fiziksel cihazlar arasındaki temel fark hizmet nesnesi veya cihaz sürücüsüdür. Fiziksel cihazlar için, hizmet nesnesi cihaz üreticisi tarafından sağlanır. Bunun tersine, çevre birim benzetici için hizmet nesneleri çevre birim benzeticinin bir parçası olarak sağlanır. Çevre birim benzetici düzgün şekilde çalıştığında, donanım profilindeki cihaz adı gerçek cihazın adıyla değiştirildiğinde cihaz düzgün şekilde çalışmazsa, üreticinin sağladığı hizmet nesnesi ile ilgili bir sorun olduğunu düşünebilirsiniz.

### <a name="training"></a>Eğitim

Çevre birim benzeticiyi, fiziksel donanım kurulumu olmadığında kasiyer eğitimine gerçekçi bir katmak eklemek için kullanabilirsiniz. Çevre birim benzetici eğitim senaryolarına dahil olduğunda, kasiyer ürün barkod taraması veya hediye kartı geçirme gibi giriş sağlayarak ve belirli bir hareket için hangi makbuzların yazdırıldığını gözlemleyerek POS ile daha etkin şekilde etkileşim kurar.

### <a name="testing"></a>Test etme

Çevre birim benzeticiyi fiziksel donanımı sanal bir ortamda dağıtmak zorunda kalmadan ürün barkodlarını, makbuz biçimlerini, vb. test etmek için kullanabilirsiniz. Fiziksel donanım gerekli olmadığından ve donanım istasyonunda veya fiziksel bir bilgisayarda POS istemcisi dağıtmak zorunda olmadığınızdan, arka ofiste yapılan değişiklikleri daha hızlı bir şekilde sınayabilirsiniz.

## <a name="set-up-the-peripheral-simulator"></a>Çevre birimi benzeticisini kurma
### <a name="set-up-a-hardware-profile"></a>Donanım profili ayarlama

1.  Çevre birim benzeticisini kurmak için **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri**'ne gidin.
2.  Yeni bir profil oluşturmak için **Yen**'ye tıklayın.
3.  **Profil numarası** ve **Açıklama** alanlarına değer girin.
4.  Test edilmesi gereken sanal cihazları kurmak için aşağıdaki tabloyu kullanın. Tablodaki sütunların açıklaması aşağıdadır:
    -   **Cihaz** – Bu sütun cihazı ayarlamak için genişlettiğiniz Hızlı Sekmenin adını verir.
    -   **Cihaz türü** – Bu sütun cihaz adıyla etiketlenen alanda seçtiğiniz değeri verir.
    -   **Cihaz adı** – Bu sütun cihaz adı için girdiğiniz tam değeri verir. **Önemli:** Burada verilen cihaz adları gereklidir çünkü donanım istasyonu cihazlara ulaşmak için bu belirli adları kullanır. Bu özel adları kullanmazsanız cihaz kullanılamaz.

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

**Not:** Barkod tarayıcı ve MSR'den gelen klavye emülasyonu olaylarının benzetimini yapmak için donanım profilinde özel bir kurulum gerekli değildir.

### <a name="assign-the-hardware-profile-to-a-register"></a>Donanım profilini bir kasaya atama

1.  Donanım profili oluşturduktan sonra **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kasalar**'a gidin.
2.  **POS kasaları** listesinde **Kayıt numarası** alanında çevre birim benzeticisini kullanması gereken kasa için bağlantıyı tıklayın.
3.  **Düzenle**'yi tıklatın.
4.  **Profil** bölümünde, **Donanım profili** alanında, sanal çevre birimleri için oluşturduğunuz donanım profilini seçin.
5.  **Kaydet**'e tıklayın.

### <a name="synchronize-changes-to-the-channel-database"></a>Değişiklikleri kanal veritabanıyla eşleştirme

1.  **Perakende ve ticaret** &gt; **Perakende BT** &gt; **Dağıtım planı** öğelerini seçin.
2.  Dağıtım planı **1090**'ı seçin.
3.  Değşiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a  tıklayın.

Veriler eşitlendikten sonra yeni donanım profili ve kasadaki değişiklikler kanal veritabanında kullanılabilir.

## <a name="install-the-peripheral-simulator"></a>Çevre birimi benzeticisini yükleme
1.  **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri** öğesine gidin.
2.  **İndir**'e ve ardından **PeripheralSimulator**'a tıklayın. **Not:** Çevre birim benzeticisini indirmek için açılır pencere engelleyicilerini devre dışı bırakmanız gerekir.
3.  İndirme işlemi tamamlandıktan sonra **İndirmeler** klasörünü açın ve yükleyiciyi başlatmak için **VirtualPeripherals.msi**'ye çift tıklayın.
4.  Çevre birim benzeticisini varsayılan ayarları kullanarak yükleyin.

Çevre birim benzeticisine ek olarak, Monroe Danışmanlık Hizmetlerinden genel denetim nesnelerini yüklemeniz gerekir. Aksi halde, çevre birim benzetici düzgün çalışmaz. Genel denetim nesnelerini indirmek için şu adrese gidin: <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Çevre birimi benzeticisini kullanma
Çevre birim benzeticisini başlatmak için bilgisayarınızda **Başlat**'a tıklayın, **Perakende çevre birim benzeticisi** yazın ve arama sonuçlarında göründüğünde uygulamayı seçin. Çevre birim benzeticisini başlattıktan sonra desteklenen cihazları görmek için bir cihaz adına tıklayın. Bu cihazlar, pencerenin sol tarafında sekmeler olarak listelenir. Belirli bir cihazı görüntülemek için bu cihazın sekmesine tıklayın.

### <a name="line-display-capabilities"></a>Satır görüntüleme yetenekleri

Satır görüntüleme cihazı, çevre birim benzeticide listelenen ilk cihazdır. Sanal satır görüntüleme yapılandırıldığında, satır maddelerini POS hareketinde taranmış gibi gösterir. Satır maddelerinin yanı sıra, ekran POS'ta bir ödeme seçildiğinde vadesi gelmiş olan toplamı da gösterir. Ayrıca, bir ödeme girildiğinde vadesi gelmiş bakiyeyi de gösterir ancak bakiye hareket için vadesi gelmiş olarak kalmaya devam eder. POS kullanılmadığında, kasa çekmecesinin kapalı olduğunu göstermek için bir ileti görüntülenebilir. İletiyi donanım profilinin **Satır ekranı** Hızlı sekmesinden yapılandırmanız gerekir.

### <a name="cash-drawer-capabilities"></a>Kasa çekmecesi yetenekleri

Kasa çekmecesi, çevre birim benzeticide listelenen ikinci cihazdır. Donanım profili sanal kasa çekmeceleri kullanmak üzere yapılandırıldığında, POS ödeme bildirimi gibi çekmece işlemlerine karşılık olarak etkin vardiya için kasa çekmecesini açar ve böylece kasiyer standart peşin ödeme hareketleri sırasında değişiklik yapabilir veya nakit havale edebilir. Sanal kasa çekmecelerinde **Ana çekmece** ve **İkinci çekmece** etiketleri bulunur. Bu etiketler sırasıyla donanım profilinceki Çekmece ve Çekmece 2'yi temsil eder. Bir çekmece kapalı olduğunda, kapalı kasa çekmecesi görüntüsü gösterilir ve kapalı kasa çekmecesindeki düğme **Çekmeceyi aç** olarak etiketlenir. Bu düğmeye tıklarsanız, resim bir açık çekmece görüntüsüyle değiştirilir ve çekmecenin açık olduğunu belirtir. Açık para çekmecesi düğmesi **Çekmeceyi kapat** oarak etiketlenir. POS'taki birçok işlem para çekmecesinin açılmasına neden olabilir. Kasa çekmecesi açıkken çoğu işlem sürdürülemez. Özel durumlar bazı gün sonu yordamlardır. POS kullanıcısı para çekmecesi açık olduğunda bir işlemin gerçekleştirilemediğini bildiren bir hata iletisi alırsa, kullanıcı devam etmek için fiziksel veya sanal kasa çekmecesini kapatmalıdır. Kasa çekmecesi donanım profilinde **Paylaşılan** olarak işaretlenmişse, sistem çekmecenin bir işlemden önce kapalı olup olmadığını kontrol etmez. Kasa çekmecesi açık olsa bile, işlem her zaman olduğu gibi devam eder. Bu davranış, kasa çekmecelerinin satış yetkilileri arasında paylaştırıldığı ve bir yetkilinin diğer bir yetkili kendi POS cihazında alakasız bir görev gerçekleştirirken kasa çekmecesimi kullandığı senaryoları destekler. Kasa çekmecesinde yapılan değişiklikler geçerli vardiya kapatılana ve yeni bir vardiya açılana kadar belli değildir.

### <a name="msr-capabilities"></a>MSR becerileri

Çevre birimi benzeticisi, OPOS modunda veya klavye emülasyon modunda çalışarak, sanal MSR işlemleri için güçlü destek sağlar. OPOS modu, MSR'nin donanım profilinde bir OPOS cihazı olarak çalışmak üzere yapılandırılmasını gerektirir. Klavye emülasyon modu, yalnızca klavye emülasyon verisi olaylarını Microsoft Windows'a gönderir. Kurulum farklarının yanı sıra, OPOS ve klavye emülasyon modları aşağıdaki şekillerde farklılık gösterir:

-   POS istemcisi OPOS MSR cihazlarını, bağlılık programı veya hediye kartı girişi için manyetik bant verilerine izin verilen senaryolar gibi belirli senaryolar için etkinleştirir.
-   Klavye emülasyonu modunda, çevre birim benzeticisi klavye emülasyon verilerini veri gönderilirlen etkin olan alana gönderir. Bu davranış, verilerin bir klavye kullanılarak girilmesi durumunda ortaya çıkan davranışa benzer. MSR'yi bir klavye emülasyonu olarak kullanmak için, verinin doğru alana alındığından emin olmak üzere kullanıcının Retail Modern POS'a (MPOS) geçmesi gerekir. Bu nedenle, bir gecikme yapılandırabilirsiniz, böylece kullanıcının verilerin doğru alana gönderdiğinden emin olmak için zamanı olur.

#### <a name="testing-gift-and-payment-card-swipes"></a>Hediye ve ödeme kartı geçişlerini sınama

Çevre birim benzeticisinin sağladığı sanal MSR, hediye ve ödeme kartı geçişleri için senaryoları test etmek amacıyla berlirli bir MSR verisi yapılandırmanıza da olanak tanır. Bir kart oluşturmak için artı işareti (**+**) bulunan düğmeye tıklayın ve kart türünü seçin. Daha sonra kart numarasını belirtin veya tanımladığınız kartın sona sona erdiği ay ve yılla birlikte POS'a gönderilmesi gereken verileri izleyin. **Kart türü** alanında seçtiğiniz değer kartla eşlenebilen bir etikettir. Bu etiket, kartların çevre birim benzeticisinden geçirildiklerinde daha kolay tanımlanmasını sağlar. Çevre birim benzeticisinde yapılandırılan kartları, kart görüntüsünün üstündeki sol ok (**&lt;**) ve sağ ok (**&gt;**) düğmelerini kullanarak seçebilirsiniz. Kartları artı işareti (**+**) düğmesinin yanındaki **Düzenle** ve **Sil** düğmelerini kullanarak düzenleyebilir veya silebilirsiniz.

### <a name="pin-pad"></a>PIN pad

PIN pad benzeticisini bir OPOS PIN pad benzetimi yapmak için yapılandırabilirsiniz. POS'ta bir elektronik fon transferi (EFT) hareketi gerçekleştirildiğinde ve PIN girişi gerektiğinde, donanım istasyonu PIN girişi isteminde bulunması için PIN cihazını çağırır. Çalışmak için, çevre birim benzeticisindeki PIN pad EFT ödeme bağlayıcı desteği gerektirir.

### <a name="printer"></a>Yazıcı

Sanal çevre birim yazıcısı makbuzları POS'tan yazdırılacağı şekilde gösterir. Yazdırma işlemi birden çok giriş oluşturursa, girişler arasında gezinebilirsiniz.

#### <a name="configure-receipt-printing"></a>Makbuz yazdırmayı yapılandırma

1.  **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri** öğesine gidin.
2.  Sanal çevre birimleri için oluşturduğunuz donanım profilini seçin.
3.  **Yazıcı** Hızlı sekmesinde **Düzenle**'ye tıklayın.
4.  **Makbuz profili kimliği** alanında, bir makbuz profili seçin.
5.  **Kaydet**'e tıklayın.

### <a name="scale"></a>Ölçek

POS hareketine bir terazi ürünü eklendiğinde ve bir terazi yapılandırıldığında, POS ağırlığı teraziden alır. Hem sanal hem de fiziksel terazi için, ürün veya ağırlık ürün harekete eklenmeden önce belirtilmelidir. Terazi ürününü harekete eklemeden önce, çevre birim benzeticisindeki teraziye gidin ve artı (**+**) ve eksi işareti (**-**) düğmelerini kullanarak terazinin bildirmesi gereken ağırlığı ayarlayın. Ayrıca, **Geçerli değer** alanından istediğiniz ağrılığı doğrudan girebilirsiniz. Artı işareti (**+**), **Düzenle** ve **Sil** düğmelerini kullanarak terazi için ağırlık birimlerini ayarlayabilirsiniz. Bu şekilde, birimler tartılan ürünler temel alınarak veya terazinin kullanıldığı yerel konuma göre belirtilebilir.

#### <a name="configure-a-scale-product"></a>Bir terazi ürünü yapılandırma

1.  **Perakende ve ** **ticaret** &gt; **Ürünler ve kategoriler** &gt; **Kategoriye göre serbest bırakılmış ürünler**'e gidin.
2.  Ürün kaydını açın.
3.  Tartılacak ürünü seçin.
4.  **Perakende** Hızlı sekmesinde, **Terazi ürünü** seçeneğini **Hayır** yerine **Evet** olarak ayarlayın.

#### <a name="synchronize-changes-to-the-channel-database"></a>Değişiklikleri kanal veritabanıyla eşleştirme

1.  **Perakende ve ticaret** &gt; **Perakende BT** &gt; **Dağıtım planı** öğelerini seçin.
2.  Dağıtım planı **1040**'ı seçin.
3.  Değşiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a  tıklayın.

Veri eşitlendikten sonra, POS hareketine bir terazi ürünü eklendiğinde, POS ağırlık için teraziyi kontrol eder.

### <a name="signature-capture"></a>İmza alma

Sanal imza yakalama cihazı, kullanılan ödeme imza gerektirdiğinde kullanıcıdan sanal imza yakalama pedinde bir imza sağlamasını ister. Kullanıcı POS'ta göstermek için imzayı kabul edebilir. Ardından kasiyer imzayı kabul edebilir. Bu durumda imze ödeme ile birlikte kaydedilir ve diğer hareket verileriyle birlikte arka ofisle eşitlenir.

#### <a name="set-up-a-tender-to-require-a-signature"></a>İmza gerektirecek şekilde bir ödeme ayarlama

1.  **Perakende ve ticaret** &gt; **Kanallar** &gt; **Perakende mağazaları** &gt; **Tüm perakende mağazaları**'na gidin.
2.  Perakende mağaza seçin.
3.  **Düzenle**'yi tıklatın.
4.  **Ayarla**'ya ve ardından **Ayarla** bölümünde **Ödeme yöntemleri**'ne tıklayın.
5.  **Düzenle**'yi tıklatın.
6.  İmza gerektiren ödeme yöntemini seçin.
7.  **Genel** bölümünde, **İmza Yakalama** altında **İmza yakalama cihazını kullan** için **Evet** seçeneğini ayarlayın.
8.  **İmza yakalama minimum tutarı** alanında, imza yakalamayı tetiklemesi gereken minimum tutarı girin.

#### <a name="synchronize-changes-to-the-channel-database"></a>Değişiklikleri kanal veritabanıyla eşleştirme

1.  **Perakende ve ticaret** &gt; **Perakende BT** &gt; **Dağıtım planı** öğelerini seçin.
2.  Dağıtım planı **1070**'i seçin.
3.  Değşiklikleri POS ile eşitlemek için **Şimdi çalıştır**'a  tıklayın.

Veriler eşitlendikten sonra, imza gerektiren bir ödeme kullanıldığında ve tutar imza eşik değerini karşıladığında, POS sanal imza yakalama cihazında imza isteminde bulunur.

## <a name="additional-configuration"></a>Ek yapılandırma
Test ettiğiniz senaryolara daha uygun şekilde karşılık vermesi için çevre birim benzeticisinin yapılandırma dosyasını düzenleyebilirsiniz. Yapılandırma dosyasını C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config konumunda bulabilirsiniz. Yapılandırma dosyası terazi testi için kullanılan birimler, test için kullanılabilen kart türlerini ve barkod türlerini tanımlar. Örneğin, yapılandırma dosyasındaki metin değerlerini değiştirerek, çalışma zamanında seçilebilecek yeni kart türü veya ölçü birimi ekleyebilirsiniz. Yeni değerler uygulama yeniden başlatıldığında görüntülenir.

## <a name="troubleshooting"></a>Sorun Giderme
Çevre birim benzeticisi etkinlikleri çevre birim benzeticisi günlüğüne kaydedilir. Günlüğü at C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config konumunda bulabilirsiniz. Çevre birim benzeticisi sorunları Windows olay günlüğüne de bildirir; bu günlüğe **Uygulama ve Hizmet Günlükleri** &gt; **Microsoft** &gt; **DynamicsAX** yolundan erişebilirsiniz. Donanım profili veya diğer alanlarında yapılan değişiklikler açık değilse, MPOS veya çevre birim benzeticisi kullandığınızda, verileri kanal veritabanıyla eşitlemek için kullandığınız dağıtım planlayıcısı işlerini denetleyin. Değişiklikler eşitlenmişse ancak hala POS'ta görünmüyorsa, POS istemcisini yeniden başlatın. Yapılandırılmış kasa çekmesinde yapılan değişiklikler yeni bir vardiya oluşturulana kadar etkin değildir. Bu nedenle, kasa çekmecelerinde değişiklik yaparsanız, yeni kasa çekmecesi kurulumunu test etmek için daima mevcut vardiyayı kapattığınızdan emin olun. Bazen, üreticinin sürücüsü Monroe Danışmanlık Hizmetleri tarafından sağlanan genel denetim nesnelerinden sonra yüklenirse, sürücü genel denetim nesnelerinin düzgün çalışmayı durdurmasına neden olabilir. Bu durumda, genel denetim nesnelerini yeniden yüklemeniz gerekir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Perakende çevre birimlerine genel bakış](retail-peripherals-overview.md)




