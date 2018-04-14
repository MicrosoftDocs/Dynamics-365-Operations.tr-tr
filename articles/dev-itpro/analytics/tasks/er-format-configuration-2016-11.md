--- 
title: "Elektronik raporlama (ER) için bir biçim yapılandırması oluşturma"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için bir biçim yapılandırması oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir. Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar. Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.


## <a name="create-a-new-format-configuration"></a>Yeni bir biçim yapılandırması oluşturma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.
4. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
5. Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.
6. İsim alanına, "BACS (UK hayali)" yazın.
    * BACS (UK hayali)  
7. Açıklama alanına, 'BACS Satıcı ödeme biçimi (UK hayali)' yazın.
    * BACS Satıcı ödeme biçimi (UK hayali)  
    * Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir. Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır. Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.  
    * Elektronik belgenin belirli bir biçimi tanımlanabilir. Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.  
8. Veri modeli tanımı alanına bir değer girin veya seçin.
9. Konfigürasyon oluştur'u tıklatın.
    * Yeni bir yapılandırma oluşturuldu. Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.  

## <a name="design-format-of-electronic-document"></a>Elektronik belgenin biçimini tasarlayın.
1. Tasarımcı'yı tıklatın.
2. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
3. Ağaçta seçin 'Common\File'.
4. İsim alanına bir 'Xml' yazın.
    * Xml  
5. Kodlama alanına 'UTF-8' yazın.
    * UTF-8  
6. Tamam'a tıklayın.
7. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
8. Ağaçta seçin 'XML\Element'.
9. İsim alanına 'Mesaj' yazın.
    * İleti  
10. Tamam'a tıklayın.
11. Ağaçta, "Xml\İleti" öğesini seçin.
12. Öğe Ekle'ye tıklayın.
13. İsim alanında 'ProcessingDate' yazın.
    * ProcessingDate  
14. Tamam'a tıklayın.
15. Öğe Ekle'ye tıklayın.
16. İsim alanına 'MessageId' yazın.
    * MessageId  
17. Tamam'a tıklayın.
18. Öğe Ekle'ye tıklayın.
19. İsim alanına 'Ödemeler' yazın.
    * Ödemeler  
20. Tamam'a tıklayın.
21. Ağaçta, "Xml\İleti\Ödemeler" öğesini seçin.
22. Öğe Ekle'ye tıklayın.
23. İsim alanına 'Madde' yazın.
    * Madde  
24. Tamam'a tıklayın.
25. Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.
26. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
27. Ağaçta seçin 'XML\Attribute'.
28. İsim alanına 'Kimlik' yazın.
    * Kod  
29. Tamam'a tıklayın.
30. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
31. Ağaçta seçin 'XML\Element'.
32. İsim alanına bir 'Satıcı' yazın.
    * Satıcı  
33. Tamam'a tıklayın.
34. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı" öğesini seçin.
35. Öğe Ekle'ye tıklayın.
36. İsim alanında 'İsim' yazın.
    * Dosya Adı  
37. Tamam'a tıklayın.
38. Öğe Ekle'ye tıklayın.
39. İsim alanına 'Banka' yazın.
    * Banka  
40. Tamam'a tıklayın.
41. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka" öğesini seçin.
42. Öğe Ekle'ye tıklayın.
43. İsim alanına 'RoutingNumber' yazın.
    * RoutingNumber  
44. Tamam'a tıklayın.
45. Öğe Ekle'ye tıklayın.
46. İsim alanına 'AccountNumber' yazın.
    * AccountNumber  
47. Tamam'a tıklayın.
48. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı" öğesini seçin.
49. Kopyala'yı tıklatın.
50. Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.
51. Yapıştır'a tıklayın.
52. İsim alanına 'Ödeyen' yazın.
    * Ödeyen  
53. Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.
54. Öğe Ekle'ye tıklayın.
55. İsim alanına 'Para birimi' yazın.
    * Para birimi  
56. Tamam'a tıklayın.
57. Öğe Ekle'ye tıklayın.
58. İsim alanına 'Açıklama' yazın.
    * Açıklama  
59. Tamam'a tıklayın.
60. Öğe Ekle'ye tıklayın.
61. İsim alanına 'TransDate' yazın.
    * TransDate  
62. Tamam'a tıklayın.
63. Öğe Ekle'ye tıklayın.
64. İsim alanına 'Tutar' yazın.
    * Tutar  
65. Tamam'a tıklayın.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın
1. Ağaçta, "Xml\İleti\ProcessingDate" öğesini seçin.
2. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
3. Ağaçta, "Metin\DateTime" öğesini seçin.
4. Biçim alanına 'gün-ay-yıl' yazın.
    * gg.AA.yyyy  
5. Tamam'a tıklayın.
6. Ağaçta, "Xml\İleti\Ödemeler\Madde\TransDate" öğesini seçin.
7. Tarih/Saat Ekle'ye tıklayın.
8. Biçim alanına 'gün-ay-yıl' yazın.
    * gg.AA.yyyy  
9. Tarih/Saat türü alanında "Tarih" öğesini seçin.
10. Tamam'a tıklayın.
11. Ağaçta, "Xml\İleti\MessageId" öğesini seçin.
12. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
13. Ağaçta seçin 'Text\String'.
14. Tamam'a tıklayın.
15. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad" öğesini seçin.
16. Dize Ekle'ye tıklayın.
17. Tamam'ı tıklatın.
18. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber" öğesini seçin.
19. Dize Ekle'ye tıklayın.
20. Tamam'ı tıklatın.
21. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber" öğesini seçin.
22. Dize Ekle'ye tıklayın.
23. Tamam'ı tıklatın.
24. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Ad" öğesini seçin.
25. Dize Ekle'ye tıklayın.
26. Tamam'ı tıklatın.
27. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber" öğesini seçin.
28. Dize Ekle'ye tıklayın.
29. Tamam'ı tıklatın.
30. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber" öğesini seçin.
31. Dize Ekle'ye tıklayın.
32. Tamam'ı tıklatın.
33. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi" öğesini seçin.
34. Dize Ekle'ye tıklayın.
35. Tamam'ı tıklatın.
36. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama" öğesini seçin.
37. Dize Ekle'ye tıklayın.
38. Tamam'ı tıklatın.
39. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar" öğesini seçin.
40. Dize Ekle'ye tıklayın.
41. Tamam'ı tıklatın.
42. Kaydet'e tıklayın.
43. Sayfayı kapatın.


