---
title: "Project Service Automation'dan proje gider kategorilerini eşitleme"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations ile Dynamics 365 for Project Service Automation arasında proje gider kategorilerini eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme

Bu konu, Microsoft Dynamics 365 for Finance and Operations ile Dynamics 365 for Project Service Automation arasında proje gider kategorilerini eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır.

> [!NOTE]
> Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automation ve Finance and Operations için veri akışı

Project Service Automation ve Finance and Operations tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gider hareketi kategorileri hakkındaki verilerin Project Service Automation ile Finance and Operations arasında akışına olanak sağlar.

Proje gider kategorilerinin ana kaydı Finance and Operations'ta üretiliyorsa, tümleştirme akışı ilk olarak Finance and Operations'tan Project Service Automation'a doğru olur ve sonra proje gider kategorilerinin tümleştirme kodları, Project Service Automation'dan Finance and Operations'a eşitlemeyle güncelleştirilir.

Proje gider kategorilerinin ana kaydı Project Service Automation'da üretiliyorsa, tümleştirme akışı ilk olarak Project Service Automation'dan Finance and Operations'a doğru olur. Project Service Automation'dan eşitleme yapılmadan önce proje kategorileri Finance and Operations'ta yapılandırılmış olmalıdır. Bunun ardından, geriye, yani Finance and Operations'tan Project Service Automation'a ve ardından yine Project Service Automation'dan Finance and Operations'a eşitleme yapın. Bu, kategorilerin birbiriyle bağlantılı olmasını sağlar ve yinelemeler oluşmaz.

> [!NOTE]
> Proje gider kategorilerinin ana kaydı genellikle Finance and Operations'ta üretilecektir. Durum böyle değilse veya gider kategorilerini önceden Project Service Automation'da oluşturduysanız, ilk olarak Proje gider hareketi kategorilerini kullanarak eşitleme yapmanız (PSA'dan Fin and Ops'a) ve ardından yine Proje gider hareketi kategorilerini kullanarak (Fin and Ops'tan PSA'ya) bir kez daha eşitleme yapmanız gerekir. Bunun ardından PSA'dan Fin and Ops'a eşitlemeyi bir kez daha çalıştırmanız gerekir.

> Eşitleme ilk olarak Project Service Automation'dan yapılıyorsa, proje kategorileri önceden Finance and Operations'ta ayarlanması ve Project Service Automation hareket kategorileriyle eşitlenmesi gereken tüm proje kategorilerinin **Günlüklerde etkin** olacak şekilde ayarlanması gerekir.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps Yönetim Merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görev, proje gider kategorilerini Finance and Operations'tan Project Service Automation'a eşitlemek için kullanılır:

-  **Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya)
-  **Projedeki görevin adı:** Kategorileri PSA'ya eşitleme

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Kategoriler için tümleştirme varlığı    | Hareket kategorileri        |

## <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.

## <a name="power-query"></a>Power Query

Project Service Automation'a eşitleme yaparken hareket kategorisinde faturalama türünü ayarlamak için Microsoft Power Query kullanmanız gerekir. Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonunda bir varsayılan sütun ve eşleme zaten sağlanmıştır. Kendi şablonunuzu oluşturuyorsanız, Power Query'de koşullu bir sütun eklemeniz gerekir.
- Proje gider kategorilerini eşleme görevinin içinden Gelişmiş Sorgu ve Filtreleme formunu açın.
- **Koşullu Sütun Ekle**'yi seçin.
- Yeni sütuna bir ad verin (örneğin FaturalamaTürü).
- Şu koşulu girin: if **CATEGORYID not equal to null then 19235001, Otherwise null**.
- Sütunda **Tamam**'a tıklayın.
- Bu yeni sütunu Eşleme sayfasında eşlediğinizden emin olun.

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor. Eşleme, Finance and Operations'tan Project Service Automation'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Aşağıdaki şablon ve temel görev, proje gider kategorilerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

-**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a) -**Projedeki görevin adı:** Kategorileri Fin Ops'a eşitleme

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Hareket kategorileri          | Kategoriler için tümleştirme varlığı  | 

## <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir. Geriye, yani Finance and Operations'a eşitleme, Project Service Automation'dan tümleştirme kodunu Finance and Operations proje kategorisinde güncelleştirir.

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.

> [!NOTE]
> Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

