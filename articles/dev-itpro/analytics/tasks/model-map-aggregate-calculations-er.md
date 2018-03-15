--- 
title: "Veritabanı düzeyinde toplam hesaplamalar için bir model eşleme yapılandırması kullanma (ER)"
description: "Bu yordam yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlama ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanma hakkında bilgiler sağlar."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 3c3558d9e25dcfd56f3306e69884528d01324cbd
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a>Veritabanı düzeyinde toplam hesaplamalar için bir model eşleme yapılandırması kullanma (ER) 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlama ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanma hakkında bilgiler sağlar. Bu yordamda, Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. 

Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.

 Bu adımları tamamlamak için ilk olarak “ER, toplam hesaplamaları veritabanı düzeyinde gerçekleştirerek bunların verimliliğini artırır (Bölüm 1: Yapılandırmaları hazırlama)” yordamındaki adımları tamamlamanız gerekir.

1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, "Intrastat modeli" öğesini genişletin.
3. Ağaçta, 'Intrastat modeli\Intrastat örnek eşlemesi''ni seçin.
4. Tasarımcı'yı tıklatın.
5. Tasarımcı'yı tıklatın.
6. Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' seçin.
7. Kök ekle'ye tıklayın.
    * Gruplamak istediğiniz kayıtları temsil eden yeni bir veri kaynağı ekleyin.  
8. İsim alanına, 'Hareketler' yazın.
    * Hareketler  
9. Tablo alanına 'Intrastat' yazın.
    * Intrastat  
10. Tamam'a tıklayın.
11. Ağaçta 'İşleveler\Grupla'yı seçin.
    * Bu veri kaynağı türü çalışma zamanında kayıtları gruplandırmak ve istenen toplamları hesaplamak için yeni bir veri kaynağı sağlamak için kullanılır.  
12. Kök ekle'ye tıklayın.
13. Ad alanına 'TransactionsGroups' yazın.
    * TransactionsGroups  
14. Grubu buna göre düzenle'ye tıklatın.
15. Ağaçta, 'Hareketler'i seçin.
    * Gruplandırmak istediğiniz kayıtları temsil eden 'Kayıt listesi' türündeki eklenen veri kaynağını seçin.  
16. Alanı buna ekle'yi tıklatın.
17. Neler gruplanacak'ı tıklayın.
18. Ağaçta, 'Hareketler'i genişletin.
19. Ağaçta, 'Hareketler\Yön''ü seçin.
20. Alanı buna ekle'yi tıklatın.
21. Gruplandırılmış alanlar'ı tıklatın.
    * Gruplandırma düzeyi belirtmek için alanı seçin. Bu seçimi temel alınarak, veri kaynağı çalışma zamanında Instrastat tablosunda karşılanacak yön kodlarında ne kadar hareket grubu varsa bunları döndürecektir.  
22. Ağaçta, 'Hareketler\Fatura tutarı(AmountMST)' öğesini seçin.
    * Toplam hesaplama için kaynağı belirtmek üzere alanı seçin.  
23. Alanı buna ekle'yi tıklatın.
24. Toplam alanları'nı tıklatın.
25. Listede, seçili satırı işaretleyin.
26. Yöntem alanında 'Toplam' öğesini seçin.
    * Toplam türünü seçin.  
27. Ad alanına 'SumOfAmountMST' yazın.
    * Yapılandırılan veri kaynağında bu toplamın adını belirtin.  
28. Kaydet'e tıklayın.
    * 'Yürütme konumu' alanının bu gruplandırmanın çalışma zamanında SQL veritabanında gerçekleştirileceğini belirttiğini unutmayın.  
29. Sayfayı kapatın.
30. Tamam'a tıklayın.
31. Ağaçta 'Toplamlar' öğesini genişletin.
32. Ağaçta 'TransactionsGroups' öğesini genişletin.
33. Ağaçta, 'TransactionsGroups\toplanan' öğesini seçin.
34. Ağaçta, 'TransactionsGroups\toplanan\SumOfAmountMST' öğesini seçin.
35. Ağaçta 'Toplamlar\Toplam fatura değeri(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')' öğesini seçin.
36. Bağla'ya tıklayın.
    * Bu ayarı temel alarak, bu veri kaynağı her hareket grubu için ‘AmountMST’ alanındaki değerlerin toplamını hesaplayacaktır. Bu toplam hesaplaması TransactionsGroups.aggregated.TotalAmount öğesi olarak kullanılabilecektir.  
37. Ağaçta 'TransactionsGroups' öğesini genişletin.
38. Ağaçta 'TransactionsGroups' öğesini seçin.
39. Düzenle öğesine tıklayın.
40. Grubu buna göre düzenle'ye tıklatın.
41. Ağaçta, 'Hareketler'i genişletin.
42. Ağaçta, 'Hareketler\Fatura tutarı(AmountMST)' öğesini seçin.
43. Alanı buna ekle'yi tıklatın.
44. Toplam alanları'nı tıklatın.
45. Listede, seçili satırı işaretleyin.
46. Yöntem alanında 'Maks' öğesini seçin.
47. Ad alanına 'MaxOfAmountMST' yazın.
48. Kaydet'e tıklayın.
    * Şu anda, GROUPBY veri kaynaklarını yürütme işlemi bazı kısıtlamalarla SQL veritabanı düzeyine çevrilebilir. Çeviri ‘Kayıt listesi’ türündeki veri kaynakları veya FİLTRE işlevi kullanılarak bir ifade olarak temsil edilen veri kaynakları için yapılabilir. Ayrıca, tek bir gruplandırma kayıtları alanı için yalnızca bir toplam yapılandırıldığında da yapılabilir.  
    * AmountMST alanı için birden fazla toplam yapılandırılmış olsa bile ‘Yürütme konumu’ alanı bu gruplamanın çalışma zamanında SQL veri tabanında gerçekleştirileceğini belirtmeye devam eder. Bunun nedeni, veri modeli öğesine yalnızca bir toplamın bağlanmış olması ve bunun çalışma zamanında bu veri kaynağından verileri çekmek için kullanılacak olmasıdır.  
49. Sayfayı kapatın.
50. Tamam'a tıklayın.
51. Ağaçta 'TransactionsGroups' öğesini genişletin.
52. Ağaçta, 'TransactionsGroups\toplanan' öğesini seçin.
53. Ağaçta, 'TransactionsGroups\toplanan\MaxOfAmountMST' öğesini seçin.
54. Ağaçta, 'Toplamlar\Toplam istatistiksel değer(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')' öğesini seçin.
55. Bağla'ya tıklayın.
56. Ağaçta 'TransactionsGroups' öğesini genişletin.
57. Ağaçta 'TransactionsGroups' öğesini seçin.
58. Düzenle öğesine tıklayın.
59. Grubu buna göre düzenle'ye tıklatın.
    * Aynı alandaki her iki toplam da veri modeli öğelerine bağlı olduğundan 'Yürütme konumu' alanının bu gruplamanın çalışma zamanında bellekte gerçekleştirileceğini gösterdiğini unutmayın.   
60. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
61. Sil'i tıklatın.
62. Evet'i tıklatın.
63. Sil'i tıklatın.
64. Evet'i tıklatın.
65. Alanı buna ekle'yi tıklatın.
66. Neler gruplanacak'ı tıklayın.
67. Ağaçta 'Emtia kaydı(Intrastat)' öğesini seçin.
68. Kaydet'e tıklayın.
    * Tanımlanan toplamlar olmamasına ve 'Tablo kayıtları' türündeki seçilen veri kaynağı aynı 'Intrastat' tablosuna başvuruda bulunmasına rağmen 'Yürütme konumu' alanı bu gruplamanın çalışma zamanında bellekte gerçekleştirileceğini gösterir. Bunun nedeni, veri kaynağının henüz SQL veritabanı düzeyine çevrilmemiş olan bazı hesaplanmış alanlar içermesidir.  


