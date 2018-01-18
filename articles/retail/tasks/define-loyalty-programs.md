--- 
title: " Bağlılık programları tanımlama"
description: "Bu yordam, iki bağlılık katmanıyla bir bağlılık programı ayarlamayla ilgili açıklamalar içerir."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 4bc90da445765ab662fe920a3230681959469a90
ms.contentlocale: tr-tr
ms.lasthandoff: 11/14/2017

---
# <a name="define-loyalty-programs"></a> Bağlılık programları tanımlama

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam, iki bağlılık katmanıyla bir bağlılık programı ayarlamayla ilgili açıklamalar içerir. Bu yordam, USRT demo veri şirketini kullanır.

1. Perakende ve ticaret > .. > Bağlılık programları.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Satır ekle'ye tıklayın.
6. Düzey alanına bir sayı girin.
7. Katman alanına bağlılık katmanı için bir ad girin.
8. Tanım alanına bir değer girin.
9. Tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bu tarih aralığı geleceğe dönük olarak genişletilmelidir. Örneğin, gold katmanı için seçili tarih aralığı bir yıl olduğunda, gold katmanına uygun olan tüm müşteriler gold katmanına bir yıl için atanan ödülleri alma hakkına sahip olur. Müşteri gold katmandayken yeniden gold katmana hak kazanırsa, katmanın sona erme tarihi yeniden hak kazanılan tarihten itibaren bir yıl daha uzatılır.  
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Satır ekle'ye tıklayın.
12. Düzey alanına bir sayı girin.
13. Katman alanına bağlılık katmanı için bir ad girin.
14. Tanım alanına bir değer girin.
15. Tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. Kaydet'e tıklayın.
18. Listede, istenen kaydı bulun ve seçin.
    * Katman kuralları, katmana girmeye hak kazanmak için belirli bir süre boyunca kazanılması gereken minimum ödül puanı sayısını belirler.  
19. Katman kuralları bölümünün genişletilmiş görünümüne geçin.
20. Yeni'ye tıklayın.
    * Katman başına birden fazla katman kuralınız olabilir. Örneğin, bir katmanı kazanmak için üç farklı ölçüt belirleyebilirsiniz; bir ay içinde 500 $ harcama, bir yıl süresince 1000 $ harcama ve bir yılda 20 hareket gerçekleştirme. Bunu yapmak için üç katman kuralı oluşturmanız gerekir.  
21. Ödül puanı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bunun kullanılamayan bir bağlılık ödül puanı olması gerekir.  
22. Listede, seçili satırdaki bağlantıya tıklayın.
23. Minimum verilen puan alanına bir sayı girin.
    * En düşük katman seviyesinde, tüm müşteriler programa katılarak katmana hak kazanacaksa '0' değerini girin.  
24. Değerlendirme tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bu tarih aralığını geçmişe dönük olarak genişletilmelidir. Yalnızca bu tarih aralığında kazanılan puanlar verilen minimum puan değerine ulaşmak için geçerli sayılır.  
25. Listede, seçili satırdaki bağlantıya tıklayın.
26. Kaydet'e tıklayın.
27. Listede, istenen kaydı bulun ve seçin.
28. Yeni'yi tıklatın.
29. Ödül puanı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
30. Listede, seçili satırdaki bağlantıya tıklayın.
31. Minimum verilen puan alanına bir sayı girin.
32. Değerlendirme tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bu tarih aralığını geçmişe dönük olarak genişletilmelidir.  
33. Listede, seçili satırdaki bağlantıya tıklayın.
34. Kaydet'e tıklayın.
35. Fiyat grupları'na tıklayın.
    * Bağlı müşterilere indirimler vermek istiyorsanız. bir veya birden fazla fiyat grubun bağlılık programına atamalı ve fiyat gruplarını indirimlere atamalısınız. En iyi uygulama, farklı türdeki iskonto varlıkları üzerinde fiyat gruplarını karıştırmamaktır.  Örneğin, aynı fiyat grubunu bir bağlılık iskontosu ve kanal iskontosu için kullanmayın.  
36. Fiyat grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Sayfanın üst kısmındaki fiyat grupları bağlantısı bağlılık programı içindir. Program katmanları hızlı sekmesindeki Fiyat grupları bağlantısı yalnızca belirli bir bağlılık katmanı için kullanılır.  
37. Listede, seçili satırdaki bağlantıya tıklayın.
38. Kaydet'e tıklayın.
39. Sayfayı kapatın.
40. Kaydet'e tıklayın.


