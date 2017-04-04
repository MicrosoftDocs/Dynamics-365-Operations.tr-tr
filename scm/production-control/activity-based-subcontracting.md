---
title: "Etkinlik tabanlı Taşeron"
description: "Bu konu, ayrıntılı olarak Taşeron faaliyetleri üretim akışında yalın üretim için kullanmayı açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Etkinlik tabanlı Taşeron

Bu konu, ayrıntılı olarak Taşeron faaliyetleri üretim akışında yalın üretim için kullanmayı açıklar.

İşlemler için Microsoft Dynamics 365 Taşeron için iki yaklaşım vardır: üretim emirleri ve yalın üretim. Yalın üretim yaklaşımda, Taşeron iş üretim akışının bir faaliyetle ilgili bir hizmet olarak modellenmiştir. Maliyet grubu türü olarak adlandırılan özel türde bir **dış kaynak doğrudan** kullanılmaya başlanan, ve taşeron Hizmetleri artık bir ürün reçetesi (BOM) parçasıdır. Taşeron İş Maliyet muhasebesi yalın üretim için maliyetlendirme çözüm içine tamamen tümleşiktir.

## <a name="production-flows-that-involve-subcontractors"></a>Alt yüklenicileri içeren üretim akışları
Bir üretim akışının temel ilke etkinlikleri Taşeron değiştirmiyor. Malzeme hala konumlar arasında akan, işlem etkinliklerini malzeme ürünleri için dönüştürmek ve transfer etkinlikleri malzeme veya ürün bir konumdan diğerine taşımak. Konumlar modeller ve hücreler olarak satıcı tarafından yönetilen bir ambar veya bir kaynak grubunun kaynak için satıcı hesabı atama çalışma.  

Bu yetenekler üzerinde bağlı olarak, yalın üretim, malzeme ve ürünleri akışını desteklemek için herhangi bir özel özelliği gerektirmez. Üretim veya taşıma hizmetleri sağlayıcıları modellenebilir gibi satıcılarla ilgili tüm olası senaryolar, üretim akışı ve aktivitelerin mimarisine dayalı.  

Örneğin, bir alt yüklenici Taşeron bulunan bir süpermarket dışında çalışır. Birimlerin yönetilmesi alt yüklenici boşaltıldığında, kanban kartları derleme hücreye sonraki sevk irsaliyesi ile birlikte verilir. Alt yüklenici, süpermarket sonra yenilenir. Alt yüklenici gelen ve Giden Transferler çekme ve sevkiyat işlemini desteklemek için açık bir transfer aktiviteleri olarak modellenebilir. Açık bir kaydı fiziksel aktarım desteklemek için gerekli değildir, bir transfer aktiviteleri atlanabilir.  

Bir taşeron yükünü dengelemek üretim akışının genel kapasite için kullanılabilir. Örneğin, bir üretim akışı zamanlanmış kanban kuralları kullanılarak modellenmiştir. Planlayıcının Tahta zamanlamak ve yük düzeyi için zamanlama kanban isteğe bağlı olarak her iki iş hücre kullanır. Planlayıcının süpermarket konsolide tedarik zamanlaması üzerinde de izler **tedarik zamanla** sayfa. Bir veya birden çok üretim akışlarında birden çok alt yüklenicilere modellenebilir ve aynı ürün farklı etkinlikler ile aynı konuma sağlamak için kullanılan kanban birden çok kural olabilir. Planlayıcıya iç üretimi için alternatif bir işlem için oluşturulan bir kanban yeniden zamanlamak için bir alternatif kanban kural kanbans dönüştürebilirsiniz. Aslında, Taşeron iş hücre yapısı üretim akışı üzerinde hiçbir etkisi olmaz. İki paralel iç iş hücre veya taşeron iki hücre aynı çalışma prensibi geçerlidir.   

Başka bir aktivite gibi üretim akışında, Taşeron aktiviteleri tüketen ve tedarik inventoried, inventoried (çalışma devam ediyor \[Süren\]) ve yarı bitmiş malzeme ve ürünleri. Tüm durumlarda, zamanlama ve taşeron faaliyetleri yürütmek için işlemler aynıdır. Ayrıca, bunlar iç iş süreçlerini aynı işlem.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Taşeron etkinlikler (Hizmetler) için satın alma süreci
Taşeron etkinlikler için satın alma süreci kanban ilerleyişini tarafından örneğin kayıtlı fiziksel malzeme akışına dayalıdır, başlatmak veya tamamlamak. Taşeron Çalışma maliyet finansal akışı, örneğin, fiziksel akışını izleyen bir ikincil akış şeması aşağıda gösterilmiştir. Aynı zamanda, satınalma işleminin her adımı sırasında satınalma belgeleri el ile ayarlanmasına izin veren bağımsız bir işlemdir. Taşeron etkinlikler için satın alma süreci aşağıdaki gibidir:

1.  Bir satın alma sözleşmesi oluşturun. Satın alma sözleşmesi hizmeti için oluşturulan ve üretim akışının faaliyete bağlı.
2.  Bir satınalma siparişi oluşturmak. Satınalma sevk emri kanbanı zamanlanan işlere göre hizmet için oluşturulabilir. İşler aynı hizmeti için satınalma siparişi satırlarına güne, haftaya veya aya göre gruplandırılabilir. Satınalma siparişi satırları kanban işleri oluşturduktan sonra herhangi bir zamanda oluşturulabilir. Satınalma siparişi satırları olgu sonra bile oluşturulabilir. Bir taşeron Taşeron aldığı kanbans veya kanban kartları dayalı ek bildirmeden hizmetleri sağlıyorsa, bu seçenek genellikle seçilir. Bu durumda, satınalma siparişi ve faturayı arasındaki sapmalar en aza indirilebilir.
3.  Kanban kartları, malzeme ve işleme için hazırlamak üzere taşerona göndermek için bir malzeme çekme listesi oluşturun. Üretim akışı ayrıntılı model oluşturma göre hazırlık kanban tahtada işlem faaliyetleri için malzeme çekme listesi ve hazırlama işlevi kullanılarak yapılır. Alternatif olarak, hazırlık kanban tahtada transfer işleri için malzeme çekme listesi ve başlangıç veya tamamlama kullanılarak yapılır. İnventoried malzeme için her iki süreç WMS çekme ve sevkiyat işlemi tarafından desteklenebilir. Konşimento, isteğe bağlı olarak oluşturulabilir.
4.  Kanban işleme birimleri ve kanban kartları oluşturur. İşlemden sonra kartları taşerondan döndürülür. Genellikle, sevk edildi fiziksel malzeme belirten bir teslimat notu kartları içerir. Sağlanan hizmetleri başvuru gerekli deðildir. Malzeme veya müşteri ürünü gelişini kanban tahtada kanban kartları bağlı olarak kaydedilir. (İşlem etkinliklerini kanban panosu veya transfer işleri kanban Tahta Modellenen aktiviteleri bağlı olarak kullanılır.).
5.  Danışma belgesi bir giriş oluşturun. Danışma belgesi alış irsaliyesi Sevk değiştirmek için kullanılan irsaliyesi belgesi alınan hizmetler için. Alış irsaliyesi danışma tamamlanmış kanban işleri Taşeron faaliyet için seçilen döneme göre oluşturulabilir. Her işi alış irsaliyesi için danışma ilgili satınalma siparişi satırı için oluşturulur. Danışma belgesi giriş yazdırılır ve taşerona giriş teyidi olarak gönderilir.
6.  Bir fatura oluşturun.

Taşeron bir dönemde faturalandığında işlemi sonlandırır. Fatura eşleşme oluşturulan giriş danışma karşı yapılır. Tam fiziksel giriş malzeme giriş danışma temsil ettiğinden, üç yollu eşleşen basitleştirir.

## <a name="configuring-activities-for-subcontracting"></a>Taşeron için faaliyetler yapılandırma
Aşağıdaki bölümlerde, Taşeron için faaliyetler konfigüre etme yöntemleri açıklanmaktadır.

### <a name="subcontracted-services"></a>Taşeron Hizmetleri

Etkinlik tabanlı Taşeron olarak kullanılan ödeme öğe aşağıdaki özelliklere sahip bir ürün olması gerekir:

-   **Ürün türü:** hizmeti
-   **Stok modeli grubu:** stoğu olmayan

Bu gereksinim ilk kullanımını zorlar içinde ilk çıkar (FIFO) stok modeli. **Not:** ürünlerin maliyet hesaplama gerektirir service standart maliyetini tanımlanması. Satıcıyla bir satın alma sözleşmesi gerek yoktur. Aksi halde, Taşeron etkinlik tabanlı hizmet kullanılamaz.

### <a name="subcontracted-process-activities"></a>Taşeron işlemi etkinlikleri

Bir işlem etkinliği Taşeron bir etkinlik olarak yapılandırmak için aşağıdaki adımları izleyin.

1.  Taşeron iş hücre yapılandırın. İş hücre Taşeron olarak yapılandırmak için bir kaynak oluşturmak **satıcı** yazın ve iş hücre (kaynak grubu) ile ilişkilendirin. Çalışma zamanı maliyet kategorisini **dış kaynak doğrudan** maliyet grubu türü iş hücreye atanmış. Kurulum ve miktar için maliyet kategorilerini gerekli değildir.
2.  Bir işlem etkinliği oluşturduğunuzda veya bir taşeron iş hücreyle ilişkili üretim akışı sürümünün etkinleştirilebilmesi için önce bir servis aktivitesi için yapılandırmanız gerekir. Bu adımı tamamlamak **faaliyet****ayrıntıları** sayfa. Bir taşeron çalışma hücresiyle ilişkilendirilmiş aktiviteleri için **hizmet şartları** hızlı gösterilir. Bu hızlı sekmesinde, tüm çıkış maddeler için geçerli olan varsayılan hizmet ekleyin. Belirli bir çıktı öğeleri farklı hizmetler veya farklı bir hizmet hesaplama parametreleri (örneğin, farklı hizmet oranı) gerektiriyorsa, aktivite diğer hizmetleri ekleyebilirsiniz.

## <a name="subcontracted-transfer-activities"></a>Taşeron bir transfer aktiviteleri
Transfer etkinlik bağlı olarak, Taşeron bir etkinlik olarak yapılandırılmış **Navlun sorumlusu** transfer etkinliğini ayarlama. Aşağıdaki seçenekler bulunur:

-   **Taşıyıcı** – ambardaki transfer (bir ambar özelliği tarafından tanımlanan) satıcı tarafından yönetiliyorsa etkinlik Taşeron. Seçili satınalma Hizmetleri sözleşmelerini tüm ambar olarak aynı satıcı kimliği olması gerekir.
-   **Alıcı** – ambara transfer (bir ambar özelliği tarafından tanımlanan) satıcı tarafından yönetiliyorsa etkinlik Taşeron. Seçili satınalma Hizmetleri sözleşmelerini tüm ambar olarak aynı satıcı kimliği olması gerekir.
-   **Taşıyıcı** – etkinlik hizmetleri sağlayan herhangi bir satıcı için Taşeron. Geçerli olması için bir taşıyıcı ambar yönetimi için oluşturulan ve atanan satıcı hesabı olması gerekir.

İşlem etkinliklerini olduğu gibi Taşeron transfer etkinlikler için varsayılan hizmet üzerinde yapılandırmalısınız **hizmet şartları** hızlı **faaliyet****ayrıntıları** sayfa.

## <a name="service-quantity-calculation"></a>Hizmet miktarı hesaplama
Tüm satın alma süreci bir madde başvuru hizmeti dayanır. Bu madde başvuru ölçü birimi, bir hizmetin içinde ölçülür. Hizmetler genellikle Hizmetleri (birim) sayısı veya zaman olarak ölçülür. Kanban işlerinin kayıtlı tamamlanma dayalı hizmet miktarını hesaplamak için aşağıdaki yöntemleri kullanabilirsiniz:

-   **İşleri sayısını temel alan hesaplama** – bir kanban iş eşittir *n* sağlanan ürün miktarı ne olursa olsun, servis birimleri. Yalın üretim içinde bir iş işleme birimine karşılık gelir. Bu hesaplama yöntemi işleme birim başına sabit bir fiyata sahip tüm hizmetler için geçerlidir. Bu nedenle, bu yöntem genellikle etkinlikleri aktarmak için geçerlidir. Ancak, tüm işleme birimleri işlem işlem etkinliklerini de uygulayabilirsiniz.
-   **Ürün miktar temel alınarak hesaplama** – planlanan ve sağlanan ürün miktarı göreceli olarak hizmet miktarıdır. Sağlanan ürün miktarı hesaplanırken hata miktarlarını da dahil etmek veya hariç. Bu hesaplama yöntemi burada hizmet gören ürün birim fiyatı üzerinde anlaşmaya varılan tüm servis talepleri için geçerlidir.
-   **Etkinlik saati esas alarak hesaplama** – etkinliği işlem süresine dayalı teorik etkinlik saatler hesaplanır toplam işlenen miktar ve işlenen ürünün verim oranı. Bu hesaplama yöntemi saat başına ödenen hizmetler için geçerlidir ve işlenmiş ürün her zaman bir fark vardır.

## <a name="cost-accounting-of-subcontracted-services"></a>Maliyet muhasebesi Taşeron Hizmetleri
Girişinin değeri üretim akışı WIP hesaplarında danışma alış irsaliyesi veya sevk irsaliyesi (diğer bir deyişle, kanban işleri Taşeron etkinlikler için temel alarak oluşturulan bir satınalma siparişi) bir üretim akışı için oluşturulan satınalma siparişine satıcı deftere nakledildiğinde, hesaba katılmış olur. Üretim akışı için sapmalar faturaların da hesaba katılmış. Taşeron Çalışma için bir maliyet kategorisinin tanıttı. Bu maliyet kategorisinin saydam Süren İŞTEN ayrılan ve her dönem için tüketilen Taşeron iş değerinin izlenmesini sağlar.  

Yalın üretim maliyet dönemi sonunda için maliyetlendirme tamamlandığında malzeme çek üretim akışından maliyetlendirme dönemde üretilen ürünlerin gerçek farklarını hesaplar.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelleme Taşeron aktiviteleri olarak aktarır.
İnsanlar genellikle taşıma toplanması ve düşünme, hiçbir değer ekler düşünün. Ancak, iç üretim maliyetine taşeron maliyeti karşılaştırıldığında ek taşıma faaliyetleri maliyetini dikkate alınmalıdır. Taşıma maliyeti müşteriye ürünleri sağlama maliyetinin bir parçası olarak birden çok konuma yayılmış ve taşıma hizmetleri gerektiren bir üretim akışı model. 

Yalın üretim etkinlik tabanlı Taşeron taşıyıcılar bütünleştirmek ve malzeme ve ürünleri üretim akışının konumlar arasında hareket eden satıcılar taşıma sağlar. Transfer etkinlik model oluşturma, bir taşıyıcı veya satıcı atayabilirsiniz. Etkinlikler/iş transfer hizmeti ve satınalma Sözleşmesi'nde dayanır ve satınalma siparişleri ve giriş danışma, gerçek transfer işlere göre oluşturabilirsiniz. Bu işlevsellik işlevleriyle ilgili Taşeron işlem etkinliklerini aynıdır.  

Bu nedenle, Dynamics 365 taşıma hizmetleri, ilgili oluşturulmasını destekler ürün reçetesi hesaplaması satınalma siparişleri, tümleşik giriş kayıt ve aktarım tümleştirme artık işlemleri için maliyetleri üretim akışı maliyetlendirme içine hizmet.


