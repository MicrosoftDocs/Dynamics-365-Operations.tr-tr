---
title: Bilanço mali raporları
description: Bu makale, bilançolar için varsayılan raporları açıklar. Ayrıca, bu raporlarla ilişkili olan yapı taşlarını açıklar.
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643836"
---
# <a name="balance-sheet-financial-reports"></a>Bilanço mali raporları

[!include [banner](../includes/banner.md)]

Bu makale, bilançolar için varsayılan raporları açıklar. Ayrıca, bu raporlarla ilişkili olan yapı taşlarını açıklar. 

## <a name="default-balance-sheet-reports"></a>Varsayılan bilanço raporları

İki farklı varsayılan bilanço raporu vardır. Bir raporda bölümler üst üste yerleştirilir. Diğer raporda ise bölümler yan yanadır.

| Varsayılan rapor                       | Ne yapar                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| Bilanço – Varsayılan              | İlgili yıl için organizasyonun mali pozisyonunun görünümünü sağlar.                    |
| Bilanço ve Gelir Beyanı Yan Yana - Varsayılan | İlgili yıl için kuruluşun mali durumunun yan yana görünümünü sağlar. |

## <a name="building-blocks"></a>Yapı taşları
Bilanço mali raporları aşağıdaki yapı taşlarını kullanır.

| Varsayılan rapor                       | Satır tanımı                       | Sütun tanımı             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Bilanço - Varsayılan              | Bilanço - Varsayılan              | YTD ve Fark - Varsayılan    |
| Bilanço ve Gelir Beyanı Yan Yana - Varsayılan | Bilanço ve Gelir Beyanı Yan Yana - Varsayılan | Yılbaşından Bugüne Sütunu - Varsayılan |

### <a name="row-definition"></a>Satır tanımı

Her iki bilanço raporu için satır tanımları klasik bir bilançonun her bir parçası için bölümler içerir. Yan yana rapor bir sütun boşluğu içerir, böylece borç ve şirket sahibinin öz varlığı, kıymetlerin yanında görüntülenir. Ana Hesap Kategorisi boyutu her iki satır tanımının oluşturulması için kullanılır. Bu nedenle, hiçbir değişiklik yapmadan herkes rapor oluşturabilir.

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



## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlamaya genel bakış](financial-reporting-getting-started.md)

[Mali raporları görüntüleme](view-financial-reports.md)

[Dynamics Mali Raporlama Blogu](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
