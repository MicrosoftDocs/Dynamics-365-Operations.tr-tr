---
title: Sabit kıymet alımları teklif etme
description: Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448669"
---
# <a name="propose-fixed-asset-acquisitions"></a>Sabit kıymet alımları teklif etme

[!include [banner](../../includes/banner.md)]

Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar. Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır. Sabit kıymeti sabit kıymet teklif günlüğü aracılığıyla almak için önce sabit kıymet kaydını oluşturmanız ve sonra kıymet defterinde edinme fiyatını tanımlamanız gerekir.

1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. Eylem bölmesinde, **Satırlar**'ı seçin.
5. **Teklifler**'i seçin.
6. **Alım teklifi**'ni seçin.
7. **Filtre**'yi seç. Önceki değerleri temizlemek için **Sıfırla**'yı seçin.
8. **Sabit varlık numarası** satırını seçin.
9. **Ölçütler** alanında bir değer girin veya seçin. Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.  
10. Bölmeden çıkmak için, iki kere **Tamam**'ı seçin.
- Oluşturulan hareket satırlarını doğrulayın.  
- Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.  
11. Bu sayfada **Defterler** sekmesini seçin.
12. **Naklet**'i seçin.
