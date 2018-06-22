---
title: "Project Service Automation'dan proje görevlerini eşitleme"
description: "Bu konu, proje görevlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonu ve temel görevi açıklamaktadır."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Project Service Automation'dan proje görevlerini Finance and Operations'taki proje faaliyetlerine doğrudan eşitleme

Bu konu, proje görevlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonu ve temel görevi açıklamaktadır.

> [!NOTE]
> Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation'dan Finance and Operations'a veri akışı

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje görevleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Şablon ve görev

Şablona erişmek için, Microsoft PowerApps Yönetim Merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görev, proje görevlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

-**Veri tümleştirmedeki şablonun adı:** Proje görevleri (PSA'dan Fin and Ops'a) -**Projedeki görevin adı:** Proje görevleri

Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.

## <a name="entity-set"></a>Varlık kümesi

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Proje Görevleri                           | Proje görevi için tümleştirme varlığı.   |

## <a name="entity-flow"></a>Varlık akışı

Proje görevleri Project Service Automation'da yönetilir ve Finance and Operations'a proje faaliyetleri olarak eşitlenir.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.

## <a name="power-query"></a>Power Query

Şu koşullar karşılanırsa, verilere filtre uygulamak için Microsoft Power Query kullanmanız gerekir:

- Bir proje görevinde kaynağa özgü kayıtlarınız vardır.

Power Query kullanmanız gerekiyorsa şu yönergeleri takip edin:

- Project görevleri (PSA'dan Fin and Ops) şablonunda, bir proje görevi içinden, **IsLineTask**'taki filtreyi **Yanlış**'a ayarlayarak kaynağa özgü kayıtları hariç tutmak için kullanılan bir varsayılan filtre vardır. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde bir şablon görev eşlemeleri örneği gösteriliyor. Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


