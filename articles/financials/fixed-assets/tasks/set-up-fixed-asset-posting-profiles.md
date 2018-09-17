--- 
title: "Sabit kıymet deftere nakil profilleri ayarlama"
description: "Bu görev kılavuzunda Sabit kıymet deftere nakil profilleri ayarlanacak."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Sabit kıymet deftere nakil profilleri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda Sabit kıymet deftere nakil profilleri ayarlanacak.  Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.  Özel hesap planınız ve mali raporlama gereksinimleriniz için deftere nakil profilleri oluşturulması gerekmesine karşın, bu görev kılavuzunda verilen örnekler temel bir deftere nakil profiline aittir.

1. Sabit kıymetler > Kurulum > Sabit kıymet deftere nakil profilleri'ne gidin.
2. Yeni'ye tıklayın.
3. Deftere nakil profili alanına bir değer girin.
4. Açıklama alanına bir değer girin.
    * Sabit kıymetlerle çalışırken kullanacağınız her sabit kıymet hareket türü için bir nakil profili oluşturmanız gerekir.  Bu görev kılavuzu Alım hareket türüyle başlayacak.  
5. Ekle öğesini tıklatın.
6. Defter alanına bir değer girin veya seçin.
    * Gruplandırma alanı, deftere nakil profilini Tablo (her sabit kıymet için ayarlanmış bir hesap) veya Grup (her sabit kıymet grubu için ayarlanmış bir hesap) olarak tanımlamanıza olanak sağlar.  Bu görev kılavuzu için belirtilen Defterdeki tüm sabit kıymetlere uygulanmak üzere değeri "Tümü" olarak bırakacağım.  
7. Ana hesap alanında istediğiniz değerleri belirtin.
    * Alımlar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.    
8. Hareket türü alanında "Alım düzeltmesi"ni seçin.
    * Alım düzeltme hareketleri için, Alım hareketlerinde kullanılan hesapları kullanacağız.  
9. Ekle öğesini tıklatın.
10. Defter alanına bir değer girin veya seçin.
11. Ana hesap alanında istediğiniz değerleri belirtin.
    * Alım düzeltmeleri için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.    
12. Hareket türü alanında "Amortisman"ı seçin.
13. Ekle öğesini tıklatın.
14. Defter alanına bir değer girin veya seçin.
15. Ana hesap alanında istediğiniz değerleri belirtin.
16. Mahsup hesap alanında istediğiniz değerleri belirtin.
17. Hareket türü alanında "Amortisman düzeltmesi"ni seçin.
    * Amortisman düzeltme hareketleri için, Amortisman hareketlerinde kullanılan hesapları kullanacağız.  
18. Ekle öğesini tıklatın.
19. Defter alanına bir değer girin veya seçin.
20. Ana hesap alanında istediğiniz değerleri belirtin.
21. Mahsup hesap alanında istediğiniz değerleri belirtin.
22. Hareket türü alanında "Satış çıkışı"nı seçin.
23. Ekle öğesini tıklatın.
24. Defter alanına bir değer girin veya seçin.
25. Ana hesap alanında istediğiniz değerleri belirtin.
    * Elden çıkarmalar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.  
26. Hareket türü alanında "Hurda çıkışı"nı seçin.
    * Satışla elden çıkarma ve Iskartaya çıkararak elden çıkarma için aynı hesapları kullanacağız.  
27. Ekle öğesini tıklatın.
28. Defter alanına bir değer girin veya seçin.
29. Ana hesap alanında istediğiniz değerleri belirtin.
    * Elden çıkarmalar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.  
30. Elden çıkarma bölümünü genişletin.
    * Hem satış hem de ıskarta için elden çıkarma deftere nakil profilleri ayarlamanız gerekir.  Elden çıkarma satış hareketleriyle başlayalım.  
31. Ekle öğesini tıklatın.
32. Defter alanına bir değer girin veya seçin.
33. Nakledilecek değer alanında "Alım değeri"ni seçin.
    * Alım değeri, tüm yıllar için Alım ve Alım düzeltme değerlerini karşılayacak.  Bu hareket türleri için hesapları ayrı ayrı da tanımlayabilirsiniz.  
    * Elden çıkarma sonuçlarının kar veya zarar olmasına bağlı olarak, elden çıkarma işlemini farklı hesaplar kullanacak şekilde ayarlayabilirsiniz.  Tüm elden çıkarma türlerinde aynı hesapları kullanmak üzere Satış değeri türünü "Tümü" yapacağız.  
34. Ana hesap alanında istediğiniz değerleri belirtin.
35. Mahsup hesap alanında istediğiniz değerleri belirtin.
36. Ekle öğesini tıklatın.
37. Defter alanına bir değer girin veya seçin.
    * Nakledilecek değer alanında "Amortisman (önceki yıllar)"ı seçin.  
38. Ana hesap alanında istediğiniz değerleri belirtin.
39. Mahsup hesap alanında istediğiniz değerleri belirtin.
40. Ekle öğesini tıklatın.
41. Defter alanına bir değer girin veya seçin.
42. Nakledilecek değer alanında "Amortisman (bu yıl)"ı seçin.
43. Ana hesap alanında istediğiniz değerleri belirtin.
44. Mahsup hesap alanında istediğiniz değerleri belirtin.
45. Ekle öğesini tıklatın.
46. Defter alanına bir değer girin veya seçin.
47. Nakledilecek değer alanında "Amortisman düzeltmeleri (önceki yıllar)"ı seçin.
48. Ana hesap alanında istediğiniz değerleri belirtin.
49. Mahsup hesap alanında istediğiniz değerleri belirtin.
50. Ekle öğesini tıklatın.
51. Defter alanına bir değer girin veya seçin.
52. Nakledilecek değer alanında "Amortisman düzeltmeleri (bu yıl)"ı seçin.
53. Ana hesap alanında istediğiniz değerleri belirtin.
54. Mahsup hesap alanında istediğiniz değerleri belirtin.
55. Ekle öğesini tıklatın.
56. Defter alanına bir değer girin veya seçin.
57. Nakledilecek değer alanında "Net defter değeri"ni seçin.
58. Ana hesap alanında istediğiniz değerleri belirtin.
59. Mahsup hesap alanında istediğiniz değerleri belirtin.
60. Satış veya ıskartaya çıkarma alanında "Iskarta"yı seçin.
61. Ekle öğesini tıklatın.
62. Defter alanına bir değer girin veya seçin.
63. Nakledilecek değer alanında "Alım değeri"ni seçin.
64. Ana hesap alanında istediğiniz değerleri belirtin.
65. Mahsup hesap alanında istediğiniz değerleri belirtin.
66. Ekle öğesini tıklatın.
67. Defter alanına bir değer girin veya seçin.
    * Nakledilecek değer alanında "Amortisman (önceki yıllar)"ı seçin.  
68. Ana hesap alanında istediğiniz değerleri belirtin.
69. Mahsup hesap alanında istediğiniz değerleri belirtin.
70. Ekle öğesini tıklatın.
71. Defter alanına bir değer girin veya seçin.
72. Nakledilecek değer alanında "Amortisman (bu yıl)"ı seçin.
73. Ana hesap alanında istediğiniz değerleri belirtin.
74. Mahsup hesap alanında istediğiniz değerleri belirtin.
75. Ekle öğesini tıklatın.
76. Defter alanına bir değer girin veya seçin.
77. Nakledilecek değer alanında "Amortisman düzeltmeleri (önceki yıllar)"ı seçin.
78. Ana hesap alanında istediğiniz değerleri belirtin.
79. Mahsup hesap alanında istediğiniz değerleri belirtin.
80. Ekle öğesini tıklatın.
81. Defter alanına bir değer girin veya seçin.
82. Nakledilecek değer alanında "Amortisman düzeltmeleri (bu yıl)"ı seçin.
83. Ana hesap alanında istediğiniz değerleri belirtin.
84. Mahsup hesap alanında istediğiniz değerleri belirtin.
85. Ekle öğesini tıklatın.
86. Defter alanına bir değer girin veya seçin.
87. Nakledilecek değer alanında "Net defter değeri"ni seçin.
88. Ana hesap alanında istediğiniz değerleri belirtin.
89. Mahsup hesap alanında istediğiniz değerleri belirtin.


