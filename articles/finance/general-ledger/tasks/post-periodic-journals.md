---
title: Periyodik günlükleri deftere nakletme
description: Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir.
author: aprilolson
ms.date: 11/21/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc1d9f67a515e3cdc45e173b88982feceb0ebfd
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799399"
---
# <a name="post-periodic-journals"></a>Periyodik günlükleri deftere nakletme

[!include [banner](../../includes/banner.md)]

Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir. Periyodik günlük oluştururken, yineleme için dönem aralığını gün veya ay olarak belirtirsiniz. Bu görev kılavuzu, aylık yinelenen bir periyodik günlük oluşturur.

1. **Gezinti bölmesi > Modüller > Genel muhasebe > Periyodik görevler > Periyodik günlükler**'e gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Tanım** alanına bir değer girin. Açıklama, daha sonra alındığında Periyodik günlüğün adı olacaktır. Bu yüzden ilgili bir ad verdiğinizden emin olun.
6. **Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın. Periyodik günlük genellikle birkaç günlük satırı içerir. Bu görev kılavuzu ise yalnızca bir satır ekler.
7. **Tarih** alanına bir tarih girin. **Tarih** alanı, günlük deftere bir sonraki transfer için nakil tarihini içerir. Her ay alınacak günlükler için, deftere nakledileceği tarihi kullanmanız önerilir. Bu, genellikle dönemin ilk veya son tarihidir. **Boş tarih** alanını kullanarak **Tarih** alanını boş bırakıp günlük alındığında bir tarih vermek mümkündür. Alan, hareketler alındığında sonraki yinelenen tarih için güncelleştirilir. 
8. **Hesap** alanında istediğiniz değerleri belirtin.
9. **Açıklama** alanında bir değer seçin.
10. Sayfayı kapatın.
11. **Borç** alanına bir sayı girin.
12. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
13. **Birim** alanında **Aylar**'ı seçin.
14. **Birim sayısı** alanına **1** girin.
15. **Son tarih** alanına bir tarih girin. Önceki dönemin son tarihini girmek, yanlış başlatma döneminde yanlışlıkla yinelenen günlük oluşturulmasını engeller. Son tarih, daha sonra periyodik her alındığında güncelleştirilir. 
16. **Kaydet**'e tıklayın.
17. **Gezinti bölmesi > Modüller > Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.
18. **Yeni**'ye tıklayın.
19. **Ad** alanına bir değer girin veya buradan bir değer seçin.
20. Listede, istenen kaydı bulun ve seçin.
21. Listede, seçili satırdaki bağlantıya tıklayın.
22. **Tanım** alanına bir değer girin.
23. **Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın.
24. **Eylem bölmesi**'nde **Periyodik günlük**'e tıklayın.
25. **Günlüğü al**'a tıklayın.
26. **Bitiş tarihi** alanına bir tarih girin. **Bitiş tarihi**, periyodik fiş satırları için kesme tarihi görevi görür. Yineleme ayarına bağlı olarak, sonuç olarak oluşturulan günlüğe **Son tarih** ve **Bitiş tarihi** için aynı satır bir kereden fazla eklenebilir. **Bitiş tarihi**, periyodik satırın günlüğe son kez aktarıldığını oturumun tarihine göre otomatik olarak güncelleştirilir. 
27. **Periyodik günlük numarası** alanına bir değer girin veya buradan bir değer seçin.
28. Listede, seçili satırdaki bağlantıya tıklayın.
29. **Tamam**'a tıklayın. Dönem günlüğü artık gözden geçirilebilir, onaylanabilir veya gereklilik ve ayara bağlı olarak deftere nakledilebilir.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
