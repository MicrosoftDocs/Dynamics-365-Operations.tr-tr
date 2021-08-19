---
title: Mağaza sipariş karşılama
description: Bu konu, Mağaza sipariş karşılama konusuna genel bir bakış sağlar.
author: rubencdelgado
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67a0199cd15e0a10b41ed3ab288951f86c9790ba0499fee0754f05876faf4843
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714078"
---
# <a name="store-order-fulfillment"></a>Mağaza sipariş karşılama

[!include [banner](includes/banner.md)]

Birçok satıcı, mağazaların siparişleri karşılamasını sağlayarak sipariş karşılama yeteneğini en iyi duruma getirmek istemektedir. Mağaza seviyesinde sipariş karşılama belirli bir mağazayla ilgili aşırı stok senaryolarını kolay hale getirmeye yardımcı olabilir ve bir mağazanın ekstra kapasitesi olması veya müşteriye daha yakın bir sevkiyat mesafesinde yer alması durumunda lojistik açıdan gerekli olabilir. Bu ihtiyacı karşılamak için, satış noktasında birleştirilmiş sipariş karşılama işlemi bulunmaktadır.

Belirli bir mağaza tarafından karşılanması gereken siparişlerde siparişin başlığında veya satırlarında atanan mağazanın deposu yer alır.

Satış noktasındaki sipariş karşılama işlemi, satış noktasında siparişleri işlemek için kullanılabilecek tek bir çalışma alanı sağlar. Bu siparişin kabul edilmesinden sevk edildi olarak işaretlenmesine veya mağazadan çekme işleminin başlatılmasına kadar tüm aşamaları içerir.

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Satış noktasındaki birleştirilmiş sipariş karşılamaya erişme

Siparişin karşılama, [928 işlem kodu](pos-operations.md), satış noktasında mağaza sipariş karşılama çalışma alanına erişmek için kullanılabilir.

Sipariş karşılama işleminin kullanıma hazır kendi izni bulunmamaktadır ancak kullanıcılar gelecekte işlemi satış noktasından çağırmak için **Sipariş almaya izin ver** iznini kullanabilecektir.

Mağaza seviyesinde, bir sipariş satırının satış noktası içinden el ile kabul edilip edilmemesi gerektiğini belirlemek için kullanılan bir yapılandırma ayarı bulunur. Bu yapılandırma seçeneği ayarlanmazsa, sipariş satırları varsayılan olarak kabul edilir. Bu yapılandırma seçeneği etkinleştirilse, satış noktasındaki kullanıcıların siparişleri satış noktası içinden kabul etmek için **Siparişi kabul etmeye izin ver** iznini kullanması gerekir.

Ayrıca sipariş satırları satış noktasından reddedilebilir. Bir sipariş satırının reddedilmesi, bu satırın mağazada karşılanmayacağı anlamına gelir ve satış satırı başka bir mağazaya veya ambara atanmak üzere geri gönderilir. Sipariş satırını reddetme izni **Siparişi reddetmeye izin ver** izniyle sağlanır.

## <a name="order-fulfillment-operation-parameters"></a>Sipariş karşılama işlemi parametreleri

Sipariş karşılama, satış noktasında çağrıldığında işleme uygulanabilen kullanıma hazır parametreler sağlar. **Tüm siparişler** parametresi yapılandırıldığında, işlem kullanıldığında tüm siparişler gösterilir. **Sevk edilecek siparişler** parametresi, yalnızca mağazadan sevk edilmesi gereken siparişleri gösterir ve **Çekilecek siparişler** mağazadan çekilecek olan siparişleri gösterir.

## <a name="orders-for-fulfillment"></a>Karşılanacak siparişler

Sipariş karşılama işlemi, yalnızca geçerli mağazadan çekilecek olan veya sevk edilecek olan siparişleri gösterir. Sipariş karşılama işlemi kullanıldığında, diğer mağazalar tarafından karşılanacak siparişler listelenmez.

## <a name="line-selection"></a>Satır seçimi

Satırlar Eylem Bölmesindeki **Seç** işlevi kullanılarak seçilebilir. **Seç** seçeneği etkinleştirildiğinde, işlenmek üzere birden fazla satır seçilebilir. Seçili satırları aynı satıra yeniden tıklayarak temizleyebilirsiniz.

## <a name="line-details"></a>Satır ayrıntıları

Satır ayrıntıları satır ayrıntıları açılır menüsü kullanılarak görüntülenebilir. Bu menü kullanıldığında, seçili satır için ek bilgileri görüntülemek üzere üç sekme sağlanır. İlk sekme olan **Satır ayrıntıları**, sipariş edilen ve kalan miktar gibi satırın kendisiyle ilgili ayrıntıları gösterir. Çekilen, paketlenen ve faturalanan miktar ve teslimat şekli ve adresi gibi ek bilgiler sağlanır. **Sipariş ayrıntıları** sekmesi müşteri, müşteri kodu, sipariş numarası, toplam tutar ve bakiye dahil olmak üzere sipariş başlığı bilgilerini gösterir. **Stok** sekmesi, kullanılabilir stok, ayrılmış stok ve sipariş edilen stok cinsinden seçilen satıra ilişkin bilgileri gösterir.

Birden çok satır seçiliyse, sipariş satırı ayrıntıları açılır menüsü yalnızca birden çok satırın seçili olduğunu belirtir. Tek bir satırın ayrıntıları göstermek için, yalnızca tek bir satır kalana kadar satırları temizleyin.

## <a name="pending-order-lines"></a>Beklemedeki sipariş satırları

Birleştirilmiş sipariş karşılama siparişleri el ile kabul etmek özelliği içerir. Varsayılan olarak, mağazada karşılanacak siparişler zaten kabul edilir. Ancak, iş süreçleri mağaza düzeyinde bir çalışanın siparişleri kabul etmesini gerektiriyorsa, perakende mağazası düzeyinde el ile kabul etkinleştirilebilir. Sipariş kabulünü etkinleştirmek için **Perakende ve Ticaret** \> **Kanallar** \> **Mağazalar** \> **Tüm perakende mağazalar** öğesine gidin. İstediğiniz mağazayı açın ve **Genel** sekmesinde **Sipariş karşılama** alt başlığını bulun. Bu alt başlıkta bir **El ile kabul** seçeneği bulunur. Bu seçenek varsayılan olarak **Hayır** olarak ayarlanmıştır. Bu seçeneği **Evet** olarak ayarlayıp değişiklikleri kanal veritabanıyla eşitlediğinizde, sipariş satırları kabul sürecine geçebilir.

**Siparişi kabul etmeye izin ver** iznine sahip olan çalışanlar sipariş karşılamayı açıp satırları kabul etmek üzere seçebilir. Satırlar kabul edildikten sonra durumlar **Beklemede** yerine **Kabul edildi** olarak değişir ve sipariş karşılama işleminin kalan kısmına devam edilebilir. **El ile kabul** açık olduğunda, siparişler kabul edilene kadar işlenmez.

Mağazadan çekilecek siparişlerin durumu hiçbir zaman **Beklemede** olmaz. Bunun nedeni, müşterinin mağaza geldiğinde ilgili ayrıcalığa sahip çalışanın mağazada olmaması nedeniyle sipariş satırının işlenememesi gibi bir senaryoyu önlemektir.

## <a name="accepted-order-lines"></a>Kabul edilen sipariş satırları

Satır durumu **Kabul edildi** olan siparişler, satış noktasında sipariş karşılama sürecinin kalan kısmı aracılığıyla işlenebilir. Bir sipariş kabul edildikten sonra, sipariş satırıyla ilgili kalan tüm eylemler yerine getirilebilir.

Örneğin, kabul edilmiş bir sipariş satırı seçilebilir ve çekme ve paketleme sürecine gitmeye gerek kalmadan doğrudan çekilebilir.

## <a name="line-actions"></a>Satır eylemleri

### <a name="pick"></a>Malzeme çekme işlemleri

**Çek** eylem kategorisi, sipariş satırlarının raflardan çekilmesine yardımcı olmak amacıyla sağlanır. Çekme eylemi, yalnızca önceden kabul edilmiş olan sipariş satırları üzerinde gerçekleştirilebilir.

**Eylem: Çekme**

- **Neden olduğu POS durumu:** Çekme
- **Neden olduğu arka ofis durumu:** Değişiklik yok

Bir sipariş kabul edildikten sonra, satırlar seçilebilir ve **Çekme** olarak işaretlenebilir. Bir satırı **Çekme** olarak işaretlemek, satırda çekme işinin zaten gerçekleştirildiğini belirtmenin bir yoludur. Bu, iki çalışanın aynı anda aynı sipariş satırlarını çekmeye çalışmasını engeller.

**Eylem: Malzeme çekme listesini yazdır**

- **Neden olduğu durum:** Çekme
- **Neden olduğu arka ofis durumu:** Değişiklik yok

Malzeme çekme listeleri, çalışanların çekme işlemini gerçekleştirmesine yardımcı olmak üzere satış noktasında yazdırılabilir. Yazdırılan bir malzeme çekme listesi çekme işlemini gerçekleştiren çalışanın yanında olabilir ve ürünler çekildikçe çalışan malzeme çekme listesinde ürünleri çekildi olarak işaretleyebilir.

Malzeme çekme listesi biçimi, Commerce'da yapılandırılıp makbuz profiline eklenir. Makbuz profilleri ayarlama hakkında daha fazla bilgi için bkz. [Makbuz şablonları ve yazdırma](receipt-templates-printing.md).

Satırlar seçilir ve bu satırlar için bir malzeme çekme listesi yazdırılırsa, bunlar otomatik olarak **Çekme** durumuyla güncelleştirilir.

**Eylem: Çekildi olarak işaretle**

- **Neden olduğu durum:** Çekildi veya kısmen çekildi
- **Neden olduğu arka ofis durumu:** Çekildi veya kısmen çekildi

Fiziksel çekme işlemi tamamlandıktan sonra satırlar **Çekildi** olarak işaretlenebilir. Bir satırı seçip **Çekildi** olarak işaretlemek, sipariş satırının güncelleştirilmesi için gerçek zamanlı bir çağrı yapar. Satır satış noktasında **Çekildi** olarak işaretlendikten sonra, arka ofis durumu da **Çekildi** olarak güncelleştirilir ve stok hareketleri belirtilen miktarın düşüldüğünü gösterir.

Siparişler zaman içinde işlendiğinde, belirli bir satır için kısmi miktarlar işlenebilir. Bir satır seçiliyse ve **Çekildi olarak işaretle** eylemi gerçekleştirildiyse ve miktar birden büyükse, kullanıcıdan miktar belirtmesi istenir. Çekilecek kalan miktar otomatik olarak doldurulur. Kalan tutardan daha az tutar belirtilirse, satır durumu **Kısmen çekildi** olur. Sipariş satırı arka ofiste güncelleştirildiğinde, kısmen çekildi durumunu da yansıtır ve kullanıcı tarafından girilen miktar stoğu güncelleştirmek için kullanılır.

Bir sipariş satırı yanlışlıkla çekilirse, arka ofiste sipariş satırında çekmeyi iptal et işlemi gerçekleştirilmesi gerekir. Şu anda satış noktasında çekmeyi iptal etme eylemi desteklenmemektedir.

Farklı siparişlerden sipariş satırları seçilebilir ve **Çekme** olarak işaretlenebilir, aynı malzeme çekme listesinde yazdırılabilir veya **Çekildi** olarak işaretlenebilir.

### <a name="pack"></a>Paket

Sipariş satırları sipariş satırı kabul edildikten sonra herhangi bir noktada paketlenebilir.

**Eylem: Sevk irsaliyesini yazdır**

- **Neden olduğu durum:** Paketlendi veya kısmen paketlendi
- **Neden olduğu arka ofis durumu:** Teslim edildi veya kısmen teslim edildi

Bu eylem satırları paketlendi veya kısmen paketlendi olarak işaretler ve sevk irsaliyesini yazdırır. Bir arada paketlenen ürünleri doğrulamak için bir sevk irsaliyesi yazdırılabilir. Sevk irsaliyesi, Commerce'de yapılandırılıp makbuz profiline eklenir. Makbuz profilleri ayarlama hakkında daha fazla bilgi için bkz. [Makbuz şablonları ve yazdırma](receipt-templates-printing.md).

**Eylem: Paketlendi olarak işaretle**

- **Neden olduğu durum:** Paketlendi veya kısmen paketlendi
- **Neden olduğu arka ofis durumu:** Teslim edildi veya kısmen teslim edildi

**Paketlendi olarak işaretle** eylemi, bir sevk irsaliyesi yazdırmadan satırların paketlendiğini belirtmek amacıyla kullanılabilir. Hem **Sevk irsaliyesi yazdır** hem de **Paketlendi olarak işaretle** arka ofiste stok hareketlerine neden olur. Satış noktasındaki paketleme satırları arka ofiste sevk irsaliyesi günlüklerinin oluşturulmasına neden olur.

Bir sipariş satırı hatayla paketlenirse, sevk irsaliyesi günlüğünün arka ofiste düzeltilmesi gerekir.

Yalnızca aynı siparişteki ve aynı teslimat şekline sahip olan satırlar aynı anda paketlenebilir.

Şu anda, mağazada çekme satırlarını **Paketlendi** olarak işaretleme seçeneği devre dışı bırakılmıştır. Bu özellik gelecekteki bir sürümde eklenecektir. Sevk irsaliyesi oluşturma işlemi, sevk irsaliyesi sürecine üçüncü taraf bilgilerinin eklenmesini desteklemek üzere geliştirilecektir.

### <a name="pick-up"></a>Al

Mağazadan çekilecek siparişler, satış noktasında alındıktan sonra doğrudan çekilebilir. Mağazadan çekilen siparişler kabul etme işlemine tabi değildir.

**Eylem: Çekme**

- **Neden olduğu durum:** Faturalandı veya kısmen faturalandı
- **Neden olduğu arka ofis durumu:** Faturalandı veya kısmen faturalandı

Bir satır birleştirilmiş sipariş karşılamadan çekilmek üzere seçildiğinde, tüm sipariş satış noktasına yüklenir ve seçilen satır için tüm miktar işaretlenir. Siparişteki diğer satırlar da satış noktasındaki hareket görünümüne yüklenir ancak miktar sıfır olarak işaretlenir.

Çekilecek satırlar hareket görünümüne yüklendikten sonra, hareket her zamanki gibi ödenebilir.

Çekme aracılığıyla tamamen faturalanan satırlar bundan sonra birleştirilmiş sipariş işlemede gösterilmez. Kısmen çekilen satırlar, tamamen çekilene kadar birleştirilmiş sipariş karşılamada görünmeye devam eder.

Bir satır yanlışlıkla çekilirse, hatayı düzeltmek için iade gerçekleştirilmesi gerekir.

Yalnızca aynı siparişteki ve aynı teslimat şekline sahip olan satırlar aynı anda çekilebilir.

### <a name="shipping"></a>Sevkiyat

Mağazadan sevk edilecek sipariş satırları **Sevk et** eylemi kullanılarak birleştirilmiş sipariş karşılama üzerinden işlenebilir.. El ile sipariş kabulü kanal düzeyinde yapılandırıldıysa, siparişlerin sevkiyattan önce kabul edilmesi gerekir. Bir sipariş satırı kabul edildikten sonra, durumu **Bekleme** veya başka bir durumda olduğunda, satırlar sevk edilebilir.

**Eylem: Sevk et**

- **Neden olduğu durum:** Faturalandı veya kısmen faturalandı
- **Neden olduğu arka ofis durumu:** Faturalandı veya kısmen faturalandı

Birleştirilmiş sipariş karşılamadan sevk edilen satırlar, arka ofisten sipariş doğrudan arka ofisten faturalanıyormuş gibi faturalandırılır. Birleştirilmiş sipariş karşılamadan sevk edilen satırlar hareket görünümüne yüklenmez ve satırlar sevk edildiğinde gerçekleştirilen bir ödeme işlemi yoktur.

Tamamen sevk edilen sipariş satırları artık birleştirilmiş sipariş karşılamada görüntülenmez. Kısmen sevk edilen satırlar, tamamen sevk edilene kadar birleştirilmiş sipariş karşılamada görünmeye devam eder.

Yalnızca aynı siparişteki satırlar aynı anda sevk edilebilir. Aynı siparişteki satırların teslimat şekilleri farklı olsa bile sevkiyat için aynı anda seçilebilirler.

### <a name="reject"></a>Reddet

Satırlar veya kısmi satırlar reddedilebilir. Bu, satırların arka ofisten başka bir mağazaya veya ambara atanmasına olanak tanır. Satırlar yalnızca henüz çekilmemiş veya paketlenmemiş olması durumunda reddedilebilir. Çekilmiş veya paketlenmiş olan bir satırı reddetmek için, arka ofis tarafından bu satırdaki çekme veya paketleme işleminin geri alınması gerekir.

**Eylem: Reddet**

- **Neden olduğu durum:** Reddedildi
- **Neden olduğu arka ofis durumu:** Değişiklik yok

Reddedilen sipariş satırları **Satış siparişi işleme ve sorgulama** çalışma alanından görüntülenebilir. Mağazalardaki reddedilen tüm sipariş satırlarını görüntülemek için çalışma alanında kişi filtresini temizleyin. **Siparişler ve sık kullanılanlar** bölümü altındaki **Reddedilen sipariş satırları** sipariş satırı ayrıntılarını görüntüler. Ayrıca, **Özet** bölümü altındaki **Reddedilen sipariş satırları** düğmesine tıklayarak bir satış siparişi görünümüne gidebilirler. Bu görünüm, bir veya daha fazla reddedilmiş satırı bulunan tüm siparişleri gösterir. Dağıtılan Sipariş Yönetimi (DOM) etkinleştirilirse, reddedilen bu siparişler otomatik olarak karşılama için uygun olan mağazalara atanır ancak bu sipariş satırları el ile de yeniden atanabilir. Bunu yapmak için **Karşılama durumu** **Reddedildi** olarak görünen satırı seçin ve tesisi/ambarı gerektiği gibi değiştirin. **Satırı güncelleştir** açılır menüsünü ve **Karşılama durumunu sıfırla**'yı tıklayarak karşılama durumunu sipariş karşılama ayarına bağlı olarak **Reddedildi** yerine **Kabul edildi** veya **Beklemede** olarak değiştirin. Karşılama durumu sıfırlandıktan sonra, mağaza çalışanları POS'ta sipariş satırlarını görebilir.

## <a name="line-quantity-tracking"></a>Satır miktarını izleme

Birden büyük olan tek bir satır miktarı zaman içinde işlenebilir. Bu, sipariş satırlarında birden çok alt duruma neden olur. Örneğin, bir müteahhittin 500 levha gerektiren bir projesi olması ancak müteahhit için proje süresince bir defada belirli bir miktar çekilmesi veya teslim edilmesi durumunda, aynı anda çekilen, paketlenen ve sevk edilen miktarlar olabilir.

Bir satır her seçildiğinde, satır için kalan tutar, kalan miktarın işleneceğini varsaymak üzere otomatik olarak doldurulur. Yukarıdaki örnekten devam edildiğinde, 200 levhanın zaten çekilmiş ve levhalar için satırın çekme işlemi için seçilmiş olması durumunda, kalan tutar olan 300 miktar kısmına otomatik olarak girilir. Aynı durum, 200 levhanın zaten faturalanmış olması durumunda da geçerlidir. Bu durumda, yalnızca kalan miktar otomatik olarak doldurulur.

Yukarıdaki örnek üzerinden devam edersek, 200 levhanın paketlendi olarak işaretlenmesi ve sevkiyatın seçilmiş olması durumunda, tüm tutar olan 500 otomatik olarak doldurulur. Yalnızca 200 levha sevk edilirse, sistem önceden paketlenen levhaların sevk edileceğini ve paketlenen miktarın düşürüleceğini varsayar. 201 levha sevk edilirse, paketlenen levhalar öncelikle kalan tek levha kalan tutardan düşürülerek düşürülür.

## <a name="line-statuses"></a>Satır durumları

Satış noktasındaki sipariş satırlarının, sipariş satırının durumunu yansıtan çeşitli durumları bulunur. Satış noktasındaki durumlar ile arka ofis her zaman eşleşmez. Sipariş satırı durumu, sipariş karşılama işlemleri kullanılarak satış noktasından görüntülenebilir. Arka ofiste, sipariş satırları sipariş ayrıntılarından görüntülenir. Sipariş ayrıntılarına **Perakende ve Ticaret** \> **Müşteriler** \> **Tüm müşteri siparişleri**'nden erişilebilir. Sipariş ayrıntılarını görmek için **Sipariş kodu**'nu seçin. Sipariş ayrıntılarından **Satış siparişi** sekmesini seçin ve ardından **Görünüm** alt başlığı altından **Ayrıntılı durum**'u seçin.

- **Beklemede** – Bir mağazaya atanan ancak henüz kabul edilmemiş olan sipariş satırlarının durumu satış noktasından görüntülendiğinde **Beklemede** olur. Satış noktasında kabul edilmeyi bekleyen satırların durumu arka ofiste **Sipariş işleniyor** olacaktır.
- **Kabul edildi** – El ile veya otomatik olarak kabul edilen sipariş satırlarının durumu satış noktasından görüntülendiğinde **Kabul edildi** olur. **Kabul edildi** durumunda olan satırlar arka ofiste **Sipariş işleniyor** olarak görüntülenir.
- **Çekme** – Mağaza düzeyinde çekilmekte olan satırların durumu **Çekme** olur. Aynı satırlar arka ofisten görüntülendiğinde durumları **Sipariş işleniyor** olacaktır.
- **Çekildi** ve **Kısmen çekildi** – Satış noktasında çekilmiş veya kısmen çekilmiş olan satırların durumu **Çekildi** veya **Kısmen çekildi** olur. Aynı satırlar arka ofiste de **Çekildi** veya **Kısmen çekildi** olarak görünür.
- **Paketlendi** ve **Kısmen paketlendi** – Satış noktasında paketlenmiş veya kısmen paketlenmiş olan satırların durumu **Paketlendi** veya **Kısmen paketlendi** olur. Aynı satırlar arka ofiste de **Teslim edildi** veya **Kısmen teslim edildi** olarak görünür.
- **Kısmen faturalandı** – Kısmen çekilmiş veya kısmen sevk edilmiş olan satırların durumu satış noktasında ve arka ofiste **Kısmen faturalandı** olacaktır.
- **Faturalandı** – Satış noktasında tamamen faturalanmış olan satırlar artık karşılama için gösterilmez. Arka ofiste söz konusu satırların durumu **Faturalandı** olur.

## <a name="order-fulfillment-filtering"></a>Sipariş karşılama filtreleme

Satış noktasında sipariş karşılama, kullanıcının ihtiyacı olanı bulmasına yardımcı olmak amacıyla filtreleme özelliği içerir. Filtreler, **Satış noktası** ekranının alt kısmındaki Eylem Bölmesinden değiştirilebilir. Varsayılan olarak, işlemin nasıl ayarlandığına bağlı olarak, **Teslimat türü** filtresi uygulanır. İşlem **Tüm siparişler** parametresiyle ayarlanmışsa, bu filtre sipariş karşılamaya erişildiğinde uygulanır. Aynı durum **Mağazadan çekme** ve **Mağazadan sevkiyat** parametreleri için de geçerlidir. Sipariş karşılama görünümüne uygulanabilecek filtreler şunlardır:

- Müşteri numarası
- Müşteri adı
- Müşteri e-postası
- Sipariş numarası
- Teslimat şekli
- Makbuz numarası
- Kanal referansı kodu
- Kaynak mağaza numarası
- Satır durumu
- Oluşturulma tarihi
- Teslimat tarihi
- Giriş tarihi


[!INCLUDE[footer-include](../includes/footer-banner.md)]