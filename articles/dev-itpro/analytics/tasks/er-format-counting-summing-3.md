---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "347089"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a>ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3: Çıktıyı hazırlamak için işlemleri kullanma)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 2: Hesaplamaları yapılandırma)" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Sayım ve toplama bilgisini kullanmak için bu raporu yapılandırma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta, "Intrastat modeli" öğesini genişletin.
4. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.
5. Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.
6. Tasarımcı'yı tıklatın.
7. Eşleme sekmesini tıklatın.
8. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
    * Belleğe alınan blokların listesini almak için yeni bir veri kaynağı ekleyin.  
9. Ağaçta, 'Functions\Calculated field' seçin.
10. Ad alanına "$BlocksList" yazın.
    * $BlocksList  
11. Formülü düzenle'ye tıklayın.
12. Ağaçta, "Veri toplama işlevleri\TOPLANANLİSTE" öğesini seçin.
13. Fonksiyon ekle'ye tıklayın.
14. Veri kaynağı ekle'ye tıklayın.
15. Formül alanına "TOPLANANLİSTE('$BlockName', " yazın.
    * TOPLANANLİSTE ('$BlockName ',  
16. Formül alanına "TOPLANANLİSTE('$BlockName', "*")" yazın.
    * TOPLANANLİSTE('$BlockName', "*")  
17. Kaydet'e tıklayın.
    * "*" modeli, bu kaydın listesine tüm blokların dahil olacağı anlamına gelir.  
18. Sayfayı kapatın.
19. Tamam'a tıklayın.
20. Formül sekmesine tıklayın.
21. Ağaçta, "Intrastat\Veri" öğesini seçin.
22. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
23. Ağaçta, "Metin\Sıra" öğesini seçin.
24. Ad alanına 'Bloklara göre toplamlar' yazın.
    * Bloklara göre toplamlar  
25. Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.
26. Tamam'a tıklayın.
27. Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar" öğesini seçin.
28. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
29. Ağaçta seçin 'Text\String'.
30. Ad alanına "Blok kodu" yazın.
    * Blok kodu  
31. Tamam'a tıklayın.
32. Dize Ekle'ye tıklayın.
33. Ad alanına "Satır sayımı" yazın.
    * Satır sayımı  
34. Tamam'a tıklayın.
35. Dize Ekle'ye tıklayın.
36. Ad alanına "Toplam tutar" yazın.
    * Toplam tutar  
37. Tamam'a tıklayın.
38. Eşleme sekmesini tıklatın.
39. Ağaçta, "$BlocksList" metnini seçin.
40. Bağla'ya tıklayın.
    * Belleğe alınan her blok için bir özet satırı oluşturun.  
41. Formül sekmesine tıklayın.
42. Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Blok kodu" öğesini seçin.
43. Eşleme sekmesini tıklatın.
44. Formülü düzenle'ye tıklayın.
45. Formül alanına ""Blok kodu: " & " metnini girin.
    * "Blok kodu: " &  
46. Ağaçta, "$BlocksList" metnini genişletin.
47. Ağaçta, "$BlocksList\Değer" öğesini seçin.
48. Veri kaynağı ekle'ye tıklayın.
49. Kaydet'e tıklayın.
50. Sayfayı kapatın.
51. Formül sekmesine tıklayın.
52. Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar\Satır sayımı" öğesini seçin.
53. Eşleme sekmesini tıklatın.
54. Formülü düzenle'ye tıklayın.
    * Bu raporda sunulan her bloktaki satır sayıları için çıkış oluşturun.  
55. Formül alanına ""Bu bloktaki satır sayısı: " & " metnini girin.
    * "Bu bloktaki satır sayısı: " &  
56. Formül alanına ""Bu bloktaki satır sayısı: " & TEXT (" metnini girin.
    * "Bu bloktaki satır sayısı: " & TEXT(  
57. Ağaçta, "Veri toplama işlevleri\ÇOKEĞERSAY" öğesini seçin.
58. Fonksiyon ekle'ye tıklayın.
59. Veri kaynağı ekle'ye tıklayın.
60. Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', " yazın.
    * "Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName',  
61. Ağaçta, "$BlocksList" metnini genişletin.
62. Ağaçta, "$BlocksList\Değer" öğesini seçin.
63. Veri kaynağı ekle'ye tıklayın.
64. Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, " yazın.
    * "Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer,  
65. Ağaçta, "$RecName" öğesini seçin.
66. Veri kaynağı ekle'ye tıklayın.
67. Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "*"))" yazın.
    * "Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "*"))  
68. Kaydet'e tıklayın.
69. Sayfayı kapatın.
70. Formül sekmesine tıklayın.
71. Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Toplam tutar" öğesini seçin.
72. Eşleme sekmesini tıklatın.
73. Formülü düzenle'ye tıklayın.
    * Bu raporda sunulan her bloğun faturalanan tutar toplamı olacak çıkışı oluşturun.  
74. Formül alanına ""Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKEĞERSAY('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "*"))" yazın.
    * "Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKETOPLA('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "*"))  
75. Kaydet'e tıklayın.
76. Sayfayı kapatın.
77. Kaydet'e tıklayın.
78. Sayfayı kapatın.

