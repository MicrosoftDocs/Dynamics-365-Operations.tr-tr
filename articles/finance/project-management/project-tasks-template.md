---
title: Proje görevlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme
description: Bu konuda, doğrudan Microsoft Dynamics 365 Project Service Automation'dan alınan proje görevlerini Dynamics 365 Finance ile eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770278"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Proje görevlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu proje fiili değerlerini, doğrudan Dynamics 365 Project Service Automation üzerinden Dynamics 365 Finance üzerine eşitlemekte kullanılan şablonu ve alttaki görevi açıklar.

> [!NOTE]
> - Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme sürüm 8.0 içinde kullanılabilir.
> - Enterprise Edition 7.3.0 kullanıyorsanız KB 4132657 ve KB 4132660'ı yükledikten sonra proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağılımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.
> - Fiili değerlerin tümleştirmesi sürüm 8.0.1 veya sonrasında kullanılabilir.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation'dan Finance'e veri akışı

Project Service Automation ile Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje görevleri hakkındaki verilerin Project Service Automation'dan Finance'e akışına olanak tanır.

Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.

[![Project Service Automation ile Finance tümleştirmesi için veri akışı](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Şablon ve görev

Şablona erişmek için, Microsoft Power Apps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görev, Project Service Automation'dan alınan proje görevlerini Finance ile eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje görevleri (PSA'dan Fin and Ops'a)
- **Projedeki görevin adı:** Proje görevleri

Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                             |
|----------------------------|-------------------------------------|
| Proje Görevleri              | Proje görevi için tümleştirme varlığı |

## <a name="entity-flow"></a>Varlık akışı

Proje görevleri, Project Service Automation'da yönetilir ve Finance ile proje faaliyetleri olarak eşitlenir.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.

## <a name="power-query"></a>Power Query

Bu koşul karşılanırsa verilere filtre uygularken Excel için Microsoft Power Query kullanmanız gerekir:

- Proje görevinde kaynağa özgü kayıtlarınız vardır.

Power Query kullanmanız gerekiyorsa şu yönergeyi takip edin:

- Project görevleri (PSA'dan Fin and Ops) şablonunda, bir proje görevi içinden **IsLineTask** filtresini **Yanlış** olarak ayarlayarak kaynağa özgü kayıtları hariç tutan bir varsayılan filtre vardır. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde bir şablon görev eşlemeleri örneği gösteriliyor. Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
