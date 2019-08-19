---
title: Amortisman önerisi oluştur
description: Bu prosedür, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840013"
---
# <a name="create-depreciation-proposal"></a>Amortisman önerisi oluştur

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar. Bu görevde USMF demo şirketi ve muhasebeci rolü kullanılmaktadır.


## <a name="create-depreciation-proposal"></a>Amortisman önerisi oluştur
1. Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.
2. Günlüğün adı alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Bitiş tarihi alanına bir tarih girin.
    * Aylık amortismanları bir günlük satırında özetlemek için Amortismanı özetle'yi seçin.  
    * Örneğin, Bitiş tarihi değeri 31 Mart 2015 ise, aşağıdaki açıklama oluşturulur: "31 Ocak 2015'ten itibaren amortisman". Önerilen günlük satırları üzerindeki Tarih alanı 31 Mart 2015'tir.  
    * Amortisman teklifine, kıymet, kıymet grubu veya diğer ölçütlere göre Filtre seçeneği kullanılarak filtre uygulanabilir.  
    * Sabit kıymetler için alım veya amortisman teklifleri oluşturun formunu kullanırken amortismanı toplu işler halinde teklif edebilirsiniz. Bu, daha fazla sistem kaynağı kullanan büyük teklifler için önerilir. Toplu iş seçeneğini belirtirseniz, bu süre içinde diğer görevleri tamamlayabilirsiniz. Amortismanı bu yolla teklif ettiğiniz zaman, sabit kıymetlerle ilgili değer modelleri için amortisman hesaplanır.  
5. Günlük oluştur'a tıklayın.

## <a name="review-depreciation-entries"></a>Amortisman girişlerini gözden geçirin
1. Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Satırlar seçeneğine tıklayın.
4. Deftere Naklet öğesine tıklayın.

