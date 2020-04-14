---
title: Amortisman önerisi oluşturma
description: Bu konu, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142837"
---
# <a name="create-a-depreciation-proposal"></a>Amortisman önerisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar. Bu görevde USMF demo şirketi ve muhasebeci rolü kullanılmaktadır.


## <a name="create-a-depreciation-proposal"></a>Amortisman önerisi oluşturma
1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Amortisman önerisi oluştur**'a gidin.
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

