---
title: Bütçe planlamasını yükseltme
description: Bu konu nelerin yeniden yapılandırılması gerektiğin ve yükseltme tamamlandıktan sonra dikkate alınması gereken yeni özellikleri açıklar.
author: panolte
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: panolte
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 86c4d83d35c7ca6bd5fe3a9f6c09e0457b40c523
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565076"
---
# <a name="upgrade-budget-planning"></a>Bütçe planlamayı yükselt

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012 ve Dynamics 365 Finance arasında bütçe planlamada önemli farklar vardır. Bazı özellikler yükseltilmemiştir ve bu nedenle yeniden yapılandırma gerektirmektedirler. Bu konu nelerin yeniden yapılandırılması gerektiğin ve yükseltme tamamlandıktan sonra dikkate alınması gereken yeni özellikleri açıklar.  

Finance'teki bütçe planlama, Dynamics AX 2012'de bulunmayan pek çok geliştirme içermektedir. Bu konu, yükseltme yapacak müşterilerin gerçekleştirmesi gereken değişiklikleri açıklar. Yükseltme işleminde dikkate alınması gereken yeni özellikleri de ortaya koyar. Değişikliklerin kapsamı yüzünden, bu konuda altı çizilen değişiklikler gerçekleştirilene kadar mevcut bütçe planlarından hiçbiri açılamayacaktır. Ancak, raporlar çalışmaya devam edecektir ve ek değişiklikler gerektirmemektedir.

## <a name="overview-of-changes"></a>Değişimlerin özeti
Finance and Operations için Bütçeleme içerisinde pek çok önemli değişiklik yapılmıştır. Bu değişiklikler Bütçe planlamanın yapılandırmasını daha kolay hale getirmek ve yeniden kullanılabilirliği artırarak yıldan yıla bakımı ve kurulumu azaltmak amacıyla yapılmıştır. AX 2012'deki şu alanlar Finance'te artık bulunmamaktadır:

-   Bütçe planı şablonları (Bütçe planlama yapılandırması)
-   Bütçe planı klasörleri (Bütçe planlama yapılandırması)
-   Senaryo kısıtlamaları (Bütçe planlama yapılandırması)
-   Bütçe planlama aşaması kuralları ve şablonları için şablonlar (Bütçe planlama işlemi)
-   Çalışma sayfası şablonlarının matris alanları
-   Bütçe planı Microsoft Excel şablonu sihirbazı

Bazı yeni kavramlar, önceki işlevden doğrudan yükseltilemez. Bu nedenle, bu yeni kavramlara yönelik olarak bazı yeniden yapılandırmalar gerçekleştirmeniz gerekir. Aşağıdaki bölümler, önceki listedeki öğelerin yerini alan kavramları açıklar.

### <a name="columns"></a>Sütunlar

Sütunlar, Excel şablonu ve matris alanlarının bazı parçalarının yerini alan yeni bir kavramdır. Sütunlar bir dönemi, bir ayı, çeyreği, yılı veya tüm zamanı temsil edebilir. Zaman referansı dinamiktir. Bütçeleme işleminin referansı içindeki bir dönem veya yılı gösterir. Örneğin, bir **Önceki Yıl Ocak** sütunu, yıl -1 için mali yıl 1'i referans gösterir. Bir sütun, bir bütçe planı senaryosuna sabittir, örneğin gerçek veya bütçe istekleri gibi.

### <a name="layouts"></a>Düzenler

Düzenler, Excel şablonunun yerini alan yeni bir kavramdır. Düzenler, hangi bütçe veya gerçek verilerin ve dönemlerin gösterilmesi gerektiğini tanımlayan sütunları içerir. Sütunlar, istemci ve Excel eklentisi arasında da paylaşılır. Bu nedenle, Finance and Operations istemcisi içinde veri girdiğinizde veya görüntülediğinizdeki kullanıcı deneyimi, AX 2012'den daha iyidir. Finance istemcisinde veri girmek için, hareket görünümde tek bir senaryo görüntüleme ve girmeyle artık sınırlı değilsiniz. Bunun yerine, bir karşılaştırma görünümü, birden fazla dönem ve hesap için aynı anda kolayca tutar girmenizi ve görmenize izin verir. Düzenler para birimi, açıklamalar ve diğer isteğe bağlı verileri girebilmeniz veya görüntüleyebilmeniz için de tanımlanabilir. Düzenler hangi genel muhasebe boyutlarının ve boyut açıklamalarının gösterileceğini de tanımlamanızı sağlar. Düzenler ayrıca senaryo kısıtlamalarını, bir şablondaki hangi sütunların düzenlenebileceğini ve hangilerinin Excel içerisinde kullanılabilir olacağını tanımlamak için kullanır. Bir düzeni tanımladıktan sonra, bunun için bir şablon oluşturulur. Artından bu şablon, karşılık gelen Excel şablonunu oluşturur. Daha sonra Excel şablonunu daha fazla formül ve biçimlendirme kullanmak üzere düzenleyebilir ve yeniden yükleyebilirsiniz. Düzenler, **Bütçe planlama işlemi** sayfasındaki her bir aşama kuralına atanır. Düzenle bu nedenle benzer şekilde atanan ve kullanılan şablonların yerini alır.

### <a name="budget-planning-processes"></a>Bütçe planlama süreçleri

Bütçe planlama işlemleri, AX 2012'dekiyle büyük ölçüde aynıdır. En önemli değişiklik, şablonlarla düzenlerin yer değiştirmesidir. Daha önce AX 2012'de herhangi bir işlem tamamlandıysa, işlemler değişikliklerin yapılabileceği işlem sürüyor durumuna güncelleştirilir. Plan, istemci içerisinde açıldığında hangi senaryo ve zaman dönemlerinin görüntüleneceğini belirtmek için her bir aşama kuralı için düzenler atamanız gerekir. Düzenler bütçeyi görebilmeniz için hangi Excel şablonunun Dynamic 365 Finance dışında açılacağını da belirler. **Varsayılan hesap yapısı**, Bütçe planlama işlemi için yeni bir gerekli alandır. Her bir Bütçe planlama işlemi için, bütçeleme için kullanılacak birincil hesap yapısını atayın.

### <a name="attachments"></a>Ekler

AX 2012'de, gerekçe belgeleri bir ek klasörüne kaydedilmekteydi. Önceki gerekçe belgelerinden hiçbiri yükseltilmedi. Gerekçe belgeleri artık veritabanında depolanır. Bu bilgi yükseltilmiş sürümde kaydedilecekse, nihai gerekçe belgelerini her bir plan için Eylem Bölmesi'ndeki **Gerekçe** düğmesini kullanarak bir ek olarak yükleyebilirsiniz. AX 2012'de, her bütçe planı için Excel çalışma sayfaları, şablonu temel alarak oluşturulmaktaydı. Finance'te tüm planlar düzenin bir kopyasını açar. Ancak, hiçbir değişiklik Excel dosyasında kaydedilmez. Plana dayalı olarak kullanılan herhangi bir formül veya destekleyici bilgi, açıklamalar, bir gerekçe belgesi veya diğer ek işlemler ile eklenmelidir.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>AX 2012'den bir yükseltilmiş ortam yapılandırmak
Yükseltilmiş sistemi nasıl yapılandıracağınızı belirlemeye yardımcı olmak için aşağıdaki örnek, AX 2012 demo verisinden yükseltilmiş bir bütçeyi kullanır. Sütunlar için varsayılan yapılandırma verisi, yükseltme işlemine yardımcı olmak için oluşturuldu. Yapılandırma gereksinimlerinizi karşılaşmıyorsa, bu varsayılan veriyi güncelleştirebilir veya silebilirsiniz. **Not:** Sistemde ayarlanmayan yeni gerekli alanlar mevcuttur. Bir sayfada takılır kalırsanız, örneğin **Bütçe planlama yapılandırması** sayfası gibi, ve başka yere gidemezseniz, ayrıntıları doğru sırada girmek için tarayıcınızı kapatabilir ve yeni bir sayfaya yeniden açabilirsiniz. Henüz ayarlanmamış gerekli alanlar vardır. Bu nedenle, her şey yapılandırılana ve tüm gerekli alanları ayarlanana kadar sorunları ortaya çıkabilir. Bu konu, bu alanları gerektiği gibi nasıl ayarlanacağını açıklar. Gerek duyulan alanlardan bazıları şunlardır:

-   **Bütçe planlama işlemi** sayfası: **Varsayılan hesap yapısı** alanı
-   **Bütçe planlama işlemi** sayfası: **Bütçe planlama aşaması kuralları ve düzenleri** hızlı sekmesi üzerindeki **Düzen** alanı

### <a name="define-columns-and-layouts"></a>Sütunları ve düzenleri tanımla

1. **Bütçe planlama yapılandırması** sayfasında **Sütunlar** sekmesine tıklayın. Güncelleştirmenin parçası olarak, yeni sütunlar bütçe planlama satırlarınıza dayanarak otomatik oluşturulur. Sütunlar artık dinamik tarihler kullanır, bunlarda ise zaman ve yıl, Bütçe planlama işleminde tanımlanan mali yıldan mahsup edilmiştir. **Not:** Yükseltme sırasında performansı artırmak için tüm bütçe döngülerinin mali yıl yerine takvim yılını temsil ettiği var sayılır. Mali yılları kullanıyorsanız, sütunları mali yılları ile doğru bir şekilde eşleştirmek düzenlemeler yapmanız gerekir. Örneğin, aşağıdaki öğeler AX 2012 içinde mevcuttu:
   -   Bütçe planı senaryoları: Fiili değerler, Temel, Bütçe İsteği, Bütçe Onaylandı
   -   2017 içindeki tüm senaryolar için Bütçe planı satırları ve hem 2017 hem de 2016 için Fiili değerler

   Finance and Operations'da aşağıdaki sütunlar oluşturulur:

   | Sütun adı    | Bütçe planı senaryosu | Sütun dönemi | Yıl denkleştirme |
   |----------------|----------------------|--------------------|-------------|
   | Oca Senaryo 1 | Gerçek değerler              | 1                  | 0           |
   | Oca Senaryo 2 | Temel             | 1                  | 0           |
   | Oca Senaryo 3 | Bütçe İsteği       | 1                  | 0           |
   | Oca Senaryo 4 | Bütçe Onaylı      | 1                  | 0           |
   | Oca Senaryo 5 | Gerçek değerler              | 1                  | -1          |
   | Şub Senaryo 1 | Gerçek değerler              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   Bu örnekte, **Oca Senaryo 1** olarak adlandırılan bir sütun, Ocak'ta hareketlerin mevcut olduğu en son bütçe planı hareketi için oluşturulur. Verilere sahip her senaryo için benzer bir sütun oluşturulur. Bu yıldaki tüm dönemler için sütunlar mevcut olduğunda, önceki yıllar için sütunlar oluşturulur.
2. Sütun adlarını ve açıklamalarını, diğer ayrıntılar da dahil olacak şekilde, ister istemci içerisinde el ile isterseniz de, bütçe planının veri varlığına işaret eden Excel eklentisi içerisinden toplu güncelleştirmeler yaparak. Matris alanlar için daha önce ayarlanmış olan herhangi bir filtre, şimdi sütunlar içinde ayarlanır.
3. Yeni bir bütçe planı düzeni oluştur. Bir düzen, Excel ve istemci içerisinde belirecek görünümü tanımlamak için birden fazla sütuna işaret eder. Düzen, ilk önce bir genel muhasebe boyutu setini, hangi mali boyutların girilebileceğini belirlemeniz için belirtmenizi gerektirir. Boyut kümesi belirttikten sonra, **Açıklamalar** üzerine tıklayarak, düzene dahil edilecek boyut açıklamalarını seçin.
4. **Düzen öğeleri** hızlı sekmesi üzerinde, her bir satır için bir para birimi, bir açıklama, gelir - gider satırlarının karşılaştırmasını belirleyecek bir bütçe sınıfı gibi meta veri eklemek için **Ekle** üzerine tıklayın. Daha sonra, aynı zaman dönemi için sütunlar ve bu bütçe döngüsüne ve aşamasına uyan senaryolar ekleyin. Bu değişiklikleri istemci içerisinde le ile veya bütçe planı düzeninin öğeler veri varlığına işaret eden Excel eklentisi aracılığıyla yapabilirisiniz.
5. Her bir düzen öğesi için sütunun düzenlenebilir olup olmadığını ve sütunun, bu düzen için Excel çalışma kitabında görünüp görünmeyeceğini seçin. **Not:** Geçmiş tarihi planlarımız için, bu işlem için tüm bütçe planı senaryoları için 12 aylık sütunlar gösteren bir düzen tercih edebilirsiniz.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Her bütçe aşası için uygun düzeni kullanmak için bütçe planlama işlemini güncelleştir

1.  **Bütçe planlama işlemi** sayfası üzerinde, yapılandırılacak işlemi seçin.
2.  Eylem Bölmesinde, **Düzenle** öğesine tıklayın.
3.  Bu bütçe işlemi için varsayılan hesap yapısını belirtin. **Varsayılan hesap yapısı**, ayarlanması gereken yeni, gerekli bir alandır.
4.  **Bütçe planlama aşaması kuralları ve düzeni** hızlı sekmesi üzerindeki **Düzen** alanında, önceden yapılandırılmış olan ve bu aşama için uygun olan bir düzen seçin.
5.  Aynı veya farklı düzenleri, çeşitli bütçe planlama aşamaları için seçmeye devam edin ve daha sonra değişikliklerinizi kaydedin.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Bütçeleme işleminiz için dikkate alınması gereken ek özellikler
### <a name="budget-planning-workspace"></a>Bütçe planlama çalışma alanı

Bu çalışma alanı hem bütçe sahibi hem de bireysel bütçe katılımcıları için tasarlanmıştır. İlginizi gerektiren tüm bütçe belgelerine bağlantılar içerir. Ayrıca bütçe işlemleri için kilit performans göstergeler (KPI'lar) ve raporları da içerir. Bütçe yöneticisi mevcut Bütçe planlama işlemini, tüm kullanıcılar için **Bütçe parametreleri** sayfasında tanımlayabilir. **Çalışma alanı** sekmesinde, **Bütçe planlama** hızlı sekmesi, bütçe planlama işlemini seçebileceğiniz bir alan içerir.

### <a name="alternate-layouts"></a>Diğer düzenler

Farklı düzenler, planları farklı bir düzende görüntülemenize olanak sağlayan yeni bir özelliktir. Bir veya daha fazla düzen, seçenekler olarak sağlanabilir. Daha sonra bir bütçe planını aylık düzende veya çeyreklik düzende görüntüleyebilirsiniz. Farklı düzenleri **Planlama aşaması kuralları ve düzenleri bütçesi** hızlı sekmesindeki **Bütçe planlama işlemi** sayfasında tanımlayabilirsiniz.

### <a name="budget-milestones"></a>Bütçe kilometre taşları

Bütçe işleminin parçası olarak, önemli tarihleri ve son tarihleri anlamanız önemlidir. Şimdi tarihleri, açıklamalara sahip olacakları şekilde yapılandırabilirsiniz. Bütçeleme kullanıcıları, bu açıklamaları bütçelerini düzenlemek veya onlara atanmış herhangi bir şeyi görüntülemek için açtıklarında göreceklerdir.

### <a name="copy-from-budget-plan-allocation"></a>Bütçe Planı tahsisatından kopyala

Yeni bir tahsisat yöntemi, bir üstten bir çocuk plana, hiyerarşideki ara seviyeden geçmeden dağıtmanıza izin verir. Bu yöntem, özellikle sadece bütçeleme ve onaylar için mali boyutlar oluşturan müşteriler için son derece kullanışlıdır.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Yeni bütçe kaynaklarından bütçe planı oluşturmak

Aşağıdaki seçenekler periyodik işlemler olarak eklendi. Bu seçenekler, başka bir modülde varolan verileri bir başlangıç noktası olarak kullanarak bir bütçe planı oluşturmanızı sağlar:

-   Talep Tahmininden Bütçe Planı oluştur
-   Tedarik Tahmininden Bütçe Planı oluştur
-   Projeden Bütçe Planı oluştur
-   Bütçe Kaydından Bütçe Planı oluştur

### <a name="more-complete-tracking-of-amounts"></a>Tutarların daha ayrıntılı izlemeleri

AX 2012'de bütçe planlama her bir değer için kaydedilmiş olan tek bir tutara sahipti. Finance'te veri modeli genişletildi. Şimdi her değer için muhasebe para birimi, hareket para birimi ve raporlama para birimi vardır. Yükseltme sırasında bu yeni sütunlar varolan veriler için otomatik olarak doldurulur.

### <a name="do-not-convert-currency-in-aggregation"></a>Toplamdaki para birimini dönüştürme

Genellikle bir çocuk plan bir üst düzeye toplandığında, tutarlar otomatik olarak hareket para biriminden, kuruluşun muhasebe para birimine dönüştürülür. **Toplamda para birimini dönüştürme** seçeneğini **Hayır** olarak işaretlerseniz, toplanan tutarlar orijinal para biriminde kalır. Bu nedenle, bu seçenek döviz kuru dalgalanmalarından etkilenenlerin daha kesin ayarlamalarını sağlar.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Bütçe planından bütçeye katkıda bulunan diğer modüllere geriye bakmak

Bütçe planları, talep veya tedarik tahminden, projelerden veya diğer alanlardan oluşturulabilir, Boyut kümesine göre bütçe planları sorgulaması bütçe planının kaynağı olan verileri belirlemeye yardımcı olması için sorguları yürütmenize olanak sağlayan çeşitli seçenekler içerir.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Tahsisat planları için planlama için üzerine yaz veya ekle

Dağıtılması gereken tutarlar için birden fazla kaynak varsa, tutarların ilave olacağını belirtebilirsiniz. Bu durumda, tutarlar mevcut tutarların üzerine yazmaz. Bunun yerine, mevcut tutarlara eklenir.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Bütçe planlama yapılandırması için varsayılan mali boyut kümesi

**Bütçe planlama yapılandırma** sayfası artık varsayılan mali boyut kümesini belirleyebileceğiniz bir alan içerir. Bu alan isteğe bağlı olsa da, bazı sorgular için gerekli olabilir. Boyut kümesine göre gruplama raporları için gruplama veya filtreleme istiyorsanız gerekli olabilir.

### <a name="data-entities"></a>Veri varlıkları

Bütçe planlamanı hızlı uygulamasını sağlamak için birden fazla veri varlığı eklenmiştir. Bu varlıklar, Excel üzerinden değişiklik yapmanıza da olanak sağlar. Bu nedenle, öğeleri istemci üzerinden birer birer oluşturmak zorunda kalmazsınız. Yeni veri varlıklarının bir listesi aşağıda verilmiştir:

-   Varlık adı
-   Bütçe parametreleri
-   Bütçe planı parametresi
-   Bütçe planı senaryoları
-   Bütçe planı aşamaları
-   Bütçe planı iş akışı aşaması
-   Bütçe planı tahsisat zaman çizelgeleri
-   Bütçe planı aşama tahsisatları
-   Bütçe planı öncelikleri
-   Bütçe planı sütunları
-   Bütçe planı düzen öğeleri






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]