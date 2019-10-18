---
title: Bilanço mali raporları
description: Bu makale, bilançolar için varsayılan raporları açıklar. Ayrıca, bu raporlarla ilişkili olan yapı taşlarını açıklar.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180307"
---
# <a name="balance-sheet-financial-reports"></a>Bilanço mali raporları

[!include [banner](../includes/banner.md)]

Bu makale, bilançolar için varsayılan raporları açıklar. Ayrıca, bu raporlarla ilişkili olan yapı taşlarını açıklar. 

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



<a name="additional-resources"></a>Ek kaynaklar
--------

[Mali raporlama](financial-reporting-getting-started.md)

[Mali raporları görüntüleme](view-financial-reports.md)

[Dynamics Mali Raporlama Blogu](https://blogs.msdn.com/b/dynamics_financial_reporting/)


