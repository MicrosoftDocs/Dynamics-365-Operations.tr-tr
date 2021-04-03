---
title: Bakım planları
description: Bu konuda Varlık Yönetimi'ndeki bakım planları açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectType, EntAssetCounterType, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09ae8b0ce56b08db0ba400b19676bd698c90a561
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500826"
---
# <a name="maintenance-plans"></a>Bakım planları

[!include [banner](../../includes/banner.md)]

Bakım planı, bir varlık üzerinde önceden planlı bir önleyici bakım işinin gerçekleştirilme zamanını tanımlar. Bakım planları; varlıklar, varlık türleri, işlem yapılacak yerleşimler veya işlem yapılacak yerleşim türleriyle ilgili olabilir ancak önce şirketinizde kullanılacak bakım planları oluşturursunuz.

Bakım planında birden çok bakım planı satırı olabilir. Bakım işi türü ve aralığı, bakım planı satırında belirtilir. İki tür bakım planı satırı vardır:

- Zaman
- Sayaç

"Zaman" türündeki bakım planı satırları, sabit zaman aralıklarına bağlı olarak planlı bakımı yinelemek için kullanılır. "Sayaç" türündeki bakım planı satırları, varlık sayacı kayıtlarına bağlı olarak planlı bakım veya reaktif bakım için kullanılır. Bakım planı, iki türdeki birkaç bakım planı satırını içerebilir.

>[!NOTE]
>Varlıktaki sayaç türü için sayaç değerleri kaydedilmediyse bakım planı satırları atlanır.

İlk olarak, önleyici bakım işleriniz için gerekli bakım planlarını oluşturur ve her bakım planıyla ilgili olması gereken varlık türlerini, varlıkları, işlem yapılacak yerleşim türlerini ve işlem yapılacak yerleşimleri seçersiniz. Daha sonra, gerekirse **Tüm kıymetler** \> kıymet seç \> **Kıymet bakım planları** hızlı sekmesinde veya **Tüm işlem yapılacak yerleşimler** \> işlem yapılacak yerleşim seç \> **Bakım planları** hızlı sekmesinde yapılacak şekilde kıymet ya da işlem yapılacak yerleşime bakım planları ekleyebilirsiniz.

Varlık türlerine veya işlem yapılacak yerleşim türlerine bakım planı eklerseniz bu, bu varlık türleri veya işlem yapılacak yerleşim türleriyle yeni varlık ya da işlem yapılacak yerleşim oluşturduğunuzda varlık veya işlem yapılacak yerleşimin bakım planına otomatik olarak ekleneceği anlamına gelir. Bakım planıyla ilgili başlangıç tarihi, ayarlanması gerekebilen geçerli tarih olur.

## <a name="set-up-maintenance-plans"></a>Bakım planlarını ayarla

Bu bölümde bakım planı satırlarının nasıl ayarlanacağı açıklanmakta ve kullanılabildikleri örnekler sağlanmaktadır.

1. **Kıymet yönetimi \> Kurulum \> Önleyici bakım \> Bakım planları**'na gidin.

1. Yeni bir sıralama oluşturmak için **Yeni**'yi seçin.

1. **Bakım sırası** alanına bir kimlik ve **Ad** alanına bir ad ekleyin.

1. **Plan tarihi** alanına bakım planında planlamanın yapılabileceği başlangıç tarihini ekleyin. Zaman temelli bakım planı satırlarının diğer plan tarihlerine sahip olabildiğini unutmayın.

1. Bakım planını etkinleştirmek için **Etkin** geçiş düğmesinde "Evet"i seçin.

    >[!NOTE]
    >Bakım planını devre dışı bırakırsanız bir zamanlama bakım planı işi çalıştırdığınızda bakım zamanlamasında zamanlama gönderileri oluşturulmaz.

1. **Önceki tolerans günleri** ve **Sonraki tolerans günleri** alanları, **Çakışan bakım işlerini gizle** onay kutusunun seçildiği bakım planı satırlarıyla ilgilidir (17. adıma başvurun). "Tolerans" alanları, birkaç bakım planı çakışırsa bakım planı zamanlaması sırasında en kapsamlı / en büyük işin bakım zamanlaması satırı olarak oluşturulduğu ve ayrıca bakım planı zamanlaması sırasında en sık çakışan işlerin atlandığı durumda gün cinsinden aralığı genişletmek için kullanılır. **Önceki tolerans günleri** alanına gün sayısını, örneğin "2" girin.

1. **Önceki tolerans günleri**'ne değer girdiyseniz **Sonraki tolerans günleri** alanına da gün sayısını, örneğin "2" ekleyin.

    >[!NOTE]
    >Bunda ve önceki adımda açıklanan örnek, birkaç bakım planı satırı çakışırsa ve **Çakışan bakım işlerini gizle** bir veya birden çok satır için seçilirse bakım zamanlaması satırlarının atlanması döneminin toplam beş güne (bakım zamanlaması satırında beklenen başlangıç tarihi *ve* bu tarihten iki gün önce *ve* iki gün sonra) genişletileceği anlamına gelir.

1. **Ayrıntılar** hızlı sekmesinde **Ayrıntılar** grubundaki alanlar, bakım planında ayarlanan bakım planı satırlarının sayısını ve bakım planıyla ilgili varlık ve işlem yapılacak yerleşim sayısını gösterir.

1. **Satırlar** hızlı sekmesinde yeni bakım planı satırı oluşturmak için **Zaman satırı ekle**'yi veya **Varlık sayaç satırı ekle**'yi seçin.

1. **İş emri açıklaması** alanına satır için açıklama ekleyin. Açıklama, ilgili iş emirlerine transfer edilir.

1. **Bakım işi türü** alanında bakım planı satırının ilgili olduğu iş türünü seçin.

1. **Bakım işi türü çeşidi** ve **Ticaret** alanlarında bakım işi türüyle ilgili çeşidi ve ticareti seçin.

1. **Günler içinde bitirin** ve **Saatler içinde bitirin** alanlarına gün veya saat cinsinden beklenen bitiş tarihini ekleyebilirsiniz. Beklenen bitiş tarihi, bakım zamanlaması satırları oluşturulduğunda hesaplanan beklenen başlangıç tarihiyle ilgili olarak eklenir. Örneğin, ilgili işin beklenen başlangıç tarihinden itibaren bir hafta içinde tamamlanması gerektiğini belirtecek şekilde **Günler içinde bitir** alanına "7" ekleyebilirsiniz.

1. **Aralık türü** alanında bakım planı satırında kullanılacak aralık türünü, örneğin "Yinelenen" veya "Bir kez"i seçin. Aralık türleri ve satır türleri arasındaki ilişkinin açıklaması için aşağıdaki [Aralık türleri özeti](#interval-types) tablosuna başvurun.

1. **Dönem** alanı yalnızca zaman temelli satır türleriyle ilgilidir. Dönem sıklığıyla ilgili dönem türünü seçin.

1. **Dönem sıklığı** alanına satırın önleyici bakım işlerini planlamak için kullanılması gereken zaman sayısını ekleyin. Örnek: "Sayaç" türünde bir satır oluşturduysanız ve sayacınız üretim miktarıysa ve bu alana "20000" sayısını eklerseniz önleyici bakım zamanlaması sırasında sizden 20.000 daha fazla madde üretmenizin beklendiği her defasında yeni bakım sırası satırları oluşturulur.

1. **Çakışan bakım işlerini gizle** onay kutusu, zaman temelli ve sayaç temelli satır türleriyle ilgilidir. Aynı tarihte oluşturulan bakım zamanlaması girişlerini silmek için onay kutusunu seçin. Bu, örneğin 1 aylık inceleme satırı, 6 aylık inceleme satırı ve 1 yıllık inceleme satırı oluşturmanız durumunda ilgilidir. 1 yıllık inceleme için zaman aralığına sığacak diğer iki incelemenin değil, yalnızca bu incelemenin yapılmasını istersiniz. Bu örneği doğru şekilde ayarlamak için 1 yıllık inceleme satırını ilk satır olarak, 6 aylık satırı ikinci satır olarak ve 1 aylık satırı üçüncü satır olarak ayarlarsınız ve 1 aylık ve 6 aylık satırlar için **Çakışan bakım işlerini gizle** onay kutusunu seçersiniz. Bu şekilde 1 yıllık işaretine ulaştığınızda bir ay ve altı ay için incelemelerin atlanmasını ve bakım zamanlaması satırının yalnızca 1 yıllık inceleme satırı için oluşturulmasını sağlarsınız.

    >[!NOTE]
    >Bu adımda açıklanan örnek, en fazla görev sayısı içeren ve bu kadar sıklıkla yapılmayan en kapsamlı işin her zaman ilk satır olarak eklenmesi gerektiğini gösterir. Daha sonra daha sık işler, en sık iş listenin alt kısmına yerleştirilecek şekilde sıklık sırasında ayrı satırlar olarak eklenir.

1. **Sayaç** alanı yalnızca sayaç temelli satır türleriyle ilgilidir. Satırda kullanılacak sayaç türünü seçin. Sayaç türü ilgili varlıkta etkin değilse bakım planı satırı atlanır.

1. **Gün cinsinden varlık sayacı zaman dilimi** alanı yalnızca sayaç temelli satır türleriyle ilgilidir. Bakım planı zamanlaması tamamlandığında sayaç kayıtlarının denetleneceği geriye doğru kaç gün olduğunu tanımlayan sayıyı ekleyin. Bu, kaç bakım zamanlaması satırının oluşturulduğunu belirleyen eğilimi hesaplamak için esas olarak kullanılan verilerin (var olan sayaç kayıtları) kaç gün öncesine uzandığı anlamına gelir.

    >*Örnek:* Sayaç kayıtlarının ayda bir kez yapılması bekleniyorsa bakım planı zamanlaması her zaman son 12 aya dayandığından bu alana '365' sayısını ekleyebilir ve böylece geçen yılın eğilimine bağlı olarak bakım zamanlaması satırları oluşturabilirsiniz. Diğer taraftan, bu alana '10' sayısını eklerseniz sayaç kayıtlarının daha sık, örneğin günlük olarak yapılmasını beklersiniz. Bu, bakım planı zamanladığınızda son 10 gün için sayaç kayıtlarının bakım zamanlaması satırlarının zamanlaması için esas olarak kullanıldığı anlamına gelir.

1. **Plan tarihi** alanı yalnızca zaman temelli satır türleriyle ilgilidir. Bakım planı satırı tüm bakım planından farklı planlama tarihine sahipse satırda **Plan tarihi** alanında bir tarih seçin.

1. **Servis düzeyi** alanında iş emirlerinde servis düzeyi olarak kullanılmak üzere bakım planı satırında daha fazla sınırlandırma olarak bir iş emri servis düzeyi seçebilirsiniz.

1. Bakım planları zamanlarken seçilen bakım planı satırına göre iş emrini otomatik olarak oluşturmak isterseniz **Otomatik oluştur** onay kutusunu seçin.

1. **Otomatik oluştur** onay kutusunu seçerseniz otomatik oluşturulan iş emri için **İş emri türü** alanında iş emri türü seçebilirsiniz. **Otomatik oluştur** onay kutusunu seçerseniz ve bu alanda iş emri türü seçmezseniz **Kıymet yönetimi \> Kurulum \> Kıymet yönetimi parametreleri \> İş emirleri** bağlantısı \> **Önleyici iş emri türü** alanında seçilen iş emri türü kullanılır.

1. 12 aylık dönem içinde yinelenen zaman temelli bakım planı satırı oluşturmak için **Mevsim başlangıcı** ve **Mevsim bitişi** alanlarını kullanın. *Örnek:* Yeşil alanları korumak için kullanılan ekipman için önceden tanımlanan dönem içindeki her ilkbaharda servis gerekir. Yinelenecek dönemin başlangıç tarihini **Mevsim başlangıcı** alanına girin.

1. Yinelenecek dönemin bitiş tarihini **Mevsim bitişi** alanına girin.

1. **Sonuçta oluşan dönem** alanında yinelenecek geçerli dönem gösterilir. Geçerli dönem geçtiğinde ve yeni bir yıl başlattığınızda bu alanda gösterilen dönem, yineleme sırasındaki sonraki dönemi yansıtacak şekilde güncelleştirilir.

1. **Varlıklar** hızlı sekmesinde bakım planıyla ilişkili olması gereken varlıkları seçin.

1. **Varlık türleri** hızlı sekmesinde bakım planıyla ilişkili olması gereken varlık türlerini seçin.

1. **İşlem yapılacak yerleşimler** hızlı sekmesinde bakım planıyla ilişkili olması gereken işlem yapılacak yerleşimleri seçin. Gerekirse ilgili varlık türü, üretici ve model seçerek kurulumu daha özel hale getirebilirsiniz.

1. **İşlem yapılacak yerleşim türleri** hızlı sekmesinde bakım planıyla ilişkili olması gereken işlem yapılacak yerleşim türlerini seçin.

>[!NOTE]
>İş emirleri satıcı garantisi ile kapsanan varlıklarda el ile oluşturulduğunda kullanıcının garantiden haberdar olmasını sağlamak için bir iletişim kutusu gösterilir. İş emrinin oluşturulması daha sonra iptal edilebilir. Otomatik olarak oluşturulan iş emirleri için garanti ilişkisi denetimi atlanır.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Aralık türlerine genel bakış

| Aralık türü ve açıklaması | Satır Türü: Zaman | Satır Türü: Sayaç |
|---|---|---|
| **Aralık türü: Plan tarihinden itibaren yinelenen** Sayım, kullanılan plan tarihinden başlar. Bakım planlarını zamanladığınızda aralığa ulaşıldığında bakım zamanlaması satırları oluşturulur. | Bakım planı satırındaki **Plan tarihi** kullanılır. Satırda plan tarihi seçilmezse bakım planı için **Plan tarihi** kullanılır. Örnek: **Dönem sıklığı** alanına "3" sayısı eklenirse ve **Dönem** alanında "Yıl" seçilirse 3 yılda bir yeni dönem zamanlaması satırı oluşturulur. | Bakım planı için **Plan tarihi** kullanılır. Sayaç değiştirilirse en son değiştirme tarihi plan tarihi olarak kullanılır. |
| **Aralık türü: Başlangıç tarihinden itibaren yinelenen** Sayım, varlık ilişkisindeki başlangıç tarihinden başlar. Tarih, **Tüm kıymet** ayrıntıları görünümü \> **Kıymet yönetimi planları** hızlı sekmesi \> **Başlangıç tarihi** alanında veya **Tüm işlem yapılacak yerleşimler** ayrıntıları görünümü \> **Bakım planları** hızlı sekmesi \> **Başlangıç tarihi** alanında seçilir. Bakım planları zamanladığınızda, aralığa ulaşıldığında bakım zamanlaması satırı oluşturulur. | Varlık veya işlem yapılacak yerleşimde bakım planı satırının başlangıç tarihi kullanılır. Bu alan boşsa bakım planı için **Plan tarihi** kullanılır. | Varlık veya işlem yapılacak yerleşimde bakım planı satırının başlangıç tarihi kullanılır. Bu alan boşsa bakım planı için **Plan tarihi** kullanılır. |
| **Aralık türü: Son iş emrinden itibaren yinelenen** Sayım, bu özel bakım işi türü/bakım işi türü değişkeni/ticaret kombinasyonuyla varlıkta tamamlanan en son iş emrinin fiili bitiş tarihi ve saatinden başlar. Bu tarih ve saat, **Tüm iş emirleri** ayrıntıları görünümünde **Fiili bitiş** alanında gösterilir. | Bu özel bakım işi türü/bakım işi türü değişkeni/ticaret kombinasyonuyla varlıkta tamamlanan iş emrinin fiili bitiş tarihi ve saati. Tamamlanan iş emri bulunmazsa bunun yerine yukarıda açıklanan "Başlangıç tarihinden itibaren yinelenen" aralık türünde kullanılan tarihlerden biri kullanılır. | Varlık *ve* bakım işi türü / bakım işi türü çeşidi / ticaret birleşiminde tamamlanan iş emrinin fiili bitiş tarihi ve saati. kullanılır. İş emrinde bitiş tarihi ve saati boş bırakıldıysa bunun yerine yukarıda açıklanan "Başlangıç tarihinden itibaren yinelenen" aralık türünde kullanılan tarihlerden biri kullanılır. |
| **Aralık türü: Plan tarihinden itibaren bir kez** Yukarıdaki "Plan tarihinden itibaren yinelenen" aralık türünün açıklamasına bakın. Tek fark, bu aralık türünün yalnızca bir kez kullanılacak olmasıdır. | Yukarıdaki "Plan tarihinden itibaren yinelenen" aralık türünün açıklamasına bakın. Bu aralık genellikle tek seferlik bakım veya servis işi için kullanılır. | Yukarıdaki "Plan tarihinden itibaren yinelenen" aralık türünün açıklamasına bakın. Bu aralık genellikle tek seferlik bakım veya servis işi için kullanılır. **Not 1:** Bu aralık türü yalnızca sayacın bakım veya servis işi gerçekleştirdiğiniz her defasında değiştirilmesi durumunda ilgilidir. Herhangi bir nedenle planlı aralığın sonundan önce bir sayaç değiştirilirse bu iş için sayacın değiştirilme saatinden itibaren yeni bir saat hesaplanır. **Not 2:** Bakım veya servis işi tamamlanırken sayaç değiştirilirse bu aralık türü, yukarıdaki "Plan tarihinden itibaren yinelenen" aralık türü olarak işlev görür. |
| **Aralık türü: Başlangıç tarihinden itibaren bir kez** Yukarıdaki "Başlangıç tarihinden itibaren yinelenen" aralık türünün açıklamasına bakın. Tek fark, bu aralık türünün yalnızca bir kez kullanılacak olmasıdır. | Yukarıdaki "Başlangıç tarihinden itibaren yinelenen" aralık türünün açıklamasına bakın. Bu aralık genellikle tek seferlik bakım veya servis işi için kullanılır. | Yukarıdaki "Başlangıç tarihinden itibaren yinelenen" aralık türünün açıklamasına bakın. Bu aralık genellikle tek seferlik bakım veya servis işi için kullanılır. **Not 1** Üst sınır ayrıca bu aralık türü için de geçerlidir. **Not 3:** Bakım veya servis işi tamamlanırken sayaç değiştirilirse bu aralık türü, yukarıdaki "Başlangıç tarihinden itibaren yinelenen" aralık türü olarak işlev görür. |
| **Aralık türü: Üst sınıra ulaşıldı** Bu aralık türü yalnızca sayaçlarla ilgilidir ve bakım planı satırında ayarlanan üst sınırı göstermek için kullanılır. Bakım zamanlaması girişleri sayaç kaydının beklenen başlangıç tarihi ve saatine sahip olur. Bu, bu girişlerin sistem tarihine eşit veya daha erken bir beklenen başlangıç tarihiyle oluşturulacağı anlamına gelir. | Geçerli değil | Sayaç aralığı üst sınırı belirtir. Bu sınır sayaç kaydı oluşturduğunuzda aşılırsa bakım zamanlaması satırı, önleyici bakım zamanladığınızda oluşturulur. |
| **Aralık türü: Alt sınıra ulaşıldı** Bu aralık türü yalnızca sayaçlarla ilgilidir ve bakım planı satırında ayarlanan alt sınırı göstermek için kullanılır. Bakım zamanlaması girişleri sayaç kaydının beklenen başlangıç tarihi ve saatine sahip olur. Bu, bu girişlerin sistem tarihine eşit veya daha erken bir beklenen başlangıç tarihiyle oluşturulacağı anlamına gelir. | Geçerli değil | Sayaç aralığı alt sınırı belirtir. Bu sınır sayaç kaydı oluşturduğunuzda geçilirse bakım zamanlaması satırı, önleyici bakım zamanladığınızda oluşturulur. |
| **Aralık türü: Başlangıç tarihinden itibaren bağlantılı** Bu aralık türü, yalnızca bir kez bir bakım zamanlaması satırı oluşturur. Bakım planı, bu aralık türünü kullanarak daha fazla bakım planı satırı içerebilir ve bu satırlar bağlantılıdır. Genellikle, yalnızca bu aralık türündeki satırları içeren bir bakım planı oluşturursunuz. Bakım zamanlaması satırları, ilk beklenen başlangıç tarihi ve saatine sahip bakım planı satırını tanımlayarak oluşturulur. | Yukarıdaki "Başlangıç tarihinden itibaren bir kez" türünün açıklamasına bakın. Örnek: Bir araçtaki servis işi için bakım planında iki satır oluşturursunuz: 1 yıllık döneme sahip zaman temelli satır ve 25.000 km. sınıra sahip sayaç temelli satır. Bakım zamanlaması satırı, ilk olarak ulaşılan sınır için oluşturulur. Bu satır türü için 1 yıllık döneme sahip satırı oluşturursunuz. | Yukarıdaki "Başlangıç tarihinden itibaren bir kez" türünün açıklamasına bakın. Örnek: Bir araçtaki servis işi için bakım planında iki satır oluşturursunuz: 1 yıllık döneme sahip zaman temelli satır ve 25.000 km. sınıra sahip sayaç temelli satır. Bakım zamanlaması satırı, ilk olarak ulaşılan sınır için oluşturulur. Bu satır türü için 25.000 km. sınıra sahip satırı oluşturursunuz. İki sayaç satırı oluşturma örneği: Ayrıca ilk satırda 10.000 madde miktarı üretim sınırı olan ve ikinci satırı 3.000 saat çalışmanın ardından servis gerektiren makine veya iş merkezi ile ilgili iki bağlantılı ve sayaç temelli satıra sahip bakım planı da ayarlayabilirsiniz. |
| **Aralık türü: Son iş emrinden itibaren bağlantılı** Bu aralık türü, her tamamlanan iş emrinden sonra yeni bakım zamanlaması satırı oluşturur. Bakım planı, bu aralık türünü kullanarak daha fazla satır içerebilir ve bu satırlar bağlantılıdır. Normal şartlarda, yalnızca bu aralık türündeki bakım planı satırlarını içeren bir bakım planı oluşturursunuz. Bakım zamanlaması satırları, ilk beklenen başlangıç tarihi ve saatine sahip bakım planı satırını tanımlayarak oluşturulur. | Bu aralık türü temelde yukarıda açıklanan "Başlangıç tarihinden bağlantılı" olarak çalışır. Tek fark, aralık türünün temel alındığı tarihtir. Kullanılan tarih, varlık *ve* bakım işi türü / bakım işi türü çeşidi / ticaret birleşiminde tamamlanan en son iş emrinin fiili tarihi ve saatidir. | Bu aralık türü temelde yukarıda açıklanan "Başlangıç tarihinden bağlantılı" olarak çalışır. Tek fark, aralık türünün temel alındığı tarihtir. Kullanılan tarih, varlık *ve* bakım işi türü / bakım işi türü çeşidi / ticaret birleşiminde tamamlanan en son iş emrinin fiili tarihi ve saatidir. |
| **Aralık türü: Toplam değerde tekrarlama (Yalnızca sayaç)** Bakım planı çalıştırıldığında, bir kıymet sayacının birikmiş değeri dönem sıklığına veya dönem sıklığının katlarına ulaştığı her seferinde bir zamanlanmış bakım satırı oluşturulur. (Dönem sıklığı bakım planı satırında tanımlanır.)<p>Bu işlevi etkinleştirme ve kullanma hakkında daha fazla bilgi için bu konunun ilerleyen kısımlarındaki [Sayaç tabanlı bakım geliştirmeleri](#counter-based-maintenance) bölümünü inceleyin. | Geçerli değil | **Örnek:** AK-101 kıymeti için bir saat sayacı ayarlanmıştır. Kıymet için bir kıymet planı satırı da ayarlanır. Bu satırın aralık türü, *Toplam değerde tekrarlanma (Yalnızca sayaç)* seçeneğidir ve dönem sıklığı *1000* olarak ayarlanmıştır. Bakım planı çalıştırıldığında, sayacın toplam değeri 1000 saati aştığında bir zamanlanmış bakım satırı oluşturulur. Daha sonra, sayacın toplam değeri 2000 saati aştığında, bir zamanlanmış bakım satırı daha oluşturulur ve her ek 1000 saat için bu işlem tekrarlanır. |
| **Aralık türü: Toplam değerde bir kere (Yalnızca sayaç)** Bakım planı çalıştırıldığında, bir kıymet sayacının toplam değeri bakım planı satırında tanımlanan dönem sıklığına her ulaştığında zamanlanmış bakım satırı oluşturulur.<p>Bu işlevi etkinleştirme ve kullanma hakkında daha fazla bilgi için [Sayaç tabanlı bakım geliştirmeleri](#counter-based-maintenance) bölümünü inceleyin. | Geçerli değil | **Örnek:** AK-101 kıymeti için bir saat sayacı ayarlanmıştır. Kıymet için bir kıymet planı satırı da ayarlanır. Bu satırın aralık türü, *Toplam değerde bir kez (Yalnızca sayaç)* seçeneğidir ve dönem sıklığı *1000* olarak ayarlanmıştır. Bakım planı çalıştırıldığında, sayacın toplam değeri 1000 saati aştığında bir zamanlanmış bakım satırı oluşturulur. |

>[!NOTE]
>Bakım zamanlaması satırları zaman temelli bakım planı satırları için oluşturulduğunda beklenen zaman her zaman günün başlangıcıdır. Sayaç temelli bakım planı satırları için beklenen zaman gün içinde herhangi bir zaman olabilir.

Zaman temelli ve sayaç temelli bakım planı satırlarının kurulum örneklerini aşağıda bulabilirsiniz:

**1. Örnek: Zaman temelli bakım planı satırı:** Haftada bir kez gerçekleşen sabit aralıklarla bir yağlama işi ayarlanabilir. Bu amaçla, **Aralık türü** alanında "Plan tarihinden itibaren yinelenen" seçeneğini belirleyin. Aşağıdaki çizimde bulunan örneğe bakın.

![Haftada bir gerçekleşen sabit aralığa göre ayarlanmış bir servis işi](media/02-preventive-maintenance.png "Haftada bir gerçekleşen sabit aralığa göre ayarlanmış bir servis işi")

**2. Örnek: Zaman temelli bakım planı satırı:** Yaklaşık olarak haftada bir kez gerçekleştirilecek şekilde bir inceleme işi ayarlanabilir. Bu amaçla, **Aralık türü** alanında "Son iş emrinden itibaren yinelenen" seçeneğini belirleyin. Aşağıdaki çizimde bulunan örneğe bakın.

![Yaklaşık olarak haftada bir kez yapılmaya ayarlanmış denetim işi](media/03-preventive-maintenance.png "Yaklaşık olarak haftada bir kez yapılmaya ayarlanmış denetim işi")

**3. Örnek: Sayaç temelli bakım planı satırı:** Aşağıdaki grafik çiziminde her 250 saatlik sürenin sonunda yeni bir bakım zamanlaması satırının oluşturulduğu saat sayacı gösterilmektedir. Bu sayaç temelli satır için aralık türü "Başlangıç tarihinden itibaren yinelenen"dir. Başlangıç tarihi, **Tüm kıymetler** ayrıntıları görünümü \> **Kıymet bakım planları** hızlı sekmesi \> **Başlangıç tarihi** alanında veya **İşlem yapılacak yerleşim** ayrıntıları görünümü \> **Bakım planları** hızlı sekmesi \> **Başlangıç tarihi** alanındaki ilgili kıymetlerin başlangıç tarihidir. Bakım zamanlaması satırının eşiğe (+ 250) her ulaşıldığında otomatik olarak oluşturulması nedeniyle bu bir *önleyici* bakım planı örneğidir.

![Düzenli aralıklarla bakım çizelgesi satırları oluşturan bir saat sayacı](media/04-preventive-maintenance.png "Düzenli aralıklarla bakım çizelgesi satırları oluşturan bir saat sayacı")

**4. Örnek: Sayaç temelli bakım planı satırı:** Aşağıdaki grafik çiziminde, fren balatasındaki aşınma ölçülerek sayaç değerindeki azalma gösterilmektedir. Fren balatasında 20 mm. altında bir sayaç kaydı oluşturulduğunda bakım zamanlaması satırı oluşturulur. Bu sayaç temelli satır için aralık türü "Alt sınıra ulaşıldı" veya "Son başlangıç tarihinden itibaren bir kez"dir. Bakım zamanlaması satırının 20 mm. altında ölçüm kaydedilene kadar oluşturulmaması nedeniyle bu bir *reaktif* bakım planı örneğidir.

![Fren balatasındaki aşınmayı ölçen sayaç değerinde azalma](media/05-preventive-maintenance.png "Fren balatasındaki aşınmayı ölçen sayaç değerinde azalma")

**5. Örnek: Sayaç temelli bakım planı satırı:** Aşağıdaki grafik çiziminde -18 santigrat derece eşiğine sahip sayaç gösterilmektedir. -18 santigrat derecenin üzerinde sayaç kaydı yapıldığında bakım zamanlaması satırı oluşturulur. Bu sayaç temelli satır için aralık türü "Üst sınıra ulaşıldı"dır. Bakım zamanlaması satırının -18 santigrat dereceden yüksek ölçüm kaydedilene kadar oluşturulmaması nedeniyle bu bir *reaktif* bakım planı örneğidir.

![-18 santigrat derece eşiğe sahip sayaç](media/06-preventive-maintenance.png "-18 santigrat derece eşiğe sahip sayaç")

- Yeni kıymet oluşturduğunuzda ve bu kıymetin bakım planıyla ilgili bir kıymet türü kullanması durumunda, bakım planı **Tüm nesneler \> Kıymet bakım planları** hızlı sekmesine otomatik olarak eklenir. Ayrıca, **Varlık türü varsayılanları**'nda **Bakım planları** hızlı sekmesine ilgili bakım planları otomatik olarak eklenir.
- **Bakım planları**'na varlık türleri veya işlem yapılacak yerleşim türleri eklerseniz ya da kaldırırsanız bu değişiklik yalnızca değişikliği yapmanızın ardından oluşturulan yeni varlıklara yansır.
- **Bakım planları**'na kıymet veya işlem yapılacak yerleşim eklerseniz ya da kaldırırsanız bu değişiklik  **Tüm kıymetler \> Kıymet bakım planları** hızlı sekmesinde veya **Tüm işlem yapılacak yerleşimler \> Bakım planları** hızlı sekmesinde otomatik olarak güncelleştirilir.

Aşağıdaki çizimde **Bakım planları** sayfasındaki bir "Kamyon servisi" bakım planı örneği gösterilmektedir.

![Kamyon servis bakım planına örnek](media/07-preventive-maintenance.png "Kamyon servis bakım planına örnek")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Bir varlığa bakım planı ekleme

1. **Kıymet yönetimi \> Genel \> Kıymetler \> Tüm kıymetler** veya **Etkin kıymetler**'e gidin.

1. Bakım planı ayarlamak istediğiniz varlığı seçin ve **Düzenle**'yi seçin.

1. **Kıymet bakım planları** hızlı sekmesinde kıymete bakım planı eklemek için **Satır ekle**'yi seçin.

1. **Bakım planı** alanında ilgili bakım planını seçin.

1. **Başlangıç tarihi** alanında önleyici bakım işlerini planlamanın yapılabilmeye başlanacağı tarihi seçin. 

1. **Kaydet**'i seçin. **Etkin** alanı otomatik olarak güncelleştirilir.

Aşağıdaki çizimde **Tüm varlıklar** sayfasında bulunan bir varlıktaki bakım planları ayarı örneği gösterilmektedir.

![Bir kıymet üzerinde ayarlanan bakım planları örneği](media/08-preventive-maintenance.png "Bir kıymet üzerinde ayarlanan bakım planları örneği")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Sayaç tabanlı bakım geliştirmeleri

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

*Sayaç tabanlı bakım geliştirmeleri* özelliği aşağıdaki işlevleri sağlar:

- Bir kıymet oluşturulduğunda, değeri *0* (sıfır) olan bir sayacı otomatik olarak ekleme seçeneği. Bu seçenek, sayaçları temel alan tahmine dayalı bakımı kullandığınızda yararlı olabilir. *Sayaç tabanlı bakım geliştirmeleri* özelliği kullanılmazsa, değeri *0* (sıfır) olan sayaçlar el ile eklenmelidir.
- Bir sayacı, bir iş emri tamamlandığında otomatik olarak sıfırlanacak şekilde yapılandırabilme. Bu işlev, son iş emri tamamlandığından bu yana toplam değere dayalı olarak bakım zamanlamak istediğinizde yararlıdır.
- *Toplam değerde tekrarlama (Yalnızca sayaç)* adlı yeni bir bakım planı aralığı türü. Bu tür, sayacın toplam değeri belirli bir değerin katlarına her ulaştığında bakımı tetikler. Örneğin, bakım her 10.000 saatte bir tetiklenebilir. Daha fazla bilgi için bu konunun önceki kısımlarında yer alan [Aralık türlerine genel bakış](#interval-types) bölümüne bakın.
- *Toplam değerde bir kez (Yalnızca sayaç)* adlı başka bir yeni bakım planı aralığı türü. Bu tür, sayacın toplam değeri belirli bir değere ulaştığında (ör. 8000 saat) bakımı tetikler. Daha fazla bilgi için [Aralık türlerine genel bakış](#interval-types) bölümüne bakın.

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Sayaç tabanlı bakım geliştirmeleri özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Kıymet Yönetimi*
- **Özellik adı:** *(Önizleme) Sayaç tabanlı bakım geliştirmeleri özelliğini açma*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Bir kıymet oluşturulduğunda sayaçlar oluşturma ve başlatma

Bir kıymet oluşturduğunuzda, sisteminizi ayarlamanız ve kıymeti doğru oluşturduğunuz takdirde *0* (sıfır) değerinde başlatılan ilgili kıymet sayaçları otomatik olarak oluşturulabilir.

1. **Kıymet yönetimi \> Kurulum \> Kıymet türleri**'ne gidin.
1. Planlanan yeni kıymet için geçerli olan bir kıymet türüne sahip olduğunuzdan emin olun. Gereken şekilde bir kıymet türü oluşturun. **Sayaçlar** hızlı sekmesinde, ilgili tüm sayaçların seçilmiş olduğundan emin olun.
1. **Kıymet yönetimi \> Kurulum \> Kıymet türleri \> Sayaçlar**'a gidin.
1. İlgili her sayaç için **Toplama toplamı** alanının *Toplam* olarak ayarlandığından emin olun.
1. **Tüm kıymetler** sayfasında, kıymeti oluşturun.
1. **Kıymet türü** alanını, 2. adımda belirlediğiniz veya oluşturduğunuz kıymet türü olarak ayarlayın.
1. Yeni kıymetin ayarlamalarını gereken şekilde yapın.
1. **Kıymet yönetimi \> Sorgular \> Kıymetler \> Sayaçlar**'a gidin. Yeni kıymetiniz için ayarlanmış olan başlatılmış sayaçlarınızı bulabilmeniz gerekir.

> [!NOTE]
> Başlatılmış kıymet sayaçları oluşturulduğunda, kıymetin sisteme eklenmeden önce hiç kullanılmamış olduğu varsayılır. Bakım zamanlaması ilk kez çalıştırıldığında, hesaplama gelecek bakımı hesaplamak için temel olarak tarihi ve *0* (sıfır) sayaç değerini kullanır. Kıymet sisteme eklendiğinde yeni değilse sayaç değerini gerçek sayaç değeriyle eşleşecek şekilde el ile ayarlayabilirsiniz. Bir sayaç değerini ayarlamak için ilgili kıymeti **Tüm kıymetler** sayfasında açın ve ardından Eylem Bölmesindeki **Kıymet** sekmesinde yer alan **Önleyici** grubunda **Sayaçlar**'ı seçin. Seçilen kıymetin **Kıymet sayaçları** sayfasında, başlangıç sayacı kaydı için **Değer** sütunundaki değeri gereken şekilde ayarlayın.

### <a name="automatically-reset-a-counter-value"></a>Sayaç değerini otomatik olarak sıfırlama

Sistemi, ilgili iş emrinin seçili durum değerine her ulaştığında otomatik olarak sayacın sıfırlanacağı şekilde yapılandırabilirsiniz.

1. **Kıymet yönetimi \> Kurulum \> Önleyici bakım \> Bakım planları**'na gidin.
1. Liste bölmesinde bir bakım planı seçin. Sayaç sıfırlama, bu planı kullanan tüm kıymetler için geçerli olacak.
1. **Satırlar** bölümünde, sayacını sıfırlamak istediğiniz bir kıymet sayacı satırı bulun ve bu satır için **Sayacı sıfırla** onay kutusunu seçin. (Kıymet sayacı satırları, **Sayaç** sütununda bir değer sahiptir. Bu sütunda belirtilen sayaç, ilgili kıymet için sıfırlanacak sayaçtır.)
1. **Kıymet yönetimi \> Kurulum \> İş emirleri \> Yaşam döngüsü durumları**'na gidin.
1. Liste bölmesinde, ilgili sayacın sıfırlanacağı iş emri yaşam döngüsü durumunu seçin.
1. **Genel** hızlı sekmesinde, **Sayacı sıfırla** seçeneğini *Evet* olarak ayarlayın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]