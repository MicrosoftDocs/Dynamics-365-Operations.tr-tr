---
title: "Çekme kanbanlarıyla stok yenileme"
description: "Bu konu, çekme kanbanının malzeme stok yenileme ve üretim etkinlikleri için nasıl kullanılacağını açıklar."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 152b7908364db82481c5af4a05a9775fbabca042
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="replenishment-with-withdrawal-kanbans"></a>Çekme kanbanlarıyla stok yenileme

[!include[banner](../includes/banner.md)]


Bu konu, çekme kanbanının malzeme stok yenileme ve üretim etkinlikleri için nasıl kullanılacağını açıklar.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Çekme kanbanı kullanan malzeme stok yenileme için iş akışı
-------------------------------------------------------------------

Çekme kanbanı, malzemenin tüketildiği tek bir öğenin kanbanını ambarlar ve üretim konumları arasında taşımak için kullanılabilir. Çekme kanbanı, malzeme stok yenileme için belirli bir talep için tedariki tetiklemek üzere bir çekme sinyalinin gerekli olduğu, çekmeye dayalı bir çözüm sunmaktadır. 

Aşağıdaki senaryo, bir çekme sinyalinin bir üretim işlemi için malzemenin yenilenmesini tetikleyen bir kanbanın oluşturulduğu, çekme tabanlı bir stok yenileme sistemini gösterir. 

[![Çekme sinyali, üretim işlemi için bir stok yenilenmesi amacıyla bir kanbanın oluşturulmasını tetikler](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Çekme kanbanı
2.  Kanban "kaynak" konumu ve ambar işi için koyma konumu
3.  Kanban "giden" konumu ve üretim giriş konumu
4.  Üretim işlemi
5.  Kanban malzeme çekme için ambar işi
6.  Hammadde için ambar konumları
7.  Malzeme ambarı
8.  Üretim ambarı

Bu senaryoda, bir üretim işlemi (4), üretim ambarında (8) malzemeyi bir üretim giriş konumundan (3) tüketir. Malzemenin işleme birimi (kanban) tüketildiğinde, boş olarak kaydedilir. Bir yenileme sinyali, malzeme kaynağından oluşturulur ve yeni bir kanban (1) oluşturulur. Bu durumda, madde kaynağı, malzeme ambarındaki (7) konumlardan oluşur. Kanban için malzeme çekilir ve aynı ambardaki bir konuma (2) yerleştirilir. Bir malzeme çekildiğinde, konum 2'den, üretim ambarındaki (8) üretim giriş konumuna (3) nakledilmeye hazırdır.

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Çekme kanbanı için çekme kanbanı ambar işi yapılandır

Çekme kanbanı için hammadde çekmeyi etkinleştirmek için, dalga şablonlarını, iş şablonlarını ve konum yönergelerini **Kanban çekme** iş emri türü için yapılandırın. Bu iş emri türü, çekme kanbanı için malzeme çekme işlemini desteklemekle kalmaz. Aynı zamanda, üretim kanbanı için çekme işlemini de destekler. Ancak, dalga şablonlarını, iş şablonlarını ve konum yönergelerini ayırarak her bir kanban türü için ayrı bir çekme işlemi yapılandırabilirsiniz. Dalga şablonlarını, iş şablonlarını ve konum yönergelerini ayırmak için, etkinlik türü (**İşlem** veya **Transfer**) üzerinde, bu varlıkların sorgularında kriter ayarlayın.

## <a name="configure-the-withdrawal-kanban"></a>Çekme kanbanını yapılandır

Çekme kanbanı için kullanılan hareket etkinliği, Yalın üretim akışındaki etkinleştirilmiş bir etkinliğin parçası olarak yapılandırılır. Transfer etkinliği yapılandırmasının parçası olarak, "gelen" ve giden" konumlarını transfer için belirtirsiniz. Transfer etkinliğini yapılandırdıktan sonra, bunu **Çekme** türündeki bir kanban kuralına atayabilirsiniz. Kanban kuralı, çekme kanbanı için ilkeleri ve yapılandırmaları ayarlar. Kanbanın miktarı, transfer işlemi boyunca kanbanın kaç adet kanban birimini taşıyacağını tanımlar. Sabit kanban miktarı, Sabit stok yenileme stratejisi seçildiğinde kullanılır. Bu miktar, talebin kaynağında stok veya envanter oluşturmanın bitmesini engellemek için kaç adet kanbanın gerekli olduğunu tanımlar. Sabit miktar, fiili talebe, geçmiş talebe ve hizmet düzeylerine dayalı olarak hesaplanabilir. Aşağıdaki iki senaryo, çekme kanbanını kullanan malzeme stok yenilemesini nasıl yönetebileceğinizi açıklar.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Senaryo 1: Bir sabit çekme kanbanı kullanarak bir üretim giriş konumunu yenilemek

Bir üretim işlemi, satın alınmış hammaddeyi, üretim ambarında bulunan bir üretim giriş konumundan tüketir. Hammadde satıcıdan alındığında, malzeme ambarındaki konumlarda depolanır. Malzeme için talebin bir dönem boyunca stabil olduğu kabul edildiğinden, üretimi sabit miktar kanban akışında desteklemeye ayarlanmıştır. Bir kanban üretim girişi konumunda tüketildiğinde, bir boş sinyali kaydedilir ve aynı türdeki yeni bir kanban akışa eklenir. 

Boş sinyali, bir kanban tamamlandığında otomatik gerçekleşmek üzere yapılandırılabilir. Alternatif olarak, boş sinyal, Kanban aktarma panosu veya bir mobil cihazdaki bir menüden verilen bir el ile etkileşim olarak ayarlanabilir. Kanban transfer panosu, kanban yaşam döngüsündeki tüm etkinliklerin yönetildiği çalışma alanıdır. 

Bir kanban oluşturulduğunda, hammadde için bir dalga satırı kanban dalgasına malzeme ambarı için eklenir. Kanban transfer panosunun malzeme çekme listesi bölümünde, malzemenin ve ilgili ambar işlemlerinin durumu, malzeme "transfer edilen yer" konumundan ele bulunan ve üretim giriş konumlarına aktarılmaya hazır olana kadar, dalga oluşturma - iş oluşturma üzerinden izlenebilir. Kanban ister Kanban transfer panosundan veya bir mobil cihazın menüsünden tamamlanabilir. 

Bu senaryoda, malzeme ambarındaki çekme işi, bir etkinlik olarak işlenebilir. Malzeme ambarı ve üretim ambarı arasındaki transfer etkinliği, ayrı bir etkinlik olarak işlenir. Bu yaklaşım, örneğin iki ambar arasında büyük bir fiziksel mesafe varsa faydalı olabilir. Bu durumda, kanban transfer etkinliği bir kamyon yükünü temsil edebilir. 

Ambar konumları ve üretim giriş konumu arasındaki mesafe kısaysa, transfer etkinliğini çekme işlemine dahil etmek daha verimli olabilir. Daha sonra, malzeme çekildiğinde, doğrudan üretim giriş konumuna yerleştirilebilir. Bu işlemi desteklemek için, transfer etkinliğini, çekme kanbanının çekme işlemi tamamlandığında otomatik gerçekleşmek üzere yapılandırırsınız.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Senaryo 2: Kanban çekme işi işleme alındığında transfer etkinliğini otomatik olarak tamamla

Aşağıdaki senaryoda, çekme kanbanının transfer etkinliği, aynı ambardaki iki konum arasında transfer etmek üzere yapılandırılmıştır. Çekme kanbanının transfer etkinliği, otomatik tamamlanmak üzere ayarlanmıştır. 

[![Kanban çekme işi işlendiğinde transfer etkinliği otomatik tamamlanır](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Hammadde ve üretim için paylaşılan ambar
2.  Hammaddeler için ambar konumları
3.  Kanban "kaynak" konumu ve ambar işi için koyma konumu
4.  Çekme kanbanı
5.  Üretim giriş yeri
6.  Üretim işlemi

Bir kanban üretim girişi konumunda tüketildikten sonra, kanban boş olarak kaydedilir ve yeni bir kanban akışa eklenir. Kanban oluşturulduğunda, bir dalga satırı kanban dalgasına atanır. Bir kanban dalgası işlendiğinde, kanban çekme için bir ambar işi oluşturulur. Ambar çalışan, kanban çekme için işi işleme alır ve iş tarafından kanban için malzemeleri bir ambar konumundan almaya yönlendirilir. Bu ambar çalışanı çekmeyi onayladığında, kanban otomatik tamamlanır ve ambar çalışanı malzemeyi üretim giriş konumuna koymaya yönlendirilir.


