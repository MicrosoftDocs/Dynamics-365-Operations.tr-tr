--- 
title: "Mali boyutları bir veri kaynağı olarak kullanmak için veri modeli tasarlama"
description: "Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3e55eedba1955ae79733afee1a0b3c7072147bb5
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source"></a>Mali boyutları bir veri kaynağı olarak kullanmak için veri modeli tasarlama 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.


## <a name="create-a-new-data-model"></a>Yeni bir veri modeli oluşturma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * "Litware, Inc." emin olun sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.  
2. Raporlama konfigürasyonları'na tıklayın.
3. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
4. Ad alanına 'Mali boyutlar örnek modeli' yazın.
5. Konfigürasyon oluştur'u tıklatın.
6. Tasarımcı'yı tıklatın.
7. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
8. Ad alanına 'Giriş' yazın.
9. Ekle öğesini tıklatın.
10. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
11. İsim alanına 'Şirket' yazın.
12. Ekle öğesini tıklatın.
    * Modelimize yeni bir kayıt listesi ekleyeceğiz. Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların ayarlarını gösterir. Tüm mali boyutlar bu listede boyutun ayarını temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.  
13. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
14. Ad alanına 'Boyutlar ayarı' yazın.
15. Madde türü alanında 'Kayıt listesi'ni seçin.
16. Ekle öğesini tıklatın.
17. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
18. Ad alanına 'Kod' yazın.
19. Madde türü alanında 'Dize' seçin.
20. Ekle öğesini tıklatın.
21. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
22. İsim alanında 'İsim' yazın.
23. Ekle öğesini tıklatın.
24. Ağaçta, 'Giriş'i seçin.
25. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
26. Ad alanına 'Günlük' yazın.
27. Madde türü alanında 'Kayıt listesi'ni seçin.
28. Ekle öğesini tıklatın.
29. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
30. Ad alanına, 'Toplu İş' yazın.
31. Madde türü alanında 'Dize' seçin.
32. Ekle öğesini tıklatın.
33. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
34. Ad alanına 'Hareket' yazın.
35. Madde türü alanında 'Kayıt listesi'ni seçin.
36. Ekle öğesini tıklatın.
37. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
38. Ad alanına 'Tarih' yazın.
39. Madde türü alanında 'Tarih' seçin.
40. Ekle öğesini tıklatın.
41. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
42. Ad alanına 'Borç' yazın.
43. Madde türü alanında 'Gerçek' seçin.
44. Ekle öğesini tıklatın.
45. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
46. Ad alanına 'Alacak' yazın.
47. Ekle öğesini tıklatın.
48. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
49. İsim alanına 'Para birimi' yazın.
50. Madde türü alanında 'Dize' seçin.
51. Ekle öğesini tıklatın.
52. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
53. Ad alanına 'Fiş' yazın.
54. Ekle öğesini tıklatın.
55. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
56. Ad alanına 'Boyut verileri' yazın.
57. Madde türü alanında 'Kayıt listesi'ni seçin.
58. Ekle öğesini tıklatın.
    * Modelimize yeni bir kayıt listesi ekledik. Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların değerlerini gösterir. Tüm mali boyutlar bu listede boyutun değerlerini temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur. Boyut adı da bu kayıtta gerekirse seçim amacıyla kullanılmak üzere bir alan olarak sunulur.  
59. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
60. Ad alanına 'Kod' yazın.
61. Madde türü alanında 'Dize' seçin.
62. Ekle öğesini tıklatın.
63. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
64. İsim alanına 'Açıklama' yazın.
65. Ekle öğesini tıklatın.
66. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
67. İsim alanında 'İsim' yazın.
68. Ekle öğesini tıklatın.
69. Kaydet'e tıklayın.
70. Sayfayı kapatın.


