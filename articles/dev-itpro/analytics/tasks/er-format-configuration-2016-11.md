---
title: ER Biçim yapılandırması oluşturma (Kasım 2016)
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir.
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544783"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Biçim yapılandırması oluşturma (Kasım 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir. Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar. Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.


## <a name="create-a-new-format-configuration"></a>Yeni bir biçim yapılandırması oluşturma
1. **Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.
2. **Raporlama konfigürasyonları**'na tıklayın.
3. Ağaçta, **Ödemeler (Basitleştirilmiş model)**'i seçin.
4. İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.

 > [!NOTE]
 > **Yapılandırma oluştur**'u görmüyorsanız, tasarım modunu **Elektronik raporlama parametreleri** sayfasında etkinleştirmeniz gerekir. 
 
5. **Yeni** alanına, **Biçim veri modeline PaymentModel dayalı** girin.
6. **İsim** alanına, **BACS (UK hayali)** yazın.
7. **Açıklama** alanına, **BACS Satıcı ödeme biçimi (UK hayali)** yazın.
    * Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir. Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır. Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.  
    * Elektronik belgenin belirli bir biçimi tanımlanabilir. Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.  
8. **Veri modeli tanımı** alanına bir değer girin veya seçin.
9. **Konfigürasyon oluştur**'u tıklatın. Yeni bir yapılandırma oluşturuldu. Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.  

## <a name="design-the-format-of-an-electronic-document"></a>Elektronik belgenin biçimini tasarlayın.
1. **Tasarımcı**'yı tıklatın.
2. İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.
3. Ağaçta seçin **Common\File**.
4. **İsim** alanına **Xml** yazın.
5. **Kodlama** alanına **UTF-8** yazın.
6. **Tamam** seçeneğini tıklatın.
7. **Ekle** seçeneğini tıklatın.
8. Ağaçta seçin **XML\Element**.
9. **İsim** alanına **Mesaj** yazın.
10. **Tamam** seçeneğini tıklatın.
11. Ağaçta, **Xml\İleti** öğesini seçin.
12. **Öğe Ekle**'ye tıklayın.
13. **İsim** alanında **ProcessingDate** yazın.
14. **Tamam** seçeneğini tıklatın.
15. **Öğe Ekle**'ye tıklayın.
16. İsim alanına **MessageId** yazın.
17. **Tamam** seçeneğini tıklatın.
18. **Öğe Ekle**'ye tıklayın.
19. **İsim** alanına **Ödemeler** yazın.
20. **Tamam** seçeneğini tıklatın.
21. Ağaçta, **Xml\İleti\Ödemeler** öğesini seçin.
22. **Öğe Ekle**'ye tıklayın.
23. **İsim** alanına **Öğe** yazın.
24. **Tamam** seçeneğini tıklatın.
25. Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.
26. **Ekle** seçeneğini tıklatın.
27. Ağaçta seçin **XML\Attribute**.
28. İsim alanına **Kimlik** yazın.
29. **Tamam** seçeneğini tıklatın.
30. **Ekle** seçeneğini tıklatın.
31. Ağaçta seçin **XML\Element**.
32. İsim alanına bir **Satıcı** yazın.
33. **Tamam** seçeneğini tıklatın.
34. Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.
35. **Öğe Ekle**'ye tıklayın.
36. İsim alanında **İsim** yazın.
37. **Tamam** seçeneğini tıklatın.
38. **Öğe Ekle**'ye tıklayın.
39. **İsim** alanına **Banka** yazın.
40. **Tamam** seçeneğini tıklatın.
41. Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka** öğesini seçin.
42. **Öğe Ekle**'ye tıklayın.
43. **İsim** alanına **RoutingNumber** yazın.
44. **Tamam** seçeneğini tıklatın.
45. **Öğe Ekle**'ye tıklayın.
46. **İsim** alanına **AccountNumber** yazın.
47. **Tamam** seçeneğini tıklatın.
48. Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.
49. **Kopyala**'yı tıklatın.
50. Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.
51. **Yapıştır**'a tıklayın.
52. **İsim** alanına **Ödeyen** yazın.
53. Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.
54. **Öğe Ekle**'ye tıklayın.
55. **İsim** alanına **Para birimi** yazın.
56. **Tamam** seçeneğini tıklatın.
57. **Öğe Ekle**'ye tıklayın.
58. **İsim** alanına **Açıklama** yazın.
59. **Tamam** seçeneğini tıklatın.
60. **Öğe Ekle**'ye tıklayın.
61. İsim alanına **TransDate** yazın.
62. **Tamam** seçeneğini tıklatın.
63. **Öğe Ekle**'ye tıklayın.
64. İsim alanına **Tutar** yazın.
65. **Tamam** seçeneğini tıklatın.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın
1. Ağaçta, **Xml\İleti\ProcessingDate** öğesini seçin.
2. Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.
3. Ağaçta, **Metin\DateTime** öğesini seçin.
4. **Biçim** alanına **gün-ay-yıl** yazın.
5. **Tamam** seçeneğini tıklatın.
6. Ağaçta, **Xml\İleti\Ödemeler\Madde\TransDate** öğesini seçin.
7. **Tarih/Saat Ekle**'ye tıklayın.
8. **Biçim** alanına **gün-ay-yıl** yazın.
9. **DateTime** türü alanında **Tarih** öğesini seçin.
10. **Tamam** seçeneğini tıklatın.
11. Ağaçta, **Xml\İleti\MessageId** öğesini seçin.
12. Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.
13. Ağaçta seçin **Text\String**.
14. **Tamam** seçeneğini tıklatın.
15. Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Ad** öğesini seçin.
16. **Dize Ekle**'ye tıklayın.
17. **Tamam** seçeneğini tıklatın.
18. Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber** öğesini seçin.
19. **Dize Ekle**'ye tıklayın.
20. **Tamam** seçeneğini tıklatın.
21. Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber** öğesini seçin.
22. **Dize Ekle**'ye tıklayın.
23. **Tamam** seçeneğini tıklatın.
24. Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Ad** öğesini seçin.
25. **Dize Ekle**'ye tıklayın.
26. **Tamam** seçeneğini tıklatın.
27. Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber** öğesini seçin.
28. **Dize Ekle**'ye tıklayın.
29. **Tamam** seçeneğini tıklatın.
30. Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber** öğesini seçin.
31. **Dize Ekle**'ye tıklayın.
32. **Tamam** seçeneğini tıklatın.
33. Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi** öğesini seçin.
34. **Dize Ekle**'ye tıklayın.
35. **Tamam** seçeneğini tıklatın.
36. Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama** öğesini seçin.
37. **Dize Ekle**'ye tıklayın.
38. **Tamam** seçeneğini tıklatın.
39. Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar** öğesini seçin.
40. **Dize Ekle**'ye tıklayın.
41. **Tamam** seçeneğini tıklatın.
42. **Kaydet**'e tıklayın.
43. Sayfayı kapatın.

