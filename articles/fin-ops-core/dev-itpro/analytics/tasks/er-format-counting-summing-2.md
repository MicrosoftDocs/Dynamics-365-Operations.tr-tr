---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 2 - İşlemleri yapılandırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9f804990fab2dcc99eeac8165fe15d1f970d9091
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184980"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a>ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 2: İşlemleri yapılandırma)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 1): Biçim oluşturma" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Sayım ve toplama ayrıntıları eklemek için bir biçim yapılandırması oluşturma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta, "Intrastat modeli" öğesini genişletin.
4. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.
    * Microsoft tarafından sağlanan biçimi, Intrastat raporunun sonunda özet ayrıntıları olan satırlar ekleyerek özelleştirmeniz gerektiğini varsayalım. Değişiklikler yapabilmek için bunu kendi Intrastat yapılandırmanızı Microsoft örneğinden türeterek yapmanız gerekir.  
5. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
6. Yeni alanında "İsimden Türet: Intrastat (DE), Microsoft" girin.
7. Ad alanında "Sayım ve toplama ile Intrastat (DE)" yazın.
8. Konfigürasyon oluştur'u tıklatın.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Çıkış ayrıntılarına göre sayım ve toplama yapmak için bu raporu yapılandırma
1. Tasarımcı'yı tıklatın.
2. Çıkış ayrıntılarını topla alanında Evet'i seçin.
    * Bu bayrak, Intrastat dosyası oluşturmak için çıktı ayrıntılarını toplama işlemini çalışma zamanında etkinleştirir.  
    * Farklı Intrastat yönleri için sayım yapmanız gerekir. Bu nedenle, bu biçim yapılandırmasının veri kaynakları listesine özel model numaralandırması ekleyin.  
3. Eşleme sekmesini tıklatın.
4. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
5. Ağaçta, "Veri modeli\Numaralandırma" seçeneğini işaretleyin.
6. Ad alanına "Yön" yazın.
7. Model numaralandırma alanına bir değer girin veya seçin.
    * Değer olarak Yön'ü seçin.  
8. Tamam'a tıklayın.
9. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
10. Ağaçta, 'Functions\Calculated field' seçin.
11. Ad alanına, '$BlockName' yazın.
12. Formülü düzenle'ye tıklayın.
13. Formül alanına "blok" yazın.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.
16. Tamam'a tıklayın.
17. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
18. Ağaçta, 'Functions\Calculated field' seçin.
19. Ad alanına "$RecName" yazın.
20. Formülü düzenle'ye tıklayın.
21. Formül alanına "kayıt" yazın.
22. Kaydet'e tıklayın.
23. Sayfayı kapatın.
24. Tamam'a tıklayın.
25. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
26. Ağaçta, 'Functions\Calculated field' seçin.
27. Ad alanına "$InvName" yazın.
28. Formülü düzenle'ye tıklayın.
29. Formül alanına "InvoicedAmountEUR" yazın.
30. Kaydet'e tıklayın.
31. Sayfayı kapatın.
32. Tamam'a tıklayın.
33. Ağaçta, "Intrastat\Veri" öğesini seçin.
34. "Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın
35. Veri kaynağı ekle'ye tıklayın.
    * $BlockName  
36. Kaydet'e tıklayın.
37. Sayfayı kapatın.
38. Toplanan veri anahtarı değeri alanı için Düzenle düğmesine tıklayın.
39. Formül alanına, "EĞER(Intrastat.CommodityRecord.Direction=Direction.Import, "İthalat", "İhracat")' yazın.
    * EĞER(Intrastat.CommodityRecord.Direction=Direction.Import, "İthalat", "İhracat")  
40. Kaydet'e tıklayın.
41. Sayfayı kapatın.
    * Bu dizinin satırlarını sayın. Sonuçlar, farklı yönler için ayrı ayrı "blok" adıyla kullanılır. Her varış Intrastat hareketi için "İthalat" değeri kullanılır. Her sevk Intrastat hareketi için "İhracat" değeri kullanılır. Bunu sanal bir Excel elektronik tablosu olarak düşünün. Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur.  
42. Ağaçta "Intrastat\Veri:Sıra" öğesini genişletin.
43. Ağaçta, "Intrastat\Veri:Sıra\Gelen?" öğesini seçin.
44. "Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.
    * Bu dizinin satırlarını sayın. Sonuçlar "kayıt" adı kullanılarak belleğe alınır.  
45. Ağaçta, "$RecName" öğesini seçin.
46. Veri kaynağı ekle'ye tıklayın.
47. Kaydet'e tıklayın.
48. Sayfayı kapatın.
49. "Toplanan veri anahtarı değeri" alanı için Düzenle düğmesine tıklayın
50. Formül alanına, 'Intrastat.CommodityRecord.CommodityCode' yazın.
51. Kaydet'e tıklayın.
52. Sayfayı kapatın.
    * Bu dizinin satırlarını sayın. Sonuçlar, farklı emtia kodları için ayrı ayrı "kayıt" adıyla kullanılır. Bunu sanal bir Excel elektronik tablosu olarak düşünün. Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur ve ikinci "kayıt" bloğu emtia kodu değeri ile doldurulur.  
53. Ağaçta, "Intrastat\Veri:Sıra\Sevkler?" öğesini seçin.
54. "Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın
55. Ağaçta, "$RecName" öğesini seçin.
56. Veri kaynağı ekle'ye tıklayın.
57. Kaydet'e tıklayın.
58. Sayfayı kapatın.
59. "Toplanan veri anahtarı değeri" alanı için Düzenle düğmesine tıklayın.
60. Formül alanına, 'Intrastat.CommodityRecord.CommodityCode' yazın.
61. Kaydet'e tıklayın.
62. Sayfayı kapatın.
63. Ağaçta, "Intrastat\Veri:Sıra\Sevkler:Sıra?" öğesini genişletin.
64. Ağaçta "Intrastat\Veri:Sıra\Sevkler:Sıra?\Kayıt =  Intrastat.CommodityRecord" öğesini genişletin.
65. Formül sekmesine tıklayın.
66. Ağaçta, "Intrastat\Veri\Sevkler\Kayıt\Fatura tutarı EUR" öğesini seçin.
67. Eşleme sekmesini tıklatın.
68. "Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.
69. Ağaçta, "$InvName" öğesini seçin.
70. Veri kaynağı ekle'ye tıklayın.
71. Kaydet'e tıklayın.
72. Sayfayı kapatın.
    * Bu dizinin satırları için faturalanan tutar değerlerini özetleyin. Sonuçlar, farklı Intrastat yönleri ve emtia kodları için ayrı ayrı "InvoicedAmountEUR" adıyla kullanılır. Bunu, Excel elektronik tablosunda sanal bir oluşturma olarak düşünün. Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur. İkinci "kayıt" bloğu emtia kodu değeri ile doldurulur ve üçüncü "InvoicedAmountEUR" bloğu fatura tutarı değeri ile doldurulur.  
73. Ağaçta "Intrastat\Veri\Gelen?" öğesini genişletin.
74. Ağaçta, "Intrastat\Veri\Gelen?\Kayıt =  Intrastat.CommodityRecord" öğesini genişletin.
75. Formül sekmesine tıklayın.
76. Ağaçta, "Intrastat\Veri\Gelen\Kayıt\Fatura tutarı EUR" öğesini seçin.
77. Eşleme sekmesini tıklatın.
78. "Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.
79. Ağaçta, "$InvName" öğesini seçin.
80. Veri kaynağı ekle'ye tıklayın.
81. Kaydet'e tıklayın.
82. Sayfayı kapatın.
83. Kaydet'e tıklayın.
84. Sayfayı kapatın.

