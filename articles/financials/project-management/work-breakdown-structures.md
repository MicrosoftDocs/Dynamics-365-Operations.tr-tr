---
title: "İş kırılım yapıları"
description: "İş kırılım yapısı (WBS) bir projede yapılacak işin bir açıklamasıdır. Proje ekibinin iş bileşimi, her bir bileşen veya görevin boyut, maliyet ve süre anlayışını temsil eden bir görevler hiyerarşisidir."
author: KimANelson
manager: AnnBe
ms.date: 06/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8bc3d23fac6112622e722e57b61fdb686f5a98ed
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="work-breakdown-structures"></a>İş kırılım yapıları

[!include [banner](../includes/banner.md)]

İş kırılım yapısı (WBS) bir projede yapılacak işin bir açıklamasıdır. Proje ekibinin iş bileşimi, her bir bileşen veya görevin boyut, maliyet ve süre anlayışını temsil eden bir görevler hiyerarşisidir. Bir WBS'nin üç ana amacı vardır:

-   Görevlerdeki iş kırılımını bileşimini açıklamak.
-   Proje çalışmasını zamanlamak.
-   Her bir görevin maliyetini tahmin etmek.

Bir WBS'nin ayrıntı derecesi, tahminlerde gerekli olan kesinlik düzeyine ve bu tahminlerin gerektirdiği izleme düzeyine bağlıdır. Plan veya maliyet açısından hataya çok düşük bir toleransı olan projeler genellikle daha ayrıntılı bir WBS'yi ve bu WBS'ye göre, çalışmadaki ilerlemenin ve maliyetin dikkatli bir şekilde takibini gerektirir. Bu tür projeler inşaat ve mühendislik sektörlerinde yaygındır. 

Bunun tersine, medya ve reklam, yazılım ve BT altyapısı gibi sektörlerde projeleri benzersiz olma eğilimindedir ve verimlilik, görevi yürütenlerin deneyimine ve yetkinliğine bağlıdır. Bu nedenle, bu sektörlerde projedeki ilerlemenin ayrıntılı takibi değil de, projenin tahmini boyutunu veren bir WBS kullanılır. 

WBS oluşturma genellikle uzun dönemde yayılan yoğun bir süreçtir ve çok sayıda, farklı insanın işbirliğini ve bilgisini gerektirir. Bu konuda, Microsoft Dynamics 365 for Finance and Operations'ta, tahminler ve izleme için gereksinimlerinizi karşılayacak WBS ilerlemelerini nasıl kullanabileceğiniz açıklanmaktadır.

## <a name="prerequisites-for-creating-a-wbs"></a>WBS oluşturma önkoşulları
WBS oluşturmak için bir iş çizelgesi ve iş maliyeti çıkarabilmeniz gerekir.

### <a name="prerequisites-for-creating-a-work-schedule"></a>İş çizelgesi oluşturma önkoşulları

WBS özelliklerinin planlama yeteneklerinden tam olarak yararlanmak için aşağıdaki kurulumu tamamlayın:

1.  Birer varsayılan takvim ve proje takvimi ayarlayın:
    1.  **Proje yönetimi ve muhasebe** &gt; **Ayarla** &gt; **Proje yönetimi ve muhasebe parametreleri** &gt; **Zamanlama** üzerine tıklayın. **Varsayılan çalışma takvimi** alanında bir varsayılan takvim belirtin. Bu, oluşturulan her yeni proje için varsayılan çalışma takvimi olacaktır.
    2.  Belirli bir proje için varsayılan takvimi değiştirebilirsiniz. Proje ayrıntıları sayfasına tıklayın ve **Proje ekibi ve planlama** hızlı sekmesinde başka bir takvim seçerek **Planlama takvimi** alanını güncelleştirin.

2.  Standart çalışma günleri ve çalışma saatleri ayarlayın. Projeniz için çalışma takvimi olarak belirlediğiniz takvim, WBS'de aşağıdaki bilgileri belirlemek için kullanılır:

-   İş günleri ve tatiller
-   Günlük çalışma saati sayısı

Bir takvimin iş günlerini ve çalışma saatlerini ayarlamak veya yeni bir takvim oluşturmak için **Kuruluş yönetimi** &gt; **Ortak** &gt; **Takvimler**'e tıklayın.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Çalışma maliyetini tahmin etme önkoşulları

WBS'nin maliyet tahmini özelliklerinden tam olarak yararlanmak için, çalışanların maliyetlerini ve satış fiyatlarını, işçilik kategorilerini, giderleri, ücretleri ve maddeleri ayarlamanız gerekir.

-   İşçilik maliyet ve satış fiyatı, gider ve ücret kategorilerini ayarlamak için **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Fiyatlar**'a tıklayın.
-   Maddelerin maliyet ve satış fiyatlarını ayarlamak için, Ürün bilgileri yönetimi'nin **Serbest bırakılan ürünler** liste sayfasındaki **Ticari anlaşmalar** sayfasını kullanın.

## <a name="creating-a-wbs"></a>WBS oluşturma
WBS oluşturma işlemi üç faaliyeti kapsar:

1.  **İş ayrıştırma** – İşin parçalar ve görevler halinde bir kırılımını oluşturun.
2.  **İş çizelgesi** – Bir görevi tamamlamak için gereken süreyi tahmin edebilir, görev bağımlılıklarını ayarlayabilir, görevler için başlanıç ve bitiş tarihleri seçebilirsiniz.
3.  **Maliyet tahmini** – Her bir görev için maliyetleri tahmin edebilirsiniz.

WBS özelliklerinin bu faaliyetlerin her birinde nasıl yardımcı olabileceği aşağıdaki bölümlerde ele alınmaktadır.

### <a name="work-decomposition"></a>İş ayrıştırma

İş kırılımı veya ayrıştırması oluşturmak genellikle WBS oluşturma sürecinin ilk adımıdır. WBS işlevselliği, iş kırılımı veya ayrıştırma için aşağıdaki temel yapıları destekler. 

**Proje kök görevi** Proje kök görevi, bir projenin en üst düzey özet görevidir. Projedeki diğer görevlerin hepsi onun altında oluşturulur. Kök görev her zaman projenin adını alır. Kök düğümün iş gücü, tarihler ve süresi, kök görevin altındaki görelerin değerlerini özetler. Kök düğüm özelliklerini değiştiremez ve silemezsiniz.

**Özet veya kapsayıcı görevler** Özet görev, alt görevleri veya altında kurucu görevleri olan bir görevdir. Özet görevde kendine ait iş gücü veya maliyet yoktur. Bunun yerine, özet görevin iş gücü ve maliyeti, kendini oluşturan görevlerin iş gücü ve maliyetlerinin toplamıdır. Oluşturan görevlerin en erken başlangıç tarihi, özet görevin başlangıç tarihi olarak kullanılır ve oluşturan görevlerin en son bitiş tarihi, bitiş tarihi olarak kullanılır. Özet görevin adını değiştirebilirsiniz, ancak iş gücü, tarihler ve süre zamanlama özelliklerini değiştiremezsiniz. Bir özet görevi silerseniz, bu görevi oluşturan tüm görevler de silinir. 

**Alt düğüm görevleri** Alt düğüm, projedeki en küçük parçalı iş paketini temsil eder. Alt düğümde bir tahmini iş gücü, planlanan kaynak sayısı, planlanan başlangıç tarihi, bitiş tarihi ve süre vardır. 

Bir proje için iş hiyerarşisi veya ayrıştırma oluşturmayı etkinleştirmek için aşağıdaki hiyerarşi işlemlerini tamamlayabilirsiniz. 

**Yeni görev** Oluşturduğunuz her yeni görev, kök düğümün altına otomatik olarak eklenir ve göreve otomatik olarak WBS numarası atanır. WBS numarası, görevin hiyerarşideki düzeyini temsil eder. Proje kök görevi altındaki ilk düzey görevler için 1, 2, 3 şeklinde bir numaralandırma düzeni kullanılır. İlk düzeyin altındaki görevler için 1.1, 1.2, 1.3 şeklinde bir numaralandırma düzeni kullanılır. Bir önceki düzeyin altına eklenen her düzeye yeni bir noktalı numara dizisi eklenir. 

WBS numaralandırmasını şimdilik özelleştiremiyorsunuz. 

**Görevi girintile** Bir görevi girintilerseniz, kendisinden önceki görevin alt görevi haline gelir. Yeni alt görevin WBS numarası, yeni üst görevinin WBS numarasına göre otomatik olarak hesaplanır. Üst görev artık bir özet veya kapsayıcı görevdir ve bu nedenle, kendisini oluşturan görevlerin bir toplamı haline gelir. 

> [!NOTE] 
> Girintileme işleminden önce bir alt düğüm olan bir görev altındaki görevleri girintilediğiniz zaman, yeni oluşturulan özet görevin kendi tarihleri, iş gücü ve kaynak sayısı kaybolur. Artık, oluşturucu yeni görevlerinin değerlerinin özetini kullanır. 

**Görevin girintisini azalt** Bir görevin girintisini azalttığınızda, üst görevinin oluşturucusu olmaktan çıkar. Bu görevin WBS numarası, hiyerarşide görevin yeni düzeyini yansıtacak şekilde otomatik olarak yeniden hesaplanır. Görevin önceki üst görevinin iş gücü, maliyeti ve tarihleri, o eski üst görevi dışlamak üzere yeniden hesaplanır. 

**Yukarı taşı ve Aşağı taşı** **Yukarı taşı**'ya ve **Aşağı taşı**'ya tıkladığınızda, bir görevin konumunu üst öğesinin hiyerarşisi içinde değiştirebilirsiniz. Görevin konumu, o görevin iş gücü, maliyet, tarih veya süre bilgilerini etkilemez. Ancak, görevin WBS numarası, görevin yeni konumunu yansıtacak şekilde otomatik olarak yeniden hesaplanır.

### <a name="schedule-estimation"></a>Zamanlama tahmini

Zamanlama tahmini genellikle bir WBS oluşturmanın ikinci adımıdır. Görevleri oluşturduktan sonra zamanlama tahminini tamamlamanızı tavsiye ederiz. Finance and Operations'da **İş kırılımı yapısı** sayfasında iki bölüm vardır. Üst bölme zamanlama tahmini için kullanılırken, alt bölmede, maliyet tahmini için kullanabileceğiniz **Tahmini maliyetler ve gelirler** sekmesi bulunur. 
**Görev bağımlılıkları** WBS'de görevler arasında bir öncel ilişkisi oluşturabilirsiniz. Bir göreve öncel görevler atadığınız zaman, bu görev yalnızca tüm öncel görevleri tamamlandıktan sonra başlatılabilir. Görevin planlanan başlangıç tarihi, tüm öncellerinin en son tarihine otomatik olarak ayarlanır. 

**Microsoft Dynamics 365 for Finance and Operation görev zamanlama** Aşağıdaki etkenler, alt düğüm görevlerinin zamanlamasını belirler:

-   Önceller
-   Çalışma
-   Kaynak sayısı
-   Başlangıç ve bitiş tarihleri

Öncelleri olmayan bir alt düğüm görevinin başlangıç tarihi, projenin zamanlama başlangıç tarihine otomatik olarak ayarlanır. Bir alt düğüm görevinin süresi her zaman kendi başlangıç ve bitiş tarihleri arasındaki çalışma gün sayısı olarak hesaplanır. 

*<strong><em>Zamanlama kuralları</em></strong>* Otomatik zamanlama yardımcısı etkinleştirildiği zaman, alt düğüm görevleri için görev zamanlamasına aşağıdaki kurallar uygulanır:

-   Bir görevin başlangıç ve bitiş tarihleri, projenin zamanlama takvimine göre, çalışma günleri olmalıdır.
-   Öncelleri olan bir görevin başlangıç tarihi, öncellerinin en son bitiş tarihine otomatik olarak ayarlanır.
-   Bir görevin iş gücü, otomatik olarak aşağıdaki gibi hesaplanır:

Kişi sayısı × Süre × Proje takviminde standart bir iş gününde saat sayısı. 

Bazı durumlarda bu kurallardan sapmak isteyebilirsiniz. Finance and Operations'ın alt düğüm görevlerinin özelliklerini otomatik olarak ayarlamasını veya düzeltmesini önlemek için otomatik zamanlamayı devre dışı bırakabilirsiniz. Bir görev için, zamanlama kurallarının ihlaline neden olan bilgiler girdiğiniz zaman, görev için bir zamanlama hatası simgesi gösterilir. Zamanlama hatalarının görüntülenmesini istemiyorsanız, **Zamanlama hataları gösterilir**'e tıklayarak özelliği devre dışı bırakın. 

> [!NOTE] 
> Bir özet veya kapsayıcı görevin değerleri, otomatik zamanlama yardımcısının açık veya kapalı olmasına bakılmaksızın, kendisini oluşturan görevlerin değerlerinin toplamı olarak hesaplanmaya devam eder. 

**Zamanlama hatalarını düzeltme** Otomatik zamanlama yardımcısı açıkken zamanlama hatalarının oluşması olası değildir. Ancak, otomatik zamanlama yardımcısını kapatıp daha sonra yeniden açarsanız, WBS'de zamanlama hatası simgeleri görünebilir. 

**Zamanlama hatalarını göreve göre düzeltme** Belirli bir görevin zamanlama hatası simgesine çift tıklatığınızda, o görev için tüm zamanlama hatalarını görüntüleyen bir iletişim kutusu açılır. Görev için hangi zamanlama hatalarının düzeltileceğine karar verebilirsiniz. 

**Tüm zamanlama hatalarını düzeltme** Finance and Operations'ın WBS'deki tüm zamanlama hatalarını düzeltmesini istiyorsanız **Tüm zamanlama uyuşmazlıklarını düzelt**'e tıklayın. 

> [!NOTE] 
> Bu özellik WBS'de önemli değişikliklere neden olabilir. Hatalar aşağıdaki sıraya göre düzeltilir:

1.  Tüm görevlerdeki tahmini iş gücü değiştirilerek, proje takviminde tanımlanan kapasiteye eşit hale getirilir.
2.  Görevin başlangıç tarihi, görev tüm öncel görevleri tamamlandıktan sonra başlayacak şekilde değiştirilir.
3.  Her bir görevin başlangıç tarihi değiştirilerek, öncel görevlerin başlangıç tarihlerindeki boşluklar giderilir.

### <a name="cost-estimation"></a>Maliyet tahmini

Bu belgenin önceki bölümlerinde belirtildiği gibi, **İş kırılımı yapısı** sayfasının alt bölmesindeki **Tahmini maliyetler ve gelirler** sekmesini kullanarak her bir alt düğüm görevi için maliyet tahminlerini girersiniz. 

> [!NOTE] 
> Özet veya kapsayıcı görevin maliyet tahminini değiştiremezsiniz. Bir özet görevin maliyet tahmini, alt düğüm görevlerinin maliyet tahmini toplamına eşittir. Her bir görevin tahmini toplam maliyeti, aşağıdaki hareket türlerinin tahmini maliyet tutarlarının toplamı olarak hesaplanır:

-   İşgücü
-   Madde veya malzeme
-   Giderler

**Ücret** hareket türü, ücretli gelir tahmin etmek için kullanılır. Bu hareket türünün maliyet bileşeni yoktur ve maliyetlerin tahmini yapılırken hesaba katılmaz. 

**Açık hesap** hareket türü, sabit değer türünde bir projedeki sözleşmeli satış değerini kaydetmek için kullanılır. Maliyet tahminlerinde bu hareket türü de hesaba katılmaz. 

Her bir görevin işçilik, malzeme gider maliyetlerini tahmin ederken, tahmini maliyete bir proje kategorisi atamanız gerekir. 

**İşçilik maliyetlerini tahmin** Her alt düğüm görevi için, saat cinsinden bir iş gücü ve varsayılan bir kategori atayın. Böylece, bir görev için zamanlama ayarladığınızda, o görev için işçilik maliyeti tahmini, varsayılan işçilik kategorisine otomatik olarak eklenir. Bu maliyet tahmini, o görev için **Satır ayrıntıları** kılavuzundaki **Tahmini maliyetler ve gelir** sekmesinde görüntülenir. Daha fazla işgücü maliyeti tahminine ihtiyaç duyuyorsanız, bunları bu sekmede ekleyebilirsiniz. İşgücü maliyeti tahmininde saatleri azaltır veya artırırsanız, görev için planlama otomatik olarak yeniden hesaplanır. 

**Gider ve malzeme maliyetlerini tahmin** Tahminlere gereksiniminiz varsa, **Tahmini maliyetler ve gelir** sekmesi de bir görev için gider ve malzeme maliyetlerini tahmin etmenize olanak sağlar. 

Her bir işçilik veya gider satırının maliyet ve satış fiyatı, **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Fiyatlandırma** altındaki fiyatlandırma tablolarında her kategori için tanımlanmış olan kuruluma göre hesaplanır. Maddeler için, maliyet ve satış fiyatları maddeden veya Ürün bilgileri yönetimi'nin **Serbest bırakılan ürünler** liste sayfasındaki ticari anlaşmalardan varsayılan olarak eklenir.

## <a name="tracking-progress-on-the-wbs"></a>WBS'de ilerlemeyi izleme
Bazı sektörler bir projenin WBS'ye göre ilerlemesini çok ayrıntılı bir düzeyde izlerken, bazıları da ilerlemeyi WBS'nin daha yüksek düzeylerinde izler. Bu bölümde, proje gereksinimleriniz için WBS izlemeyi nasıl kullanabileceğiniz açıklanmaktadır. 

Bir proje WBS'si için Finance and Operations'ın üç görünümü vardır: Planlama görünümü, İş gücü izleme görünümü ve Maliyet izleme görünümü.

### <a name="planning-view"></a>Planlama görünümü

Planlama görünümünde, planlanan veya temel zamanlama ve maliyet tahmini bilgileri görüntülenir. Bir proje WBS'sinin sürümünü ve temelini izlemek için özellikler olmamasına karşın, bu görünümdeki değerlerin temel sürümü temsil etmesi amaçlanır. Bu konunun Zamanlama tahmini ve Maliyet tahmini bölümlerinde, bu görünüm ve bir WBS oluşturmak için görünümün nasıl kullanıldığı açıklanmaktadır.

### <a name="effort-tracking-view"></a>Çalışma izleme görünümü

İş gücü izleme görünümünde, WBS'deki görevlere ilişkin ilerleme izlemesi görüntülenir. Bu görünümde, bir görev için harcanmış gerçek iş gücü saat sayısı ve planlanan iş gücü saat sayısı karşılaştırılır. Aşağıdaki formüller, İş gücü izleme görünümündeki değerleri verir:

-   İlerleme yüzdesi = Görev için o tarihe kadar fiilen kullanılan iş gücü ÷ Planlanan iş gücü
-   Kalan iş gücü (Tamamlanma için tahmini gereken \[ETC\] olarak da bilinir) = Planlanan iş gücü – O tarihe kadar fiilen kullanılan iş gücü
-   Tahmini tamamlanma (EAC) = Kalan iş gücü + O tarihe kadar fiilen kullanılan iş gücü
-   Öngörülen iş gücü farkı = Planlanan iş gücü – EAC

İş gücü izleme görünümünde, görev için, EAC'nin planlanan iş gücünden daha az veya daha çok olmasına göre yapılan bir iş gücü farkı öngörüsü görüntülenir:

-   EAC planlanan iş gücünün üzerindeyse, görevin ilk planlanandan daha uzun zaman alacağı ve zamanlamanın gerisinde olduğu öngörülür.
-   EAC planlanan iş gücünün altındaysa, görevin ilk planlanandan daha az zaman alacağı ve zamanlamaya göre ileride olduğu öngörülür.

**İş gücü öngörüsünün proje yöneticisi tarafından yeniden hesaplanması** Bazen, proje yöneticisi veya proje ilerlemesini izleyen başka bir kişinin bir görevdeki ilk tahminleri gözden geçirmesi gerekir. Görev, çeşitli nedenlerle, ilk tahmin edilenden daha hızlı veya daha yavaş ilerleyebilir. Örneğin, kapsam daraltılmıştır veya çalışanların başlangıçta planlanandan daha az deneyimi vardır. Öngörüler, bir proje yöneticisinin, projedeki mevcut duruma göre tahminleri algılayışıdır. Genelde temel sayıları değiştirmeniz gerekmez çünkü proje temeli, projenin zamanlaması ve projedeki tüm paydaşların üzerinde anlaşmaya vardığı maliyet tahmini için iyi bir hazırlıkla yayınlanmış belgeyi temsil eder. 

Proje yöneticilerinin görevlerdeki iş gücünde değişiklik yapabilmesi için iki yol vardır:

-   Görevdeki fiili kalan iş gücünü güncelleştirmek için otomatik olarak ayarlanan kalan iş gücünde değişiklik yapmak.
-   Görevdeki gerçek ilerlemeyi güncelleştirmek için otomatik olarak ayarlanan ilerleme yüzdesinde değişiklik yapmak.

Bu yaklaşımlardan ikisi de görevin ETC, EAC ve ilerleme yüzdesi bilgilerinin ve görevde iş gücü için öngörülen farkın yeniden hesaplanmasına neden olur. Özet görevlerdeki EAC, ETC ve ilerleme yüzdesi de yeniden hesaplanır ve kendi öngörülen iş gücü farkları güncelleştirilir. 

**Özet görevlerde değiştirilen iş gücü** Özet veya kapsayıcı görevlerdeki iş gücünde değişiklik yapabilirsiniz. Özet görevlerde bu değerleri kalan iş gücüyle veya ilerleme yüzdesiyle değiştirmenizden bağımsız olarak, hesaplamalar otomatik olarak aşağıdaki sırada yapılır:

1.  Görevdeki EAC, ETC ve ilerleme yüzdesi hesaplanır.
2.  Alt görevlerde yeni EAC tutarı orijinal EAC tutarıyla aynı orantıda dağıtılır.
3.  Her bir alt düğüm görevinde yeni EAC hesaplanır.
4.  Etkilenen tüm alt görevlerin kalan iş gücü ve ilerleme yüzdesi, yeni EAC değerine göre yeniden hesaplanır. Görevlerin iş gücü farkı da yeniden hesaplanır.
5.  Özet görevlerin EAC'si de alt düğümlerden yeniden hesaplanır.

İş gücü izleme görünümünde **Düzeye genişlet**'e tıklayarak, WBS'nizin izleneceği ve korunacağı düzeyi ayarlayın. WBS, İş gücü izleme görünümünü açtığınızda, görünümdeki o düzeye kadar otomatik olarak genişletilir.

### <a name="cost-tracking-view"></a>Maliyet izleme görünümü

Maliyet izleme görünümünde, bir görevin maliyet tüketimi izlemesi görüntülenir. Bu görünümde bir görevin o tarihe kadar harcanan fiili maliyeti ve planlanan maliyeti karşılaştırılır. Aşağıdaki formüller, Maliyet izleme görünümündeki değerleri verir:

-   Tüketilen maliyet yüzdesi = Görev için o tarihe kadar harcanan fiili maliyet ÷ Planlanan maliyet
-   Tamamlama maliyeti (CTC) = Planlanan maliyet – O tarihe kadarki fiili maliyet
-   Toplam tamamlanma tahmini (EAC) = CTC + O güne kadarki fiili maliyet
-   Öngörülen maliyet farkı = Planlanan maliyet – EAC

Maliyet izleme görünümünde, görev için, EAC'nin planlanan maliyetten daha az veya daha çok olmasına göre yapılan bir maliyet farkı öngörüsü görüntülenir:

-   EAC planlanan maliyetin üzerindeyse, görevin ilk planlanandan daha fazla para tüketeceği ve bütçenin üzerinde olduğu öngörülür.
-   EAC planlanan maliyetin altındaysa, görevin ilk planlanandan daha az para tüketeceği ve bütçenin aşağısında olduğu öngörülür.

**Maliyet öngörüsünün proje yöneticisi tarafından yeniden hesaplanması** Proje yöneticileri bir göreve ilişkin ilk maliyet tahminini gözden geçirmek için CTC kullanmalıdır. Proje yöneticisi, CTC değerini, görevi tamamlamak için gereken maliyeti verecek şekilde değiştirebilir. CTC değerini değiştirirseniz, görevin CTC, EAC ve tüketilen maliyet yüzdesi bilgileri ve görev için öngörülen maliyet farkı yeniden hesaplanır. Özet görevlerdeki EAC, ETC ve tüketilen maliyet yüzdesi de yeniden hesaplanır ve kendi öngörülen maliyet farkı güncelleştirilir. 

> [!NOTE] 
> İş gücü izleme görünümünde bir WBS görevinin iş gücü bilgisini gözden geçirdiğiniz zaman, görevin CTC, EAC, tüketilen maliyet yüzdesi ve öngörülen maliyet farkı, Maliyet izleme görünümünde de yeniden hesaplanır. Ancak, maliyet gözden geçirme işlemleri, İş gücü izleme görünümündeki değerleri etkilemez çünkü hareket türüne göre (işçilik, malzeme, gider) maliyet veya proje kategorisi değiştirilmez. 

**Özet görevlerde maliyetlere ilişkin öngörülerin gözden geçirilmesi** Özet görevlerdeki maliyetleri gözden geçirdiğiniz zaman hesaplamalar otomatik olarak aşağıdaki sırayla yapılır:

1.  Göreve ilişkin EAC, CTC ve tüketilen maliyet yüzdesi yeniden hesaplanır.
2.  Alt görevlerde yeni EAC tutarı görevlerdeki orijinal EAC ile aynı orantıda dağıtılır.
3.  Her görev için yeni birer EAC hesaplanır.
4.  CTS ve tüketilen maliyet yüzdesi, etkilenen alt görevlerde, EAC değeri temel alınarak yeniden hesaplanır. Görevlerin maliyet farkı da yeniden hesaplanır.
5.  Tüm özet görevlerin EAC'si bu değişikliğe göre yeniden hesaplanır.

Maliyet izleme görünümünde **Düzeye genişlet**'e tıklayarak, WBS'nizin izleneceği ve korunacağı düzeyi ayarlayın. WBS, Maliyet izleme görünümünü her açtığınızda, görünümdeki o düzeye kadar genişletilir.

### <a name="earned-value-management"></a>Kazanılan değer yönetimi

Bir proje ilerlemesini izlemek için, kazanılan değer yöntemini (EVM) kullanabilirsiniz. Proje yöneticisinin Rol Merkezi'nde, kazanılan değer ölçümlerini görüntüleyebilirsiniz. Kazanılan değer grafik bileşeni, planlanan maliyetin ve fiili maliyetin zaman aşamalı değerlerini gösterir. Geçerli tarih itibariyle kazanılmış olan değer bir nokta olarak gösterilir. Kazanılan değer için zaman aşamalı veriler şimdilik kullanılamıyor. 

Kazanılan değer grafiğindeki zaman aşaması, hafta veya aya bazında görüntülenir. Bu bölümde EVM'nin üç sacayağı açıklanmaktadır: planlanan değer, kazanılan değer ve fiili maliyet. 

**Planlanan değer** EVM teorisine göre, grafikteki planlanan değer bölümü, proje ekibinin projeden kazanmayı planladığı değer oranını temsil eder. 

Finance and Operations planlanan değerin grafiğini çıkarırken, 0:100 kazanç kuralını kullanır. Bu kurala göre, görevin değeri, göreve bitiş tarihi itibariyle verilir. Görev yüzde 100 tamamlanana kadar hiçbir değer nakledilmez. 

Proje yönetimi ve muhasebe'de, alt düğümlerin bitiş tarihini ve bu tarih için planlanan maliyeti girersiniz. Planlanan değer grafiği hafta bazında görüntülendiğinde, planlanan değer proje süresince tüm alt düğüm görevleri için haftalık bazda özetlenir. 

**Kazanılan değer** EVM teorisine göre, grafikteki kazanılan değer bölümü, proje ekibinin projeden fiilen kazandığı değer oranını temsil eder. 

Finance and Operations kazanılan değerin grafiğini çıkarırken, 0:100 kazanç kuralını kullanır. Bu kurala göre, görevin değeri, göreve bitiş tarihi itibariyle verilir. Görev yüzde 100 tamamlanana kadar hiçbir değer nakledilmez. 

Kazanılan değer hesaplanırken, her görevin ilerleme yüzdesi dikkate alınır. 0:100 kazanç kuralına göre, bir dönemin bitişi itibarıyla kazanılan değer hesaplanırken yalnızca o dönem içinde tamamlanan görevler dikkate alınır. Projede kazanılan değer, grafik oluşturulduğu zaman tamamlanmış olan tüm görevler için hesaplanır. 

> [!NOTE] 
> Şimdilik, WBS izleme sisteminde her bir görevin geçmiş ilerleme yüzdelerini depolayacak veri yapıları yoktur. Bu nedenle, kazanılan değer yalnızca küpün işlendiği tarih itibarıyla bildirilebilir. Rol Merkezi'nde gösterilen kazanılmış değer verilerini güncelleştirmek için küpü düzenli olarak işleyin. 

**Fiili maliyet** EVM teorisine göre, grafikteki fiili maliyet bölümü, projede paranın harcandığı oranı temsil eder. 

Projeye nakledilen hareketler, fiili maliyet satırının grafiğini çıkarmak için kullanılır. Maliyetler tarihe göre özetlenir. Daha sonra bu veriler, kazanılan değer grafiğinde fiili maliyetlerin haftalık veya aylık temsilini çıkarmak için kullanılır.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Planlanan değer, kazanılan değer ve fiili maliyet kavramları nasıl kullanılır

**Zamanlama farkı** Planlama sırasında bir zaman çizelgesi üzerinde iş için tahmin oluşturursunuz. Bu nedenle, planlanan değer, proje planlayıcılarının projede tamamlanacağını düşündükleri iş oranıdır. Bir proje yürürlüğe girdikten sonra iş tamamlanır ve proje değer kazandırır. Planlanan değeri ve kazanılan değeri karşılaştırarak, projede işin ne kadar ilerlediğini görebilirsiniz. Bu karşılaştırmanın sonucuna zamanlama farkı denir. 

Bir dönem için planlanan değer, kazanılan değerden fazlaysa, projede tamamlanan işin tutarı, planlanan tutardan düşüktür. Bu nedenle, proje zamanlamanın gerisindedir. Planlanan değer ve kazanılan değer parasal terimlerle ifade edildiği için, projedeki gecikme süresine de bir parasal değer verilir. 

Bir dönem için planlanan değer, kazanılan değerden düşükse, projede tamamlanan işin tutarı, planlanan tutardan yüksektir. Bu nedenle, proje zamanlamanın ilerisindedir. Bu sağlama süresine de parasal bir değer verilir.

**Maliyet farkı** Kazanılan değer, maliyet fiyatını çarpan olarak kullandığı için, kazanılan değer, projede tamamlanan işin maliyetini gösterir. Proje ilerledikçe, hareket günlüğü bu projede fiilen harcanan para kaydını verir. Kazanılan değeri fiili maliyetle karşılaştırarak, harcanan para tutarını kazanılan değerle karşılaştırma halinde görüntüleyebilirsiniz. Bu karşılaştırmanın sonucuna maliyet farkı denir. 

Bir dönemde harcanan fiili maliyet, kazanılan değerden fazlaysa, kazanılandan daha fazla para harcanmıştır. Buna göre, proje bütçeyi aşmıştır. 

Bir dönemde harcanan fiili maliyet, kazanılan değerden azsa, harcanandan daha fazla para kazanılmıştır. Buna göre, proje bütçenin aşağısındadır.

## <a name="wbs-templates"></a>WBS şablonları
Projelere yönelik standart şablonlar oluşturmak için WBS şablonları işlevini kullanabilirsiniz. Şirketinizin sunduğu projeler yinelenebilir çok sayıda işi kapsıyorsa, bir WBS şablonu oluşturmayı düşünmelisiniz. 

Mevcut bir projenin WBS'sinden bir WBS şablonu oluşturarak, o projenin planlanması sırasında topladığınız bilginin ve en iyi uygulamaların ilerideki benzer projelerde yeniden kullanılabilmesini sağlayabilirsiniz. Ancak bazı durumlarda tüm WBS'yi şablon olarak kaydetmek anlamlı olmayabilir. Bu nedenle, bir projenin WBS'sinin bölümlerinden de şablonlar oluşturabilirsiniz.

### <a name="saving-a-projects-wbs-as-a-template"></a>Bir projenin WBS'sini şablon olarak kaydetme

Oluşturduğunuz şablonu yeni projenin WBS'sinde kök düğüm altına veya proje WBS'sindeki herhangi bir görevin altına alabilirsiniz.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Bir projenin WBS'sine WBS şablonu alma

Görevleri içe aktardığınız zaman, şablondaki görevler, altına alındıkları görevin başlangıç tarihine göre düzenlenir. Alma işlemi sırasında şablon görevlerindeki öncel ilişkileri, alınan görevler için başlangıç tarihlerini hesaplamada kullanılır. Hedef projenin standart çalışma takvimi, alınan görevlerin bitiş tarihlerini hesaplamak için uygulanır ve bu sayede, geçerli projenin çalışma takviminde tanımlanan iş günleri ve standart çalışma saatleri korunur. 

Tahmin satırlarındaki maliyet tutarları ve satış fiyatları, projeye veya proje sözleşmesine özel fiyatların tarihlerinin geçerli olmasını garantilemek için uygulanır.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Bir projenin WBS'si ile bir WBS şablonu arasındaki farklar

-   WBS şablonlarındaki görevlerin başlangıç ve bitiş tarihleri yoktur.

WBS şablonlarında iş günleri ve iş dışı günler ayarlanmaz.

-   WBS şablonları her zaman tüm projeler için varsayılan takvim olarak ayarladığınız zamanlama takvimini kullanır.

Varsayılan zamanlama takvimi yalnızca standart bir iş günündeki saat sayısını bulmak için kullanılır.

-   Öncel ilişkileri WBS şablonuna kopyalanmaz.

WBS şablonlarında tarih olmadığından, başlangıç tarihi mantığının bir öncelin bitiş tarihine bağlanması gerekmez.

-   WBS şablonunda bir görev oluşturulduğu zaman otomatik olarak bir işçilik maliyeti tahmin satırı oluşturulur. Satış fiyatı ve maliyet tutarı, seçili çalışandan kopyalanır.

Gider ve madde maliyetleri, tıpkı projenin WBS'sinde yapılabildiği gibi, el ile oluşturulabilir.

-   Aşağıdaki formülden sapmalar olduğunda zamanlama hataları görüntülenir:

Çalışma = Kaynak sayısı × Süre × Standart bir iş günündeki saat sayısı 

**Tüm zamanlama hatalarını düzelt**'e tıklayarak tüm zamanlama hatalarını bir defada düzeltebilirsiniz. 

Alternatif olarak, her görev için uyarı simgesine tıklayarak zamanlama hatalarını tek tek düzeltebilirsiniz.




