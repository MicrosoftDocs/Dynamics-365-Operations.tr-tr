---
title: "Bilanço mali raporları"
description: "Bu makalede varsayılan raporları Bilançolar için. Ayrıca, bu raporları ile ilişkili olan yapı taşlarını açıklanır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 664d32c2bfecb50e24fd48a66ab5b34cef6c09a3
ms.lasthandoff: 03/31/2017


---

# <a name="balance-sheet-financial-reports"></a>Bilanço mali raporları

Bu makalede varsayılan raporları Bilançolar için. Ayrıca, bu raporları ile ilişkili olan yapı taşlarını açıklanır. 

<a name="default-balance-sheet-reports"></a>Varsayılan bilanço raporları
-----------------------------

İki farklı varsayılan bilanço raporu vardır. Bir raporda bölümler üst üste yerleştirilir. Diğer raporda ise bölümler yan yanadır.

| Varsayılan rapor                       | Ne yapar                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Bakiye – Varsayılan              | İlgili yıl için organizasyonun mali pozisyonunun görünümünü sağlar.                                                                 |
| Yan Yana Bilanço – Varsayılan | İlgili yıl için organizasyonun mali pozisyonunun görünümünü sağlar. Kıymetler ve borç ve hissedarın öz varlığı yan yanadır. |

## <a name="building-blocks"></a>Yapı taşları
Bilanço mali raporları aşağıdaki yapı taşlarını kullanır.

| Varsayılan rapor                       | Satır tanımı                       | Sütun tanımı             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Bilanço - Varsayılan              | Bilanço - Varsayılan              | YTD ve Fark - Varsayılan    |
| Yan Yana Bilanço – Varsayılan | Yan Yana Bilanço – Varsayılan | Yılbaşından Bugüne Sütunu - Varsayılan |

### <a name="row-definition"></a>Satır tanımı

Her iki bilanço raporu için satır tanımları klasik bir bilançonun her bir parçası için bölümler içerir. Yan yana rapor bir sütun boşluğu içerir, böylece borç ve şirket sahibinin öz varlığı, kıymetlerin yanında görüntülenir. Ana Hesap Kategorisi boyutu her iki satır tanımının oluşturulması için kullanılır. Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan raporlar oluşturabilir.

### <a name="column-definition"></a>Sütun tanımı

Sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.

-   **YTD ve Fark – Varsayılan sütun türleri:**
    -   **DESC** – Satır tanımının açıklaması
    -   **FD** – Mevcut yıl için yılbaşından bugüne mali veriler
    -   **FD** – Geçen yıl için yılbaşından bugüne mali veriler
    -   **CALC** – Bu yıldan geçen yılın çıkarılmasıyla elde edilen fark

<!-- -->

-   **Yılbaşından Bugüne Sütunu – Varsayılan:**
    -   **DESC** – Satır tanımının açıklaması
    -   **FD** – Mevcut yıl için yılbaşından bugüne mali veriler

 

<a name="see-also"></a>Ayrıca bkz.
--------

[Financial reporting](financial-reporting-getting-started.md)

[View financial reports](view-financial-reports.md)

[Dynamics finansal raporlama Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)


