---
title: Master planlamayı ayarlama
description: Bu konu, master planlamayı ayarlamak için kullanılan çeşitli önemli stratejileri ve parametreleri açıklamaktadır.
author: t-benebo
manager: tfehr
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: a74d2987eac7409b5f576a52eccc37cf29566c7b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439112"
---
# <a name="set-up-master-planning"></a>Master planlamayı ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, master planlamayı ayarlamak için kullanılan çeşitli önemli stratejileri ve parametreleri açıklamaktadır. Master planlama tarafından kullanılan plan türlerine genel bakış içerir ve iş gereksinimlerinize bağlı olarak hangi plan stratejisini kullanmanız gerektiğini açıklar. Ayrıca, planı etkileyen başlıca parametreler açıklanır ve bu parametrelerin önerilen planlı siparişleri nasıl etkilediğini açıklar.

## <a name="types-of-master-plans"></a>Master plan türleri

Master planlamanın iki plan türü vardır: statik ve dinamik. Her tür farklı kullanım için tasarlanmıştır. En iyi performans için, senaryonuza uygun planı kullanmanızı öneririz.

### <a name="static-plan"></a>Statik plan

Bir sonraki master planlama çalıştırılıncaya kadar tedarikte ve talepte yapılan değişikliklerden bağımsız olarak statik plan değişmeden kalır.

Statik plan, önerilen siparişleri onaylamak ve kesinleştirmek için kullanılır. Çeşitli şirket personelinin kararlarına temel oluşturmak ve günlük görevlerle faaliyetleri yürütmek için (satın alan veya üretim planlayıcısı) kullanabilecekleri faaliyet planıdır.

Statik plan yeniden oluşturma desteği de destekler. Tümüyle yeni iyileştirilmiş plan, master planlama her çalıştırıldığında hesaplanır ve onaylanan mevcut siparişler silinir.

### <a name="dynamic-plan"></a>Dinamik plan

Dinamik plan genellikle statik planın bir kopyası olarak başlatılır, ancak master veriler her değiştiğinde güncelleştirilebilir. Örneğin, veriler değişirse yeni bir satış siparişi oluşturulur.

Dinamik plan, anlık planlama için kullanılır. Böylece, şirketin değişen sipariş ağını ve madde kullanılabilirliğini, diğer insanların iş işlemleri için kullandıkları statik planı bozmadan izlemesini sağlar. Özellikle teslim edilebilir miktara (CTP) göre kullanılır. Net gereksinimler sipariş sayfalarından (satış siparişi, satın alma siparişi veya üretim emri sayfaları gibi) açıldığında, dinamik plan varsayılan plandır.

Dinamik plan net değişim kullanır. Bu nedenle, çalışma süresinin daha hızlı olmasına yardımcı olur.

## <a name="strategies-for-using-master-plans"></a>Master planları kullanma stratejileri

Master planlama içinde bir veya iki plan kullanabilirsiniz. Kullanacağınız strateji iş gereksinimlerinize bağlıdır.

### <a name="one-plan-strategy"></a>Tek plan stratejisi

Tek plan stratejisi için, statik plan ve dinamik plana aynı master planı kullanırsınız. Bu strateji, genellikle bir siparişi yerine getiren bir planın benzetimini yapmak zorunda olmadığınız stoğa göre senaryolar için kullanılır.

Tek plana sahip strateji genellikle perakende ve dağıtım sektöründe veya satış teslimat tarihlerinin hizmet düzeyi sözleşmeleri (SLA'lar) teyit edildiğinde veya sağlama sürelerine göre kullanılır. Bu plan için teslimat tarihi kontrolü CTP olmadan kullanılabilir.

Benzetim yapmanız gerekiyorsa plan, benzetim gerektiren maddeler için yeniden çalıştırılabilir. Sipariş benzetimlerinin ürettiği planlı siparişler genellikle kesinleştirilir.

### <a name="two-plan-strategy"></a>İki plan stratejisi

İki plan stratejisi için statik bir plan ve farklı bir dinamik plan kullanırsınız. İki plana sahip strateji genellikle satış siparişi benzetimleri yapmak ve satış siparişleriyle ilgili tam teslimat tarihlerini hesaplamak zorunda olduğunuz, siparişe göre sipariş ve siparişe göre iş senaryoları için kullanılır, ancak hesaplamaların Gündelik işlemleri etkilememesi gerekir. Bu benzetim, dinamik planda her zaman yapılır. Örneğin, otomatik ve özgün donatım üreticisi (OEM) sektörleri için iki plan stratejisi yararlıdır.

İki plan stratejisi için teslimat tarihi kontrolü CTP kullanılabilir. CTP kullanıldığında, dinamik plandaki çalıştırmayı otomatik olarak tetikler.

### <a name="setting-up-the-plans"></a>Planlar ayarlanıyor

Planları **Master planlar** sayfasında oluşturabilirsiniz (**Master planlama \> Kurulum \> Planlar \> Master planlar**).

**Master planlama parametreleri** sayfasında **Geçerli statik master plan**'ı ve **Geçerli dinamik master plan**'ı ayarlayarak statik plan ve dinamil plan için hangi planların kullanılacağını belirleyebilirsiniz (**Master planlama \> Kurulum \> Master planlama parametreleri**). Tek planlı bir strateji kullanmak için **Geçerli statik master plan** ve **Geçerli dinamik master plan** alanlarında aynı planı seçin.

## <a name="types-of-planning-methods"></a>Planlama yöntemi türleri

Master planlama: yeniden oluşturma ve net değişimi çalıştırmak için üç hesaplama yöntemi kullanılabilir. Çalıştırıldığında her yöntem farklı bir plan oluşturur.

Planlama yöntemini **Master planlamayı çalıştır** iletişim kutusunda belirtirsiniz. Bu iletişim kutusunu açmak için **Master planlama \> Master planlama \> Çalıştır \> Master planlama**'ya gidin ya da **Master planlama** çalışma alanında **Çalıştır**'ı seçin.

### <a name="regeneration"></a>Yeniden oluşturma

Kesinleştirilmemiş ise yeniden oluşturma planlama yöntemi varolan planlı siparişleri siler. Tüm gereksinimleri temel alarak yeni planlı siparişler oluşturur. Yeniden oluşturma, statik planlar için kullanılabilen tek planlama yöntemidir.

- Tedarikdeki değişiklikler dikkate alınır. Bu değişiklikler tahmindeki değişiklikleri içerir.
- Bu yöntem **Dönem** kapsamı kodunu karşılamak için geçerlidir.
- Bu yöntem, ürün değiştirme işlevlerini (PI) destekler.

### <a name="net-change"></a>Net değişiklik

Net değişiklik planlama yöntemi, en son master planlama çalıştırılmasından sonra oluşturulan veya değiştirilen gereksinimleri kapsayacak planlı siparişler oluşturur. Bu yöntem çalıştırıldığında tedarikte değişiklik dikkate alınmaz. Sistem yeni bir kaynağı dikkate almıyorsa ve daha önce oluşturulan planlı siparişler artık gerekli değillerse silinmezler. Net değişiklik planlama yöntemi yeniden oluşturma yönteminden daha hızlı çalışır. Yalnızca dinamik planlar için kullanılabilir.

- Ancak, eylem tarihleri ve vadeli işlemler tüm gereksinimler için güncelleştirilir.
- Bu yöntem **Dönem** kapsamı kodunu karşılamak için geçerli değildir.
- Bu yöntem, planda seçilmiş olsa bile tahmini karşılamaz.
- Bu yöntem, ürün değiştirme işlevlerini (PI) desteklemez.

### <a name="net-change-minimized"></a>Minimize edilmiş net değişiklik

Net değişiklik minimize edilmiş planlama yöntemi, en son master planlama çalıştırılmasından sonra yalnızca oluşturulan veya değiştirilen gereksinimleri kapsayacak planlı siparişler oluşturur. Bu yöntemde net değişim yönteminden farklı olarak eylem tarihleri ve gelecekteki tarihler yalnızca yeni veya değiştirilmiş gereksinimler için güncelleştirilir. Bu planlama yöntemi yalnızca dinamik planlar için kullanılabilir.

## <a name="types-of-scheduling-methods"></a>Planlama yöntemi türleri

**Master planlar** sayfasının **Genel** hızlı sekmesindeki her bir plan için (**Master planlama \> Kurulum \> Planlar \> Master planlar**), üretim siparişleri için kullanılan planlama yönyemini seçmeniz gerekir. Üretimi operasyon düzeyinde ve iş düzeyinde planlayabilirsiniz.

### <a name="operations-scheduling"></a>İşlemleri planlama

Operasyon planlama çizelgelemesini zaman içinde üretim süresine dair genel bir tahmin yapmak için kullanabilirsiniz. Operasyon planlama üretim rotasının operasyonlarını işlere ayırmaz. Operasyonlar planlaması hakkında daha fazla bilgi için bkz [İşlemleri planlama](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>İş planlama

İş planlama her operasyonun bireysel görev veya işlere bölündüğü daha ayrıntılı bir planlama yöntemidir. İş planlama kapasite hakkında bilgi içerir. Bu, genellikle atölyedeki tek tek işleri anlık veya kısa bir zaman aralığında planlamak için kullanılır. İş planlama hakkında daha fazla bilgi için bkz [İş planlama](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Gün cinsinden zaman dilimleri

Her plan için, master planlama tarafından gelecekte çeşitli gereksinimlerin ve diğer hangi noktaların hesaplanması gerektiğini seçebilirsiniz. Bu dönem, *zaman dilimi* olarak bilinir. Master planlamada en iyi performans için, iş gereksinimlerinizi karşılamak üzere çeşitli zaman dilimleri ayarlamanızı öneririz. Her plan için zaman dilimlerini **Master planlar** sayfasındaki **Gün cinsinden zaman dilimleri** hızlı sekmesinde bulabilirsiniz (**Master planlama \> Kurulum \> Planlar \> Master planlar**).

> [!NOTE]
> Zaman dilimleri, çeşitli gereksinimlerin master planlama tarafından ne kadar ileride hesaplanacağını belirtir. Bu sayfada seçilen zaman dilimleri, kapsam grubunda tanımlanan süre içindeki saatleri geçersiz kılar. Bu, bir zaman dilimi seçeneğinin evet olarak ayarlanması ve bu günlerin kapsam grubunda tanımlanan zaman dilimini geçersiz kılacağı anlamına gelir. Hayır olarak ayarlandığında, zaman dilimi kapsam grubunda tanımlanacaktır. Son olarak, bir seçeneği kullanmak istemiyorsanız ya da ihtiyacınız yoksa (örneğin eylem iletilerini kullanmak istemiyorsanız) **Evet** olarak ayarlayın ve sonra zaman dilimini **0** (sıfır) güne ayarlayın.

### <a name="coverage"></a>Karşılama

Karşılama zaman dilimi, çizelge dönemini veya talebin ne kadar dahil edileceğini gösterir. Başka bir deyişle, planlama ufkunuzu gösterir.

**Karşılama** seçeneğini **Evet** olarak ayarlayıp master plan çizelgeleme sırasında madde için tanımlanan karşılama zaman dilimini geçersiz kılabilirsiniz. Bu durumda master planlama hesaplamasının gereklilikleri karşılaması gereken gün sayısını girin. Kapsam zaman dilimi geçerli tarihten ileriye doğru hesaplanır. Geçerli tarihten önceki gereksinimler her zaman işleme alınır.

> [!NOTE]
> Master planlamada en iyi performans için, planlama ufkunuza karşılama zaman dilimi ayarlamanızı öneririz.

### <a name="freeze"></a>Dondur

Dondurma zaman dilimi, yeni bir master planlama çalıştırıldığında mevcut planlı siparişlerin değiştirilmemesi durumunda geçen dönemi gösterir. Yeni planlı siparişler dondurulmuştur ve yeni planlı siparişler önerilmez.

**Dondurma** seçeneğini **Evet** olarak ayarlayıp master plan çizelgeleme sırasında madde için tanımlanan dondurma zaman dilimini geçersiz kılabilirsiniz. Bu durumda, planlama faaliyetinin dondurulduğu gün sayısı dondurulmuş olmalıdır. Bu dönem boyunca yeni planlı siparişlerin oluşturulmayacağını ve mevcut planlı siparişler değiştirilemeyeceğini unutmayın.

### <a name="firming"></a>Kesinleştirme

Kesinleştirme zaman dilimi, lanlı siparişlerin otomatik olarak üretime ve satınalma siparişlerine dönüştürüldüğü zamanı gösterir. Bu işlem, *planlı siparişlerin otomatik olarak kesinleştirilmesi* olarak da bilinir.

**Kesinleştirme** seçeneğini **Evet** olarak ayarlayıp master plan çizelgeleme sırasında madde için tanımlanan kesinleştirme zaman dilimini geçersiz kılabilirsiniz. Bu durumda , planlanan satınalma ve planlı üretim emirlerinin otomatik olarak kesinleştirileceği gün sayısını girin. Kesinleştirme zaman dilimi master planlama tarihinden ileriye doğru hesaplanır. Planlanan bir satınalma siparişinin otomatik olarak kesinleştirilmesi için bir maddenin bir satıcı ile ilişkilendirilmesi gerekir.

### <a name="forecast-plan"></a>Tahmin planı

Sabit tahmin planı zaman dilimi, gelecekteki master planlamanın ne kadar önceden talep görmüş maddelere yönelik planlı siparişler oluşturduğunu gösterir.

**Tahmin planı** seçeneğini **Evet** olarak ayarlayıp master planlama çizelgeleme sırasında madde için tanımlanan tahmin planı zaman dilimini geçersiz kılabilirsiniz. Bu durumda, tahmin planındaki satış tahmininin master planlamasına dahil edildiği gün sayısı girilmelidir.

### <a name="capacity"></a>Kapasite

Kapasite zaman dilimi, sipariş zamanlarken sistemin, kaynaklarınızın maksimum kapasitesini ne kadar dikkate aldığını belirtir. Başka bir deyişle plan, üretim emirlerini maddelerin üretim rotasını kullanarak planlar ve her kaynağın üretim rotası kaynaklarını ve maksimum kapasitesini dikkate alır.

**Kapasite** seçeneğini **Evet** olarak ayarlayıp master planlama sırasında madde için tanımlanan kapasite zaman dilimini geçersiz kılabilirsiniz. Bu durumda, planlı üretim emirleri için planlanan kapasitenin gün sayısı girilmelidir. Master planlamada maddenin etkin üretim rotası kullanılır ve gereksinim tarihinden geriye doğru plan çizelgelemesi yapılır. Planlı üretim emrinin gereksinim tarihi kapasite zaman diliminin dışında kalırsa sağlama süresi maddenin teslim süresine göre belirlenir. Kapasite zaman dilimi geçerli tarihten ileriye doğru hesaplanır.

### <a name="action-message"></a>Eylem iletisi

Eylem iletileri, tedarik planının en iyi duruma getirilmesine yardımcı olmak için varolan tedarik siparişine yapılabilecek değişiklikleri önerir. Örneğin, siparişleri ilerletmenizi, ertelemenizi veya sipariş miktarlarını artırmanızı ya da azaltmanızı tavsiye edebilir.

**Eylem iletisi** seçeneğini **Evet** olarak ayarlayıp master planlama sırasında madde için tanımlanan eylem iletisi zaman dilimini geçersiz kılabilirsiniz. Bu durumda, gereksinimler için master planlama eylem iletilerinin oluşturduğu gün sayısı girilmelidir. Eylem iletisi zaman dilimi geçerli tarihten ileriye doğru hesaplanır.

Eylem hakkında daha fazla bilgi için, bkz. [Eylem iletileri](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Eylem iletilerinin hesaplanması master planlama için daha uzun süre çalışma süresine neden olur. Eylem iletileri düzenli olarak analiz edilmez ve uygulanmazsa (günlük, haftalık, vb.), master planlama çalıştırması sırasında hesaplamayı kapatmayı düşünebilirsiniz. Hesaplamayı kapatmak için **Master planlar** sayfasından **Eylem iletisi** zaman dilimini çalıştırdığınız master plan için **0** (sıfır) olarak ayarlayın. Ayrıca, tüm kapsam grupları için **Êylem iletisi** ayarının kapatılmış olduğundan da emin olun.

### <a name="calculated-delays"></a>Hesaplanan gecikmeler

Gelecekte planlı siparişlerdeki olası gecikmelerin ne kadar algılandığını ve rapor edilebilir olduğunu belirtebilirsiniz. Bu şekilde, olası (gecikmeli) teslim tarihlerini zamanlayabilirsiniz.

Talep edilen tarihte planlı bir sipariş yerine getirilemiyorsa bir işlem için teslim sürelerine, malzeme ve kapasite kullanılabilirliğine bağlı olarak en erken yerine getirmek için planlanır.

### <a name="approved-requisitions-time-fence"></a>Onaylanmış talepler zaman dilimi

Master planlama talebini, talep amacı için planlı siparişler oluşturmak üzere ayarlayabilirsiniz. **Master** planlar sayfasındaki **Genel** hızlı sekmesinden **Talepleri dahil et** seçeneğini **Evet** olarak ayarlayın. Daha sonra, onaylı bir talebin amacı stok yenileme ise master planlama bunu yerine getirmek için otomatik olarak ilgili planlı siparişi oluşturur. Stok yenileme yöntemi, kuruluşunuzdaki maddeler için ayarlanmış tedarik ilkeleriyle belirlenir. Stok yenileme talebi oluşturulduktan ve onaylandıktan sonra ek bir kullanıcı eylemi gerekmez.

**Onaylı taleplerin zaman dilimi** seçeneğini **Gün cinsinden zaman dilimleri** hızlı sekmesinde **Evet** olarak ayarlayarak master planlama sırasında madde içi tanımlanan onaylı taleplerin zaman dilimini geçersiz kılabilirsiniz. Bu durumda, stok yenileme amacı bulunan onaylı taleplerin master planlamaya dahil edildiği geçmişteki gün sayısı girilmelidir. Örneğin, yalnızca son 10 günde oluşturulan onaylanmış taleplerden karşılanan, yerine getirilmeyen, geçmiş vadedeki talebin dikkate alınması ve planlanması gerektiğini belirtebilirsiniz.

### <a name="sequencing"></a>Sıralama

Sıralama, planlanan siparişlerin bitmiş ürünle ilişkilendirilmiş sıralama özniteliklerine dayalı olarak düzenlenmesini sağlar. Genellikle üretim emirlerini paketleme için hazırlamak amacıyla kullanılır. Örneğin, renk ve boyut temelinde belirli bir sırada kutular paketlenebilecek şekilde kullanılabilir.

**Sıralama** seçeneğini **Evet** olarak ayarlayarak işlemlerin veya işlerin ne kadar ileride sıralı alınacağını belirtebilirsiniz. Zaman dilimi ne kadar büyük olursa o kadar uzun bir süre için master planlama yapılacağını unutmayın.

### <a name="calculated-delays"></a>Hesaplanan gecikmeler

Gecikme seçenekleri, siparişlerin uygulanabilir planlanmış tarihlere sahip olmasını sağlamaya yardımcı olur. Aşağıdaki seçenekler **Master planlar** sayfasında **Hesaplanan gecikmeler** hızlı sekmesinde bulunur.

- **Planlı siparişlerin Master planlama çalıştırma tarihinden önce oluşturulmamasını sağlayın** – Siparişlerin geçmiş tarihlere göre zamanlanmamasını sağlamak için bu seçeneği **Evet** olarak ayarlayın.
- **Hesaplanan gecikmeyi gereksinim tarihine ekleyin** (**Planlanan satınalma siparişleri** altında) – hesaplanan gecikmeyi gereksinimlere eklemek için bu seçeneği **Evet** olarak ayarlayın.
- **Hesaplanan gecikmeyi gereksinim tarihine ekleyin** (**Planlı ürün emri** altında) – hesaplanan gecikmeyi gereksinimlere eklemek için bu seçeneği **Evet** olarak ayarlayın.
- **Hesaplanan gecikmeyi gereksinim tarihine ekleyin** (**Planlanan transfer** altında) – hesaplanan gecikmeyi gereksinimlere eklemek için bu seçeneği **Evet** olarak ayarlayın.
- **Hesaplanan gecikmeyi gereksinim tarihine ekleyin** (**Planlı kanban** altında) – hesaplanan gecikmeyi gereksinimlere eklemek için bu seçeneği **Evet** olarak ayarlayın.

**Hesaplanan gecikmeyi gereksinim tarihine ekle**'diğinizde , hesaplama gecikmesini gereksinim tarihi seçeneklerine **Evet** olarak ayarladığınızda, sistem kaynakların kapasitesini dikkate alır ve uygulanabilir planlı siparişler oluşturur. Planlı sipariş tarihlerinin yeniden hesaplanması, master planlama için çalışma süresini arttırır. Bu nedenle, gecikmeleri kullanmanız gerekmiyorsa seçenekleri **Hayır** olarak ayarlayın.

## <a name="positive-and-negative-days"></a>Pozitif ve negatif günler

Pozitif ve negatif günler, master planlamanın planlı siparişler ve eylemler için nasıl önerdiğini etkiler. Pozitif ve negatif günler maddenin madde karşılama grubunda ayarlanır. Çeşitli karşılama gruplarını ve bunlarını parametrelerini **Karşılama grupları** sayfasından ayarlayabilirsiniz (**Master planlama \> Kurulum \> Karşılama \> Karşılama grupları**).

### <a name="positive-days"></a>Artı günler

Pozitif günler gelecekteki master planlamanın gelecekteki bir talebi yerine getirmek için geçerli stoğun veya girişlerin ne kadar dikkate alınacağını gösterir. Örneğin, artı günler **100** olarak ayarlanmışsa sonraki 100 günde talebi karşılamak için geçerli stok kullanılabilir. Geçerli tarihten itibaren bir siparişin 150 gün varsa madde için eldeki stok, siparişi karşılayabilse bile master planlama bu talebi karşılamak için bir planlı sipariş oluşturur. Kısa teslim süresi olan hızlı hareket eden maddeler için, gelecekte stoktaki bir sipariş için eldeki stoğu kullanmak istemeyebilirsiniz. Bu hızlı taşıma olayında, eldeki geçerli stok hızlı şekilde biter ve daha fazla sipariş gelecekte, gelecek bir talebi zamanında karşılamak için yerleştirilir, böylece maddeyi kısa süre içinde teslim etmek mümkün olur.

Pozitif günler eylem iletilerini de etkiler. Örneğin, sistem, planlı bir satınalma siparişini daha sonra pozitif günlerin sayısı içinde bulunan bir talep içerecek şekilde artırmanızı önerebilir. Pozitif günler **100** olarak ayarlanmışsa ve geçerli tarihten itibaren 30 gün içinde bir madde için talep varsa sistem bu talebi karşılamak için planlı sipariş oluşturur. Geçerli tarihten itibaren 90 gün içinde aynı madde için talep varsa sistem sipariş miktarını geçerli tarihten 30 gün içinde artırmanız için siparişin aynı zamanda 90 gün içinde talebi kapsadığı şekilde kullanmanızı önerir. Ancak, geçerli tarihten itibaren 150 gün içinde madde için talep varsa sistem zaten planlanan sipariş miktarını artırmanızı önermez. Bunun yerine, yeni bir planlı sipariş oluşturulur.

Kural olarak, pozitif günler maddelerin en uzun sağlama süresi ile karşılama zaman dilimi arasında bir sayıya ayarlanır. Pozitif günlerin maddenin teslim süresine eşit olduğu bir karşılama grubuna düzenli olarak tedarik edilen veya üretilen maddeleri atamanızı öneririz.

### <a name="negative-days"></a>Eksi gün sayısı

Negatif günler geç madde girişlerinin izin verilen miktarını belirtir. Negatif stoğunuz olduğunda veya yeterli stoğunuz olmadığınıda yeni bir stok yenileme siparişi vermeden önce beklemek istediğiniz gün sayısını temsil eder. Negatif günler soruyu yanıtlıyor, Madde için yeni bir satınalma siparişi oluşturmalı mıyız, yoksa ürünün gecikeceğini bilmemize rağmen var olan bir satınalma mı kullanmalıyız?

Örneğin, geçerli tarihten 15 gün önce bir ürün için bir satış siparişi aldınız. Aynı madde için bir satın alma siparişiniz de var. Bu satınalma siparişi geçerli tarihten itibaren 20 gün içinde alınacak. Sistemin o satış siparişi için bir satınalma siparişi oluşturmasını mı yoksa satış siparişini zamanında yerine getiremeseniz de varolan siparişi kullanmasını mı istiyorsunuz? Maddenin maksimum beş güne ertelenmesini belirtmek için negatif günler **5**'ten az olarak ayarlanmışsa sistem satış siparişini karşılamak için yeni bir planlı satınalma siparişi oluşturur. Negatif günler **5**'ten büyük olarak ayarlanmışsa sistem madde için varolan siparişi kullanır.

Negatif günler, master planlamanın performansını da etkiler. Negatif günler yüksek sayıya ayarlanmışsa birçok eylem iletisi oluşturulur.

Negatif günleri maddenin sağlama süresinden daha az olan bir sayıya ayarlamanız önerilir.

### <a name="dynamic-negative-days"></a>Dinamik negatif günler

Dinamik negatif günler, maddenin teslim süresini ve belirttiğiniz negatif günleri dikkate alır. Sistem, aşağıdaki formülü kullanılarak hesaplanan negatif günler zaman dilimini temel alarak, yeni bir planlı satınalma siparişi oluşturacak:

Sağlama süresi + Negatif günler + Geçerli tarih – Gereksinim tarihi

Sistem yalnızca bu zaman dilimi içindeki planlı tedarik siparişlerini kullanır ve dışında yeni bir planlı sipariş oluşturur. Dinamik negatif günlerin avantajı, bireysel ürün teslim süresini, geçerli siparişlerin tekrar kullanılmasını ve teslim süresinden kaynaklanan gecikmeler nedeniyle daha sonraki bir gün sona erecek yeni planlı siparişlerin yaratılmasını önlemeyi içermesidir. 

Daha fazla bilgi için, bkz. [Negatif günler ve dinamik negatif günler](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]