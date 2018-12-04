---
title: "Yalın imalata genel bakış"
description: "Bu makale Dynamics 365 for Finance and Operations içindeki yalın imalat özelliklerinin genel bakışını ve açıklamasını sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 99030966587a2784f61cecbfc7f9985f75f6d779
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="lean-manufacturing-overview"></a>Yalın imalata genel bakış

[!include [banner](../includes/banner.md)]

Bu makale Microsoft Dynamics 365 for Finance and Operations içindeki yalın imalat özelliklerinin genel bakışını ve açıklamasını sağlar.

Yalın üretim, yalın operasyonları modellemede kullanabileceğiniz araçlar sunar. Bu araçlar aşağıdaki kavramları ve iş etkinliklerini öne çıkarır ve destekler:
-   Üretim ve lojistik işlemlerini, üretim akışları olarak modelleyerek yalın üretim için bir temel oluşturun.
-   Talep gereksinimlerinin sinyalini vermek için kanbanları kullanarak da bir yalın çekme sistemi uygulayabilirsiniz.
-   Kanban işlerini izleyin ve sürdürün.

Finance and Operations'daki yalın üretim mimarisi, üretim akışları, etkinlikler ve kanban kurallarından oluşur. Bu yapılar, Finance and Operations işlemleri ile tamamen tümleşiktir. Yalın üretimi çeşitli tedarik, üretim ve kaynak belirleme stratejilerini birleştiren bir karma mod üretim ortamında kullanabilirsiniz. Bu stratejilere üretim emirleri, işlem endüstrileri için toplu siparişler, satınalma siparişleri ve transfer emirleri dahildir.

| **Önemli**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finance and Operations'u, kanbanlar ile yalın üretim uygulamasını desteklemek için kullanabilirsiniz. Ancak, yalın prensiplerin başarılı bir şekilde uygulaması, kullandığınızı dahili iş süreçlerine ve gerçek üretim koşulları ve ortamına bağlıdır. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Üretimi, üretim akışları ve lojistik süreçleri olarak modelleme
Yalın üretim için bir temel oluşturmak için üretim ve lojistik işlemlerini, üretim akışları olarak modelleyin. Bu etkinlik aşağıdaki görevleri içerir:
1.  Yalın stok yenileme stratejisi uygulamak istediğiniz işlemleri tanımlayın ve sonra bu işlemleri üretim akışları olarak modelleyin. Daha sonra işlemleri çözümleyebilir ve daha verimli hale getirebilirsiniz. Yalın uygulamanın amaçlarından bir tanesi, malzeme ve bilgi akışını iyileştirip atık malzemeyi azaltmaktır.
2.  Bir üretim akışını, malzemenin akışını tanımlayan bir dizi etkinlik olarak tanımlayın. Transfer etkinlik, bir ürün veya ürünlerin bir konumdan diğerine hareketini tanımlar. Bir işlem etkinliği, bir ürüne uygulanan katma değerli bir işlemi tanımlar.
3.  Takt zamanı ile ilgili gereklilikleri tanımlayan bir üretim akışı sürümü oluşturun. Bu gereksinimler, üretim akışındaki her faaliyetin döngü sürelerini hesaplamak için kullanılır. Üretim akışlarının birden çok sürümünü oluşturabilir ve süreçleri geliştirmek için bu sürümleri kullanabilirsiniz.

## <a name="using-kanbans-to-signal-demand-requirements"></a> Talep gereksinimlerinin sinyalini vermek için kanbanlar kullanmak
Bir çekme sistemi, sadece mal gerektiğinde mal üretir. Bu yöntem fazladan stok ve teslimat sağlama sürelerini azaltır. Kanbanları üretim akışlarına dayalı olan gereksinimleri planlamak, izlemek ve işlemek için kullanabilirsiniz. Bir kanban çerçevesi oluşturmak için, kanbanların ne zaman oluşturulacağını ve gereksinimlerin nasıl karşılanacağını tanımlayan kurallar oluşturun. İki tür kanban kuralı oluşturabilirsiniz. Üretim kuralları işlem kanban işlerini oluşturur. Çekme kanban kuralları, hareket kanban işlerini oluşturur. Aşağıdaki stok yenileme stratejilerini ayarlayabilirsiniz:
-   **Sabit miktar** kanban kuralları sabir sayıda işleme birimiyle ilişkilidir, bu da etkin kanbanların sayısının sabit olduğu anlamına gelir. Bir Kanban'dan tüm ürünler tüketildiğinde ve işleme birimleri el ile boşaltıldığında, aynı türde yeni bir kanban oluşturulur. Sabit miktar kanban kuralları oluşturduğunuzda, en iyi kanban miktarlarını ve kullanılan ürün miktarlarını hesaplayabilirsiniz. Hesaplama maddeleri yenilemek için tahminleri, açık siparişlerden fiili talebi, sağlaması süresini ve geçmiş talepleri dikkate alır.
-   **Zamanlanmış** kanban kuralları master planlama tarafından hesaplanan gereksinimleri yeniler. Master planlama, kanbanlara kesinleştirilebilecek planlı kanbanları oluşturur.
-   **Olay** kanban kuralları, satış siparişi satırlarından, üretim ürün reçetesi satırlarından, kanban satırlarından ya da minimum stok ayarlarından ileri gelen gereksinimleri yeniler. Olay kanbanları oluşturulduğunda, bunlar kaynak gereksinimleriyle ilişkilendirilir.

Kanbanlar oluşturulduğunda, kanban kurallarında tanımlanan kanban akışı aktivitelerine dayanan bir veya birden fazla kanban işi oluşturulur.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Kanban işlerini izlemek ve sürdürmek
Yalın üretim, kanban kurallar tarafından yönetilen üretim ve lojistik faaliyetlerinin geçerli durumuna bir bakış sağlar. Sonuç olarak, aşağıdaki görevleri planlayabilir ve öncelik verebilirsiniz:

-   Geçerli kanban iş planlamasının genel bir bakışını elde edin.
-   Kanban işlerini planlayın ve yeniden zamanlayın.
-   Kanban işlerinin durumunu izleyin ve kaydedin.

Özelleştirilmiş kanban panoları aşağıdaki listede açıklanmaktadır:
-   Kanban iş çizelgeleme – Kanban işlerine genel bir bakış sağlar. Pano, kanban işlerini ve bunların bir veya birden çok iş hücresi için durumlarını görüntüler. İşler, üretim akışı modelde tanımlanmış planlama dönemine (gün veya hafta) göre listelenir. Zamanlanmış yüklemeleri izleyebilmeniz için tahta aynı zamanda her planlama dönemi için kapasite tüketimini de görüntüler. Kanban işlerinin durumunu değiştirebilir, farklı planlama dönemi kanban işlerini yeniden zamanlayabilir ve başka görevleri gerçekleştirebilirsiniz.
-   Transfer işleri için kanban panosu – Bu pano, geçerli aktarım işlerine genel bakış sağlar. Malzeme çekme listelerini kaydedebilir ve güncelleştirebilir, transfer işlerini başlatabilir ve tamamlayabilir ve diğer görevleri gerçekleştirebilirsiniz.
-   Süreç işleri için kanban panosu – Bu pano, normal üretim akışını desteklemek ve bir veya birden çok iş hücresinin geçerli durumuna bir bakış sağlamak üzere tasarlanmıştır. Bu tahtadan kanbanlara öncelik verebilir, çekebilir veya üretilebilir. Ayrıca bu tahta kanbanların raporlaması için barkod taramayı da desteklemek üzere tasarlanmıştır.

## <a name="kanban-jobs-and-integration-with-finance-and-operations-processes"></a>Kanban işleri ve Finance and Operations işlemleri ile tümleştirme
Kanban işleri Finance and Operations'ta stok hareketleri için geçerli işlemler ile tamamen tümleşiktir.
-   Kanban iş gereksinimlerini karşılamak için kullanılan malzeme stoğunu yenilemek için malzeme çekme etkinlikleri gerçekleştirebilirsiniz.
-   Kanban kartları, sirkülasyon kanban kartları ve malzeme çekme listelerinin kanban kullanımını desteklemek için yazdırabilirsiniz. Bu belgeler kanban işlerini ambarda ve üretim sahasında temsil etmek, izlemek ve kaydetmek için kullanılır.
-   Bar kodlarını tarayarak stoktaki malzeme çekme ve transfer etkinliklerini kaydedebilirsiniz.

Ek olarak, yalın üretim taşeron etkinlikler tarafından referans gösterilen hizmetleri satın alma ve faturalama işlemlerini de destekler.
-   Satınalma sözleşmesi satırlarını ve hizmetlerini taşeron faaliyetlerine atayabilirsiniz.
-   Hizmetlerin satınalınması ve faturalamasına destek için dönemsel satınalma siparişleri ve giriş önerileri oluşturabilirsiniz.






