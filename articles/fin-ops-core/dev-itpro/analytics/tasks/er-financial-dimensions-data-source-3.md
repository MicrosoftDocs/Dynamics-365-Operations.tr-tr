---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3 - Raporu tasarlama)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29dcf008f342603615241ab75860893cadc2b69e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182451"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a>ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3: Raporu tasarlama)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 2: Model eşleme)" yordamındaki adımları tamamlamanız gerekir.


## <a name="design-a-report-to-present-financial-dimensions"></a>Mali boyutları sunmak üzere bir rapor tasarlama
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.
3. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
4. Yeni alanına, 'Mali boyutlar örnek modeli veri modeline dayalı biçim' yazın.
    * Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.  
5. Ad alanına, 'Genel muhasebe günlüğü raporu' yazın.
6. Veri modeli tanımı alanında Giriş'i seçin.
7. Konfigürasyon oluştur'u tıklatın.
8. Tasarımcı'yı tıklatın.
9. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
10. Ağaçta seçin 'XML\Element'.
11. Ad alanına 'Kök' yazın.
12. Tamam'ı tıklatın.
13. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
14. Ağaçta seçin 'XML\Attribute'.
15. İsim alanına 'Şirket' yazın.
16. Tamam'ı tıklatın.
17. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
18. Ağaçta seçin 'XML\Element'.
19. Ad alanına 'Günlük' yazın.
20. Tamam'ı tıklatın.
21. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.
22. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
23. Ağaçta seçin 'XML\Attribute'.
24. Ad alanına, 'Toplu İş' yazın.
25. Tamam'ı tıklatın.
26. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
27. Ağaçta seçin 'XML\Element'.
28. Ad alanına 'Hareket' yazın.
29. Tamam'ı tıklatın.
30. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.
31. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
32. Ağaçta seçin 'XML\Attribute'.
33. Ad alanına 'Fiş' yazın.
34. Tamam'a tıklayın.
35. Öznitelik Ekle'ye tıklayın.
36. Ad alanına 'Tarih' yazın.
37. Tamam'a tıklayın.
38. Öznitelik Ekle'ye tıklayın.
39. İsim alanına 'Para birimi' yazın.
40. Tamam'a tıklayın.
41. Öznitelik Ekle'ye tıklayın.
42. Ad alanına, 'Borç' yazın.
43. Tamam'a tıklayın.
44. Öznitelik Ekle'ye tıklayın.
45. Ad alanına, 'Alacak' yazın.
46. Tamam'a tıklayın.
47. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
48. Ağaçta seçin 'XML\Element'.
49. Ad alanına, 'Boyutlar' yazın.
50. Tamam'ı tıklatın.
51. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.
52. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
53. Ağaçta seçin 'XML\Attribute'.
54. Ad alanına 'Kod' yazın.
55. Tamam'a tıklayın.
56. Öznitelik Ekle'ye tıklayın.
57. Ad alanına, 'Değer' yazın.
58. Tamam'a tıklayın.
59. Öznitelik Ekle'ye tıklayın.
60. Ad alanına, 'Açıklama' yazın.
61. Tamam'a tıklayın.

## <a name="map-report-elements-to-data-sources"></a>Rapor öğelerini veri kaynakları ile eşleme
1. Eşleme sekmesini tıklatın.
2. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli' öğesini genişletin
3. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini genişletin.
4. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini genişletin.
5. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini genişletin.
6. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Açıklama: XML Özniteliği' öğesini seçin.
7. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kaynak listesi\Açıklama: Dize' öğesini seçin.
8. Bağla'yı tıklatın.
9. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Değer: XML Özniteliği' öğesini seçin.
10. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Kod: Dize' öğesini seçin.
11. Bağla'yı tıklatın.
12. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Kod: XML Özniteliği' öğesini seçin.
13. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Ad: Dize' öğesini seçin.
14. Bağla'yı tıklatın.
15. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini seçin.
16. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.
17. Bağla'yı tıklatın.
18. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Alacak: XML Özniteliği' öğesini seçin.
19. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Alacak: Gerçek' öğesini seçin.
20. Bağla'yı tıklatın.
21. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Borç: XML Özniteliği' öğesini seçin.
22. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Borç: Gerçek' öğesini seçin.
23. Bağla'yı tıklatın.
24. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Para Birimi: XML Özniteliği' öğesini seçin.
25. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Para Birimi: Dize' öğesini seçin.
26. Bağla'yı tıklatın.
27. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Tarih: XML Özniteliği' öğesini seçin.
28. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Tarih: Tarih' öğesini seçin.
29. Bağla'yı tıklatın.
30. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Fiş: XML Özniteliği' öğesini seçin.
31. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Fiş: Dize' öğesini seçin.
32. Bağla'yı tıklatın.
33. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.
34. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini seçin.
35. Bağla'yı tıklatın.
36. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Toplu İş: XML Özniteliği' öğesini seçin.
37. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.
38. Bağla'yı tıklatın.
39. Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.
40. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini seçin.
41. Bağla'yı tıklatın.
42. Ağaçta, 'Kök: XML Öğesi\Şirket: XML Özniteliği' öğesini seçin.
43. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Şirket: Dize' öğesini seçin.
44. Bağla'ya tıklayın.
45. Kaydet'e tıklayın.
46. Sayfayı kapatın.

