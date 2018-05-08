---
title: "Üretimdeki alt sözleşme işini yönetme"
description: "Bu konu, alt sözleşmeli operasyonların Microsoft Dynamics 365 for Finance and Operations'ta nasıl yönetileceğini açıklar. Başka bir deyişle, bir kaynağa atanan üretim operasyonlarının bir satıcı tarafından nasıl yönetileceğini açıklar."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 26feea4d86cf8b976f41342c8543594593c4b135
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="manage-subcontracting-work-in-production"></a>Üretimdeki alt sözleşme işini yönetme

[!include [banner](../includes/banner.md)]

Bu konu, alt sözleşmeli operasyonların Microsoft Dynamics 365 for Finance and Operations'ta nasıl yönetileceğini açıklar. Başka bir deyişle, bir kaynağa atanan üretim operasyonlarının bir satıcı tarafından nasıl yönetileceğini açıklar.

[Üretim işlemlerinde](production-process-overview.md) iş, satıcıların sahip olduğu veya onlar tarafından yönetilen kaynaklar tarafından yapılabilir. Genellikle satıcı kaynakları, bir şirketin kendi kaynaklarını aşan düzenli fazla talebi düzenlemek için kullanılır. Satıcı aynı zamanda belirli [kaynak yetenekleri](resource-capabilities.md) veya kaynakları daha düşük fiyattan sunabilir.  

Bir üretim sürecinde kullanılan satıcı kaynaklarına bağlı olarak, bir [yol](routes-operations.md) çoğu zaman ek lojistik gereksinimlere sahiptir çünkü kaynaklar ve yarı bitirilmiş ürünler ilk önce satıcının sitesine taşınmak zorundadır. Daha sonra, alt sözleşmeli operasyonun sonucu bir sonraki operasyona atanmış konuma ya da bir mamul mal deposuna taşınmalıdır.  

Alt sözleşme operasyonları veya etkinlikleri kullanıldığında, bunlar operasyonun tüm aşamalarını etkiler, üretimde, maliyetlendirmede, öngörü oluşturmada, planlamada ve zamanlamada gerekli olan operasyonların tanımından, malzemelerin, yarı bitmiş ürünlerin ve mamul malların yönetimine kadar. Son olarak, bu kaynaklar muhasebe ve maliyet denetimi için kendi işlemlerine ihtiyaç duyarlar.  

Dahili kaynaklar için, sabit maliyet oranı genellikle bir dönem için tahsis edilir. Bunun tersine, alt sözleşmeli kaynakların maliyeti, ilgili hizmetin satınalma fiyatına dayanır. Hizmet, başka bir ürün olarak tanımlanır ve belirli bir alt sözleşmeli operasyonun satın alınması ve satınalma işlemlerini yürütmek için kullanılır.  

Şu anda, yarı bitmiş ürünler için Microsoft Dynamics 365 for Finance and Operations'ta açık bir kavram yoktur. Ham maddeleri mamul mala dönüştürmek için birden fazla operasyona ihtiyaç duyan bir üretim emri için mamul mal, sadece son operasyonda tekrardan stoklara geri nakledilir. Daha önceki operasyonların ürettiği yarı bitmiş ürünler, süren iş (WIP) olarak hesaba katılır, ancak stokta izlenmez veya gönderilmez. Rotaları ve ürün reçetelerini (BOM'lar) birden fazla küçük birime bölebiliyor olsanız da, bu yaklaşım yönetilmesi gereken ürünlerin, BOM'ların ve rotaların sayısını artırır.  

Üretim operasyonları için alt sözleşmeli işleri modellemenin iki yöntemi vardır. Bu yöntemler alt sözleşmeli sürecin modellenme şeklinde, yarı bitmiş ürünlerin süreçte temsil edilmesinde ve maliyet yönetiminin yönetilme şeklinde farklılık gösterir.

-   Üretim emirleri veya toplu iş emirlerinde rota operasyonlarının alt sözleşmeyle verilmesi
    -   Hizmet ürünü stoklu bir mal ve BOM'un parçası olmak zorundadır.
    -   Bu yöntem ilk giren ilk çıkar (FIFO) veya standart maliyeti destekler.
    -   Yarı bitmiş ürünler, işlemdeki hizmet ürünü tarafından temsil edilir.
    -   Maliyet kontrolü, alt sözleşmeli işin maliyetlerini malzeme maliyetleriyle ilişkilendirir.
-   Yalın imalat akışındaki üretim akışı etkinliklerinin alt sözleşmeyle verilmesi
    -   Hizmet stoksuz bir hizmet ürünüdür ve BOM'un parçası değildir.
    -   Bu yöntem, satınalma anlaşmalarını servis anlaşmaları olarak kullanır.
    -   Bu yöntem geyi dönük maliyetlendirme kullanır
    -   Bu yöntem toplanmış ve uyumsuz tedarik sağlar. (Malzeme akışı tedarik sürecinden bağımsızdır.)
    -   Maliyet kontrolü, alt sözleşmeli işi kendi maliyet dökümü bloğuna tahsis eder.

## <a name="subcontracting-of-route-operations"></a>Rota operasyonlarının alt sözleşmeyle verilmesi
Rota operasyonlarının üretim veya toplu iş emirleri için alt sözleşmeyle verilmesinde kullanılması için, hizmetin tedarik edilmesinde kullanılan hizmet ürünü, **Hizmet** türündeki bir ürün olarak tanımlanmış olmalıdır. Ek olarak, **Stok ilkesi** altındaki **Stoklu ürün** seçeneği **Evet** olarak ayarlanmış bir madde model grubuna sahip olmalıdır. Bu seçenek, bir ürünün, ürün girişinde (**Stoklu ürün** = **Evet**) stok olarak hesaba geçmiş olup olmadığını veya ürünün bir kar veya zarar hesabında harcanmış olup olmadığını (**Stoklu ürün** = **Hayır**) tanımlar. Bu davranış çelişkili görünse de, sadece bu ilkeye sahip ürünlerin maliyeti kontrolünde, planlanmış maliyeti hesaplamak ve bir üretim emri sona erdiğinde fiili maliyeti belirlemek için stok hareketlerine sahip olacakları gerçeğine dayanmaktadır.  

Planlama ve maliyet hesaplamada değerlendirilmesi için hizmetin BOM'a eklenmesi gerekir. BOM satırının **Satıcı** türünde olması ve hizmetin tahsis edildiği rota operasyonuna tahsis edilmiş olması gerekir. Bu rota operasyonu, operasyonu ve ilgili hizmetleri karşılık gelen satıcı hesabına bağlayan **Satıcı** türüne yönlendiren bir maliyetlendirme kaynağı ve maliyet gereksinimine sahip olmalıdır.  

Bu yapılandırma kullanıldığında, ilgili hizmet ürünü için bir üretim emrinin tahminine dayalı olarak bir üretim emri oluşturulur. Hizmetin satınalma emri, alt sözleşmeli operasyonlar için bir dayanak noktası olarak kullanılır. Alt sözleşmeli iş, Üretim kontrolü'nde **Alt sözleşmeli iş** listesi sayfası üzerinden yönetilebilir. Alt sözleşmeli iş, bu hizmetin hazırlığındaki satıcıya hammadde ve en sonunda, bir yarı bitmiş ürünü sevk etmek için kullanılır. Ayrıca, alt sözleşmeli işin sonunda ortaya çıkan elde edilen ürünü, hizmet ürününün gelen yarı bitmiş ürünü tanımlamak için kullanıldığı, ürün alımında teslim almak için kullanılır. Satınalma siparişi satırı alındığında, üretim operasyonu tamamlandı olarak güncelleştirilir.  

Bir üretim emrinin birçok işlemi olabilir ve her işlem farklı bir satıcıya tahsis edilebilir. Bu nedenle, uçtan uca üretim emri çok sayıda satınalma siparişini tetikleyebilir.

## <a name="subcontracting-of-production-flow-activities"></a>Üretim akışı etkinliklerinin alt sözleşmeyle verilmesi
[Yalın imalat](lean-manufacturing-overview.md) çözümü, alt sözleşmeli işi bir [üretim akışı](tasks/create-production-flow-version.md) (Görev kılavuzu konusu) faaliyetiyle ilişkili bir hizmet olarak modeller. Bu nedenle, bu tür alt sözleşmeler [etkinlik tabanlı alt sözleşme](activity-based-subcontracting.md) olarak da bilinir. **Doğrudan dış kaynak kullanımı** olarak bilinen bir özel maliyet grup türü kullanılmaya başlamıştır ve alt sözleşme hizmetleri, mamul malın BOM'unun parçası değildir. Yalın imalat kullandığınızda, tüm etkinlikler bir ya da birçok üretim akış etkinliğiyle ilişkilendirilebilir kanbanlar ile tanımlanır. Şu ana kadar bu açıklama, üretim emirleri açıklamasına benzemektedir. Ancak üretim emirleri her zaman bir mamul mal ile sonlanmak zorundayken, bir yarı bitmiş ürün sağlamak için kanbanlar oluşturabilirsiniz. Yeni ürün ve ürün reçetesi düzeyi tanıtmak zorunda değilsiniz.  

Kanban kuralları çok dinamik olabileceğinden, bir üretim akışı üzerinde aynı ürün için farklı tedarik türevleri modelleyebilirsiniz. Yalın alt sözleşme kullandığınızda, üretim akışı ve finansal akış katı bir biçimde ayrılır. Tüm malzeme akışı kanban etkinlikleri ile temsil edilir. Hizmet ürünleri ve bu hizmetlerin alış irsaliyesi deftere nakilleri, üretim akışındaki kanban işlerinin durumuna dayalı olarak otomatikleştirilebilir. Kanban işleri satınalma siparişleri başlamadan hatta oluşturulmadan önce başlatılabilir.a Alt sözleşme belgeleri (satınalma emri ve hizmetin satınalma alış irsaliyesi) dönem ve hizmet ile toplanabilmektedir. Bu nedenle, satınalma belgeleri ve satırları küçük tutulabilir, satıcıların tek bir parça akışında alt sözleşmeli hizmetler sağladığı büyük ölçüde tekrar eden operasyonlarda bile.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Bir üretim akışında alt sözleşmeyi modellemek

Bir [yalın imalat akışında](lean-manufacturing-modeling-lean-organization.md), bir işlem etkinliği, tek bir satıcı kaynağına sahip bir çalışma hücresine (kaynak grubuna) tahsis edildiğinde, alt sözleşmeli olarak tanımlanabilir. Bir iş hücresi alt sözleşmeyle verildiğinde, ilgili işlem etkinlikleri, servis maddesi ve hizmetin fiyatını içeren etkin bir satınalma sözleşmesi satırıyla ilişkilendirilmek zorundadır. Etkinliğin hizmet sözleşmesi ayrıca kanban işinin ürün miktarı ve bundan doğan hizmet miktarı hesaplaması oranını tanımlar. Hizmet miktarının iş sayısı mı, işlerde raporlanan iyi ürün miktarı veya toplam ürün miktarına (bu toplam miktar ıskarta ürünleri de içerir) dayanarak mı hesaplanacağını seçebilirsiniz.  

Transfer etkinlikleri de alt sözleşmeli olarak tanımlanabilir. Bu tanım, transfer etkinliğindeki sevkten sorumlu tarafı dolaylı olarak seçtiğinizde oluşur. **Nakliyeci** veya **Alıcı** seçtiğinizde, karşılık gelen kaynak veya hedef ambar satıcı tarafından yönetilen bir ambarsa, etkinlik alt sözleşmeli olarak kabul edilir. **Taşıyıcı** seçtiğinizde, etkinlik her zaman alt sözleşmelidir. Alt sözleşmeli işlem etkinlikleri gibi, bir alt sözleşmeli transfer etkinliğinin de üretim akışı etkinleştirilebilmeden önce bir hizmet sözleşmesine bağlanması gerekir.

### <a name="backflush-costing"></a>Geriye dönük maliyetlendirme

Alt sözleşmeli işin maliyet muhasebesi, yalın üretim çözümünün (geri dönük maliyetlendirme) maliyetlendirmesine tümüyle entegre edilmiştir. Hizmetin satınalma emri girişi deftere nakledildiğinde veya faturalandırma gerçekleştiğinde, hizmetin maliyeti üretim akışına tahsis edilir. Geri dönük maliyetlendirme için alt sözleşmeli hizmetlerin farkı, alınan malların standart maliyetinin alt sözleşme blokunun, gerçek alınan ve faturalandırılan hizmet miktarlarına mahsup edilmesiyle hesaplanır.

## <a name="material-supply-for-subcontracted-operations"></a>Alt sözleşmeli operasyonlar için malzeme tedariki
Yarı bitmiş ürünler ve ilgili diğer malzemelerin, işin fiziksel olarak gerçekleştirildiği konuma nakledilmesi zorunludur. Alt sözleşmeli operasyonlar ve etkinlikler kullandığınızda, bu transfer çoğu zaman satıcı tarafından yönetilen bir siteye ek nakliye ile ilişkilidir. Ürün reçetesinde malzemeyi alt sözleşmeli operasyona tahsis ederek, malzemenin tahsis edilmiş kaynak için kaynak grubu giriş konumunda hazırlanması gerektiğini bildirmiş olursunuz. Master planlama veya yalın yenileme daha sonra malzemeyi o konuma sağlar.  

Bir satıcı sitesinde bulunan stoku modellemek için sektördeki en iyi yöntem, satıcı tarafından yönetilen bir ambar tanımlamaktır. Yeni bir ambar oluşturarak ve satıcı hesabını atayarak, satıcı tarafından yönetilen bir ambarı kolaylıkla oluşturabilirsiniz. Bir operasyonun gerçekleştirilebilmesinden önce malzemenin satıcıya nakledilmesi gerektiğini belgelemek için, satıcı tarafından yönetilen ambarı, kaynağı bulundurmakta olan kaynak grubunun giriş ambarına atamalısınız.  

Bu ambardaki malzemeyi yenilemek için birden fazla stratejiyi kullanabilirsiniz:

-   Transfer emirleri
-   Transfer günlükleri
-   Çekme kanbanları
-   Satıcı konumuna doğrudan satınalma

Yarı bitmiş ürünler bu kuralın istisnasıdır. Yarı bitmiş ürünleri transfer etmek için şu seçeneklerle sınırlısınız:

-   Üretim ve toplu iş siparişleri için, yarı bitmiş ürünler yalnızca mantıksal olarak Malzeme çekme listesini **Alt sözleşmeli iş** listesi sayfasından kullanarak transfer edilebilir. Bu günlük, yarı bitmiş ürünleri ve hammaddeleri satıcıya transfer etmek için bir teslimat notu belgesi oluşturacaktır.
-   Üretim akışlarındaki alt sözleşmeli operasyonlar için yarı bitmiş ürünlerin transferi, satıcı konumundaki çekme alımı veya üretim kanbanları tarafından belgelenir. Açık transfer aktivitesini modellemek için bir üretim kanbanı, ek bir transfer etkinliğiyle sona erdirebilirsiniz.

**Not:** Tek bir üretim emri için bir üretim rotası, birden fazla site arası olamaz. Bu kural, alt sözleşmeli iş için de geçerlidir. Bu nedenle, satıcı tarafından yönetilen malzeme konumlarını temsil eden ambarlar, söz konusu rotada kullanılan dahili kaynaklarla aynı sitede tanımlanmalıdır. Üretim akışları siteler arası geçiş yapabilse de, yarı bitmiş ürünleri bir siteden diğerine aktaramazlar, çünkü bu operasyon maliyet bağlamında bir değişimi belirtir.  

Genellikle çıkış ambarı ve alt sözleşmeli kaynak grubunun konumu, doğrudan ambar ve operasyonun üretim akışı rotasındaki bir sonraki adımına doğrudan tahsis edilmiştir. Bu kurulum, gerçekleşen iş raporlama miktarını veya modellenmesi gereken ek transfer operasyonlarını azaltmaya yardımcı olur.




