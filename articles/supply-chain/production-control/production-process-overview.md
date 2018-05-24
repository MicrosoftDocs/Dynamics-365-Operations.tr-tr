---
title: "Üretim sürecine genel bakış"
description: "Bu konuda, üretim işlemleri hakkında genel bir bakış verilmektedir. Bu, sipariş oluşturulmasından mali dönem kapanışına dek üretim emirlerinin, toplu iş emirlerinin ve kanbanların çeşitli aşamalarını açıklamaktadır."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8a12627db93b131450015539bb92ea4780518ed3
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="production-process-overview"></a>Üretim sürecine genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda, üretim işlemleri hakkında genel bir bakış verilmektedir. Bu, sipariş oluşturulmasından mali dönem kapanışına dek üretim emirlerinin, toplu iş emirlerinin ve kanbanların çeşitli aşamalarını açıklamaktadır. 

Üretim yaşam döngüsü olarak da bilinen bir süreç olan ürün üretimi, bir maddenin üretimini tamamlamak için gereken belirli adımları izler. Yaşam döngüsü, üretim emri, toplu iş emri veya kanban oluşturulması ile başlar. Müşteriye veya başka bir üretim aşamasına hazır, bitmiş, mamul bir madde ile sona erer. Sürecin tamamlanabilmesi için, yaşam döngüsündeki her adımda farklı türde bilgiler gerekir. Adımlar bir bir tamamlandıkça, üretim emri, toplu iş emri veya kanban üretim durumunda bir değişikliği gösterir. Farklı türdeki ürünler, farklı imalat süreçleri gerektirirler.  

**Üretim kontrolü** modülü, **Ürün bilgileri yönetimi**, **Stok yönetimi**, **Genel muhasebe**, **Ambar yönetimi**, **Proje muhasebesi** ve **Organizasyon yönetimi** gibi diğer modüllerle bağlantılıdır. Bu entegrasyon, mamul maddenin üretimini tamamlamak için gereken bilgi akışını destekler.  

Üretim süreci, tipik olarak belirli bir üretim süreci için seçilen maliyet muhasebesi ve stok değerleme yöntemlerinden etkilenir. Finance and Operations, hem fiili maliyeti (ilk giren ilk çıkar \[[FIFO]\]; son giren ilk çıkar \[[LIFO]\]; hareketli ortalama ve periyodik ağırlıklı ortalama) hem de standart maliyet yöntemlerini destekler. Yalın imalat, geriye dönük maliyetlendirme ilkesine dayalı olarak uygulanır.  

Maliyet ölçümü yöntemlerinin tercihi, üretim süreci esnasında malzeme ve kaynak tüketimi hakkındaki raporlara yönelik gereklilikleri de belirler. Tipik olarak, fiili maliyet yöntemleri, iş düzeyinde isabetli raporlama gerektirirken, periyodik maliyetlendirme yöntemleri malzeme ve kaynak tüketiminin daha az ayrıntılı raporlanabilmesine imkan verir.

## <a name="mixed-mode-manufacturing"></a>Karma mod üretim
Farklı ürünler ve üretim topolojileri, farklı sipariş türleri uygulanmasını gerektirir. Finance and Operations, karma modda çeşitli sipariş türlerini uygulayabilir. Diğer bir deyişle, bir bitmiş ürün üretme uçtan uca işlemi sırasında tüm sipariş türleri gerçekleşebilir.

-   **Üretim emri** – Bu, belirli bir ürünü veya ürün varyantını verili bir miktarda ve belirli bir tarihte üretmeye yönelik klasik emir türüdür. Üretim emirleri, ürün reçetelerini (BOM) ve rotaları temel alır.
-   **Toplu iş emri** – Bu emir türü, imalat dönüştürmenin bir formüle dayalı olarak yapıldığı veya ortak ürün ve yan ürünlerin ana ürüne ek olarak veya ana ürün yerine son ürün olabildiği işlem endüstrileri ve kesikli işlemler için kullanılır. Toplu iş emirleri **Formül** türü ürün reçeteleri ve rotaları kullanırlar.
-   **Kanban** – Kanbanlar, üretim akışlarına, kanban kurallarına ve ürün reçetelerine dayalı tekrarlı yalın imalat süreçlerini işaret etmek için kullanılırlar.
-   **Proje** – Bir imalat projesi, ürün ve hizmetleri verili bir zaman çizelgesi ve bütçe ile birleştirir. Bir projenin imalat kısmı, diğer sipariş türlerinden herhangi bir üzerinden temin edilebilir.

## <a name="manufacturing-principles"></a>İmalat ilkeleri
Belirli bir ürün ve ilişkili pazar için uygun imalat ilkesini seçmek için, üretim ve lojistik gerekliliklerinin yanı sıra teslimat sağlama süreleri konusundaki müşteri beklentilerini dikkate almanız gerekir.

-   **Stoka aktar** – Bu, ürünlerin, tahmini veya asgari stok dolumuna dayalı olarak (ikincisi tipik olarak tahmine veya geçmiş tüketime dayalı olarak hesaplanır) stok için üretildiği klasik imalat ilkesidir.
-   **Siparişe göre üretim** – Standart ürünler, siparişe göre üretilir veya siparişe göre bitirilir. Ön üretim, Stoka aktar ilkesi kullanılarak yapılabilmesine rağmen, bir satış emri veya transfer emri tarafından değer zincirinin pahalı adımları veya varyantlar oluşturan adımlar tetiklenir.
-   **Siparişe göre yapılandır** – Siparişe göre üretim için olduğu gibi, değer zincirinin nihai işlemleri, siparişe göre yapılır. Üretilen gerçek ürün varyantı önceden tanımlı değildir, satış ürününün yapılandırma modeline dayalı olarak sipariş girişi zamanında oluşturulur. Siparişe göre yapılandır ilkesi, verili bir ürün hattı için belirli bir düzeyde süreç tekleşmesi gerektirir.
-   **Siparişe göre mühendislik** – Siparişe göre mühendislik süreçleri, tipik olarak bir proje üzerinden ele alınırlar ve genellikle mühendislik aşamasıyla başlarlar. Mühendislik aşamasında, siparişi karşılamak için gereken gerçek ürünler tasarlanıp ve açıklanır. Daha sonra ürünleri üretmek için üretim emirleri, toplu iş emirleri veya kanban'lar oluşturulabilir.

## <a name="overview-of-the-production-life-cycle"></a>Üretim yaşam döngüsüne genel bakış
Üretim yaşam döngüsündeki takip eden adımlar, tüm karma mod imalat türleri için gerçekleşebilir. Ancak, bunların tümü açık bir sipariş durumu olarak temsil edilmez.

1.  **Oluşturuldu** – El ile bir üretim emri, toplu iş emri veya kanban oluşturabilir ya da sistemi bunları çeşitli talep sinyallerine dayalı olarak üretecek şekilde yapılandırabilirsiniz. Master planlama, planlı siparişleri kesinleştirerek üretim emirleri, toplu iş emirleri veya kanban'lar oluşturur. Diğer talep sinyalleri, diğer üretim emirlerinden ya da kanban'lardan olan satış siparişleri veya ilişkilendirilmiş tedarik sinyalleridir. Sabit miktarlı kanban'lar için, kanban'lar boş olarak kaydedildiğinde talep sinyalleri üretilir.
2.  **Tahmini** – Malzeme ve kaynak tüketimi için tahminler hesaplayabilirsiniz. Tahmin, **Siparişe göre** durumuna sahip hammaddeler için stok hareketleri üretir. Ana ürünler, ortak ürünler ve yan ürünlere ilişkin girişler üretim emirleri veya toplu iş emirleri tahmin edilirken oluşturulur. Ürün reçetesinde **İlişkilendirilmiş tedarik** türü satırları varsa, malzemeler için satınalma siparişleri veya taşeron işlem hizmetleri oluşturulur ve üretim emri ya da toplu iş emri ile ilişkilendirilir. Maddeler veya siparişler, üretim emrinin rezervasyon stratejisine göre rezerve edilir ve bitmiş malların fiyatı parametre ayarlarına dayalı olarak hesaplanır.
3.  **Planlanan** – Üretimi operasyonlara, tek tek işlere veya ikisine birden dayalı olarak planlayabilirsiniz.
    -   **Operasyon planlaması** – Bu planlama yöntemi kaba hatlarıyla uzun vadeli bir plan sağlar. Bu yöntemi kullanarak üretim emirlerine başlangıç ve bitiş tarihleri atayabilirsiniz. Üretim emirleri rota operasyonlarına eklendiyse, bunları maliyet merkezi gruplarına atayabilirsiniz.
    -   **İş planlaması** – Bu planlama yöntemi ayrıntılı bir plan sağlar. Her bir operasyon belirli tarihlere, saatlere ve atanan operasyon kaynaklarına sahip ayrı ayrı işlere ayrılır. Sonlu kapasite kullanılıyorsa, işlere karşılanabilirlik temelinde operasyon kaynağı atanır. Planlamayı bir Gantt grafiğinde görebilir ve değiştirebilirsiniz.
    -   **Kanban planlaması** – Kanban işleri, kanban planlama panosunda planlanır veya kanban kurallarının otomatik planlama yapılandırmasına dayalı olarak otomatik olarak planlanır.

4.  **Serbest** – Planlama bittiğinde ve malzeme alınmaya ya da hazırlanmaya hazır olduğunda üretim emrini veya toplu iş emrini serbest bırakabilirsiniz. Malzeme kullanılabilirliği kontrolü, atölye süpervizörünün malzemenin üretim emirleri veya toplu iş emirleri için kullanılabilirliğini değerlendirmesine yardımcı olur. Çekme listeleri, iş kartı, rota kartı ve rotadaki iş gibi üretim emri belgelerini yazdırabilmeniz de mümkündür. Üretim emri serbest bırakıldığında, emrin durumu üretimin başlayabileceğini belirtecek şekilde değişir. Ambar yönetimi kullanılırken, üretim emrinin veya toplu iş emrinin serbest bırakılması, üretim ürün reçetesi satırlarının ambar yönetimine serbest bırakılmasını sağlar. Ardından ambar dalgaları ve ambar çalışması ambar kurulumuna göre üretilir.
5.  **Hazırlanan**/**Çekilen**– Tüm malzeme ve kaynaklar üretim konumunda hazırlandığında, üretim ürün reçetesi satırları veya kanban satırlarının durumu **Çekilen** olarak güncellenir. İlişkilendirilen tedarik siparişleri ve ilgili ambar çalışması genellikle bu aşamada tamamlanır. Üretimin geldiği aşamayı rapor etmek için gereken kanban kartları veya iş kartları atanmalı ve yazdırılmalıdır.
6.  **Başladı** – Üretim emri, toplu iş emri veya kanban başlatıldığında, malzeme ve kaynak tüketimini emre göre rapor edebilirsiniz. Sistem, emir başlatıldığında emre tahsis edilecek malzeme ve kaynak tüketimini otomatik olarak deftere nakledecek şekilde yapılandırılabilir. Bu tahsisat, ön malzeme çekme, ileri otomatik tüketim veya otomatik tüketim olarak bilinir. Ek çekme listesi günlükleri oluşturarak malzemeleri üretim emirlerine veya toplu iş emirlerine el ile tahsis edebilirsiniz. Ayrıca emre işgücü ve diğer rota maliyetlerini el ile tahsis edebilirsiniz. Operasyon planlaması kullanıyorsanız, bu maliyetleri bir rota kartı günlüğü oluşturarak tahsis edebilirsiniz. İş planlaması kullanıyorsanız, maliyetleri bir iş kartı günlüğü oluşturarak tahsis edebilirsiniz. Üretim emirleri veya toplu iş emirleri istenen nihai miktarın toplu işlerinde başlatılabilir. Bir üretim emri, toplu iş emri veya kanban dahilinde, oluşturulan işler günlükler, imalat icra terminali (MES terminali) ya da kanban panoları üzerinden ayrı ayrı başlatılabilir ve raporlanabilir.
7.  İlerleme raporu/**Tamamlanmış** işler – Üretim ilerlemesini işe veya kaynağa göre raporlamak için MES Terminalini, üretim günlüklerini, kanban panolarını veya mobil tarama özelliklerini kullanın. Malzeme ve kaynak tüketimi deftere nakledilecektir ve ilgili kanbanların, üretim emirlerinin ve toplu iş emirlerinin durumu **Alındı** veya **Bitmiş olarak raporlandı** şeklinde güncellenebilir. Ambar yapılandırmasına bağlı olarak ambar için yerine koyma çalışması oluşturulabilir.
8.  **Bitmiş olarak raporlandı** (ürün girişi) – Bir üretim emri veya toplu iş emri bitmiş olarak raporlandığında, tamamlanan bitmiş malların miktarı stokta güncellenir. Bu miktar ilgili ortak ürünlerin ve yan ürünlerin miktarını içerir. Süren iş muhasebesini kullanıyorsanız, süren iş hesaplarını düşürmek ve bitmiş mal stokunu yükseltmek için bir genel muhasebe günlüğü üretilir. Bir üretim emrinin maliyeti hesaplanırken, üretimin fiili maliyeti deftere nakledilir. Üretimle ilişkilendirilen malzeme ve işgücü maliyetleri önceden bir günlükte veya "ön malzeme çekme" yoluyla tahsis edilmediyse, bunlar geri malzeme çekme yoluyla otomatik olarak tahsis edilebilir. Ön malzeme çekimi, stok hareketinin sonradan düşürülmesi işlemlerini içerir. Üretim emri tamamlanırsa, **Son iş** onay kutusunu seçerek kalan durumu **Bitti** olarak değiştirin. Aksi takdirde, üretilen ek miktarların raporlanmasını sağlamak için alanı boş bırakın.
9.  **Miktar değerlendirmesi** – Ürün girişi, belirli ürünler için oluşturulmuş test işlemlerinin ve kalite kurallarının yapılandırmasına bağlı olarak kalite emirlerinin oluşturulmasını tetikleyebilir. Bir kalite emri, test edilen ürünlerin stok durumunu veya toplu iş özniteliğini güncelleyebileceğinden, kalite değerlendirmesi birçok sektörde zorunlu bir işlemdir.
10. **Yerine koy** ve **Siparişe göre naklet** – Ürün girişi ve kalite değerlendirmesi ardından, isteğe bağlı yerine koyma çalışması, eğer siparişe göre naklet gereklilikleri varsa, alınan ürünleri sonraki tüketim noktasına, bitmiş mal ambarına veya bir nakliye alanına yönlendirir.
11. **Bitti** – Üretim bitmeden önce, üretilen miktara yönelik fiili maliyetler hesaplanır. Tüm tahmini malzeme, işgücü giderleri ve genel giderler tersine çevrilir ve bunların yerine gerçek maliyetler konur. Maliyet hesaplamasını çalıştırdığınızda **Son iş** onay kutusunu seçerseniz, üretim emri durumu **Bitti** olarak değişir. Bu durum, tamamlanmış bir üretim emrine ek maliyetlerin nakledilmesini engeller.
12. **Dönem kapanışı** – Dönemsel ortalama, geriye dönük maliyetlendirme, FIFO veya LIFO gibi bazı maliyet muhasebesi ilkeleri, stoku veya mali dönemi kapatmak için dönemsel faaliyetler gerektirir. Genellikle, sistem tüm malzeme ve kaynak tüketimini, ayrıca stok ve ıskarta düzeltmelerini, dönemler kapatılmadan önce rapor etmeyi dener. Bu raporlama, genellikle stok hareketi günlükleri veya ayarlama günlükleri kullanılarak yapılır. Amaç, işletme birimlerinin ekonomik performansını dönem başına değerlendirmektir. Bazı durumlarda, mali raporlama dönemlerini kapsayan uzun vadeli üretim emirleri kullanılırken, dönem sonu itibariyle üretimin ilerlemesini ve kaynak tüketimini raporlamak için üretim günlükleri kullanılır.


<a name="additional-resources"></a>Ek kaynaklar
--------

[Üretim geri bildirimi](production-feedback.md)

[Ürün yapılandırma modelleri](../pim/product-configuration-models.md)

[Yalın imalat](lean-manufacturing-overview.md)




