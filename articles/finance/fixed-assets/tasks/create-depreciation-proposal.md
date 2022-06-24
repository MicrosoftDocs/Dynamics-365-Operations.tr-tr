---
title: Amortisman önerisi oluşturma
description: Bu makalede, toplu amortisman tekliflerinin nasıl işlediği ve sabit kıymetler için amortisman teklifinin nasıl yapıldığı açıklanmaktadır.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1f39a1412c6f96fe0a8261602a88a6a3c3cd6b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858510"
---
# <a name="create-a-depreciation-proposal"></a>Amortisman önerisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu makalede, toplu amortisman tekliflerinin nasıl işlediği ve sabit kıymetler için amortisman teklifinin nasıl yapıldığı açıklanmaktadır. Bu görevde USMF demo şirketi ve muhasebeci rolü kullanılmaktadır.


## <a name="create-a-depreciation-proposal"></a>Amortisman önerisi oluşturma
1. Gezinti bölmesinde **Sabit kıymetler > Günlük girişleri > Amortisman önerisi oluştur**'a gidin.
2. **Günlüğün adı** alanında, açılır menüden bir seçenek belirleyin.
3. **Bitiş tarihi** alanına bir tarih girin.

    - **Aylık amortismanlar**'ı bir günlük satırında özetlemek için Amortismanı özetle'yi seçin.  
    - Örneğin, Bitiş tarihi değeri 31 Mart 2015 ise, aşağıdaki açıklama oluşturulur: "31 Ocak 2015'ten itibaren amortisman". Önerilen günlük satırları üzerindeki **Tarih** alanı 31 Mart 2015'tir.  
    - Amortisman teklifine, kıymet, kıymet grubu veya diğer ölçütlere göre **Filtre** seçeneği kullanılarak filtre uygulanabilir.  
    - **Sabit kıymetler için alım veya amortisman teklifleri oluşturun** formunu kullanırken amortismanı toplu işler halinde teklif edebilirsiniz. Bu, daha fazla sistem kaynağı kullanan büyük teklifler için önerilir. Toplu iş seçeneğini belirtirseniz, bu süre içinde diğer görevleri tamamlayabilirsiniz. Amortismanı bu yolla teklif ettiğiniz zaman, sabit kıymetlerle ilgili değer modelleri için amortisman hesaplanır.  

4. **Günlük oluştur**'u seçin.

## <a name="review-depreciation-entries"></a>Amortisman girişlerini gözden geçirin
1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. **Satırlar**'ı seçin.
4. **Naklet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
