---
title: Etkinlik tabanlı alt sözleşme verme
description: Bu konu, alt sözleşmeli etkinliklerin yalın imalat için üretim akışında nasıl kullanılacağını ayrıntılarıyla açıklar.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ec47a13d9119c755702e019d09c76e1281b4a6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250244"
---
# <a name="activity-based-subcontracting"></a>Etkinlik tabanlı alt sözleşme verme

[!include [banner](../includes/banner.md)]

Bu konu, alt sözleşmeli etkinliklerin yalın imalat için üretim akışında nasıl kullanılacağını ayrıntılarıyla açıklar.

Microsoft Dynamics 365 Supply Chain Management'ta, alt sözleşme için iki seçenek vardır: üretim emirleri ve yalın imalat. Yalın imalat yaklaşımında, alt özleşme işi bir üretim akışının etkinliğiyle ilişkili bir hizmet olarak modellenir. **Doğrudan dış kaynak kullanımı** olarak adlandırılan özel bir maliyet grubu türü kullanılmaya başlanmıştır ve alt sözleşme hizmetleri artık bir ürün reçetesinin (BOM) parçası değildir. Alt sözleşmeli işin maliyet muhasebesi, yalın imalatın maliyetlendirme çözümüne tümüyle entegre edilmiştir.

## <a name="production-flows-that-involve-subcontractors"></a>Alt yüklenicileri içeren üretim akışları
Üretim akışının temel prensibi, etkinlikler alt sözleşmeyle verildiğinde değişmemektedir. Malzeme hala konumlar arasında akmaktadır, işlem etkinlikleri malzemeleri ürünlere dönüştürür ve aktarma etkinlikleri malzeme veya ürünleri bir konumdan diğerine taşır. konumları ve iş hücrelerini, satıcı hesabını bir ambara veya bir kaynak grubunun kaynağına atayarak hücreleri satıcı tarafından yönetilen olarak modelleyebilirsiniz.  

Bu yeteneklere dayalı olarak, yalın üretim, malzeme ve ürün akışlarını desteklemek için herhangi bir özel özellik gerektirmez. Satıcıları üretim veya taşıma hizmeti sağlayıcısı olarak içeren, mümkün olan tüm senaryolar, üretim akış ve etkinlikleri mimarisine dayalı olarak modellenebilir.  

Örneğin, bir alt yüklenici, alt yüklenicide bulunan bir süpermarket dışına çalışmaktadır. Alt yüklenicide boşaltılan birimleri yönetirken, kanban kartları bir sonraki sevkiyat ile derleme hücresine geri döndürülür. Daha sonra alt yüklenicideki süpermarket yenilenir. Alt yükleniciye giden ve gelen transferler, bir çekme ve sevkiyat işlemini desteklemek için açık transfer etkinlikleri olarak modellenebilir. Fiziksel aktarmayı desteklemek için açık bir kayıt zorunlu değilse, aktarma etkinlikleri atlanabilir.  

Bir taşeron, üretim akışının genel kapasitesinin yükünü dengelemek üzere kullanılabilir. Örneğin, bir üretim akışı, zamanlanmış kanban kuralları kullanılarak modellenmiştir. Planlayıcı,her iki iş hücresini isteğe bağlı olarak zamanlamak ve yük dengelemesini yapmak için kanban zamanlama panosunu kullanır. Planlayıcı ayrıca, süpermarket için birleştirilmiş tedarik zamanlamasını, **Tedarik zamanlamasında** sayfasında izler. Birden fazla alt yüklenici bir veya birden fazla üretim akışına modellenebilir ve aynı ürünü, aynı konuma farklı etkinlikler aracılığıyla tedarik etmek için kullanılabilecek birden fazla kanban kuralı mevcut olabilir. Planlayıcı, kanbanları, ilk başta dahili üretim veya alternatif işlem için oluşturulmuş olan bir kanbanı yeniden zamanlamak için alternatif bir kanban kuralına dönüştürebilir. Aslında, alt yüklenicinin iş hücresi yapısının üretim akışında hiçbir etkisi yoktur. Aynı çalışma prensibi, iki paralel dahili iş hücresinde veya iki alt yüklenici hücresinde geçerlidir.   

Üretim akışındaki diğer herhangi bir etkinlik gibi, alt taşeron etkinlikleri stoklanmış, stoklanmamış (süren iş \[WIP\]), ve yarı tamamlanmış malzeme ve ürünleri tüketebilir ve tedarik edebilir. Tüm durumlarda, alt yüklenici etkinliklerinin zamanlama ve yürütülmesi için işlemler aynıdır. Ek olarak, bunlar dahili işle aynı işlemleri işler.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Alt sözleşmeli etkinlikler (hizmetler) için satın alma işlemi
Alt sözleşmeli etkinlikler için satın alma işlemi, örneğin Başlat veya Tamamla gibi kanban iş işlemi ile kaydedilen fiziksel malzeme akışına dayanır. Finansal akış, örneğin alt sözleşmeli işin maliyeti, fiziksel akışı takip eden bir ikincil akıştır. Aynı zamanda, satın alma işlemi, satın alma belgelerinin her adımda el ile ayarlanmasına izin veren bağımsız bir işlemdir. Alt sözleşmeli etkinlikler için satın alma işlemi buradadır:

1.  Bir satınalma sözleşmesi oluştur. Satın alma sözleşmesi hizmet için oluşturulur ve üretim akışının etkinliğine bağlıdır.
2.  Bir satınalma siparişi oluşturmak. Bir satın alma sevk emri, zamanlanan kanban işlerine dayalı olarak hizmet için oluşturulabilir. Aynı hizmet için işler satın alma emrine gün, hafta veya ay olarak gruplandırılabilir. Satın alma emri satırları, kanban işleri oluşturulduktan sonra herhangi bir zamanda oluşturulabilir. Satınalma siparişi satırları bundan sonra bile oluşturulabilir. Bu seçenek genellikle bir alt yüklenici hizmetleri ek bildirim olmadan, yüklenicinin edindiği kanbanlar veya kanban kartlarına dayalı olarak sağladığında seçilir. Bu durumda, satınalma emri ve fatura arasındaki sapmalar en aza indirilebilir.
3.  İşlemek üzere alt yükleniciye göndermek için kanban kartları, malzemeler ve bir malzeme çekme listesi oluştur. Üretim akışının ayrıntılı modellemesine dayalı olarak, işlem etkinlikleri için hazırlanma, kanban tahtasında malzeme çekme listesi ve hazırlama fonksiyonu kullanılarak yapılır. Hazırlık, alternatif olarak transfer işleri için kanban tahtasında, malzeme çekme listesi ve başlatma veya tamamlama kullanılarak yapılır. Stoklu malzeme için her iki işlem bir WMS çekme ve sevkiyat işlemi tarafından desteklenebilir. İsteğe bağlı olarak bir konşimento oluşturulabilir.
4.  Kanban yönetme birimleri ve kanban kartları oluştur. İşlemden sonra, kartlar alt yükleniciden döndürülür. Kartlar genellikle sevk edilmiş olan fiziksel malzemeyi belirten bir teslimat notu içerir. Sağlanan hizmetlere bir başvuru gerekli değildir. Malzeme veya ürünün müşteriye gelişi, kanban kartlarına bağlı olarak kanban tahtasında kaydedilir. (Modellenen etkinliklere bağlı olarak işlem etkinlikleri için kanban tahtası ya da transfer işleri için kanban tahtası kullanılır.).
5.  Bir danışma belgesi oluşturun. Giriş önerisi, alınan hizmetler için sevk irsaliyesi belgesinin yerine geçmek için kullanılabilir.a Giriş önerileri, alt sözleşmeyle verilen etkinliklere bağlı olarak seçilen bir dönem için oluşturulabilir. Her bir iş girişi için, ilgili satınalma emri hattında öneriler oluşturulur. Giriş önerisinin çıktısı alınabilir ve girişin teyidi olarak alt yükleniciye gönderilebilir.
6.  Bir fatura oluştur.

Alt yüklenici bir dönem için faturalandığında işlem sona erer. Fatura eşleşme, oluşturulan giriş önerilerine karşılık yapılır. Giriş önerileri malzemenin tam fiziksel girişini temsil ettiklerinden, üç yollu eşleştirme basitleştirilir.

## <a name="configuring-activities-for-subcontracting"></a>Alt sözleşme için etkinlikleri yapılandırma
Aşağıdaki bölümler, alt sözleşme için etkinlikleri yapılandırma yöntemlerini açıklamaktadır.

### <a name="subcontracted-services"></a>Alt sözleşme hizmetleri

Etkinlik tabanlı alt sözleşmede kullanılan ödeme öğesi, aşağıdaki özelliklere sahip bir ürün olmalıdır:

-   **Ürün türü:** Hizmet
-   **Stok modeli grubu:** Stoksuz

Bu gereksinim ilk giren ilk çıkar (FIFO) stok modelinin kullanımını zorlar. **Not:** Ürünlerin maliyet hesaplaması, hizmetin standart maliyetinin tanımlanmış olmasını gerektirir. Satıcıyla bir satınalma sözleşmesi gereklidir. Aksi halde hizmet alt sözleşme tabanlı etkinlikler için kullanılamaz.

### <a name="subcontracted-process-activities"></a>Alt sözleşmeli işlem etkinlikleri

Bir işlem etkinliğini alt sözleşmeli bir etkinlik olarak yapılandırmak için aşağıdaki adımları izleyin.

1.  Alt sözleşmeli iş hücresi yapılandırın. Bir iş hücresini alt sözleşmeli olarak yapılandırmak için, **Satıcı** türünde bir kaynak oluşturmalı ve onu iş hücresi (kaynak grubu) ile ilişkilendirmelisiniz. **Doğrudan dış kaynak** maliyet grubu türünün çalışma zamanı maliyeti kategorisi, iş hücresine atanmalıdır. Kurulum ve miktar için maliyet kategorileri gerekli değildir.
2.  Bir işlem etkinliği oluşturulduktan ve alt sözleşmeli bir iş hücresine ilişkilendirildikten sonra, üretim akışı sürümü etkinleştirilebilmeden önce etkinlik için bir hizmet yapılandırmanız gerekir. Bu adımı **Etkinlik** **ayrıntıları** sayfasında tamamlarsınız. Alt sözleşmeli iş hücresi ile ilişkili etkinlikler için, **Hizmet şartları** hızlı sekmesi gösterilir. Bu hızlı sekmede, tüm çıkış öğeleri için geçerli olan bir varsayılan hizmet ekleyin. Belirli çıkış öğeleri farklı hizmetlere veya farklı hizmet hesaplama parametrelerine ihtiyaç duyuyorsa (örneğin farklı bir hizmet oranı gibi), bu etkinliğe başka hizmetler ekleyebilirsiniz.

## <a name="subcontracted-transfer-activities"></a>Alt sözleşmeli transfer etkinlikleri
Transfer etkinliği, transfer etkinliğinin **Navlun sorumlusu** ayarına bağlı olarak alt sözleşmeli bir etkinlik olarak yapılandırılır. Aşağıdaki seçenekler bulunur:

-   **Nakliyeci** – Ambardan transfer bir satıcı tarafından yönetiliyorsa (ambarın bir özelliği olarak tanımlanmış şekilde) etkinlik alt sözleşmeli verilir. Hizmetler için seçili tüm satınalma sözleşmelerinin ambar ile aynı satıcı kimliğine sahip olması gerekir.
-   **Alıcı** – Ambara giden transfer bir satıcı tarafından yönetiliyorsa (ambarın bir özelliği olarak tanımlanmış şekilde) etkinlik alt sözleşmeli verilir. Hizmetler için seçili tüm satınalma sözleşmelerinin ambar ile aynı satıcı kimliğine sahip olması gerekir.
-   **Taşıyıcı** – Etkinlik, bu hizmeti sağlayan herhangi bir satıcıya alt sözleşmeli verilir. Geçerli olması için bir taşıyıcının ambar yönetimi için oluşturulmuş olması ve bir satıcı hesabının atanmış olması gerekir.

İşlem etkinlikleri için alt sözleşmeli transfer etkinlikleri için **Etkinlik** **ayrıntılarının** **Hizmet şartları** hızlı sekmesinde varsayılan bir hizmet yapılandırmalısınız.

## <a name="service-quantity-calculation"></a>Hizmet miktarı hesaplama
Tüm bu satınalma işlemi, bir hizmet için öğe referansına dayanır. Bu öğe referansı, bir hizmet ölçüm biriminde ölçülür. Hizmetler genellikle ya hizmetlerin sayısı (birim) ya da zaman cinsinden ölçülür. Kanban işlerinin kayıtlı tamamlanmalarına dayanarak hizmet miktarını hesaplamak için, aşağıdaki yöntemleri kullanabilirsiniz:

-   **İşlerin sayısına dayanan hesaplama** - Bir kanban işi *n* birim hizmete karşılık gelir, sağlanan ürün miktarı ne olursa olsun. Yalın imalatta, bir iş bir işlem birimine karşılık gelir. Bu hesaplama yöntemi, işlem birimi başına sabit bir fiyata sahip tüm hizmetlere uygulanır. Bu nedenle, bu yöntem genellikle aktarma etkinlikleri için geçerlidir. Ancak, tüm işleme birimlerini işleyen işlem etkinliklerine de uygulanabilir.
-   **Ürün miktarını temel alan hesaplama** - Hizmet miktarı, zamanlanan/sağlanan ürün miktarıyla bağıntılıdır. Sağlanan ürün miktarı hesaplandığında, hata miktarları dahil edilebilir veya hariç tutulabilir. Bu hesaplama yöntemi, işlenen ürün başına birim hizmet fiyatının önceden anlaşmaya varıldığı tüm durumlara uygulanır.
-   **Etkinlik süresine dayanan hesaplama** – Teorik etkinlik süreleri, etkinliğin işleme süresine, toplam işlenen miktara ve işlenen ürünün iş çıkarma yeteneği oranına dayanarak hesaplanır. Bu hesaplama yöntemi, saat başına ödeme yapılan hizmetlere uygulanır ve işlenmiş ürün içinde bir zaman farkı vardır.

## <a name="cost-accounting-of-subcontracted-services"></a>Alt sözleşmeli hizmetlerin maliyet muhasebesi
Bir üretim akışı için oluşturulan satınalma emri üzerindeki giriş önerisi veya satıcı sevk irsaliyesi gönderildiğinde (başka bir deyişle, alt sözleşmeli etkinlikler için kanban işlerine dayanarak oluşturulmuş bir satınalma emrinde), girişin değeri, üretim akışının süren işlerinde hesaba katılır. Faturaların sapmaları da üretim akışında hesaba katılır. Alt sözleşmeli işler için bir maliyet kategorisi de kullanıma alınmıştır. Bu maliyet kategorisi, süren iş ve dönemde tüketilen alt sözleşmeli iş değerinin şeffaf bir şekilde izlenmesine olanak sağlar.  

Bir maliyet döneminin sonundaki yalın imalat için geriye dönük maliyetlendirme, maliyetlendirme dönemi sırasında üretim akışından üretilmiş ürünlerin gerçek sapmalarını hesaplar.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Transferleri alt sözleşmeli etkinlikler olarak modelleme
İnsan taşımanın genellikle verimsiz olduğunu ve hiçbir değer eklemediğini düşünür. Ancak, alt sözleşme maliyeti, dahili üretimin maliyetiyle kıyaslandığında, ek taşıma etkinliklerinin maliyeti de dikkate alınmalıdır. Birden fazla konumu kapsayan ve taşıma hizmetlerini gerektiren bir üretim akışı, taşıma maliyetini, ürünlerin tüketiciye tedarik edilme maliyetinin bir parçası olarak dikkate almalıdır. 

Yalın üretim içerisinde etkinlik tabanlı alt sözleşme, malzemeleri ve ürünleri bir üretim akışının konumları arasında nakleden taşıyıcıları ve taşıma satıcılarını bütünleştirmenize olanak sağlar. Bir transfer etkinliğini modelleyerek, bir taşıyıcı veya satıcı atayabilirsiniz. Transfer etkinlikleri/işi, bir hizmete ve satınalma sözleşmesine dayanır ve gerçek transfer işlerine dayanan satınalma emirleri ve giriş önerileri oluşturabilirsiniz. Bu işlevsellik, alt sözleşmeli işlem etkinlikleri işlevselliğiyle aynıdır.  

Supply Chain Management artık taşıma hizmetlerini içeren ürün reçetesi hesaplamasını, ilişkili satınalma emirlerinin oluşturulmasını, tümleştirilmiş giriş kayıtlarını ve taşıma hizmeti maliyetlerini üretim akışı maliyetine katmayı destekler.



