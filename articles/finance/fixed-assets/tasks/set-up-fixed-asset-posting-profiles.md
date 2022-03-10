---
title: Sabit kıymet deftere nakil profilleri ayarlama
description: Bu yordamda, sabit kıymet deftere nakil profillerinin nasıl ayarlanacağı gösterilmiştir.
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0006c9588a22d720687e7aceb49acc756b83e1
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883780"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Sabit kıymet deftere nakil profilleri ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordamda, sabit kıymet deftere nakil profillerinin nasıl ayarlanacağı gösterilmiştir. Özel hesap planınız ve mali raporlama gereksinimleriniz için deftere nakil profilleri oluşturulması gerekmesine karşın, bu konuda verilen örnekler temel bir deftere nakil profiline aittir.

1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Kurulum > Sabit kıymet deftere nakil profilleri**'ne gidin.
2. **Yeni**'ye tıklayın.
3. **Deftere nakil profili** alanına bir değer girin.
4. **Tanım** alanına bir değer girin. Sabit kıymetlerle çalışırken kullanacağınız her sabit kıymet hareket türü için bir nakil profili oluşturmanız gerekir. Bu görev kılavuzu Alım hareket türüyle başlayacak.  
5. Araç çubuğunda **Ekle**'yi tıklatın.
6. **Defter** alanına bir değer girin veya seçin. **Gruplandırma** alanı, deftere nakil profilini Tablo (her sabit kıymet için ayarlanmış bir hesap) veya Grup (her sabit kıymet grubu için ayarlanmış bir hesap) olarak tanımlamanıza olanak sağlar. Bu görev kılavuzu için belirtilen Defterdeki tüm sabit kıymetlere uygulanmak üzere değeri "Tümü" olarak bırakın.  
7. **Ana hesap** alanında istediğiniz değerleri belirtin. Alımlar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.    
8. **Genel muhasebe hesapları** hızlı sekmesinin altındaki açılan menüde 'Alım düzeltmesi'ni seçin. Alım düzeltme hareketleri için, Alım hareketlerinde kullanılan hesapları kullanacağız.  
9. **Ekle** öğesine tıklayın.
10. **Defter** alanına bir değer girin veya seçin.
11. **Ana hesap** alanında istediğiniz değerleri belirtin. Alım düzeltmeleri için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.    
12. **Genel muhasebe hesapları** hızlı sekmesinin altındaki açılan menüde 'Amortisman'ı seçin.
13. **Ekle** öğesine tıklayın.
14. **Defter** alanına bir değer girin veya seçin.
15. **Ana hesap** alanında istediğiniz değerleri belirtin.
16. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
17. **Genel muhasebe hesapları** hızlı sekmesinin altındaki açılan menüde 'Amortisman düzeltmesi'ni seçin. Amortisman düzeltme hareketleri için, Amortisman hareketlerinde kullanılan hesapları kullanacağız.  
18. **Ekle** öğesine tıklayın.
19. **Defter** alanına bir değer girin veya seçin.
20. **Ana hesap** alanında istediğiniz değerleri belirtin.
21. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
22. **Genel muhasebe hesapları** hızlı sekmesinin altındaki açılan menüde 'Satış çıkışı'nı seçin.
23. **Ekle** öğesine tıklayın.
24. **Defter** alanına bir değer girin veya seçin.
25. **Ana hesap** alanında istediğiniz değerleri belirtin. Elden çıkarmalar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.  
26. **Genel muhasebe hesapları** hızlı sekmesinin altındaki açılan menüde 'Hurda çıkışı'nı seçin. "Satış çıkışı" ve "Hurda çıkışı" için aynı hesapları kullanın.  
27. **Ekle** öğesine tıklayın.
28. **Defter** alanına bir değer girin veya seçin.
29. **Ana hesap** alanında istediğiniz değerleri belirtin. Elden çıkarmalar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.  
30. **Çıkış** hızlı sekmesini genişletin. Hem satış hem de ıskarta için elden çıkarma deftere nakil profilleri ayarlamanız gerekir.  Elden çıkarma satış hareketleriyle başlayalım.  
31. **Ekle** öğesine tıklayın.
32. **Defter** alanına bir değer girin veya seçin.
33. **Nakledilecek değer** alanında "Alım değeri"ni seçin.
    * Alım değeri, tüm yıllar için Alım ve Alım düzeltme değerlerini karşılayacak. Bu hareket türleri için hesapları ayrı ayrı da tanımlayabilirsiniz.  
    * Elden çıkarma sonuçlarının kar veya zarar olmasına bağlı olarak, elden çıkarma işlemini farklı hesaplar kullanacak şekilde ayarlayabilirsiniz. Tüm elden çıkarma türlerinde aynı hesapları kullanmak üzere Satış değeri türünü "Tümü" yapacağız.  
34. **Ana hesap** alanında istediğiniz değerleri belirtin.
35. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
36. **Ekle** öğesine tıklayın.
37. **Defter** alanına bir değer girin veya seçin.
38. **Nakledilecek değer** alanında "Amortisman (önceki yıllar)"ı seçin.  
38. **Ana hesap** alanında istediğiniz değerleri belirtin.
39. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
40. **Ekle** öğesine tıklayın.
41. **Defter** alanına bir değer girin veya seçin.
42. **Nakledilecek değer** alanında "Amortisman (bu yıl)"ı seçin.
43. **Ana hesap** alanında istediğiniz değerleri belirtin.
44. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
45. **Ekle** öğesine tıklayın.
46. **Defter** alanına bir değer girin veya seçin.
47. **Nakledilecek değer** alanında "Amortisman düzeltmeleri (önceki yıllar)"ı seçin.
48. **Ana hesap** alanında istediğiniz değerleri belirtin.
49. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
50. **Ekle** öğesine tıklayın.
51. **Defter** alanına bir değer girin veya seçin.
52. **Nakledilecek değer** alanında "Amortisman düzeltmeleri (bu yıl)"ı seçin.
53. **Ana hesap** alanında istediğiniz değerleri belirtin.
54. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
55. **Ekle** öğesine tıklayın.
56. **Defter** alanına bir değer girin veya seçin.
57. **Nakledilecek değer** alanında "Net defter değeri"ni seçin.
58. **Ana hesap** alanında istediğiniz değerleri belirtin.
59. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
60. **Satış veya ıskartaya çıkarma** alanında "Iskarta"yı seçin.
61. **Ekle** öğesine tıklayın.
62. **Defter** alanına bir değer girin veya seçin.
63. **Nakledilecek değer** alanında "Alım değeri"ni seçin.
64. **Ana hesap** alanında istediğiniz değerleri belirtin.
65. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
66. **Ekle** öğesine tıklayın.
67. **Defter** alanına bir değer girin veya seçin.
67. **Nakledilecek değer** alanında "Amortisman (önceki yıllar)"ı seçin.  
68. **Ana hesap** alanında istediğiniz değerleri belirtin.
69. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
70. **Ekle** öğesine tıklayın.
71. **Defter** alanına bir değer girin veya seçin.
72. **Nakledilecek değer** alanında "Amortisman (bu yıl)"ı seçin.
73. **Ana hesap** alanında istediğiniz değerleri belirtin.
74. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
75. **Ekle** öğesine tıklayın.
76. **Defter** alanına bir değer girin veya seçin.
77. **Nakledilecek değer** alanında "Amortisman düzeltmeleri (önceki yıllar)"ı seçin.
78. **Ana hesap** alanında istediğiniz değerleri belirtin.
79. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
80. **Ekle** öğesine tıklayın.
81. **Defter** alanına bir değer girin veya seçin.
82. **Nakledilecek değer** alanında "Amortisman düzeltmeleri (bu yıl)"ı seçin.
83. **Ana hesap** alanında istediğiniz değerleri belirtin.
84. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
85. **Ekle** öğesine tıklayın.
86. **Defter** alanına bir değer girin veya seçin.
87. **Nakledilecek değer** alanında "Net defter değeri"ni seçin.
88. **Ana hesap** alanında istediğiniz değerleri belirtin.
89. **Mahsup hesap** alanında istediğiniz değerleri belirtin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
