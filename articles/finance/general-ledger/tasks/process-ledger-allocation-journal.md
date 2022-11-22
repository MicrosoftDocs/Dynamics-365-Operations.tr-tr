---
title: Genel muhasebe tahsisat günlüğünü işleme
description: Bu makale, Dynamics 365 Finance'te bir tahsisat talebinin nasıl işleneceğini açıklar.
author: aprilolson
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779405"
---
# <a name="process-ledger-allocation-journal"></a>Genel muhasebe tahsisat günlüğünü işleme

[!include [banner](../../includes/banner.md)]

Bu makalede bir tahsisat talebinin nasıl işleneceği açıklanmaktadır. Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için **Tahsisat talebini işleme koy** sayfasını kullanın. Bir tahsisatlar günlüğü oluşturmadan önce, en az bir aktif Muhasebe defteri tahsisat kuralı olmalıdır. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Gezinti bölmesinde **Genel muhasebe > Tahsisatlar > Tahsisat talebini işleme koy**'a gidin.
2. **Kural** alanında, açılır menüden istediğiniz kaydı seçin.
3. **Başlangıç tarihi** alanında bir tarih girin.

    - Genel muhasebe kural için bir Veri kaynağı olduğunda **Başlangıç Tarihi** çok önemlidir. Bu tarih, tahsisat için eklenecek genel muhasebe bakiyelerini kontrol eder.  
    - **Sıfır kaynak** alanında **Dur**'u seçin. Bu, tahsisat işlemini durdurur ve sıfıra eşit bir kaynak tutar seçildiğini belirten bir ileti görüntüler.  

4. **Teklif seçenekleri** alanında **Yalnızca teklif** öğesini seçin. Tahsisatın genel muhasebe defterine nakledilmesinden önce **Tahsisat günlüklerindeki** sonucu isteğe bağlı olarak gözden geçirmek onaylamak için **Yalnızca teklif** öğesini seçin.  
5. **GM deftere nakil tarihi** alanında bir tarih girin.
6. **Tamam**'ı seçin.
7. Gezinti bölmesinde **Modüller > Genel muhasebe > Tahsilatlar > Tahsisat günlükleri**'ne gidin.
8. **Satırlar**'ı seçin.
9. **Naklet**'i seçin.
10. **Naklet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
