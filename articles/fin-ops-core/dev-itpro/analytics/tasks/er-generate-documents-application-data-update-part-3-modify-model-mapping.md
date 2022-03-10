---
title: Uygulama verileri içeren belgeler oluşturmak için modelleri ve eşlemeleri değiştirme
description: Bu konuda, elektronik belge oluşturmak ve uygulama verilerini güncelleştirmek için raporlama yapılandırmalarının nasıl tasarlanacağı açıklanmaktadır. (2. Bölüm - Belge oluşturma).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d7df46bab244d11509b86a27eeed3c2725400b5eb4d0fbf50af1750e7de45d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745900"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Uygulama verileri içeren belgeler oluşturmak için modelleri ve eşlemeleri değiştirme

[!include [banner](../../includes/banner.md)]

Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 2 - Belgeler oluştur)" yordamını tamamlamalısınız. 

Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak ve uygulama verisini güncelleştirmek için nasıl kullanılacağını açıklar. Bu yordamda, ER yapılandırmalarını elektronik belgeler oluşturmakta kullanmaya başlamak ve aynı zamanda uygulama verisini güncelleştirmek için de değiştirirsiniz. Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir.


## <a name="modify-data-model"></a>Veri modelini değiştir
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Intrastat (model)' öğesini seçin.
    * Veri modelini nasıl kullandığınızı genişleteceksiniz. Intrastat raporunu oluşturmak için veri kaynağı olarak kullanmanın yanı sıra, veri modeli, Intrastat raporlama işleminin ayrıntılarını toplamak için kullanılacaktır. Ayrıntılar daha sonra uygulama verisini güncelleştirmek için kullanılacaktır.   
3. Tasarımcı'yı tıklatın.
4. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
5. Yeni düğüm biçimi alanına "Model kökü" girin.
6. İsim alanında 'Uygulama veri güncelleştirmesi için' yazın.
    * Uygulama için veri güncelleştirmesi  
7. Ekle öğesini tıklatın.
8. Ağaçta, 'Uygulama veri güncelleştirmesi için' seçin.
    * Bu yeni kök öğesi (veri kaynağı olarak kullanılan) Intrastat raporundan uygulama tablolalarına (güncelleştirme hedefi) hareket eden veri akışını belirtmek için kullanılır. Farklı kök öğelerinin, giden belgeye nakledilen veriyi almak ve uygulama verisini güncelleştirmek için belgeden veriyi almak için kullanılması gerektiğini unutmayın.   
9. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
10. Ad alanına 'Arşiv başlığı' yazın.
    * Arşiv başlığı  
11. Madde türü alanında 'Kayıt listesi'ni seçin.
12. Ekle öğesini tıklatın.
    * Oluşturulan her bir Intrastat raporu için bir kayıt oluşturacağınız için, önce bunun için bir madde oluşturmalısınız.  
13. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
14. Ad alanına "Dosya adı" yazın.
    * Dosya adı  
15. Madde türü alanında 'Dize' seçin.
16. Ekle öğesini tıklatın.
17. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
18. İsim alanına 'Satır sayısı' yazın.
    * Satır sayısı  
19. Madde türü alanında 'Tamsayı' seçin.
20. Ekle öğesini tıklatın.
    * Geçerli raporlama işlemi sırasında raporlanan Intrastat hareketlerinin sayısını temsil etmek için bu öğeyi ekleyin.  
21. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
22. Ad alanına 'Arşiv satırları' yazın.
    * Arşiv satırları  
23. Madde türü alanında 'Kayıt listesi'ni seçin.
24. Ekle öğesini tıklatın.
    * Geçerli raporlama işlemi sırasında raporlanan Intrastat hareketlerinin listesini temsil etmek için bu öğeyi ekleyin.  
25. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
26. İsim alanına 'Tutar' yazın.
    * Tutar  
27. Madde türü alanında 'Gerçek' seçin.
28. Ekle öğesini tıklatın.
29. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
30. İsim alanına 'Emtia rec id' yazın.
    * Emtia rec id  
31. Madde türü alanında 'Int64' seçin.
32. Ekle öğesini tıklatın.
33. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
34. İsim alanına 'Madde numarası' yazın.
    * Madde kodu  
35. Madde türü alanında 'Dize' seçin.
36. Ekle öğesini tıklatın.
37. Kaydet'e tıklayın.
38. Sayfayı kapatın.

## <a name="modify-model-mapping"></a>Model eşlemeyi değiştir
1. Ağaçta, 'Intrastat (model)' öğesini genişletin.
2. Ağaçta, 'Intrastat (model)\Intrastat (eşleme)' öğesini seçin.
    * Mevcut model eşlemesini uygulama veri güncelleştirmesine başlamak ve Intrastat raporlama ayrıntılarını arşivlemek için kullanın.  
3. Tasarımcı'yı tıklatın.
4. Yeni'ye tıklayın.
5. Ad alanına 'Arşivi güncelleştir' yazın.
    * Arşivi güncelleştirme  
6. Yön alanında 'Hedefe'yi seçin.
7. Kaydet'e tıklayın.
    * Bu yeni eşleme, veri modelinden uygulama tablolarına (güncelleştirme hedefi) hareket eden veri (Intrastat raporlama ayrıntıları) için veri akışını belirtir. Farklı modellerin kök öğelerinin, raporlama işlemi için uygulamadan veri almak için kullanılması gerektiğini unutmayın ve daha sonra veri modelinden gelen veriyi uygulama veri güncelleştirmesi için kullanın.   
8. Tasarımcı'yı tıklatın.
9. Ağaçta, 'Veri modeli\Veri modeli' seçeneğini işaretleyin.
    * Gerekli veri kaynağını ekle. Bu, raporlanan ve arşivlenmesi gereken Intrastat hareketlerinin ayrıntılarını içeren veri modelidir.  
10. Kök ekle'ye tıklayın.
11. Ad alanında 'model' yazın.
    * model  
12. Tanım alanında, 'Uygulama veri güncelleştirmesi' değerini girin veya seçin.
    * Uygulama için veri güncelleştirmesi  
13. Tamam'a tıklayın.
14. Ağaçta, 'model'i genişletin.
15. Ağaçta, 'Functions\Calculated field' seçin.
16. Ağaçta 'model\Arşiv başlığı'nı seçin.
17. Ekle öğesini tıklatın.
    * Arşivleme için raporlanan Intrastat hareketlerini numaralandırmak istediğiniz için uygun veri kaynağının eklenmesi gerekir.  
18. İsim alanına 'Numaralandırılan satırlar' yazın.
    * Numaralandırılmış satırlar  
19. Formülü düzenle'ye tıklayın.
20. Ağaçta 'Liste\ENUMARATE'i seçin.
21. Fonksiyon ekle'ye tıklayın.
22. Ağaçta, 'model'i genişletin.
23. Ağaçta 'model\Arşiv başlığı'nı genişletin.
24. Ağaçta 'model\Arşiv başlığı\Arşiv satırları'nı seçin.
25. Veri kaynağı ekle'ye tıklayın.
26. Formül alnında, 'ENUMERATE(model.'Arşiv başlığı'.'Arşiv satırları')' girin.
    * ENUMERATE(model.'Arşiv başlığı'.'Arşiv satırları')  
27. Kaydet'e tıklayın.
28. Sayfayı kapatın.
29. Tamam'a tıklayın.
30. Hedef ekle'yi tıklatın.
    * Uygulama tablolarını, raporlanan Intrastat hareketlerinin ayrıntılarını arşivlemek için gerek duyulan hedefler olarak ekle.  
31. Ad alanında, 'Arşiv' yazın.
    * Arşivle  
32. Tablo adı alanında, 'IntrastatArchiveGeneral' yazın.
    * IntrastatArchiveGeneral  
    * Kayıt eylemini 'Ekle' olarak tutun, böylece her bir Intrastat raporlama işlemi sırasında kayıtlar ekleyebilirsiniz.  
33. infolog kaydet alanında Evet'i seçin.
    * Uygulama eri güncelleştirmesi sorunları hakkında bilgi almak için Evet'i seçin.  
34. Kaydı atlama eylemi doğrulama alanında Evet'i seçin.
    * Boş 'Intrastat arşiv kodu' alanı hakkında doğrulama hatalarını kaldırmak için Evet'i seçin. Bu, kayıtlar eklendikten sonra yapılacaktır, Dış ticaret parametreler formunda bu tablo için yapılandırılmış sıra numarası ayarlarına dayalı olarak.  
35. Tamam'a tıklayın.
    * Eklenen veri kaynağının (seçilen kök öğesine dayalı filtrelenen model) öğelerini, eklenen hedeften öğelerle bağlayın.  
36. Ağaçta, 'Arşiv' metnini genişletin.
37. Ağaçta 'Arşiv\<İlişkiler'i genişletin.
38. Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail'ı genişletin.
39. Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Amount(AmountMST)'yi seçin.
40. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar'ı genişletin.
41. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer'i genişletin.
42. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Tutar'ı genişletin.
43. Bağla'ya tıklayın.
44. Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Commodity(IntrastatCommodity)' seçeneğini işaretleyin.
45. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Emtia rec id'i genişletin.
46. Bağla'ya tıklayın.
47. Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Madde numarası(ItemId)'i seçin.
48. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Madde numarası'nı genişletin.
49. Bağla'ya tıklayın.
50. Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Satır numarası(LineNumber)'ı seçin.
51. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Numara'yı genişletin.
52. Bağla'ya tıklayın.
53. Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail'ı seçin.
54. Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar'ı seçin.
55. Bağla'ya tıklayın.
56. Ağaçta 'Arşiv\Dosya adı(FileName)'i seçin.
57. Ağaçta 'model\Arşiv başlığı\Dosya adı'nı seçin.
58. Bağla'ya tıklayın.
59. Ağaçta 'Arşiv\Satır sayısı(NumberOfLines)'ı seçin.
60. Ağaçta 'model\Arşiv başlığı\Satır sayısı'nı seçin.
61. Bağla'ya tıklayın.
62. Ağaçta, 'Arşiv'i seçin.
63. Ağaçta 'model\Arşiv başlığı'nı seçin.
64. Bağla'ya tıklayın.
65. Kaydet'e tıklayın.
66. Sayfayı kapatın.
67. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]