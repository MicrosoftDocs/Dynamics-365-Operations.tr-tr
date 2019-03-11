---
title: Periyodik günlükleri deftere nakletme
description: Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deae523d922e1d6a4f7bb05433e9b1568c9c1ee9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "351321"
---
# <a name="post-periodic-journals"></a>Periyodik günlükleri deftere nakletme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir. Periyodik günlük oluştururken, yineleme için dönem aralığını gün veya ay olarak belirtirsiniz. Bu görev kılavuzu, aylık yinelenen bir periyodik günlük oluşturur.



1. Genel muhasebe > Periyodik görevler > Periyodik günlükler'e gidin.
2. Yeni'ye tıklayın.
3. Ad alanına bir değer girin veya buradan bir değer seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Açıklama alanına bir değer girin.
    * Açıklama, daha sonra alındığında Periyodik günlüğün adı olacaktır. Bu yüzden ilgili bir ad verdiğinizden emin olun.  
6. Satırlar seçeneğine tıklayın.
    * Periyodik günlük genellikle birkaç günlük satırı içerir. bu görev kılavuzu ise yalnızca bir satır ekler.  
7. Tarih alanına bir tarih girin.
    * Tarih alanı günlük deftere bir sonraki transfer için nakil tarihini içerir. Her ay alınacak günlükler için, deftere nakledileceği tarihi kullanmanız önerilir; bu genel olarak dönemin ilk veya son tarihidir. Tarih alanını boş bırakıp günlük alındığında Boş tarih alanını kullanarak bir tarih vermek de mümkündür.    Alan, hareketler alındığında sonraki yinelenen tarih için otomatik olarak güncelleştirilir.  
8. Hesap alanında istediğiniz değerleri belirtin.
9. Açıklama alanına bir değer girin.
10. Sayfayı kapatın.
11. Borç alanına bir sayı girin.
12. Mahsup hesap alanında istediğiniz değerleri belirtin.
13. Birim alanında 'Aylar'ı seçin.
14. Birim sayısı alanına '1' girin.
15. Son tarih alanına bir tarih girin.
    * Önceki dönemin son tarihini girmek, yanlış başlatma döneminde yanlışlıkla yinelenen günlük oluşturulmasını engeller. Son tarih, daha sonra periyodik her alındığında güncelleştirilir.  
16. Kaydet'e tıklayın.
17. Varsayılan panoya gidin.
18. Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.
19. Yeni'ye tıklayın.
20. Ad alanına bir değer girin veya buradan bir değer seçin.
21. Listede, istenen kaydı bulun ve seçin.
22. Listede, seçili satırdaki bağlantıya tıklayın.
23. Açıklama alanına bir değer girin.
24. Satırlar seçeneğine tıklayın.
25. Periyodik günlük öğesine tıklayın.
26. Günlüğü al'a tıklayın.
27. Bitiş tarihi alanına bir tarih girin.
    * Bitiş tarihi, periyodik fiş satırları için kesme tarihi görevi görür. Yineleme ayarına bağlı olarak, sonuç olarak oluşturulan günlüğe Son tarih ve Bitiş tarihi için aynı satır bir kereden fazla eklenebilir. Bitiş tarihi, periyodik satırın günlüğe son kez aktarıldığını oturumun tarihine göre otomatik olarak güncelleştirilir.  
28. Periyodik günlük numarası alanına bir değer girin veya buradan bir değer seçin.
29. Listede, seçili satırdaki bağlantıya tıklayın.
30. Tamam'a tıklayın.
    * Dönem günlüğü artık gözden geçirilebilir, onaylanabilir veya gereklilik ve ayara bağlı olarak deftere nakledilebilir.  

