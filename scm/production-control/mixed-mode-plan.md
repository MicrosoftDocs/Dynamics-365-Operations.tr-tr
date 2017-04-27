---
title: "Karışık mod planlama - Ayrık, işlem ve yalın kaynak birleştirme"
description: "Bu makale, karma mod planlama hakkında bilgi sağlar. Karma mod planlamada, tedarik zincirinizi, madde akışı tabanlı olarak modelleyebilirsiniz. Microsoft Dynamics 365 for Operations, seçili olan tedarik ilkesi ne olursa olsun malzeme akışının modellerinizi takip ettiğinden emin olur (kanbanlar, üretim emirleri, satınalma emirleri, toplu siparişler veya transfer emirleri)."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Karışık mod planlama - Ayrık, işlem ve yalın kaynak birleştirme

[!include[banner](../includes/banner.md)]


Bu makale, karma mod planlama hakkında bilgi sağlar. Karma mod planlamada, tedarik zincirinizi, madde akışı tabanlı olarak modelleyebilirsiniz. Microsoft Dynamics 365 for Operations, seçili olan tedarik ilkesi ne olursa olsun malzeme akışının modellerinizi takip ettiğinden emin olur (kanbanlar, üretim emirleri, satınalma emirleri, toplu siparişler veya transfer emirleri). 

Bir ürün sağlamak için, ürün yapısı ne olursa olsun, genel strateji seçebilirsiniz.  

Örneğin, malzeme montaj alanı için üretim emirleri, kanban, transferler, toplu sıralar, kaynağı olan bir derleme veya özelliklerini, tedarik zinciri için uygun olan herhangi bir birleşimi olan kanban denetimine sahip olabilirsiniz, ancak hâlâ kaynakları arasında tam görünürlük olabilir. Bu özellik için en iyi duruma getirilmiş tedarik zinciri süreçlerine ve tedarik zincirinize geliştirilmiş görünürlük yol açar.  

Master planlamada kullanılan tedarik ilkelerinin parçalı yapısı kapsamı boyutları olarak etkin depolama boyutlarına bağlıdır. Stok yenilemeyi ve konumları farklı türde tedariği (örneğin, üretim kat için farklı üretim birimleri ayırarak veya malzeme ve mamuller Ambarlar farklı türde ayırarak) kontrol etmek için Master çizelgeleme etkinleştirmek için kapsam boyutları olarak tesis ve ambar etkinleştirmenizi öneririz. Alternatif olarak, bir Karşılama boyutu olara ambar atlanabilir. Bu durumda, Gelişmiş ambar yönetimi kullandığınızda, ambarlar arasında tüm taşımalar mevzuatı çekme kanbanları tarafından kontrol edilebilirken bir ambarın içindeki tüm taşımalar ambar çalışma tarafından denetlenir.

## <a name="supply-policies"></a>Malzeme ilkeleri
Dynamics 365 for Operations karma mod planlama bir ürününün nasıl sağlandığını ve tedariği temel alarak türetilmiş gereksinimlerin (ürün reçetesinden \[BOM\] maddelerin tüketimi) nasıl çıkarıldığını denetler. Sipariş türüne bağlı olarak, sistem otomatik olarak gereksinimlerine göre malzeme kaynaklandırır.  

Tedarik ilkeleri ürün düzeyinde veya gereksinimlerinizi destekleyen herhangi bir ayrıntı düzeyinde tanımlanabilir. Parçalı yapı tedarik ilkelerini **varsayılan sipariş ayarları**sayfasında tanımlarsınız.  

Tedarik ilkeleri, ürün, Ürün boyutları (yapılandırma, renk ve boyut), site ve ambar tarafından denetlenebilir. Bu ayar **Madde kapsamı **sayfasında yapılır.  

Varsayılan sipariş tipi, master planlamanın hangi sırayla oluştuğunu denetler.  

Tedarik zincirinin nasıl modellendiğinden bağımsız olarak, Dynamics 365 for Operations tedarik ilkeleri karışımınızı destekler. Kanbanlardan kaynaklanan üretim emirleri olabilir. Alternatif olarak, aktarımlar veya kanbanlar tarafından sağlanan bir ürün gerektiren bir toplu iş emri olabilir.  

Dynamics 365 for Operations malzeme akışının modeli izlediğinden emin olur.  

Malzeme çekme için ambar tedarik İlkesi tanımlandıktan sonra çalışma zamanında dinamik olarak atanır.  

Genellikle, bir kanban ömrü kısa olduğundan kanbanlar gelecekteki tarihler için oluşturulmaz. Tedarik zinciri içine tam görünürlük sağlamak için biz türetilen gereksinimleri hesaplamak için kullanılan ve gerçek kanban oluşturulduğunda kullanılan aynı mantığı dayanarak gereksinimlerin kaynağa dayanmasını garanti etmeye yardımcı bir "planlanan kanban" yeni planlama kavramı sunduk.  

Diğer tüm tedarik ilke türleri için aynı mantık mevcuttur. Bu nedenle, uzun dönemli malzemeleri planlama, üretim ve tedarik onaylandıktan sonra gerçek siparişlerle ile çalıştırmak için beklediğiniz aynı mantığa dayanır.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Tedarik arası malzeme tahsisatı ilkesi – Ürün reçetelerindeki kaynak tüketimi
Kaynak tüketimi önemli bir işlevdir. Kaynak tüketimi (sipariş türü) tedarik ilkesini temel alarak bir ambar için dinamik olarak seçilen malzeme çekme sağlar ve ayrıca temel verilerin bakımını kolaylaştırır.  

Kaynak tüketimi gelen malzemelerin çekildiği ambarın ürünün tedarik şekline göre atanmasını gerektirir. Diğer bir deyişle, çalışma zamanında sistem üretim için kullanılması gereken kaynaklar bulur. Bu kaynaklara bağlı olarak, sistem sonra malzeme çekme ambarı bulur.  

Bir tedarik ilkesinden bağımsız çalışma için, tedarik değişirse ürün reçetesindeki bilgileri değiştirmeniz gerekmez. Geçici değişiklikler için Dynamics 365 for Operations malzemelerin doğru ambardan alınmasını sağlar.

## <a name="process-manufacturing--the-production-type"></a>İşlem üretimi - Üretim türü
Karma modda tam esneklik sağlamak için tüm ürünler için üretim tipi ürün reçetelerini kullanmanızı öneririz. Daha sonra ürün tedarik etmek için üretim emirleri, kanban, transfer emirleri veya satınalma siparişleri kullanabilirsiniz. İşlem üretim için **formül**, **ortak ürün**, **yan ürün**, veya **planlama madde** üretim türü kullanmanız gerekir. Kanbanlar ve üretim siparişleri bu üretim türleri için kullanılamaz.




