---
title: Çoklu kanal gelişmiş otomatik ücretleri
description: Bu konu Commerce kanal düzeni masraflar otomatik gelişmiş özelliklerini kullanmak için ek sipariş masrafları yönetmek için kullanılan özellikleri açıklar.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: 826c955b7c99073ff41c8a5ed75254c824359925
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175166"
---
# <a name="omni-channel-advanced-auto-charges"></a>Çok yönlü kanal gelişmiş otomatik masrafları

[!include [banner](includes/banner.md)]

Bu konu Dynamics 365 for Retail sürüm 10.0.'da yapılandırma ve dağıtım için kullanılabilir olan gelişmiş otomatik masraflar özelliği hakkında bilgi sağlar.

Gelişmiş otomatik masraflar özellikleri etkinleştirildiğinde, desteklenen herhangi bir Commerce kanalında (satış noktası (POS), çağrı merkezi ve çevrimiçi) içinde oluşturulan siparişler [otomatik masraflar](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) yapılandırmalarından hem başlık hem de satır düzeyi ile ilişkili masraflar için faydalanabilirler.

Retail sürüm 10.0 öncesi sürümlerde [otomatik masraf](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) yapılandırmalarına yalnızca e-Ticaret ve çağrı merkezi kanallarında oluşturulan siparişler tarafından erişilebilir. Sürümler 10.0 ve sonrasında, POS tarafından oluşturulan siparişler otomatik masraf yapılandırmalarını kullanabilir. Bu şekilde, ek sair masraflar sistematik olarak satış işlemlerine eklenebilir.

10.0 öncesi sürümler kullanılırken, bir POS kullanıcısının sevkiyat masrafını "sevk tüm" veya "seçilen sevk" POS hareketi sırasında el ile girmesi istenir. Uygulamanın sair masraflar yeteneği, masrafların siparişe nasıl yazıldığıyla ilgilidir, sistematik hesaplama sağlanmaz; hesaplama, masrafların değerini belirlemek için kullanıcının girdisine dayanmaktadır. masraflar yalnızca tek bir "sevkiyat" ile ilgili masraf kodu satırı olarak eklenebilir ve POS içinde oluşturulduktan sonra değiştirilemez veya düzenlenemez.

Sevkiyat masrafları eklemek için el ile uyarıların kullanımı sürüm 10.0 ve sonrasında kullanılabilir. Bir kuruluş **Gelişmiş Otomatik masraflar** parametresini etkinleştirmezse, POS masrafların el ile girişini aynı kalacaktır.

Gelişmiş otomatik masraflar özelliğiyle, POS kullanıcıları tanımlanan herhangi bir sair masraflara dayanan sistematik masraflara sahip olabilirler. Ek olarak, kullanıcılar sınırsız sayıda ek masraf ve ücreti herhangi bir POS satışı hareketine başlık veya satır düzeyinde ekleme ve düzenleme olanağına sahip olurlar.

## <a name="enabling-advanced-auto-charges"></a>Gelişmiş otomatik masrafları etkinleştirmek

**Perakende ve Ticaret \> Genel merkez kurulumu \> Parametreler \> Ticaret parametreleri** sayfasında, **Müşteri siparişleri** sekmesine gidin. **Masraflar** hızlı sekmesinde, **Gelişmiş otomatik masrafları kullan**'ı **Evet** olarak ayarlayın.

![Gelişmiş Otomatik masraflar Parametresi](media/advancedchargesparameter.png)

Gelişmiş otomatik masraflar etkin olduğunda, kullanıcıların bir sevkiyat masrafını POS terminalinde, tümünü sevk veya seçilen müşteri siparişini sevk seçeneği seçildiğinde sevkiyat masrafını el ile girmeleri daha fazla gerekmez. POS sipariş masrafları sistematik olarak hesaplanır ve POS hareketine eklenir (oluşturulan siparişin kriteriyle eşleşen, karşılık gelen otomatik masraf tablosu bulunursa). Kullanıcılar ayrıca, POS ekranı düzenlerine eklenebilecek başlık veya satır düzeyi masrafları el ile yeni eklenen POS işlemleri üzerinden ekleyebilir veya koruyabilir.

Gelişmiş otomatik masraflar etkinleştiğinde, mevcut **Sevkiyat masrafları kodu** ve **Geri ödeme sevkiyat masrafları** için **Ticaret parametreleri** artık kullanılmaz. Bu parametreler yalnızca **Gelişmiş otomatik masraflar kullan** parametresi **Hayır** olarak ayarlandığında uygulanabilir.

Bu özelliği etkinleştirmeden önce, çalışanlarınızı eğittiğinizden ve test ettiğinizden emin olun, çünkü bu, sevkiyat veya diğer masrafların nasıl hesaplandığı ve POS satış siparişlerine eklendiği iş işlemi akışını değiştirecektir. POS'tan işlemlerin oluşturulması işlem akışı üzerindeki etkisini anladığınızdan emin olun. Çağrı merkezi ve e-ticaret siparişleri için gelişmiş otomatik masrafların etkisi asgari düzeydedir. Çağrı merkezi ve e-ticaret uygulamaları, geçmişte otomatik masraflar tablosunda ek sipariş ücretleriyle ilgili sahip oldukları eski davranışa sahip olacaktır. Çağrı merkezi kanalı kullanıcıları, sistem tarafından hesaplanan otomatik masrafları başlık veya satır düzeyinde el ile düzenleme olanağına sahip olmaya devam edecektir veya sair masrafları başlık veya satır düzeyinde el ile ekleyebilirler.

## <a name="additional-pos-operations"></a>Ek POS işlemleri

Gelişmiş otomatik masrafların POS uygulaması ortamınızda doğru çalışması için yeni POS operasyonları eklenmiştir. Bu işlemlerin [POS ekran düzenlerine](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) eklenmesi ve gelişmiş otomatik masraflar dağıttığınızda POS cihazlarına dağıtılması gerekir. Bu işlemler eklenmezse, kullanıcılar sair masrafları POS hareketleri üzerinde yönetemez veya koruyamaz ve sistematik olarak otomatik masraf yapılandırmalarına dayanan masraf değerlerini değiştiremez veya ayarlayamazlar. En azından, **masrafları yönet** operasyonunu POS düzeninizde dağıtmanız önerilir.

Yeni operasyonlar şu şekildedir.

- **142 - masrafları yönet** - Bu işlemi POS kullanıcılarının el ile veya otomatik masraf hesaplamaları ile sistematik olarak eklenmiş POS hareketleri için sair masrafları görüntülemelerini ve düzenlemelerini sağlar.
- **141 - Başlık masrafları ekle** - Bu işlemi, kullanıcıya başlık düzeyinde sair masrafı herhangi bir POS hareketine el ile ekleme yeteneği sağlamak (ve kullanılacak masraf kodunu seçmek) için kullanın.
- **140 - Satır masrafları ekle** - Bu işlemi, kullanıcıya satır düzeyinde sair masrafı herhangi bir POS hareketi satırına el ile ekleme yeteneği sağlamak (ve kullanılacak masraf kodunu seçmek) için kullanın.
- **143 - masrafları yeniden hesapla** - Bu işlemi satış hareketi için masrafların tamamen yeniden hesaplanmasını gerçekleştirmek için kullanın. Daha önceden kullanıcı tarafından üzeri yazılan otomatik değişiklikler geçerli sepet yapılandırmasına dayanarak yeniden hesaplanır.

Tüm POS işlemlerinde olduğu gibi, güvenlik yapılandırmalarının işlemin gerçekleştirilebilmesi için yönetici onayına ihtiyaç duyması sağlanabilir.

Yukarıda listelenen POS operasyonlarının ayrıca POS düzenine, **Gelişmiş otomatik masrafları kullan** parametresi devre dışıysa bile eklenebileceğini anımsamak önemlidir. Bu senaryoda, kuruluşlar, el ile eklenen masrafları görüntüleyebilme ve bunları **Masrafları yönet** işlemini kullanarak düzenleme faydalarına sahip olurlar. Kullanıcılar **Başlık masrafları ekle** ve **Satır masrafları ekle** operasyonlarını POS hareketler için **Gelişmiş otomatik masraflar kullan** parametresi devre dışıysa bile kullanabilirler. **Masrafları yeniden hesapla** işlemi, **Gelişmiş otomatik masrafları kullan** seçeneği devre dışı bırakılmışsa daha az işleve sahiptir. Bu senaryoda, hiçbir şey yeniden hesaplanmaz ve otomatik olarak harekete eklenen tüm masraflar 0,00 $ tutarına sıfırlanır.

## <a name="use-case-examples"></a>Kullanım örneği

Bu bölümde, örnek kullanım vakaları size otomatik masraflar ve sair masrafların kanalı siparişleri bağlamında yapılandırılması ve kullanılmasını anlamanızda yardımcı olmak için sunulur. Bu örnekler, **Gelişmiş otomatik sair masraflar kullan** parametresi etkinleştirildiğinde uygulamanın davranışını gösterir.

### <a name="auto-charges-header-charges-example"></a>Otomatik masraflar başlık masrafları örneği

#### <a name="use-case-scenario"></a>Kullanımı vakası senaryosu

Bir perakendeci, ürünlerin müşteriye nakledilmesi gereken hareketler Ticaret kanalında oluşturulduklarında bir navlun için otomatik olarak masrafları eklemek için kullanmak istiyor. Perakendeci iki teslimat seçeneği sunmaktadır: kara ve hava yolu. Bir müşteri Karayolu teslimatını seçerse ve değer 100$'dan az ise, perakendeci müşteriden 10.00$ navlun ücreti talep etmek istemektedir. Sipariş 100$ değerin üzerindeyse ve müşteri karayolu sevkiyatını seçerse, kullanıcıdan ek navlun ücretleri talep edilmeyecektir. Kullanıcı tüm siparişleri için Hava yöntemini seçerse, toplam değerlerinden bağımsız olarak 20,00$ navlun ücreti talep edilecektir.

#### <a name="setup-and-configuration"></a>Kurulum ve yapılandırma

Bu senaryo, iki otomatik masraf tablosunun yapılandırılmasını gerektirmektedir.

Sırasıyla **Alacak hesapları \> masraflar kurulumu \> Otomatik masraflar** seçimlerini yapın.

İki farklı başlık seviyesi otomatik masrafı yapılandırmak. "Karayolu modu" teslimatı için bir adet ve "Havayolu modu" teslimatı için bir adet yapılandırın. Bu senaryo için, "Tüm müşteriler" için kullanılmak üzere yapılandırın.

Karayolu teslimatı masrafları için **Otomatik masraflar** sayfasının satırlar bölümünde, 0,01$ ve 100$ arasındaki siparişler için uygulanacak masrafı 10,00$ olarak ayarlayın. 100,01$ üzeri siparişler için masraf olmadığını belirtmek üzere başka bir masraf satırı oluşturun.

![Otomatik masraflar örneği](media/headerchargesexample.png)

Hava teslimatı masrafları için otomatik masraflar formunun satırlar bölümünde, tüm siparişlere uygulanacak 20,00$ tutarında bir masraf ayarlayın (0,01$ ve 9.999.999$ arasında değer için).

Değişiklikleri Commerce Scale Unit/Kanalı Veritabanına gönderin böylece POS onları **1040 dağıtım zamanlaması** işini çalıştırırken kullanabilir.

#### <a name="sales-processing-for-this-scenario"></a>Bu senaryo için satış işleme

Yukarıdaki yapılandırma işlemleri tamamlandıktan ve değişiklikler kanal veritabanına uygulandıktan sonra, POS, çağrı merkezi veya e-ticaret kanallarında oluşturulan ve havayolu veya karayolu yöntemlerini başlık seviyesinde uygulanmış olan tüm müşteri siparişleri veya satış hareketleri, bu masrafları otomatik olarak satışa uygulayacaktır.

Şu anda, masraflar bu teslimat modunu kullanan tüzel varlık içindeki tüm satış hareketlerine uygulanacaktır çünkü otomatik masraf yapılandırmasını yalnızca belirli bir satış kanalına uygulanmak üzere atayacak bir işlevsellik mevcut değildir.

POS ve e-ticaret senaryoları için bu siparişler üzerinde net olarak tanımlanmış bir "başlık" olmadığından, başlı düzeyi masrafları yalnızca hareket üzerindeki tüm satış satırları tam olarak aynı teslimat modu ile sevk edilmek üzere ayarlanır. POS veya e-ticaret tarafından oluşturulmuş hareketler üzerinde "karışık modlar" varsa, yalnızca satır düzeyi otomatik masraflar dikkate alınır ve uygulanır.

Çağrı merkezi senaryolarında, kullanıcı teslimat modu ayarları üzerinde sipariş başlığı üzerinde denetime sahip olacaktır, bu nedenle de başlık düzeyi masraflar bu siparişlere bazı sipariş satırları başka bir teslimat modu kullanmak üzere yapılandırılmış bile olsa uygulanacaktır. Çağrı merkezi için başlık düzeyi masrafları her zaman satış siparişinin sipariş başlık düzeyinde tanımlanmış teslimat modunu kullanacaktır.

### <a name="auto-charges-line-charges-example"></a>Otomatik masraflar satır masrafları örneği

#### <a name="use-case-scenario"></a>Kullanımı vakası senaryosu 

Bir perakendeci, müşteri belirli bir bilgisayar modeli sipariş etmek istediğinde müşteri kurulumu ücretlerine ek bir masraf eklemek istemektedir. Bu bilgisayar, perakendecinin müşteri için gerçekleştireceği ek ve isteğe bağlı olmayan kurulum işlemleri içermektedir. Perakendeci, müşteriye bu kurulum için ek ücret söz konusu olacağını bildirmiştir. Perakendeci, bu ücretle ilişkili masrafları finansal raporlama amaçları yüzünden ürün satış fiyatından ayrı olarak yönetmeyi tercih etmektedir. 19,99$ tutarında bir kurulum ücreti, müşteri herhangi bir kanaldan bu belirli bilgisayarı satın alırsa ücretlendirilecektir.

#### <a name="setup-and-configuration"></a>Kurulum ve yapılandırma

Bu senaryo, bir satır düzeyi otomatik masraf tablosunun yapılandırılmasını gerektirmektedir.

Sırasıyla **Alacak Hesapları \> masraflar kurulumu \> Otomatik masraflar** seçimlerini yapın.

**Düzey** açılır menüsünü **Satır** olarak ayarlayın ve kurulum ücretinin uygulanacağı belirli ürün veya ürün grubu için tüm müşteriler için yeni bir otomatik masraf kaydı oluşturun.

![Otomatik masraflar örneği](media/linechargesexample.png)

Değişiklikleri Commerce Scale Unit/Kanalı Veritabanına gönderin böylece POS onları **1040 dağıtım zamanlaması** işini çalıştırırken kullanabilir.

#### <a name="sales-processing-for-this-scenario"></a>Bu senaryo için satış işleme

Yukarıdaki yapılandırma adımları tamamlandıktan ve değişiklikler kanal veritabanına uygulandıktan sonra, bu ögeye siparişte sahip olan tüm POS, çağrı merkezi, e-ticaret kanalı tüm müşteri siparişi veya satışı toplam siparişe sistematik olarak bir satır düzeyi masrafın eklenmesini tetikleyecektir.

Bu noktada, masraflar tüzel varlık içinde otomatik masraf satır düzeyi yapılandırmasında eşleşen tüm satışlara uygulanacaktır, çünkü satır düzeyi otomatik masrafın yalnızca belirli bir satış kanalına uygulanmasını sağlayacak bir işlev mevcut değildir.

### <a name="manual-header-charges-example"></a>El ile başlık masrafları örneği

#### <a name="use-case-scenario-description"></a>Kullanımı vakası açıklaması

Bir perakendeci, mağazadan ürün sipariş eden bir müşteriye özel eve teslim sunmak için tipik işlemlerde bir istisna sunmaktadır. Perakendeci ve müşteri, müşterinin bu hizmet için 25$ işlem ücreti ödemesini kabul etmişlerdir. Siparişi alanın bu ek ücreti işlem eklemesi gerekmektedir. Ücreti, genel ücret olduğundan ve siparişteki tek bir ürünle ilişkili olmadığından bir başlık masrafı uygulanacaktır.

#### <a name="setup-and-configuration"></a>Kurulum ve yapılandırma

Senaryo için uygun masraf konunu tanımlamak için bu senaryoda kullanılacak masraf kodunun, **Alacak Hesapları \> masraflar kurulumu \> masraflar**'e giderek doğru şekilde yapılandırıldığından emin olun.

![masraflar örneği](media/chargesexample.png)

masraf, ilgili indirim veya promosyonlar amacıyla "sevkiyat" ile ilgili masraf olarak dikkate alınacaksa, **Nakliye masrafı**'ni masraflar kodu üzerinde **Evet** olarak ayarlayın Masrafın sistematik olarak iade işlemi sırasında POS uygulamasında sistematik olarak iade edilmesine olanak sağlanıyorsa, **İade edilebilir**'i **Evet** olarak ayarlayın. **İade edilebilir** bayrağı yalnızca **Gelişmiş otomatik masraflar** parametresi **Evet** olarak ayarlanmışsa uygulanabilir.

Değişiklikleri Commerce Scale Unit/Kanalı Veritabanına gönderin böylece POS onları **1040 dağıtım zamanlaması** işini çalıştırırken kullanabilir.

**Masraf başlığı ekle** işleminin [POS ekran düzeninizde](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) yapılandırılmış olması gerekir, böylece kullanıcıya POS üzerinden erişilebilir bir düğme bu işlemi çağırmak (işlem 141) üzere mevcut olacaktır. Ekran düzeni değişiminin kanalına, dağıtım zamanlaması işlevi üzerinden de dağıtılması gerekir.

#### <a name="sales-processing-of-manual-header-charges"></a>El ile başlık masraflarının satış işlemi

Senaryoyu POS uygulamasında gerçekleştirmek için POS kullanıcısının satış hareketini normal biçimde oluşturması, ürünleri ve diğer tüm yapılandırmaları satışa eklemesi gerekecektir. Ödeme almadan önce kullanıcının **Başlık masraf ekle** işlemini gerçekleştirmesi gerekir, bu, kullanıcının bir masraf kodunu seçmesini ve masraf değerini girmesi konusunda uyaracaktır. Kullanıcı işlemi tamamladıktan sonra, masraf satış siparişine bir başlık düzeyi masrafı olarak eklenecektir.

Bu işlem çağrı merkezinde, araç çubuğundaki **Satış** sekmesinde bulunan mevcut **Masraflar** özelliğini kullanarak uygulanabilir. **Masrafları koru** sayfasında, kullanıcı sipariş başlığına yeni masraflar satırı ekleyebilir.

### <a name="manual-line-charges-example"></a>El ile satır giderleri örneği

#### <a name="use-case-scenario"></a>Kullanımı vakası senaryosu

Bir müşteri, satış siparişindeki beş ögeden ikisinin hediye paketi yapılmasını talep etti. Perakendeci, bu isteğe bağlı hizmeti öge başına 2,00$ karşılığında sunmaktadır. Siparişi alanın bu ücretleri, hediye paketi yapılacak belirli öğelere eklemesi gerekecektir.

#### <a name="setup-and-configuration"></a>Kurulum ve yapılandırma

Senaryo için uygun masraf konunu tanımlamak için bu senaryoda kullanılacak masraf kodunun, **Alacak Hesapları \> masraflar kurulumu \> masraflar**'e giderek doğru şekilde yapılandırıldığından emin olun.

Gider, ilgili indirim veya promosyonlar amacıyla "sevkiyat" ile ilgili gider olarak dikkate alınacaksa, **Nakliye gideri**'ni giderler kodu üzerinde **Evet** olarak ayarlayın Masrafın sistematik olarak iade işlemi sırasında POS uygulamasında sistematik olarak iade edilmesine olanak sağlanıyorsa, **İade edilebilir**'i **Evet** olarak ayarlayın. **İade edilebilir** bayrağı yalnızca **Gelişmiş otomatik masraflar** parametresi **Evet** olarak ayarlanmışsa uygulanabilir.

Değişiklikleri Commerce Scale Unit/Kanalı Veritabanına gönderin böylece POS onları **1040 dağıtım zamanlaması** işini çalıştırırken kullanabilir.

**Masraf satırı ekle** işleminin [POS ekran düzeninizde](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) yapılandırılmış olması gerekir, böylece kullanıcıya POS üzerinden erişilebilir bir düğme bu işlemi çağırmak (işlem 140) üzere mevcut olacaktır. Ekran düzeni değişiminin kanalına, dağıtım zamanlaması işlevi üzerinden de dağıtılması gerekir.

#### <a name="sales-processing-of-the-manual-line-charge"></a>El ile satır masrafının satış işlemi

Senaryoyu POS uygulamasında gerçekleştirmek için POS kullanıcısının satış hareketini normal biçimde oluşturması, ürünleri ve diğer tüm yapılandırmaları satışa eklemesi gerekecektir. Ödeme almadan önce kullanıcının masrafın POS ögesi liste görünümünden ekleneceği belirli satırı seçmesi ve **Satır masrafı ekle** işlemini seçmesi gerekir. Kullanıcı, bir masraf kodu seçmek ve masraf değeri girmek üzere uyarılacaktır. Kullanıcı işlemi tamamladıktan sonra, masraf satıra bağlanacaktır ve sipariş toplamına bir satır düzeyi masrafı olarak eklenecektir. Kullanıcı, işlemi ek satır değişikliklerini diğer öge satırlarına işlem üzerine eklemek üzere tekrar edebilir.

Aynı işlem, çağrı merkezinde, **Satış siparişi** sayfasındaki **Satış siparişi satırları** bölümünde bulunan **Finansal** açılır menüsünde "masrafları koru" özelliğini kullanarak uygulanabilir Bu, **Masrafları koru** sayfasını açacaktır, burada kullanıcı işleme belirli bir yeni satır ekleyebilir.

## <a name="additional-features"></a>Ek özellikler

### <a name="editing-charges-on-a-pos-sales-transaction"></a>POS satış işlemindeki masrafları düzenlemek

**Masrafları yönet** işlemi (142), [POS ekran düzenine](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) eklenmelidir, böylece kullanıcı sistem tarafından hesaplanan veya el ile oluşturulan başlık veya satır düzeyi masrafları görüntüleyebilir ve düzenleyebilir. İşlem eklenmezse, kullanıcılar POS hareketindeki masrafların değerini ayarlayamayacaktır ve masrafların türü ve masraf kodu gibi masrafa ilişkin ayrıntıları görüntülemeyecektirler.

POS'taki **Masrafları yönet** sayfasında, kullanıcı hem başlık hem de satır düzeyi ayrıntıları görüntüleyebilir. Kullanıcılar bu sayfada bulunan **Düzenle** işlevini, belirli bir gider satırına uygulanan tutarda değişiklikler yapmak için kullanabilirler. Bir masraf satırı el ile değiştirildikten sonra, kullanıcı **Yeniden hesapla** işlemini başlatmadığı sürece sistematik olarak yeniden hesaplanmayacaktır.

**Masraf geçersiz kılma neden kodu**, kurulum sayfasında **Ticaret parametreleri** içinde yapılandırılmışsa, kullanıcı masraflar POS uygulamasında değiştirilirse bir neden kodu girmek üzere uyarılır.

Neden kodları üzeri yazılan masraflar için yakalanmamışsa, yeni bir rapor da bu geçersiz kılmaları gözden geçirmek ve değerlendirmek için mevcut olacaktır. Bu rapor **Perakende ve Ticaret \> Sorgular ve raporlar \> Geçersiz kılma geçmişi** içinde bulunabilir.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>POS iade hareketinde masrafları iade etmek

**Gelişmiş otomatik masrafları kullan** parametresi **Evet** olarak ayarlanmışsa, **Sevkiyat masraflarını iade et** için mevcut Ticaret parametresi artık uygulanamaz. Hangi masrafların sistematik olarak bir müşteriye gelişmiş otomatik masraflar kullanılırken iade edileceğini belirtmek için ilgili masraf kodları **İade edilebilir** olarak **Masraf kodları** ayar sayfasında yapılandırılmıştır. Ayarların Ticaret kanalı veritabanınıza dağıtım zamanlama işleme üzerinden eşitlenmiş olduğundan emin olun.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Sipariş iade hareketinde masrafları iade etmek

Masraflar sistematik olarak Ticaret içinde oluşturulmuş **İade siparişlerine** iade edilmez. Kullanıcıların **Sipariş iadesi** oluştururken **Masrafları kopyala** seçeneğini seçmesi gerekir. **Masrafları kopyala** seçili değilse, orijinal satış işlemindeki masraflar otomatik olarak iade edilmez. **Masrafları kopyala** seçiliyse, tüm masraflar iade siparişine kopyalanır ve kullanıcı iade edilmesini istemedikleri masrafları el ile düzenleyebilir veya kaldırabilir. Çağrı merkezi iade siparişi işlemi şu anda **Masraf kodları** ayarındaki **İade edilebilir** bayrağını tanımamaktadır.

### <a name="configuring-pos-receipts-to-show-charges"></a>Masrafları göstermek için POS girişlerini yapılandırmak

Aşağıdaki giriş ögeleri giriş satırına ve altbilgisine gelişmiş otomatik masraflar işlevini desteklemek için eklenmiştir.

- **Satır Sevkiyat Masrafları** - Bu satır düzeyi öğesi, satış satırına uygulanan belirli masraf kodlarını özetlemek için kullanılabilir. Yalnızca **Masraf kodları** sayfasındaki **Sevkiyat** masrafı olarak işaretlenmiş masraf kodları burada görüntülenir.
- **Satır Diğer Masrafları** - Bu satır düzeyi öğesi, satış satırına uygulanan sevkiyatla ilgili olmayan belirli masraf kodlarını özetlemek için kullanılabilir. Bunlar, **Masraf kodlar** sayfasındaki **Sevkiyat** bayrağının etkinleştirilmediği masraf kodlarıdır.
- **Sipariş Sevkiyat Masrafları Ayrıntısı** - Bu altbilgi düzeyi öğe, **Masraf kodları** kurulum sayfasında **Sevkiyat** masrafı olarak işaretlenmiş masraf kodlarının açıklamalarını gösterir.
- **Sipariş Sevkiyat Masrafları** - Bu altbilgi düzeyi öğe, sevkiyat ile ilişkili masrafların Dolar cinsinden değerini gösterir.
- **Sipariş Diğer Masrafları Ayrıntısı** - Bu altbilgi düzeyi öğe, Masraf kodları kurulum sayfasında Sevkiyat masrafı değil olarak işaretlenmiş masraf kodlarının açıklamalarını gösterir.
- **Sipariş Diğer Masraflar** - Bu altbilgi düzeyi öğe, sevkiyat ile ilişkili olmayan diğer masrafların dolar değerini gösterir.

Kuruluşun giriş altbilgisine serbest metin alanları eklemesi de önerilir, bu sayede masrafların özetleneceği bölgeler tanımlanır.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Masrafların, POS siparişi tamamlanmadan hesaplanmasını engellemek

Bazı kuruluşlar, masrafları hesaplamadan önce kullanıcının tüm satış satırlarını POS hareketine girmesini beklemeyi tercih etmektedirler. Öğeler POS hareketine eklenirken masraf öğelerinin hesaplanmasını engellemek için **El ile masraf hesaplaması** parametresini mağaza tarafından kullanılan **İşlev profili** içinde kapatın. Bu parametreyi etkinleştirmek, POS kullanıcısının **Toplamları hesapla** işlemini, ürünleri POS hareketine eklemeyi tamamladıklarında kullanmalarını gerektirmesine neden olur. **Toplamları hesapla** işlemi, sipariş başlığı veya satırları için otomatik masrafların hesaplanmasını tetikleyecektir.

### <a name="charges-override-reports"></a>Masraf geçersiz kılma raporları

Kullanıcılar hesaplanan masrafları el ile geçersiz kılarlarsa veya bir el ile masrafı harekete eklerlerse, bu veri **Masraf Geçersiz Kılma Geçmişi** raporunda denetleme için kullanılabilir olur. Bu rapor **Perakende ve Ticaret \> Sorgular ve raporlar \> Geçersiz kılma geçmişi** içinde bulunabilir. Bu rapor için ihtiyaç duyulan verinin kanal veritabanından HQ'ya "P" dağıtım zamanlama işleri üzerinden içe aktarılması gerektiğini unutmayın. Bu nedenle, POS içinde gerçekleştirilen geçersiz kılma hakkındaki bilgiler, bu iş mağaza hareketini HQ'ya karşıya yükleyene kadar bu raporda derhal kullanılabilir olmayabilirler.

## <a name="additional-resources"></a>Ek kaynaklar

[Kanala göre otomatik masrafları etkinleştirme ve yapılandırma](auto-charges-by-channel.md)

[Başlık masraflarını eşleşen satış satırlarına eşit dağıtma](pro-rate-charges-matching-lines.md)

