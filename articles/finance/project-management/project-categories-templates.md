---
title: Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme
description: Bu konuda proje gider kategorilerini Microsoft Dynamics 365 Finance ile Dynamics 365 Project Service Automation arasında eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770324"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme

[!include[banner](../includes/banner.md)]

Bu konu projeleri Dynamics 365 Finance üzerinden Dynamics 365 Project Service Automation üzerine proje maliyet kategorilerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.

> [!NOTE]
> - Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme sürüm 8.0 içinde kullanılabilir.
> - Fiili değerlerin tümleştirmesi sürüm 8.0.1 veya sonrasında kullanılabilir.
> - Enterprise Edition 7.3.0 kullanıyorsanız KB 4132657 ve KB 4132660'ı yükledikten sonra proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağılımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Project Service Automation ve Finance için veri akışı

Project Service Automation ve Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gider hareketi kategorileri hakkındaki verilerin Finance ile Project Service Automation arasında akışına olanak tanır.

Proje gider kategorilerinin ana kaydı Finance'te üretiliyorsa tümleştirme akışı, öncelikle Finance'ten Project Service Automation'a doğru olur. Proje gider kategorilerinin tümleştirme kimlikleri, Project Service Automation'dan Finance'e eşitleme yoluyla güncelleştirilir.

Proje gider kategorilerinin ana kaydı Project Service Automation'da üretiliyorsa tümleştirme akışı, öncelikle Project Service Automation'dan Finance'e doğru olur. Proje kategorileri, Project Service Automation'dan eşitleme yapılmadan önce Finance'te yapılandırılmış olmalıdır. Daha sonra Finance'ten Project Service Automation'a ve ardından yine Project Service Automation'dan Finance'e geri eşitleme yapın. Bu şekilde kategorilerin bağlantılı olduğundan ve yinelemelerin oluşmadığından emin olursunuz.

> [!NOTE]
> Proje gider kategorilerinin ana kaydı, genellikle Finance'te üretilir. Ancak Finance'te üretilmezlerse veya gider kategorileri Project Service Automation'da zaten oluşturulmuşsa öncelikle Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a) şablonunu kullanarak eşitlemeniz gerekir. Ardından Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonunu kullanarak eşitleyin. Daha sonra, Project Service Automation'dan Finance'e eşitlemeyi bir kez daha çalıştırmanız gerekir.
>
> Öncelikle Project Service Automation'dan eşitleme yaparsanız eşitleme çalıştırılmadan önce Finance'te aşağıdaki gereklilikler karşılanmalıdır:
>
> - Project Service Automation'da ayarlanan proje kategorisiyle eşleşen paylaşılan kategori mevcut olmalı ve **Proje** ile **Gider** için etkinleştirilmiş olmalıdır.
> - Tümleştirilmesi gereken her Finance tüzel kişiliği için aşağıdaki proje kategorileri mevcut olmalıdır:
>
>     - **Proje kategorisi** var. 
>     - **Giderde Kullan** etkinleştirildi.
>     - **Günlüklerde etkin** etkinleştirildi.
>     - **Hareket türü** **Gider** olarak ayarlandı.

Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.

[![Project Service Automation ile Finance tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Finance'ten Project Service Automation'a proje gider kategorisi eşitlemesi

### <a name="template-and-task"></a>Şablon ve görev

Şablona erişmek için, Microsoft Power Apps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görev, proje gider kategorilerini Finance'ten Project Service Automation'a eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya)
- **Projedeki görevin adı:** Kategorileri PSA'ya eşitleme

### <a name="entity-set"></a>Varlık kümesi

| Finans                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategoriler için tümleştirme varlığı | Hareket kategorileri     |

### <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri, Finance'te yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.

### <a name="power-query"></a>Power Query

Project Service Automation'a eşitleme yaparken Excel'de hareket kategorisinde faturalama türünü ayarlamak için Microsoft Power Query kullanmanız gerekir. Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonu bir varsayılan sütun ve eşleme sunar. Kendi şablonunuzu oluşturuyorsanız, Power Query'de koşullu bir sütun eklemeniz gerekir. Aşağıdaki adımları izleyin.

1. Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonundaki proje gideri kategorileri görevini açmak için oka tıklayın.
2. Power Query'yi açmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısına tıklayın.
2. **Koşullu Sütun Ekle**'yi seçin.
3. Yeni sütun için **Faturalama Türü** gibi bir ad girin.
4. Şu koşulu girin: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Sütunda **Tamam**'a tıklayın.
6. Bu yeni sütunu eşleme sayfasında eşlediğinizden emin olun.

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor. Eşlemede Finance'ten Project Service Automation'a eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Project Service Automation'dan Finance'e proje gider kategorisi eşitlemesi

### <a name="template-and-task"></a>Şablon ve görev

Aşağıdaki şablon ve temel görev, proje gider kategorilerini Project Service Automation'dan Finance'e eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a)
- **Projedeki görevin adı:** Kategorileri Fin Ops'a eşitleme

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                           |
|----------------------------|-----------------------------------|
| Hareket kategorileri     | Kategoriler için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri, Finance'te yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir. Finance'e geri eşitleme, Finance'teki proje kategorisini Project Service Automation'daki tümleştirme kimliği ile güncelleştirir.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.

> [!NOTE]
> Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
