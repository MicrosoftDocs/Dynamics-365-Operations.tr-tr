---
title: Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme
description: Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Project Service Automation üzerine proje maliyet kategorilerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.
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
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838379"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme

[!include[banner](../includes/banner.md)]

Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Project Service Automation üzerine proje maliyet kategorilerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.

> [!NOTE]
> - Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme Microsoft Dynamics 365 for Finance and Operations sürüm 8.0 içinde kullanılabilir.
> - Fiili değerlerin tümleştirmesi Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 veya sonrasında kullanılabilir.
> - Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automation ve Finance and Operations için veri akışı

Project Service Automation ve Finance and Operations tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gider hareketi kategorileri hakkındaki verilerin Project Service Automation ile Finance and Operations arasında akışına olanak tanır.

Proje gider kategorilerinin ana kaydı Finance and Operations'ta üretiliyorsa tümleştirme akışı ilk olarak Finance and Operations'tan Project Service Automation'a doğru olur. Proje gider kategorilerinin tümleştirme kimlikleri Project Service Automation'dan Finance and Operations'a eşitleme aracılığıyla güncelleştirilir.

Proje gider kategorilerinin ana kaydı Project Service Automation'da üretiliyorsa, tümleştirme akışı ilk olarak Project Service Automation'dan Finance and Operations'a doğru olur. Proje kategorileri, Project Service Automation'dan eşitleme yapılmadan önce Finance and Operations'ta yapılandırılmış olmalıdır. Sonrasında, geriye, yani Finance and Operations'tan Project Service Automation'a ve ardından yine Project Service Automation'dan Finance and Operations'a eşitleme yapın. Bu şekilde kategorilerin bağlantılı olduğundan ve yinelemelerin oluşmadığından emin olursunuz.

> [!NOTE]
> Proje gider kategorilerinin ana kaydı genellikle Finance and Operations'ta üretilir. Ancak Finance and Operations'ta üretilmezlerse veya gider kategorileri Project Service Automation'da zaten oluşturulmuşsa öncelikle Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a) şablonunu kullanarak eşitlemeniz gerekir. Ardından Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonunu kullanarak eşitleyin. Daha sonra Project Service Automation'dan Finance and Operations'a eşitlemeyi bir kez daha çalıştırmanız gerekir.
>
> Öncelikle Project Service Automation'dan eşitlerseniz, eşitleme çalıştırılmadan önce Finance and Operations'ta aşağıdaki gereksinimler karşılanmalıdır:
>
> - Project Service Automation'da ayarlanan proje kategorisiyle eşleşen paylaşılan kategori mevcut olmalı ve **Proje** ile **Gider** için etkinleştirilmiş olmalıdır.
> - Tümleştirilmesi gereken her Finance and Operations tüzel kişiliği için aşağıdaki proje kategorileri mevcut olmalıdır:
>
>     - **Proje kategorisi** var. 
>     - **Giderde Kullan** etkinleştirildi.
>     - **Günlüklerde etkin** etkinleştirildi.
>     - **Hareket türü** **Gider** olarak ayarlandı.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Finance and Operations'tan Project Service Automation'a proje gider kategorisi eşitlemesi

### <a name="template-and-task"></a>Şablon ve görev

Şablona erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görev, proje gider kategorilerini Finance and Operations'tan Project Service Automation'a eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya)
- **Projedeki görevin adı:** Kategorileri PSA'ya eşitleme

### <a name="entity-set"></a>Varlık kümesi

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategoriler için tümleştirme varlığı | Hareket kategorileri     |

### <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.

### <a name="power-query"></a>Power Query

Project Service Automation'a eşitleme yaparken Excel'de hareket kategorisinde faturalama türünü ayarlamak için Microsoft Power Query kullanmanız gerekir. Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonu bir varsayılan sütun ve eşleme sunar. Kendi şablonunuzu oluşturuyorsanız, Power Query'de koşullu bir sütun eklemeniz gerekir. Aşağıdaki adımları izleyin.

1. Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonundaki proje gideri kategorileri görevini açmak için oka tıklayın.
2. Power Query'yi açmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısına tıklayın.
2. **Koşullu Sütun Ekle**'yi seçin.
3. Yeni sütun için **Faturalama Türü** gibi bir ad girin.
4. Şu koşulu girin: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Sütunda **Tamam**'a tıklayın.
6. Bu yeni sütunu eşleme sayfasında eşlediğinizden emin olun.

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor. Eşleme, Finance and Operations'tan Project Service Automation'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation'dan Finance and Operations'a proje gider kategorisi eşitlemesi

### <a name="template-and-task"></a>Şablon ve görev

Aşağıdaki şablon ve temel görev, proje gider kategorilerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a)
- **Projedeki görevin adı:** Kategorileri Fin Ops'a eşitleme

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Hareket kategorileri     | Kategoriler için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir. Geriye, yani Finance and Operations'a eşitleme, Finance and Operations'taki proje kategorisini Project Service Automation'dan tümleştirme kodu ile güncelleştirir.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.

> [!NOTE]
> Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
