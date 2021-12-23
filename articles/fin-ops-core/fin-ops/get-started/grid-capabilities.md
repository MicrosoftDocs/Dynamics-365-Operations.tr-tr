---
title: Kılavuz yetenekleri
description: Bu konu, kılavuz denetiminin çeşitli güçlü özelliklerini açıklamaktadır. Bu özelliklere erişebilmek için yeni ızgara özelliğini etkinleştirmeniz gerekir.
author: jasongre
ms.date: 12/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ba3640cf13fecc54f4cc58cd8996e434cd16cf60
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890892"
---
# <a name="grid-capabilities"></a>Kılavuz yetenekleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Yeni ızgara denetimi, kullanıcı üretkenliğini artırmak, verilerinizin daha ilginç görünümlerini elde etmek ve verilerinize anlamlı bilgiler yüklemek için kullanılabileceğiniz çeşitli yararlı ve güçlü yetenekler sağlar. Bu makalede aşağıdaki yetenekler ele alınıyor: 

-  Toplamların hesaplanması
-  Sistemi önceden hazırlama
-  Matematik ifadelerini değerlendirme 
-  Sekmeli verileri gruplandırma (**Kılavuzlar halinde gruplandırma** özelliğini kullanarak ayrıca etkinleştirilmiştir)
-  Sütunları dondurma
-  Otomatik olarak sütun genişliğine sığdır
-  Uzatılabilir sütunlar

## <a name="calculating-totals"></a>Toplamların hesaplanması
Finance and Operations uygulamalarında kullanıcılar toplamları ızgaralardaki sayısal sütunların alt kısmında görebilme yeteneğine sahiptir. Izgaranın altındaki alt bilgi bölümü bu toplamları gösterir. 

### <a name="showing-the-grid-footer"></a>Kılavuz alt bilgisini gösterme
Finance and Operations uygulamalarda her sekmeli kılavuzun altında altbilgi alanı vardır. Altbilgi, kılavuzda görülen verilerle ilgili değerli bilgileri gösterebilir. Aşağıda bu bilgilerin örnekleri verilmiştir:

- Tablodaki seçili satır sayısı (birden fazla kayıt seçtiğinizde)
- Yapılandırılan sayısal sütunların en altındaki genel toplamlar
- Veri kümesindeki satır sayısı 

Bu alt bilgi varsayılan olarak gizlidir ancak kolayca etkinleştirebilirsiniz. Bir kılavuzun alt bilgisini göstermek için, kılavuz başlığında **Kılavuz seçenekleri** düğmesini seçin ve **Alt bilgiyi göster** seçeneğini belirleyin. Belirli bir ızgara için alt bilgiyi açtıktan sonra, kullanıcı alt bilgiyi gizlemeyi seçene kadar bu ayar hatırlanır. Alt bilgiyi gizlemek için **Kılavuz seçenekleri** menüsünde **Alt bilgiyi gizle**'yi seçin.  

### <a name="specifying-columns-with-totals"></a>Sütunları toplamlarla belirtme
Şu anda hiçbir sütun varsayılan olarak toplamları göstermez. Bunun yerine, bu, ızgaralardaki sütunların genişliklerini ayarlamaya benzer şekilde bir kerelik kurulum faaliyeti olarak görülüyor. Bir sütunun toplamlarını görmek istediğinizi belirttiğinizde, sayfayı bir sonraki ziyaretinizde bu ayar hatırlanır.  

Bir sütunu toplam gösterecek şekilde yapılandırmanın iki yolu vardır: 

- Bir toplam görmek istediğiniz sütuna sağ tıklayın ve **Bu sütunun toplamını al**'ı seçin. Bu eylem üç olayın oluşmasına neden olur:

    1. Altbilgi görünür hale gelir. 
    2. Bu sütunda bir toplam görme tercihiniz kaydedilir. 
    3. Bu sütun ve toplamlarını görmek istediğiniz diğer sütunlar için bir toplam hesaplaması başlatır. Bir toplamı göstermek için gerekli olan zaman, topladığınızdan önce veri kümesinin boyutuna bağlıdır.

- Altbilgi görünür olduktan sonra, toplam görmek istediğiniz sütunun alt bilgi alanında **toplamı göster** 'i seçin. Yapılandırılmış sütun yoksa, **Toplamı göster** düğmesi tüm sayısal sütunlarda görünür. 

    Toplamlar için en az bir sütun yapılandırıldıktan sonra, **Toplamı göster** düğmeleri yalnızca üzerine gelindiği veya odaklanıldığı zaman ortaya çıkacaktır. **Toplamı göster** eylemi, yalnızca bu sütunda bir toplamı görmek için tercihlerinizi kaydeder; böylece, daha sonra sayfaya yapılan ziyaretlerin tercihi uygulanır. Altbilgide, bu durum sütunda görünen bir çizgiyle belirtilir. (Alternatif olarak, veri kümesi yeterince küçükse, toplam olarak derhal gösterilir.)

Bir hata yapar ve artık belirli bir sütundaki toplamı artık görmek istemezseniz, sütuna sağ tıklayın ve **Toplamı gizle**'yi seçin veya bu sütundaki alt bilgide bulunan **Toplamı gizle** düğmesini seçin. Bu tercih, sayfaya ileride yapılacak ziyaretler için de kaydedilecektir. 

### <a name="calculating-totals"></a>Toplamlar hesaplanıyor
Alt bilginin görünür olduğu ve sütunların toplamlar için daha önce yapılandırıldığı bir sayfaya geldiğiniz zaman, toplamlar alt bilgide gösterilebilir veya gösterilmeyebilir. Bu durum sayfadaki veri kümesinin boyutuna bağlıdır. Veri kümesi yeterince küçükse, veri kümesindeki satır sayısıyla birlikte toplamlar otomatik olarak gösterilecektir. Toplamlar için yapılandırdığınız sütunların altındaki alt bilgide tireler varsa, veri kümesi sistemin toplamları hemen gösteremeyeceği kadar büyüktür ve toplamları hesaplamak için belirli bir eylem gerekir. Bunu yapmak için, alt bilgideki **Hesapla** düğmesine tıklayın veya toplamını almak istediğiniz bir sütuna sağ tıklayın ve **Bu sütunun toplamını al**'ı seçin.  

Hesaplama çok uzun sürerse, **İptal** düğmesini seçerek işlemi iptal edebilirsiniz. Ancak bazen veri kümesi toplamları hesaplamak için çok büyük olur (kuruluşunuz tarafından uygulanan bir sınıra göre) ve bunun yerine size verilerinizi daha fazla filtrelemeniz gerektiği bildirilir.

Siz veri kümesinde güncelleştirme, silme veya satır oluşturma işlemleri yaptıkça toplamlar otomatik olarak güncelleştirilir.  

## <a name="typing-ahead-of-the-system"></a>Sistemi önceden hazırlama
Birçok iş senaryosunda, sisteme verileri hızlı şekilde girebilme çok önemlidir. Yeni kılavuz denetimi tanıtılmadan önce, kullanıcılar yalnızca geçerli satırdaki verileri değiştirebiliyordu. Yeni bir satır oluşturmadan veya farklı bir satıra geçiş yapmadan önce, sistemin herhangi bir değişikliği başarıyla doğrulamasını beklemek zorundaydılar. Kullanıcıların bu doğrulamaların tamamlanmasını beklediği süreyi azaltmak ve kullanıcı üretkenliğini artırmak için, yeni kılavuz bu doğrulamaları zaman uyumsuz olacak şekilde ayarlıyor. Bu nedenle, kullanıcı önceki satır doğrulamaları beklenirken değişiklik yapmak için diğer satırlara geçebiliyor. 

Bu yeni davranışı desteklemek için, satır seçim sütunu düzenleme modundayken, satır durumu için yeni bir sütun kılavuzun en sağına eklenir. Bu sütun aşağıdaki durumlardan birini gösterir:

- **Boş** – Herhangi bir durum görüntüsü satırın sistem tarafından başarıyla kaydedildiğini göstermez.
- **İşlem beklemede** – Bu durum, satırdaki değişikliklerin sunucu tarafından henüz kaydedilmediğini, ancak işlenmesi gereken değişiklikler sırasında olduğunu gösterir. Kılavuzun dışında bir eylem gerçekleştirmeden önce, bekleyen tüm değişikliklerin işlenmesi için beklemeniz gerekir. Ek olarak, bu satırlardaki metinler, satırların kaydedilmemiş durumunu gösterecek şekilde italik yapılır. 
- **Geçersiz durum** – Bu durum, satırın işlenmesi sırasında bazı uyarı veya iletinin tetiklenmesini ve sistemin bu satırdaki değişiklikleri kaydetmesini engellemiş olabileceğini gösterir. Eski kılavuzda, kaydetme işlemi başarısızsa sorunu hemen düzeltmek için satıra geri dönmeniz gerekiyordu. Ancak, yeni kılavuzda bir doğrulama sorunuyla karşılaşıldığı size bildirilir, ancak satırdaki sorunları ne zaman düzeltmek istediğinize karar verebilirsiniz. Sorunu düzeltmeye hazır olduğunuzda, odağı yeniden el ile satıra taşıyabilirsiniz. Alternatif olarak, **Bu sorunu düzelt** eylemini seçebilirsiniz. Bu eylem, odağı hemen sorunun bulunduğu satıra geri taşır ve kılavuzun içinde veya dışında düzenlemeler yapmanıza olanak sağlar. Bu doğrulama uyarısı giderilene kadar sonraki bekleyen satırların işlenmesinin durdurulduğunu unutmayın. 
- **Duraklatıldı** – Bu durum, bir satırın doğrulanması kullanıcı girişi gerektiren bir açılan iletişim kutusunu tetiklediği için işlemin sunucu tarafından duraklatıldığını belirtir. Kullanıcı başka bir satıra veri giriyor olabileceğinden açılır iletişim kutusu o kullanıcıya hemen sunulmayacaktır. Bunun yerine, kullanıcı işlemeyi sürdürmeyi seçtiğinde gösterilecektir. Bu durum, kullanıcıyı durumla ilgili bilgilendiren bir bildirimle birlikte gösterilir. Bildirim, açılır iletişim kutusunu tetikleyecek bir **İşlemeyi sürdür** eylemi içerir.  
    
Kullanıcılar, sunucunun işlediği yerin önüne veri girerken arama eksikliği, denetim düzeyinde doğrulama ve varsayılan değerlerin girişi gibi veri giriş deneyimlerinde bazı aksaklıklarla karşılaşabilirler. Bir değerin bulunması için açılan listeye gereksinim duyan kullanıcıların, sunucunun geçerli satırı yakalamasını beklemeleri önerilir. Sunucu o satırı işlediğinde, denetim düzeyinde doğrulama ve varsayılan değerlerin girişi de gerçekleşir.   

### <a name="pasting-from-excel"></a>Excel'den yapıştırma
Kullanıcılar her zaman Finance and Operations uygulamalarındaki kılavuzlardan Microsoft Excel'e **Excel'e aktar** mekanizmasını kullanarak veri aktarabiliyordu. Ancak, sistemden önce veri girebilme özelliği, yeni kılavuzun Excel'den tablo kopyalanmasına ve onları Finance and Operations uygulamalarında doğrudan ızgaralara yapıştırmasına olanak tanır. Yapıştırma işleminin başlatıldığı kılavuz hücresi kopyalanan tablonun nereye yapıştırılacağını belirler. Şu iki durum dışında, kılavuzun içeriği üzerine kopyalanan tablonun içeriği yazılır:

- Kopyalanan tablodaki sütun sayısı, yapıştırma konumundan başlayarak kılavuzda kalan sütun sayısını aşarsa, kullanıcıya ek sütunların yok sayıldığı bildirilir. 
- Kopyalanan tablodaki satır sayısı, yapıştırma konumundan başlayarak kılavuzdaki satır sayısını aşarsa, yapıştırılan içerik için varolan hücrelerin üzerine yazılır ve kopyalanan tablodaki tüm ek satırlar kılavuzun en altına yeni satırlar olarak eklenir. 

## <a name="evaluating-math-expressions"></a>Matematik ifadelerini değerlendirme
Verimlilik rampa olarak, kullanıcılar bir kılavuzdaki sayısal hücrelere matematiksel formüller girebilecek. Bu kullanıcılar, sistem dışındaki bir uygulamada hesaplama yapmaları gerekmez. Örneğin **= 15\*4** girerseniz ve alanın dışına gitmek için **sekme** tuşuna basarsanız, sistem ifadeyi değerlendirir ve alan için **60** değerini kaydeder.

Sistemin bir değeri ifade olarak tanımasını sağlamak için, değeri bir eşittir işaretiyle (**=**) başlatın. Desteklenen işleçler ve söz dizimi hakkında daha fazla bilgi edinmek için bkz. [Desteklenen matematik simgeleri](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Sekmeli verileri gruplandırma
İş kullanıcılarının sıklıkla anlık olarak veri analizi yapmaları gerekir. Bu işlem Microsoft Excel'e veri aktararak ve özet tablolar kullanarak yapılırken, yeni kılavuz denetim özelliğine bağlı olan **Kılavuzlarda gruplandırma** özelliği sayesinde kullanıcılar sekmeli verilerini Finance and Operations uygulamalarında ilginç yollarla düzenleyebilir. Bu özellik **Toplamlar** özelliğini genişlettiği için, **Gruplandırma** da grup düzeyinde alt toplamlar sunarak verilere anlamlı bilgiler yüklemenize olanak sağlar.

Bu özelliği kullanmak için, gruplandırmada kullanmak istediğiniz sütuna sağ tıklayın ve **Bu sütuna göre gruplandır**'ı seçin. Bu eylem, verileri, seçilen sütuna göre sıralar, kılavuzun başına yeni bir **Gruplandırma ölçütü** sütunu ve her grubun başına "üst bilgi satırları" ekler. Bu üst bilgi satırları her grup hakkında aşağıdaki bilgileri sağlar: 
-  Grubun veri değeri 
-  Sütun adı (bu bilgi özellikle birden çok gruplandırma düzeyine sahip olduğunuzda yararlıdır)  
-  Bu gruptaki veri satırlarının sayısı
-  Toplamları gösterecek şekilde yapılandırılan sütunların alt toplamları

[Kayıtlı görünümler](saved-views.md) etkinleştirildiğinde, sayfayı bir sonraki ziyaretinizde hızlı erişim için bir görünümün parçası olarak bu gruplandırma kişiselleştirerek gruplandırılabilir.  

### <a name="multiple-levels-of-grouping"></a>Birden çok gruplandırma düzeyi
Verileri tek bir sütuna göre gruplandırdıktan sonra, istediğiniz sütunda **Bu sütuna göre gruplandır**'ı seçerek verileri farklı bir sütuna göre gruplandırabilirsiniz. Bu işlem, iç içe geçmiş 5 gruplandırma düzeyine sahip oluncaya kadar tekrarlanabilir. Bu, desteklenen derinlik üst sınırıdır. Bu aşamada, ek sütunlara göre gruplandırma yapamazsınız.  

Dilediğiniz zaman, bir sütuna sağ tıklayıp **Grubu Çöz**'ü seçerek söz konusu sütundaki gruplandırmayı kaldırabilirsiniz. Ayrıca, **Izgara seçenekleri**'ni ve ardından **Tümünün grubunu çöz**'ü seçerek tüm sütunlardaki gruplandırmayı kaldırabilirsiniz.   

### <a name="expanding-and-collapsing-groups"></a>Grupları genişletme ve daraltma
Verilerin ilk gruplandırmasında tüm gruplar genişletilmiş olacaktır. Tek grupları daraltarak verilerin özetlenmiş görünümlerini oluşturabilir veya verilerde gezinmeye yardımcı olması için grup genişletme ve daraltma özelliklerini kullanabilirsiniz. Bir grubu genişletmek veya daraltmak için, ilgili grup üst bilgisi satırında çift ayraç (>) düğmesini seçin. Bireysel grupların genişletme/daraltma durumunun kişiselleştirme bölümünde **kaydedilmeyeceğini** unutmayın.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Grup düzeyinde satır seçme ve seçimi kaldırma
Kılavuzdaki ilk sütunun en üstündeki onay kutusunu seçerek kılavuzdaki tüm satırları seçmeniz (veya seçimini kaldırmanız) için, ilgili grup üst bilgi satırındaki onay kutusunu seçerek bir gruptaki tüm satırları hızlıca seçebilir (veya seçimini kaldırırsınız). Grup üst bilgi satırındaki onay kutusu, tüm satırlar seçili, hiçbir satır seçilmemiş veya yalnızca bazıları seçili olsa bile, bu gruptaki satırların geçerli seçim durumunu her zaman yansıtır.

### <a name="hiding-column-names"></a>Sütun adlarını gizleme
Veriler gruplandırılırken, varsayılan davranış sütun adını grup başlık satırında göstermektir. **Izgara seçenekleri** > **Grup sütun adını gizle** seçeneğini belirleyerek grup üst bilgisi satırlarında sütun adını gizlemeyi seçebilirsiniz.

### <a name="grouping-on-date-and-time-columns"></a>Tarih ve saat sütunlarında gruplandırma
10.0.24 sürümünden itibaren, Tarih veya Tarih Saat alanları için yıl, ay veya güne göre gruplandırma seçeneği eklendi. İlgili başlık satırı içindeki "değer" grubu, o alandaki biçimle eşleşir. Ayrıca, Tarih Saat ve Saat alanları için saat, dakika veya saniye olarak gruplandırma olanağınız da olacaktır.    

## <a name="freezing-columns"></a>Sütunları dondurma
Izgaradaki bazı sütunlar, bağlam açısından görünümün dışında kalmalarını istemeyeceğiniz kadar önemli olabilir. Bunun yerine, bu sütunlardaki değerlerin her zaman görünür olmasını isteyebilirsiniz. **Izgaradaki sütunları dondur** özelliği kullanıcılara bu esnekliği sağlar. 

Bir sütunu dondurmak için sütunun üst bilgisine sağ tıklayın ve **Sütunu dondur**'u seçin. Bu adımı ilk kez tamamladığınızda, seçili sütun ilk sütun olur ve artık görünümden kaymaz. Dondurulan sonraki sütunlar son dondurulmuş sütunun sağına eklenir. Dondurulmuş sütunları gereken şekilde yeniden sıralamak için standart taşıma işlevini kullanabilirsiniz. Ancak, dondurulmuş sütunlar, dondurulmamış sütunlar kümesi arasında görünecek şekilde taşınamaz. Benzer şekilde, dondurulmamış sütunlar, dondurulmuş sütunlar kümesi arasında görünecek şekilde taşınamaz.

Bir sütunu çözmek için donmuş sütunun üst bilgisine sağ tıklayın ve **Sütunu çöz**'ü seçin. 

Yeni ızgaradaki satır seçimi ve satır durumu sütunlarının, her zaman ilk iki sütun olarak dondurulduğunu unutmayın. Bu nedenle, bu sütunlar bir ızgaraya dahil edildiğinde, kılavuzdaki yatay kaydırma konumundan bağımsız olarak her zaman kullanıcılar tarafından görülecektir. Bu iki sütun yeniden sıralanamaz.

## <a name="autofit-column-width"></a>Otomatik olarak sütun genişliğine sığdır
Excel'e benzer şekilde, kullanıcılar bir sütunu o sütunda o anda gösterilen içeriğe göre yeniden boyutlandırmaya otomatik olarak zorlayabilir. Bunu yapmak için, sütundaki boyutlandırma tutamaçlarını çift tıklatın veya odağı sütun başlığına yerleştirin ve **A**'ya basın (otomatik sığdırma için). Bu özellik 10.0.23 sürümünden itibaren sunulmaktadır.  

## <a name="frequently-asked-questions"></a>Sık sorulan sorular
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Yeni kılavuz denetimini ortamımda nasıl etkinleştirebilirim? 

**Yeni kılavuz denetimi** özelliği, herhangi bir ortamda doğrudan Özellik yönetiminde kullanılabilir. Özellik yönetiminde özelliği etkinleştirdikten sonra, sonraki tüm kullanıcı oturumları yeni ızgara denetimini kullanır. 

Bu özellik, 10.0.21 sürümünden itibaren varsayılan olarak etkinleştirilir ve sürüm 10.0.25 ile zorunlu hale gelmesini hedeflenmiştir. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Geliştirici] Ayrı sayfalar için yeni ızgarayı kullanmayı devre dışı bırakma 
Kuruluşunuz yeni kılavuzla ilgili bazı sorunlar içeren bir sayfayı saptadığı zaman, tek bir formun, sistemin geri kalanında yeni kılavuz denetimiyle yararlanmaya devam ederken, eski kılavuz denetimini kullanmasına izin veren bir API kullanılabilir. Ayrı bir sayfayı yeni kılavuzdan geri çevirmek için forma ait `run()` yöntemine aşağıdaki `super()` çağrı gönderisini ekleyin.

 ```this.forceLegacyGrid();```

Bu API şu anda Nisan 2022 için hedeflenen yeni ızgara denetimi zorunlu olana kadar kabul edilecektir. Herhangi bir sorun bu API'nin kullanılmasını gerektiriyorsa, bunları Microsoft'a bildirin.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Daha önce ızgarayı devre dışı bıraktıktan sonra bir sayfayı yeni ızgarayı kullanmaya zorlama
Yeni ızgaranın tek bir sayfada kullanılmamasını seçtiyseniz ilgili sorunlar çözüldükten sonra yeni ızgarayı yeniden etkileştirmek isteyebilirsiniz. Bunu yapmak üzere `forceLegacyGrid()` için çağrıyı kaldırmanız gerekir. Değişiklik, aşağıdakilerden biri gerçekleşene kadar etkili olmaz:

- **Ortam yeniden dağıtımı**: Ortam güncelleştirilip yeniden dağıtıldığında yeni ızgaranın devre dışı bırakıldığı sayfaları depolayan tablo (FormControlReactGridState) otomatik olarak temizlenir.

- **Tabloyu el ile temizleme**: Geliştirme senaryoları için FormControlReactGridState tablosunu temizlemek üzere SQL kullanmanız ve ardından AOS'u yeniden başlatmanız gerekir. Bu eylem birleşimi, yeni ızgaranın kullanım dışı bırakıldığı sayfaların önbelleğe alınmasını sıfırlar.  

## <a name="developer-size-to-available-width-columns"></a>[Geliştirici] Boyutlandırılabilir sütunlar
Bir geliştirici yeni kılavuzun içindeki sütunlar için **WidthMode** özelliğini **SizeToAvailable** olarak ayarladığında, bu sütunlar, özelliğin **SizeToContent** olarak ayarlanmış olması durumunda, ilk başta sahip olacakları aynı genişliğe sahip olurlar. Ancak, kılavuzun içinde kullanılabilen ek bir genişliği kullanmak için genişler. Özellik birden çok sütun için **SizeToAvailable** olarak ayarlandıysa, tüm bu sütunlar kılavuzun içinde kullanılabilir olan ek bir genişliği paylaşır. Ancak, bir kullanıcı bu sütunlardan birini el ile yeniden boyutlandırırsa, sütun statik hale gelir. Bu genişlikte kalacak ve artık fazladan kullanılabilir kılavuz genişliği kaplamayacak şekilde genişlemeyecek.  

## <a name="known-issues"></a>Bilinen sorunlar
Bu bölüm, yeni ızgara denetimiyle ilgili bilinen sorunların listesini içerir.  

### <a name="open-issues"></a>Açık sorunlar
-  **Yeni kılavuz denetimi** özelliğini etkinleştirdikten sonra, bazı sayfalar varolan kılavuz denetimini kullanmaya devam eder. Bu, aşağıdaki durumlarda ortaya çıkar:  
    -  Çoklu sütunlarda işlenen sayfada bir kart listesi vardır.
    -  Sayfada gruplanmış bir kart listesi vardır.
    -  Tepki olmayan genişletilebilir bir denetimi olan kılavuz sütunu.

    Bir kullanıcı bu durumlardan biriyle karşılaştığında, sayfayı yenileme hakkında bir ileti görüntülenecektir. Bu ileti görüntülendikten sonra, bir sonraki ürün sürümü güncelleştirilinceye kadar, sayfa tüm kullanıcılar için varolan kılavuzla çalışmaya devam eder. Yeni kılavuzun kullanılabilmesi amacıyla gelecekteki bir güncelleştirme için bu senaryoların daha iyi işlenmesi dikkate alınacaktır.    
    
-  [KB 4582758] Yakınlaştırmayı 100'den başka bir yüzdeye değiştirdiğinizde kayıtlar bulanıklaşır
-  [KB 4592012] Excel'den birden çok satır yapıştırırken IE11 içinde beklenmeyen istemci hatası
    -  Microsoft bu sorun için bir düzeltme aramamaktadır

### <a name="fixed-as-part-of-10016"></a>10.0.16'nin parçası olarak düzeltildi

-  [KB 4598335] Çok satırlı dize denetimleri listelerde/kartlarda DisplayHeights öğelerine uymuyor 
-  [KB 4591891] Satırların işaretleri kaldırılırken fatura teklifi satırları kayboluyor
-  [KB 4592104] "Sorunu düzelt"i tıkladıktan ve doğrulama sorununu düzeltmeden bir sonraki satıra geçtikten sonra kayıtlar düzenlenemiyor
-  [KB 4594449] Tarih seçicide "Asla" ve "Temizle" düğmeleri eksik 
-  [KB 4594448] Saati girme işlemi yeni ızgarada farklı ele alınıyor
-  [KB 4600059] E-posta azaltmayla ilgili beklenmeyen istemci hatası
-  [KB 4574584] Makbuz simgesi üzerine gelindiğinde gider eki önizlemesi kullanılamıyor

### <a name="fixed-as-part-of-10015"></a>10.0.15'nin parçası olarak düzeltildi    

-  (Kalite güncelleştirmesi) [KB 4594444] Bölümlenmiş girdi denetimi için önizlemeyle ilgili beklenmeyen istemci hatası
-  [KB 4582723] Form yaşam döngüsünde daha sonra yapıldığında görüntüleme seçenekleri gösterilmiyor
-  [KB 4591988] ReferenceGroup aramasından değer seçmek için klavyeyi kullanmayla ilgili sorunlar
-  [KB 4588958] Regression Suite Automation Tool (RSAT) testi şu hatayı vererek başarısız oluyor: TypeError: Tanımsız "metin" özelliği okunamıyor
-  [KB 4591970] Excel'den yapıştırma işlemi ızgaraya tıkladıktan hemen sonra yapıldığında beklenmeyen istemci hatası
-  [KB 4591904] Kullanıcı bir denetimi düzenledikten hemen sonra farklı bir denetimin aramasına tıklayıp açarsa veri değişiklikleri kaydedilmiyor
-  [KB 4584752] Proje faturası teklifleri sayfasında beklenmeyen istemci hatası
-  [KB 4584540] Bir günlük satırına tek bir satır yapıştırılırken kılavuzda ayrılamama
-  [KB 4591908] Yeni bir satır oluştururken odaklama içinde olduğunuz sütunda kalıyor

### <a name="fixed-as-part-of-10014"></a>10.0.14'nin parçası olarak düzeltildi

-  (Kalite güncelleştirmesi) [KB 4584752] Proje faturası teklifleri sayfasında beklenmeyen istemci hatası
-  [KB 4583880] Regression Suite Automation Tool (RSAT) testi, "Tanımsız RowIndex özelliği okunamıyor" hatasıyla OpenLookup eyleminde başarısız oldu
-  [KB 4583847] Aramalarda gezinirken beklenmedik istemci hatası

### <a name="fixed-as-part-of-10013"></a>10.0.13'nin parçası olarak düzeltildi

-  (Kalite güncelleştirmesi) [KB 4584752] Proje faturası teklifleri sayfasında beklenmeyen istemci hatası
-  [KB 4583880] Regression Suite Automation Tool (RSAT) testi, "Tanımsız RowIndex özelliği okunamıyor" hatasıyla OpenLookup eyleminde başarısız oldu
-  [KB 4583847] Aramalarda gezinirken beklenmedik istemci hatası 
-  (Kalite güncelleştirmesi) [Hata 471777] Bir mobil uygulama düzenlemek veya oluşturmak için ızgaradaki alanlar seçilemiyor
-  [KB 4582727] Kullanıcı birden çok miktarı olan maddeler için iletişim kutusunu gördükten sonra ızgara donuyor
-  [Hata 474851] Referans grup denetimlerindeki köprüler çalışmıyor 
-  [Hata 474848] Kılavuzlarla geliştirilmiş önizlemeler görüntülenmiyor
-  [KB 4582726] RotateSign özelliği dikkate alınmıyor  
-  [Hata 470173] Etkin olmayan satırlardaki onay kutuları hücredeki boşluk tıklandığında geçiş yapıyor
-  [Hata 474848] Kılavuzlarla geliştirilmiş önizlemeler görüntülenmiyor
-  [Hata 474851] Referans grup denetimlerindeki köprüler çalışmıyor 
-  [Hata 471777] Bir mobil uygulama düzenlemek veya oluşturmak için kılavuzdaki alanlar seçilemiyor
-  [KB 4569441] Çok sütunlu kart listeleri, görüntülerdeki araç ipuçları ve bazı alanlardaki görüntüleme seçenekleri ile ilgili sorunlar
-  [KB 4575279] Genel Günlükte işaretlenen satırların tümü silinmiyor
-  [KB 4575233] Görüntü seçenekleri başka bir satıra taşındıktan sonra geri yüklenemiyor
-  [Hata 477884] Yeni bir ızgara denetimi etkinleştirildiğinde aramalar yanlış değer/kayıt döndürüyor
-  [KB 4571095] yanlışlıkla Enter tuşuna basıldığında ürün girişi deftere nakli yapılıyor (bir sayfanın varsayılan eyleminin doğru işlenmesi)
-  [KB 4575437] Düzenlenebilir denetimlerle yapılan aramalar beklenmedik şekilde kapanıyor
-  [KB 4569418] Teslimat çizelgesi formunda tekrarlanan satır oluşturuluyor
-  [KB 4575435] Gelişmiş önizleme bazen fare işaretçisi alanın yakınında olmadığında bile kalıyor
-  [KB 4575434] Alan değiştirildiğinde arama filtrelenmiyor
-  [KB 4575430] Parola alanlarındaki değerler kılavuzda maskelenmiyor
-  [KB 4569438] Tedarikçi hareketleri kapatılırken satırlar işaretlendikten sonra "Bir doğrulama sorunu nedeniyle işlem durduruldu" görüntüleniyor
-  [KB 4569434] Tüzel kişileri yenileme, daha az kayda neden oluyor
-  [KB 4575297] Odak, bir kılavuz üzerinden düzenleme ve sekme geçişi sırasında görev kaydedici bölmesine geçiyor
-  [KB 4566773] Düzeltme hareketleri fiş hareketleri sorgulamasında negatif olarak gösterilmiyor 
-  [KB 4575288] Basit bir listedeki satırlar arasındaki kenarlığı seçerken odak etkin satıra sıfırlanıyor
-  [KB 4575287] Günlüklerde yeni bir satır oluşturmak için aşağı ok kullanılırken odak ilk sütuna dönmüyor
-  [KB 4564819] Serbest metin faturasındaki satırlar silinemiyor (veri kaynağı ChangeGroupMode=ImplicitInnerOuter olduğu için)
-  [KB 4563317] Araç ipuçları/gelişmiş önizlemeler resimler için gösterilmiyor

### <a name="fixed-as-part-of-10012"></a>10.0.12'nin parçası olarak düzeltildi

- [KB 4558545] Tablo denetimleri, görüntülenen öğelerin içeriğini güncelleştirmiyor.
- [KB 4558570] Kayıt silindikten sonra öğeler hala sayfada gösteriliyor.
- [KB 4558572] Liste Paneli **ExtendedStyle** ile ilişkilendirilmiş uygulanmıyor.
- [KB 4558573] Gerekli değişiklik kılavuzun dışında olduğunda doğrulama hataları düzeltilemiyor.
- [KB 4558584] Eksi sayılar doğru işlenmiyor.
- [KB 4560726] Liste görünümü denetimi kullanılarak listeler arasında takas işlemi yapıldıktan sonra "beklenmeyen istemci hatası" oluşur.
- [KB 4562141] Yeni bir kayıt eklendikten sonra kılavuz indisleri kapalıdır.
- [KB 4562151] **Doğrula** ve **Kopyala** görev Kaydedicisi seçenekleri tarih/sayı denetimleri için kullanılamıyor. 
- [KB 4562153] Liste/kart kılavuzlarda çoklu seçim onay kutuları görünmez.
- [KB 4562646] Kılavuzdaki satırları çoklu olarak seçtikten sonra kılavuzun dışına tıklayamıyorsunuz.
- [KB 4562647] Güvenlik rolleri ızgarasına yeni bir satır eklendikten sonra, odak **Yayımla** iletişim kutusundaki ilk denetime sıfırlanır.
- [KB 4563310] Gelişmiş önizleme bir satır değiştirildikten sonra kapatılmadı.
- [KB 4563313] Aramada bir değer seçildiğinde Internet Explorer'da "beklenmeyen istemci hatası" durumu ortaya çıkar .
- [KB 4564557] Aramalar ve açılan menüler Internet Explorer'da açılmıyor
- [KB 4563324] **Personel yönetimi** çalışma alanı açıldıktan sonra gezinme çalışmaz.

### <a name="fixed-as-part-of-10011"></a>10.0.11'nin parçası olarak düzeltildi

- [Sorun 432458] Boş veya yinelenen satırlar bazı alt koleksiyonların başlangıcında gösteriliyor.
- [KB 4549711] Yeni kılavuz denetimi etkinleştirildikten sonra ödeme teklifindeki satırlar doğru şekilde kaldırılamıyor.
- [KB 4558374] Çok biçimli seçici iletişim kutusu gerektiren kayıtlar oluşturulamıyor.
- [KB 4558375] Yardım metni yeni kılavuzdaki sütunlarda gösterilmiyor.
- [KB 4558376] Liste Paneli ızgaraları, Internet Explorer'da doğru yükseklikte işlenmiyor.
- [KB 4558377] **SizeToAvailable** genişliği olan birleşik açılan kutu sütunları bazı sayfalarda işlenmiyor.
- [KB 4558378] Detaya gitme bazen yanlış kaydı açıyor.
- [KB 4558379] **ReplaceOnLookup**=**Hayır** olduğunda aramalar açıldığında hata oluşuyor.
- [KB 4558380] Kılavuzdaki kullanılabilir alan, sayfanın bir bölümü daraltıldıktan hemen sonra doldurulmuyor.
- [KB 4558381] Eksi sayılar doğru işlenmiyor / Kullanıcılar bazen doğrulama sorunlarıyla karşılaştıktan sonra takılıyor.
- [KB 4558382] Beklenmeyen istemci hataları oluşuyor.
- [KB 4558383] Son kayıt silindikten sonra kılavuzun dışındaki denetimler güncelleştirilemiyor.
- [KB 4558587] Değiştirme alanları için birleşik kutular içeren referans grupları değerleri göstermiyor.
- [KB 4562143] Alanlar satır değişikliğinden sonra güncelleştirilimiyor / Kılavuz işleme satır silme işleminden takılıyor.
- [KB 4562645] Regression Suite Automation Tool (RSAT) testleri çalışırken bir arama açıldığında özel durum oluşur.

### <a name="fixed-as-part-of-10010"></a>10.0.10'un parçası olarak düzeltildi

- [Sorun 414301] Yeni satırlar oluşturulduğunda, önceki satırlardaki veriler kayboluyor.
- [Hata 417044] Liste stili kılavuzlar için boş kılavuz iletisi yok.
- [KB 4539058] Bazı kılavuzlar (genellikle hızlı sekmelerde) bazen işlenmiyor (ancak, uzaklaştırdığınızda işleniyorlar).
- [KB 4549734] İşaretleme sütunu gizli ise, etkin satırlar işaretlenmiş olarak kabul edilmiyor.
- [KB 4549796] Bir kılavuzda görünüm modundayken değerler düzenlenemiyor.
- [KB 4558367] Satırlar değiştiğinde metin seçimi tutarsız.
- [KB 4558368] Tek seçimli senaryolarda klavyeyle çoklu seçim yapılmasına izin veriliyor.
- [KB 4558369] Durum görüntüleri hiyerarşik kılavuzda kayboluyor.
- [KB 4558370] Yeni bir satır görünüme kaydırılmıyor.
- [KB 4558372] Yapıştırıldığı içerikteki sütun sayısı kılavuzdaki kalan sütunların sayısını aşarsa, yeni kılavuz işleme modunda takılıyor.
- [KB 4562631] Zaman değerleri doğru şekilde biçimlendirilmiyor.

### <a name="quality-update-for-1009platform-update-33"></a>10.0.9/Platform güncelleştirmesi 33 için kalite güncelleştirmesi

- [KB 4550367] Zaman değerleri doğru şekilde biçimlendirilmiyor.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
