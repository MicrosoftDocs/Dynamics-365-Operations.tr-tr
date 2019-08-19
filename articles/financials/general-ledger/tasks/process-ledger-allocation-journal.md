---
title: Genel muhasebe tahsisat günlüğünü işleme
description: Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için Tahsisat talebini işleme koy sayfasını kullanın.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846379"
---
# <a name="process-ledger-allocation-journal"></a>Genel muhasebe tahsisat günlüğünü işleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için Tahsisat talebini işleme koy sayfasını kullanın. Bir tahsisatlar günlüğü oluşturmadan önce, en az bir aktif Muhasebe defteri tahsisat kuralı olmalıdır. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Genel muhasebe > Tahsisatlar > Tahsisat talebini işlem koy'a gidin.
2. Kural alanında, aramayı açmak için açılır menü düğmesini tıklatın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Başlangıç tarihi alanında bir tarih girin.
    * Genel muhasebe kural için bir Veri kaynağı olduğunda Başlangıç Tarihi çok önemlidir. Bu tarih, tahsisat için eklenecek genel muhasebe bakiyelerini kontrol eder.     Sıfır kaynak alanında Dur'u seçin. Bu, tahsisat işlemini durdurur ve sıfıra eşit bir kaynak tutar seçildiğini belirten bir ileti görüntüler.  
6. Teklif alanında 'Yalnızca teklif' öğesini seçin.
    * Tahsisatın genel muhasebe defterine nakledilmesinden önce Tahsisat günlüklerindeki sonucu isteğe bağlı olarak gözden geçirmek onaylamak için Yalnızca teklif öğesini seçin.  
7. GM deftere nakil tarihi alanında bir tarih girin.
8. Tamam'a tıklayın.
9. Genel muhasebe > Tahsisatlar > Tahsisat günlükleri'ne gidin.
10. Satırlar seçeneğine tıklayın.
11. Deftere Naklet öğesine tıklayın.
12. Deftere Naklet öğesine tıklayın.

