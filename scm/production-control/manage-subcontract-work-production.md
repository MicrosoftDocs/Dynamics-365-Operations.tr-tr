---
title: "Üretimde Taşeron iş yönetme"
description: "Bu konu açıklar nasıl Taşeron işlemleri Microsoft Dynamics 365 işlemleri için yönetilir. Diğer bir deyişle, üretim işlemlerinin bir kaynağa ayrılmış satıcı tarafından nasıl yönetildiğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Üretimde Taşeron iş yönetme

Bu konu açıklar nasıl Taşeron işlemleri Microsoft Dynamics 365 işlemleri için yönetilir. Diğer bir deyişle, üretim işlemlerinin bir kaynağa ayrılmış satıcı tarafından nasıl yönetildiğini açıklar.

İçinde [üretim işlemleri](production-process-overview.md), iş sahibi veya satıcılar tarafından yönetilen kaynaklar tarafından yapılabilir. Genellikle, satıcı kaynakları kullanılır, şirketin kullanılabilir kapasitesini karşıladığından düzey dönemsel aşırı talep için kaynaklara sahip. Satıcı Ayrıca belirli sunmak mümkün olabilir [kaynak yetenekleri](resource-capabilities.md)veya daha düşük bir fiyatla kaynakları.  

Bir üretim sürecinde kullanılan satıcı kaynaklara bağlı olarak bir [yol](routes-operations.md) malzeme ve yarı bitmiş ürünler öncelikle satıcının siteye taşınmasını gerekir çünkü genellikle Lojistik ek gereksinimleri vardır. Taşeron işleminin sonucu ya da sonraki operasyon veya mamul malların ambar için ayrılan yere taşınmasını sonra.  

Taşeron işlemler veya etkinlikler kullanıldığında, tüm işlemleri, üretim, maliyetlendirme, tahmini, planlama ve zamanlama, malzeme, yarı bitmiş ürünler ve Mamul mallar için Lojistik yönetimi için gerekli işlemleri tanımından aşamalarını etkilerler. Son olarak, bu kaynaklar için hesap ve maliyet denetimi kendi işlemlerinin izlenmesini gerektirir.  

İç kaynaklar için sabit maliyet oranı genellikle bir dönem için tahsis edilir. Bunun tersine, Taşeron kaynakların maliyeti ilgili hizmeti satın alma fiyatına dayanır. Hizmet başka bir ürün olarak tanımlanır ve tedarik sürücü ve satın alma işlemleri için verilen bir taşeron işlemi için kullanılır.  

Şu anda, yarı bitmiş ürünler, Microsoft Dynamics 365 işlemleri için açık kavramı yoktur. Hammadde tamamlanmış mal dönüştürmek üzere birden çok işlem gerektiren bir üretim emri için Tamamlanan malın son operasyondan stoka yalnızca uygulamasına geri nakledilir. Süren İş'de Süren iş (WIP) önceki işlemleri üretmek yarı bitmiş ürünler hesaba katılmış, ancak deftere olmayan veya stokta izlenir. Rota ve ürün reçeteleri (BOM), birden çok daha küçük birimlere bölebilirsiniz olsa da, bu yaklaşım ürünler, ürün reçeteleri ve yönetilmelidir yolların sayısı artar.  

Taşeron üretim operasyonları için iş modelleme için iki yöntem vardır. Bu yöntemler, Taşeron işlemi, yarı bitmiş ürünler, süreç içinde temsil edilir ve maliyet denetimi şekilde yönetilen yolu modellenebilir emin bir şekilde farklılık gösterir.

-   Rota operasyonları üretim emirleri veya toplu iş emirleri, Taşeron
    -   Servis Ürün stoklu ürün olmalı ve ürün Reçetesinin parçası olmalıdır.
    -   Bu yöntem, ilk giren ilk çıkar (FIFO) veya standart maliyet destekler.
    -   Yarı bitmiş ürünler hizmet ürün işlemi tarafından temsil edilir.
    -   Taşeron iş malzeme maliyetleri ile ilişkilendirilmiş maliyetler maliyet kontrol ayırır.
-   Yalın üretim akışını üretim akışı faaliyetlerinin Taşeron
    -   Servis hizmeti stoğu olmayan bir üründür ve ürün Reçetesinin parçası değildir.
    -   Bu yöntem, satın alma anlaşmaları servis anlaşmaları kullanır.
    -   Bu yöntemi tamamlandığında malzeme çek maliyetlendirme kullanır.
    -   Bu yöntem için toplanmış ve zaman uyumsuz tedarik sağlar. (Malzeme akışı tedarik sürecinin bağımsızdır.)
    -   Maliyet kontrolü kendi Maliyet dökümü bloktaki Taşeron iş ayırır.

## <a name="subcontracting-of-route-operations"></a>Rota operasyonlarında Taşeron
Rota operasyonları üretim veya toplu siparişler için Taşeron kullanmak için hizmet satın alma için kullanılan hizmet ürün bir ürün olarak tanımlanan **hizmet** türü. Ayrıca, olan bir madde model grubu olması gerekir **Stocked ürün** altında seçenek **stok İlkesi** ayarlamak **Evet**. Bu seçenek bir ürün stok ürün alış irsaliyesindeki aldığından olup olmadığını tanımlar (**Stocked ürün** = **Evet**), veya kar ve zarar hesabında ürünü olup expensed (**Stocked ürün** = **yok**). Bu davranış çelişkili görünse de, bu ilke ayarının yapılmış olduğu ürünleri kullanılabilir stok hareketlerini hesaplamak Planlanan Maliyet ve fiili maliyeti üretim siparişi sonlandığında belirlemek için Maliyet kontrolü oluşturacak dayanarak gerçeğine olur.  

Planlama ve maliyet hesaplamasına değerlendirilmesi için hizmet ürün reçetesi ile eklenmesi gerekir. Ürün reçetesi satırı olması gerekir **satıcı** türü ve gerekir tahsis edildiği servis tahsis edilen Rota operasyonu. Bu rota operasyonu maliyetlendirme kaynak ve bir kaynağa işaret eden kaynak gereksinimi olan **satıcı**, operasyon ve ilgili hizmet ilgili satıcı hesabına bağlanan türü.  

Bu yapılandırma kullanıldığında, bir üretim emrinin tahmin hakkında temel servisle ilgili ürün için bir satınalma siparişi oluşturulur. Satınalma siparişi hizmetinin bir tutturucu olarak Taşeron işlemleri için kullanılır. Taşeron iş üzerinden yönetilen **Taşeron iş** üretim Denetim Listesi sayfasında. Taşeron Çalışma operasyon için hazırlık satıcıya hammadde ve en sonunda, yarı bitmiş ürün sevk etmek için kullanılır. Bu da Madde varışı Taşeron işleminin sonuç ürünü almak için hizmet ürün yarı mamulü gelişini tanımlamak için kullanıldığı kullanılır. Satınalma siparişi satırında alındığında, üretim işlemi tamamlandı olarak güncelleştirilir.  

Bir üretim emri birçok işlemi olabilir ve her işlem için farklı bir satıcı tahsis edilebilir. Bu nedenle, bir uçtan uca üretim emri birden çok satınalma siparişleri tetikleyebilir.

## <a name="subcontracting-of-production-flow-activities"></a>Üretim akışı etkinliklerini Taşeron
[Yalın üretim](lean-manufacturing-overview.md)çözüm modelleri Taşeron iş aktivite için ilgili bir hizmet olarak bir [üretim akışı](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (görev Kılavuzu konusu). Bu nedenle, bu tür Taşeron da olarak bilinir [etkinlik tabanlı Taşeron.](activity-based-subcontracting.md) Özel bir maliyet grubu türü **dış kaynak doğrudan**, kullanılmaya başlanan, ve taşeron Hizmetleri tamamlanmış malların ürün Reçetesinin parçası değildir. Yalın üretim kullandığınızda, tüm faaliyetleri bir veya birden çok üretim akışı aktiviteleriyle ilgili kanbans tarafından tanımlanır. Şu ana kadar bu açıklama yalnızca üretim emirlerinin bir açıklama gibi sesleri. Ancak, üretim emirleri her zaman bitmiş bir ürün ile bitmelidir gelirken, yarı bitmiş ürün sağlamak için kanbans oluşturabilirsiniz. Yeni ürün ve ürün reçetesi düzeyi tanıtmak zorunda değilsiniz.  

Kanban kuralları çok dinamik olabileceğinden, bir üretim akışı üzerinde farklı türevleri için aynı Ürün tedarik modelleyebilirsiniz. Yalın kullandığınızda, Taşeron, malzeme akışını ve finansal akışı kesinlikle ayrılır. Tüm malzeme akışı kanban etkinlikler tarafından temsil edilir. Üretim akışındaki kanban işlerinin durumunu temel hizmet ürünleri ve bu hizmetlerin alış irsaliyesi deftere nakiller için satınalma siparişleri otomatikleştirilebilir. Kanban işleri başladı ve satınalma siparişleri bile oluşturulmadan önce tamamlandı. Taşeron belgeleri (satınalma siparişi ve satınalma alış irsaliyesi servisin) dönemi ve hizmeti tarafından toplanabilir. Bu nedenle, satınalma belgeleri ve satırların sayısını bile burada satıcıları Taşeron hizmetlerinde tek parça akış sağlamak çok yinelenen işlemler küçük tutulabilir.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Taşeron üretim akışında modelleme

İçinde bir [Yasla üretim akışı](lean-manufacturing-modeling-lean-organization.md), bir işlem etkinliği tek satıcı kaynak olan bir iş hücre (kaynak grubu) tahsis edilirken Taşeron olarak tanımlanabilir. İlgili işlem etkinliklerini iş hücre Taşeron, servis maddesi ve hizmetin fiyatını içeren bir etkin satın alma anlaşması satırına bağlanması gerekir. Aktivitesinin servis anlaşması da kanban işin ürün miktarı ile elde edilen hizmet miktarı arasındaki hesaplama oranını tanımlar. İşleri, işlerine bildirilen iyi ürün miktarını veya toplam ürün miktarı (ıskarta ürünleri bu toplam miktarı içerir) sayısına göre hesaplanan hizmet miktar seçebilirsiniz.  

Transfer etkinlikleri, Taşeron olarak tanımlanabilir. Bu tanım dolaylı olarak sorumlu parti sevkiyat için transfer etkinliğinde seçtiğinizde oluşur. Seçtiğinizde, **taşıyıcı** veya **alıcı**, satıcı tarafından yönetilen bir ambar ise, karşılık gelen kaynak veya hedef ambar faaliyeti olarak kabul edilir Taşeron. Seçtiğinizde, **taşıyıcı**, etkinlik her zaman Taşeron. Gibi Taşeron işlem etkinliklerini, üretim akışı etkinleştirilebilmesi için önce bir taşeron transfer etkinliği servis anlaşmasına bağlı olması gerekir.

### <a name="backflush-costing"></a>Geriye dönük maliyetlendirme

Taşeron İş Maliyet muhasebesi (tamamlandığında malzeme çek maliyetlendirme) yalın üretim çözümü için maliyetlendirme içine tamamen tümleşiktir. Hizmet satınalma sipariş girişi deftere nakledildiğinde veya faturalama ortaya çıktığında, servis maliyeti üretim akışı için tahsis edilir. Tamamlandığında malzeme çek maliyetlendirme için Taşeron Hizmetleri farkını gerçek alındı ve Faturalandı servis miktarları karşı alınan ürünlerin standart maliyet Taşeron bloğunu mahsubu tarafından hesaplanır.

## <a name="material-supply-for-subcontracted-operations"></a>Taşeron operasyonları için malzeme tedarik
Yarı bitmiş ürünler ve diğer ilgili malzemeleri iş fiziksel olarak gerçekleştirildiği konumun aktarılması gerekir. Taşeron operasyonlarını ve etkinlikleri kullandığınızda, bu transfer genellikle bir satıcı işletilen sitesine ek taşıma ilişkilidir. Malzeme Taşeron operasyon için ürün reçetesinde ayırarak malzeme için tahsis edilen kaynağın kaynak grubunun giriş konumda hazırlanmalıdır bildirin. Master planlama veya yalın yenileme sonra o konuma malzeme sağlar.  

Satıcı sitesinde bulunur stok model oluşturmak için satıcı tarafından yönetilen bir ambar tanımlamak için sektörde en iyi yöntem olduğunu. Satıcı tarafından yönetilen bir ambar, yeni bir ambar ve satıcı hesabı atama tarafından kolayca tanımlayabilirsiniz. İşlem gerçekleştirilmeden önce bu malzeme belgelemek için satıcıya aktarılması gerekir, satıcı tarafından yönetilen ambar giriş ambarına tutan kaynağın kaynak grubunun tahsis.  

Bu ambarda malzeme stoğunu yenilemek için çoklu stratejiler kullanabilirsiniz:

-   Transfer emirleri
-   Transfer günlükleri
-   Mevzuatı kanbans
-   Satıcı konumuna doğrudan satınalma

Bu kuralın istisnası yarı bitmiş ürünler şunlardır. Yarı bitmiş ürünler transfer etmek için bu seçenekleri sınırlı:

-   Üretim ve toplu siparişler için yarı bitmiş ürünler yalnızca mantıksal olarak malzeme çekme listesi günlüğü'nden kullanarak transfer edilebilir **Taşeron iş** listesi sayfası. Bu günlük, yarı bitmiş aktarmak için kullanılan teslimat notu belge ve hammadde satıcıya oluşturur.
-   Üretim akışları, Taşeron işlemleri için satıcı konumda mevzuatı veya üretim kanbans alındığını tarafından yarı bitmiş ürünler transferini belgelenmiştir. Açık transfer aktivite modellemek için bir üretim kanbanı ek transfer etkinliği ile sona erdirebilir.

**Not:** bir tek bir üretim emri için üretim rotasında birden çok siteler arası olamaz. Bu kural, Taşeron iş için de geçerlidir. Bu nedenle, ambarlar, satıcı tarafından yönetilen malzeme konumları aynı sitede rotada kullanılan iç kaynaklar olarak tanımlanmalıdır temsil eder. Üretim akışları siteler arası, ancak bu işlem maliyeti bağlam değişikliği gösterdiğinden bunların bir siteden diğerine, yarı bitmiş ürünler aktarım olamaz.  

Genellikle, bir taşeron kaynak grubunun konumunu ve çıkış ambarı doğrudan operasyon rota veya üretim akışındaki sonraki adıma konumunu ve ambar için ayrılır. Bu kurulum işi oluşan raporlama veya model alınacak sayı ek aktarım işlemleri azaltmak yardımcı olur.


