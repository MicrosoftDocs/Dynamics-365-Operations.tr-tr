---
title: Genel muhasebe tahsisat günlüğünü işleme
description: Bu konu, Dynamics 365 Finance'de bir tahsisat talebinin nasıl işlem yapılacağını açıklar.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186084"
---
# <a name="process-ledger-allocation-journal"></a>Genel muhasebe tahsisat günlüğünü işleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konuda bir tahsisat talebinin nasıl işleneceği açıklanmaktadır. Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için Tahsisat talebini işleme koy sayfasını kullanın. Bir tahsisatlar günlüğü oluşturmadan önce, en az bir aktif Muhasebe defteri tahsisat kuralı olmalıdır. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Gezinti bölmesinde **Modüller > Genel muhasebe > Tahsilatlar > Tahsisat talebini işleme koy**'a gidin.
2. **Kural** alanında, açılır menüden istediğiniz kaydı seçin.
3. **Başlangıç tarihi** alanında bir tarih girin.

    - Genel muhasebe kural için bir Veri kaynağı olduğunda **Başlangıç Tarihi** çok önemlidir. Bu tarih, tahsisat için eklenecek genel muhasebe bakiyelerini kontrol eder.  
    - **Sıfır kaynak** alanında **Dur**'u seçin. Bu, tahsisat işlemini durdurur ve sıfıra eşit bir kaynak tutar seçildiğini belirten bir ileti görüntüler.  

4. **Teklif seçenekleri** alanında **Yalnızca teklif** öğesini seçin. Tahsisatın genel muhasebe defterine nakledilmesinden önce Tahsisat günlüklerindeki sonucu isteğe bağlı olarak gözden geçirmek onaylamak için **Yalnızca teklif** öğesini seçin.  
5. GM deftere nakil tarihi alanında bir tarih girin.
6. **Tamam**'ı seçin.
7. Gezinti bölmesinde **Modüller > Genel muhasebe > Tahsilatlar > Tahsisat günlükleri**'ne gidin.
8. **Satırlar**'ı seçin.
9. **Naklet**'i seçin.
10. **Naklet**'i seçin.

