--- 
title: "Kaynak belgeler için denetim ilkeleri tanımlama"
description: "Bu prosedür, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını gösterir."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ca4c8735258170c41dc907ed0ef8afca250ea9dd
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Kaynak belgeler için denetim ilkeleri tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını gösterir. Örnekte, otel gideri türünde gider raporları kullanılmaktadır. Bu yordam, USMF demo şirketini kullanır. Denetçi rolü bu görevleri gerçekleştirmek için uygun izinleri içerir.

1. Audit workbench > Setup > Policy rule type (Denetim çalışma ekranı > Ayar > İlke kuralı türü) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Kural adı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Sorgu adı alanında Gider raporu satırı'nı seçin
6. Sorgu türü alanında Topla'yı seçin
7. Tüzel kişilik alanında Tüzel kişilik'i seçin
8. Belge tarihi referansı alanında Değiştirilme tarihi ve saati'ni seçin
9. Kaydet'e tıklayın.
10. Audit workbench > Setup > Audit policies (Denetim çalışma ekranı > Ayar > Denetim ilkeleri) menüsüne gidin.
11. Yeni'ye tıklayın.
12. İsim alanına bir değer yazın.
13. İlke organizasyonları bölümünü genişletin.
14. Ağaçta "Contoso Eğlence Sistemi Türkiye"yi (Contoso Entertainment System USA) seçin.
15. Ekle öğesini tıklatın.
16. Ağaçta "Contoso Danışmanlık Türkiye"yi (Contoso Consulting USA) seçin.
17. Ekle öğesini tıklatın.
18. Ağaçta "Contoso Perakende Türkiye"yi (Contoso Retail USA) seçin.
19. Ekle öğesini tıklatın.
20. İlke organizasyonları bölümünü daraltın.
21. İlke kuralları bölümünü genişletin.
22. Listede, önceden oluşturulmuş İlke Kuralı'nı bulup seçin.
23. İlke kuralı oluştur'a tıklayın.
24. Yürürlük tarihi alanına bir tarih ve saat girin.
25. Filtre'ye tıklayın.
26. Listede, Gider kategorisi için satırı seçin ve Ayrıntılar ayarını Otel yapın
27. Ölçütler alanında bir değer girin veya seçin.
28. Topla sekmesine tıklayın.
29. Ekle öğesini tıklatın.
30. Listeden, Hareket tutarı için bir alan değeri seçin
31. Alan alanında bir değer girin veya seçin.
32. Toplama İşlevi (AggregateFunction) alanında Toplam'ı (Sum) seçin.
33. Gruplama ölçütü sekmesine tıklayın.
34. Ekle öğesini tıklatın.
35. Listeden, Çalışan için bir değer seçin  
36. Ekle öğesini tıklatın.
37. Listeden, Gider kategorisi için bir değer seçin
38. Alan alanında bir değer girin veya seçin.
39. Sahip sekmesine tıklayın.
40. Ekle öğesini tıklatın.
41. Hareket tutarı'nı seçin
42. Alan alanında bir değer girin veya seçin.
43. Toplama İşlevi (AggregateFunction) alanında Toplam'ı (Sum) seçin.
44. Ölçütler alanına '>2000' yazın.
45. Tamam'a tıklayın.
46. Sına'yı tıklatın.
47. Belge seçim başlangıç tarihi alanına tarih ve saat girin.
48. Belge seçim bitiş tarihi alanına tarih ve saat girin.
49. Testi çalıştır'a tıklayın.
50. Eylem Bölmesinde, Denetim ilkesi'ne tıklayın.
51. Ek seçenekler'e tıklayın.
52. Başlangıç tarihi alanına tarih ve saat girin.
53. Bitiş tarihi alanına tarih ve saat girin.
54. Toplu iş'e tıklayın.
55. Arka planda çalıştır bölümünü genişletin.
56. Toplu işleme alanında Evet'i seçin.
57. Tamam'a tıklayın.
58. Audit workbench > Audit cases (Denetim çalışma ekranı > Denetim vakaları) menüsüne gidin.
59. Listede, istenen kaydı bulun ve seçin.
60. Listede, seçili satırdaki bağlantıya tıklayın.
61. İlişkilendirmeler bölümünü genişletin.
62. Listede, istenen kaydı bulun ve seçin.
63. Listede, seçili satırdaki bağlantıya tıklayın.


