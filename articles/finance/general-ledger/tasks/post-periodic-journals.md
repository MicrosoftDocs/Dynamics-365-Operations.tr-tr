---
title: Periyodik günlükleri deftere nakletme
description: Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99d157e82f8451e2c8f0bc7946ba30ca48e99add
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968516"
---
# <a name="post-periodic-journals"></a>Periyodik günlükleri deftere nakletme

[!include [banner](../../includes/banner.md)]

Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir. Periyodik günlük oluştururken, yineleme için dönem aralığını gün veya ay olarak belirtirsiniz. Bu görev kılavuzu, aylık yinelenen bir periyodik günlük oluşturur.

1. **Gezinti bölmesi > Modüller > Genel muhasebe > Periyodik görevler > Periyodik günlükler**'e gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Tanım** alanına bir değer girin. Açıklama, daha sonra alındığında Periyodik günlüğün adı olacaktır. Bu yüzden ilgili bir ad verdiğinizden emin olun.
6. **Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın. Periyodik günlük genellikle birkaç günlük satırı içerir. bu görev kılavuzu ise yalnızca bir satır ekler.
7. **Tarih** alanına bir tarih girin. **Tarih** alanı, günlük deftere bir sonraki transfer için nakil tarihini içerir. Her ay alınacak günlükler için, deftere nakledileceği tarihi kullanmanız önerilir; bu genel olarak dönemin ilk veya son tarihidir. Tarih alanını boş bırakıp günlük alındığında Boş tarih alanını kullanarak bir tarih vermek de mümkündür. Alan, hareketler alındığında sonraki yinelenen tarih için otomatik olarak güncelleştirilir. 
8. **Hesap** alanında istediğiniz değerleri belirtin.
9. **Açıklama** alanında bir değer seçin.
10. Sayfayı kapatın.
11. **Borç** alanına bir sayı girin.
12. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
13. **Birim** alanında "Aylar"ı seçin.
14. **Birim sayısı** alanına "1" girin.
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
26. **Bitiş tarihi** alanına bir tarih girin. **Bitiş tarihi**, periyodik fiş satırları için kesme tarihi görevi görür. Yineleme ayarına bağlı olarak, sonuç olarak oluşturulan günlüğe Son tarih ve Bitiş tarihi için aynı satır bir kereden fazla eklenebilir. Bitiş tarihi, periyodik satırın günlüğe son kez aktarıldığını oturumun tarihine göre otomatik olarak güncelleştirilir. 
27. **Periyodik günlük numarası** alanına bir değer girin veya buradan bir değer seçin.
28. Listede, seçili satırdaki bağlantıya tıklayın.
29. **Tamam**'a tıklayın. Dönem günlüğü artık gözden geçirilebilir, onaylanabilir veya gereklilik ve ayara bağlı olarak deftere nakledilebilir.   
