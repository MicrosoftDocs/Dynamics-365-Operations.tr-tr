--- 
title: "Tahsilat bilgilerini gözden geçirme"
description: "Bu yordam, tahsilat bilgilerini gözden geçirmenin yanı sıra çeşitli seçenekleri ve tahsilat hareketlerini ayarlamayı adım adım açıklar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b28d41d5ecf63b22cb84aff0c12a36cb0d728945
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="review-collections-information"></a>Tahsilat bilgilerini gözden geçirme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, tahsilat bilgilerini gözden geçirmenin yanı sıra çeşitli seçenekleri ve tahsilat hareketlerini ayarlamayı adım adım açıklar. Bu yordam, USMF demo şirketini kullanır.


## <a name="create-customer-pools"></a>Müşteri havuzları oluşturma
1. Alacak ve tahsilatlar > Ayarlar > Yaşlandırma Müşteri havuzları'na gidin.
    * Tahsilatlar veya yaşlandırma işlemleri için görüntülenebilen veya yönetilebilen müşteri hesaplarının bir grubunu tanımlayan müşteri havuzları ayarlamak için bu sayfayı kullanın. Tahsilatlar listesi sayfasında ve ilgili liste sayfalarında bilgileri filtrelemek için müşteri havuzlarını kullanın. Yaşlandırma anlık görüntüsü oluşturulduğunda eklenecek müşteri hesaplarını filtrelemek için de müşteri havuzlarını kullanabilirsiniz.  
    * Yaşlandırma anlık görüntüsü oluşturulduğunda eklenecek müşteri hesaplarını filtrelemek için müşteri havuzlarını kullanabilirsiniz.  
2. Yeni'ye tıklayın.
3. Havuz Kodu alanında bir değer girin.
4. Havuz açıklaması alanında bir değer girin.
5. Havuz ölçütlerini seç'e tıklayın.
6. Ölçütler alanına bir değer yazın.
7. Tamam'a tıklayın.
8. Müşteri havuzunu önizle'ye tıklayın

## <a name="create-collections-agents"></a>Tahsilat temsilcileri oluşturma
1. Alacak ve tahsilatlar > Ayarlar > Tahsilat temsilcisi'ne gidin.
    * Çalışanları tahsilat temsilcileri olarak ayarlamak ve isteğe bağlı olarak onlara müşteri havuzları atamak için bu sayfayı kullanın. Tahsilat temsilcisi, ödemelerin zamanında tahsil edildiğinden emin olmak için müşterilerle birlikte çalışan kişidir.  
    * Bu sayfada ayarlanan tahsilat temsilcileri tahsilatlar ekibine otomatik olarak eklenir. Bir takım alacak hesapları parametreleri sayfasının Takım alanında seçilirse, tahsilat temsilcileri bu takıma eklenir. Bir takım seçilmemişse, Tahsialatlar adlı yeni bir takım otomatik olarak oluşturulur tahsilat temsilcileri bu takıma eklenir.  
2. Yeni'ye tıklayın.
3. Ekle öğesini tıklatın.
4. Kapat’a tıklayın.
5. Ekle öğesini tıklatın.
6. Listede, seçili satırı işaretleyin.
7. Havuz kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, istenen kaydı bulun ve seçin.
9. Varsayılan havuz onay kutusunu işaretleyin veya temizleyin.
    * Seçili tahsilat temsilcisi için filtre listelerindeki tüm müşteri havuzlarını dahil etmek için bu seçeneği belirleyin. Bu seçenek seçili değilse, yalnızca tahsilat temsilcisine atanan müşteri havuzları filtre listelerinde kullanılabilir.  

## <a name="create-aging-period-definition"></a>Yaşlandırma dönemi tanımı oluşturma
1. Alacak ve tahsilatlar > Kurulum > Yaşlandırma dönemi tanımları'na gidin.
    * Müşteri hesaplarının ve satıcı hesaplarının vadesini girdiğiniz bir tarihe göre analiz etmek için yaşlandırma dönemi tanımlarını kullanabilirsiniz. Yaşlandırma dönemi tanımı için ayarladığınız her bir yaşlandırma dönemi, analiz gerçekleştirildiğinde liste sayfasındaki veya formdaki ya da rapordaki bir sütuna karşılık gelir.  
2. Yeni'ye tıklayın.
3. Yaşlandırma dönemi tanımı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
    * Dönem adını, birimini ve yaşlandırma dönemi tanımına eklenecek her bir yaşlandırma dönemi aralığını belirtin. Birim alanında 0 (sıfır) bulunan satır, analizin çalıştırıldığı tarihi temsil eder. Birim alanında varsayılan giriş olarak sıfırdan önceki satırlarda -1 ve sıfırdan sonraki satırlarda 1 bulunur ancak bu değiştirilebilir.  Satırları yeniden düzenlemek için Yukarı ve Aşağı düğmelerine tıklayın. 0 (sıfır) satırı taşınamaz.  
    * İşaretçiyi yeni satır eklemek istediğiniz konuma getirin ve Ekle'yi tıklatın.  
    * Tahsilatlar formunda ve liste sayfasında yaşlandırma dönemini temsil edecek göstergeyi seçin. Örneğin, geçerli dönem bir yeşil gösterge, 30 günü geçmiş dönem için sarı bir gösterge ve 90 günü geçmiş dönem için kırmızı bir gösterge seçebilirsiniz.  
    * Yaşlandırma aralığı tanımının yazdırma yönünü seçin. Bu seçim sütunun Müşteri yaşlandırma raporu veya Satıcı yaşlandırma raporu üzerinde görüntülenme sırasını belirler.  İleriye doğru – Sütunları başlıkların tabloda göründüğü gibi üstten başlayarak yazdırın.  Geriye doğru – Sütunları başlıkların tabloda göründüğünün tersi olacak şekilde alttan başlayarak yazdırın.    

## <a name="setup-collections-parameters"></a>Tahsilat parametrelerini ayarlama
1. Alacak ve tahsilatlar > Kurulum > Alacak hesapları parametreleri'ne gidin.
2. Tahsilatlar sekmesine tıklayın.
3. Tahsilatlar bölümünü genişletin veya daraltın.
    * Tahsilatlar formunda kullanılacak varsayılan yaşlandırma anlık görüntüsü için bir yaşlandırma dönemi tanımı seçin.  
    * Tahsilat temsilcisi formunda tahsilat temsilcilerinin atanacağı bir ekip seçin. Listede yalnızca Tahsilat ekibi türündeki ekipler görüntülenir.  
4. Silme bölümünü genişletin veya daraltın.
    * Tahsilatlar formu veya ilgili liste sayfaları kullanılarak bir hareket silindiğinde kullanılmak üzere günlük muhasebe defterleri için ayarlanmış günlük adını seçin.  
    * Tahsilatlar formu veya ilgili liste sayfaları kullanılarak silme hareketleri oluştururken kullanılacak varsayılan neden kodunu seçin.  
    * Tahsilatlar sayfası veya ilgili liste sayfaları kullanılarak silme hareketleri oluştururken satış vergisi tutarları için ayrı bir günlük satırı oluşturmak için bu seçeneği seçin. Bu seçeneği seçerseniz, silme hareketlerine dahil edilen satış vergisi hareketlerini kolayca izleyebilirsiniz. Etkilenen dönem için satış vergisi borcunuzu daha kolay ayarlamanıza yardımcı olması için satış vergisi tutarlarını ayrı ayrı izleyebilirsiniz.  
5. E-posta şablonu bölümünü genişletin veya daraltın.
    * Tahsilatlar formunda E-posta > İlgili kişi işlemi hareketleri'ni kullanarak bir e-posta gönderdiğinizde kullanılacak e-posta şablonunu seçin.  
    * Tahsilatlar formunda E-posta > İlgili kişi işlemi ekstresi'ni kullanarak bir e-posta eki olarak bir müşteri ekstresi gönderdiğinizde kullanılacak e-posta şablonunu seçin.  
    * Tahsilatlar formunda E-posta > Satış temsilcisi işlemi hareketleri'ni kullanarak bir e-posta gönderdiğinizde kullanılacak e-posta şablonunu seçin.  

## <a name="age-customer-balance"></a>Müşteri bakiyelerini yaşlandırma
1. Alacak ve tahsilatlar > Dönemsel görevler > Müşteri bakiyelerini yaşlandır'a gidin.
    * Bir yaşlandırma dönemi tanımı seçin. Yaşlandırma anlık görüntü işlemi, hareketleri seçili yaşlandırma dönemi tanımında tanımlanan yaşlandırma dönemlerine göre yaşlandırır.  
    * Bir müşteri havuzu seçin veya tüm müşteriler için bir yaşlandırma anlık görüntüsü oluşturmak için bu alanı boş bırakın. Müşteri havuzu seçtiyseniz, yaşlandırma anlık görüntüsü işlemi yalnızca müşteri havuzunun bir parçası olan müşteri hesaplarına uygulanır. Seçili müşteri havuzu Yaşlandırma anlık görüntüsü türünde olmalıdır.  
    * Yaşlandırma anlık görüntüsünün temel alacağı tarih tipini seçin.    Hareketi tarihi – Hareket tarihine göre her bir hareketin yaşıdır.    Vade tarihi – Vade tarihine göre her hareketin yaşıdır.    Belge tarihi – Belge tarihine göre her hareketin yaşıdır.  
    * Yaşlandırma anlık görüntüsü için geçerli tarihi olarak kullanılacak tarihi seçin. Yaşlandırma dönemleri bu tarih temel alınarak hesaplanır.    Bugünün tarihi – Sistem tarihini kullanın. İşlem tekrarlayan bir toplu işte gerçekleştirilmek üzere ayarlanırsa bu seçeneği kullanın. Bu tarihi kullanırsanız, tekrarlayan toplu iş düzenli aralıklarla çalıştırılabilir ve o zamandaki sistem tarihi kullanılır.    Seçili tarih – Belirttiğiniz tarihi kullanın. Bu seçeneği belirlerseniz, yaşlandırma tarihini girin.  
2. Tamam'a tıklayın.

## <a name="view-aged-customer-balances"></a>Yaşlandırılmış müşteri bakiyelerini görüntüleme
1. Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler.
    * Müşteri bakiyelerini ve yaşlandırma dönemine göre yaşlanan miktarları görüntülemek için bu liste sayfasını kullanın. Bu bilgiler bir yaşlandırma anlık görüntüsünde depolanır. Yaşlandırma dönemleri, kullanılan yaşlandırma dönemi tanımı tarafından belirlenir. Yaşlandırma dönemi tanımı, havuz sorgusu için belirtildiyse, müşteri havuzundan alınır. Müşteri havuzunda bir yaşlandırma dönemi tanımı yoksa, Alacak hesapları parametreleri formunda belirtilmiş varsayılan yaşlandırma dönemi tanımı kullanılır.  
2. İlgili Kişi Bilgi Kutusunu genişletin.
    * Müşterinin tahsilat ilgili kişisi.  
    * Müşterinin varsayılan satış temsilcisi.  
3. Kredi limiti Bilgi Kutusunu genişletin.
    * Müşterinin kredi limitini ve geçerli bakiye bilgilerini görüntülemek için alacak bilgileri Bilgi kutusunu kullanın.  

## <a name="view-customer-collections-details"></a>Müşteri tahsilatlarının ayrıntılarını görüntüleme
1. Listede, seçili satırdaki bağlantıya tıklayın.
2. Adres Bilgi Kutusunu genişletin.
3. İlgili Kişi Bilgi Kutusunu genişletin.
4. Yaşlandırma Bilgi Kutusunu genişletin.
5. Kredi limiti Bilgi Kutusunu genişletin.
6. Eylem Bölmesinde, Tahsil et'e tıklayın.
    * Hareket tarihlerinin karşılaştırılacağı yaşlandırma tarihi olarak geçerli tarihi kullanarak müşterinin yaşlandırma anlık görüntüsünü güncelleştirin. Yaşlandırma anlık görüntüsü birden çok tüzel kişilik bilgisi içeriyorsa, güncelleştirilmiş yaşlandırma anlık görüntüsü aynı tüzel kişilikler kümesinin bilgilerini içerir. Miktarlar yaşlandırma anlık görüntüsünü güncelleştirdiğinizde oturum açtığınız tüzel kişiliğin muhasebe para biriminde depolanır.  
    * Bir yaşlandırma dönemi tanımı seçin. Varsayılan olarak, müşteri yaşlandırma anlık görüntüsüyle ilişkili yaşlandırma dönemi tanımı görüntülenir. Yaşlandırma dönemi tanımı, yaşlandırılmış bakiyeler ve Alacak bilgileri bilgi kutularında gösterilen yaşlandırma dönemlerini ve tutarları denetler.  
    * Aşağıdaki öğeleri içeren bir menü açın:     Şirket – Yaşlandırılmış bakiyeler ve alacak bilgileri bilgi kutularındaki tutarları tüzel kişinin muhasebe para birimi cinsinden görüntüler.    Müşteri – Yaşlandırılmış bakiyeler ve alacak bilgileri bilgi kutularındaki tutarları müşterinin para birimi cinsinden görüntüler.  
    * Görüntülenecek bilgiler için müşterinin yaşlandırma anlık görüntüsünde bir veya daha fazla tüzel kişi seçin. Listede gösterilen tüzel kişilikler yaşlandırma anlık görüntüsü oluşturulduğunda seçilmiştir.  
    * Müşterinin ekstresini Microsoft Excel biçiminde görüntüleyin. Ekstreye eklenecek hareketlerin aralığı için bir başlangıç tarihi seçebilir ve yalnızca açık ekstreleri mi yoksa hem açık hem de kapatılan hareketleri mi ekleyeceğinize karar verebilirsiniz. Yaşlandırma anlık görüntüsü birden çok tüzel kişiliğe ilişkin bilgiler içeriyorsa, tüm tüzel kişiliklerin hareketleri eklenir.  
    * Belgeleri veya dekontları düzenleyebildiğiniz Belgeler formunu açın.  
7. Eylem Bölmesinde, İletişim Kur öğesini tıklatın.
    * İlgili kişi alanında belirtilen ilgili kişiye e-posta iletisi gönderebileceğiniz Outlook'u açın. Müşteri ilgili kişisi belirtilmemişse müşterinin belirtilen birincil adres kullanılır. Birincil ilgili kişi belirtilmemişse, İlgili kişiler formunda listelenen ilk adrese e-posta iletileri gönderilir. Seçilen hareketler bir ek olarak dahil edilir. Ek, Excel biçimindedir ve üç çalışma tablosu içerir. Müşteri ilgili kişilerine gönderilen iletiler için Alacak hesapları parametreleri formunda bir e-posta şablonu belirtilebilir.  
    * Bu formda seçilen kişinin ayarlanmış bir e-posta adresi yoksa, bu düğme kullanılamaz.  
    * Bir ekstre hazırlayın ve İlgili kişi alanında belirtilen adrese ekstre eklenmiş bir e-posta iletisi göndermek için Outlook'u açın. Müşteri ilgili kişisi belirtilmemişse müşterinin belirtilen birincil adres kullanılır. Birincil ilgili kişi belirtilmemişse, İlgili kişiler formunda listelenen ilk adrese e-posta iletileri gönderilir.  
    * Bu formda seçilen kişinin ayarlanmış bir e-posta adresi yoksa, bu düğme kullanılamaz.  
    * Müşteriye atanan satış grubu için satış temsilcisi olarak belirtilen çalışana bir e-posta iletisi gönderebileceğiniz Outlook'u açın. Hareketler seçilirse, bir ek olarak dahil edilirler. Ek, Excel biçimindedir ve iki çalışma tablosu içerir. Satış temsilcisine gönderilen iletiler için Alacak hesapları parametreleri formunda bir e-posta şablonu belirtilebilir.  
    * Bu formda gösterilen satış temsilcisinin ayarlanmış bir e-posta adresi yoksa, bu düğme kullanılamaz.  
    * Müşteriye ilişkin hareketlere ait eylemleri görüntüleyin ve gerçekleştirin. Merkezi ödeme kullanıyorsanız, müşterinin yaşlandırma anlık görüntüsüne eklenen tüm tüzel kişilik bilgileri dahil edilir. Eylem Bölmesindeki seçili grupta Şirket düğmesini kullanarak tüzel kişilik bilgilerini kısıtlayabilirsiniz.  
    * Seçili hareketlerin tahsilat durumlarını değiştirin.    İhtilaflı değil – Hareket için hiçbir tahsilat işlemi gerçekleşmemiştir.    İhtilaflı – Müşteri hareketle ilgili bir sorun olduğunu bildirmiştir.    Ödeme taahhüdü verildi – Müşteri hareket tutarını ödemeyi kabul etmiştir.    Çözümlendi – Harekete ilişkin tüm sorunlar çözülmüş ve hiçbir tahsilat işlemi gerekli değildir.  
    * Bir menüyü açın ve bu formda görüntülenecek hareketleri belirtmek için aşağıdaki öğelerden birini seçin:    Aç – Yalnızca kapatılmamış olan hareketleri görüntüleyin.    Açık ve kapalı – Hem açık hem de kapatılmış olan tüm hareketleri görüntüleyin.  
    * Seçilen ödemeyi yetersiz fon (NSF) ödemesi olarak işleme koyar.    Bu düğme yalnızca seçili hareket bir ödeme günlüğünde girilmiş bir ödemeyse (faturasız alacak bakiyesiyse), hareket için bir banka hesabı atandıysa ve ödeme önceden iptal edilmemişse kullanılabilir .  
    * Seçili hareketleri silin.  
    * Birbirleriyle kapatmak için seçilen hareketleri işaretleyin.  
    * Seçili hareket için belgeyi görüntüleyebileceğiniz ve yazdırabileceğiniz Orijinal belge formunu açın.  
    * Aşağıdaki öğeleri içeren bir menü açın:    Tahsilatlar – Yalnızca Tahsilatlar formunda oluşturulan işlemleri görüntüleyin.    Tümü – Nerede oluşturulduğuna bakılmaksızın müşterinin tüm işlemlerini görüntüleyin.  
    * Aşağıdaki öğeleri içeren bir menü açın:    Aç – Kapatılmamış olan işlemleri görüntüleyin.    Açık ve kapalı – Durumlarına bakılmaksızın tüm işlemleri görüntüleyin.  
    * Müşteriye atanan tahsilat vakalarını seçin veya bu alanı boş bırakın. Bir vaka seçilirse, yalnızca bununla ilişkili hareketler ve işlemler bu formda görüntülenir.  
8. Listeyi göster'e tıklayın.
    * Bir müşteri hesabı seçin veya varsayılan girişi kabul edin. Varsayılan olarak liste sayfasındaki veya bu formu açtığınız formdaki seçili müşteri hesabıdır. Formu bir liste sayfasından açtıysanız, listedeki müşteriler listesi sayfasında kullanılan tahsilatlar havuzuna eklenmiş müşterilerdir.  


