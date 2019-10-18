---
title: Gelir tablosu mali raporu
description: Bu makale varsayılan rapor için gelir tablolarını açıklar. Ayrıca, bu raporla ilişkili olan yapı taşlarını açıklar.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180295"
---
# <a name="income-statement-financial-report"></a>Gelir tablosu mali raporu

[!include [banner](../includes/banner.md)]

Bu makale varsayılan rapor için gelir tablolarını açıklar. Ayrıca, bu raporla ilişkili olan yapı taşlarını açıklar. 

<a name="default-income-statement-report"></a>Varsayılan gelir tablosu raporu
-------------------------------

| Varsayılan rapor             | Ne yapar                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Gelir Beyanı – Varsayılan | Geçerli dönem ve ayrıca yılbaşından bugüne kadar olan süre için organizasyonun karlılığını gösterir. |

## <a name="building-blocks"></a>Yapı taşları
Gelir tablosu mali raporu aşağıdaki yapı taşlarını kullanır.

| Varsayılan rapor             | Satır tanımı                     | Sütun tanımı          |
|----------------------------|------------------------------------|----------------------------|
| Gelir Tablosu - Varsayılan | Özet Gelir Tablosu - Varsayılan | Dönemsel ve YTD - Varsayılan |

### <a name="row-definition"></a>Satır tanımı

Satır tanımı, Özeti Gelir Tablosu – Varsayılan, klasik bir gelir tablosunun her bir kısmı için bir bölüm içerir. Ana Hesap Kategorisi boyutu bu satır tanımının oluşturulması için kullanılır. Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan rapor oluşturabilir.

### <a name="column-definition"></a>Sütun Tanımı

Sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.

-   **Dönemsel ve YTD – Varsayılan sütun türleri:**
    -   **DESC** – Satır tanımının açıklaması
    -   **FD** – Mevcut dönem için mali veriler
    -   **FD** – Yılbaşından bugüne kadar olan süre için mali veriler



<a name="additional-resources"></a>Ek kaynaklar
--------

[Mali raporlama](financial-reporting-getting-started.md)

[Mali raporları görüntüleme](view-financial-reports.md)

[Dynamics Mali Raporlama Blogu](https://blogs.msdn.com/b/dynamics_financial_reporting/)



