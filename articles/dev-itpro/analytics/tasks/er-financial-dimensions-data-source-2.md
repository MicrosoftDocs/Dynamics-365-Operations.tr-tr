--- 
title: "Mali boyutları bir veri kaynağı olarak kullanmak için modelleri eşleme"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.openlocfilehash: c26713a8a391f9f10a6e24f6619c24c1615d4560
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source"></a>Mali boyutları bir veri kaynağı olarak kullanmak için modelleri eşleme 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 1: Veri modeli tasarlama)" yordamındaki adımları tamamlamanız gerekir.


## <a name="add-required-data-sources-to-model-mapping"></a>Gerekli veri kaynaklarını model eşlemeye ekleme
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.
3. Tasarımcı'yı tıklatın.
4. Modeli veri kaynağına eşle'yi tıklayın.
5. Yeni'ye tıklayın.
6. Tanım alanında Giriş'i seçin.
7. Ad alanına 'Boyut verileri eşleme' yazın.
8. Açıklama alanına 'Boyut verileri eşleme' yazın.
9. Kaydet'e tıklayın.
10. Tasarımcı'yı tıklatın.
11. Ağaçta, 'Dynamics 365 for Operations\Tablo' seçin.
12. Kök ekle'ye tıklayın.
13. İsim alanına 'Şirket' yazın.
14. Tablo alanına 'CompanyInfo' yazın.
15. Tamam'ı tıklatın.
16. Ağaçta, 'İşlevler\Mali boyutların ayrıntıları' öğesini seçin.
17. Kök ekle'ye tıklayın.
    * Bu veri kaynağı, mali boyutların kapsamının veri kaynağı olarak bu modeli kullanacak tüm raporlar için nasıl tanımlanacağını belirtir.  
18. İsim alanına bir değer yazın.
19. Boyutları iste alanında Evet'i seçin.
    * Kullanıcının Kullanıcı iletişim formunda çalışma zamanında boyutları seçmesine izin vermek için Evet'i seçin. Bu seçenek Hayır olarak ayarlandığında, geçerli kurulumun tüm mali boyutları varsayılan olarak kullanılır.  
20. Mali boyutlar seçimi alanında, 'Tüzel kişilik'i seçin.
    * Kullanıcının Arama alanında geçerli kurulum için istenen boyutları seçmesine izin vermek için Tümü'nü seçin.  Kullanıcının Arama alanında şirket için istenen boyutları seçmesine izin vermek için Tüzel kişilik'i seçin.  Kullanıcının tek bir boyut kümesi kullanan boyutları seçmesine izin vermek için Boyut'u seçin.  
21. Ana hesap iste alanında Evet'i seçin.
    * Kullanıcıların ana hesabı boyutlar listesinin bir parçası olarak seçmesine izin vermek için 'Ana hesabı iste' seçeneğini Evet olarak ayarlayın.   Bu seçenek Hayır olarak ayarlandığında, ana hesap boyutlar listesine dahil edilmez ve 'Ana hesap zorunlu' seçeneği etkinleştirilir. "Ana hesap zorunlu" seçeneği Evet olarak ayarlandığında, kullanıcının seçiminden bağımsız olarak, ana hesabı boyutlar listesine ekleyin.  
22. Tamam'a tıklayın.
23. Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' seçin.
24. Kök ekle'ye tıklayın.
25. Ad alanına 'LedgerJournal' yazın.
26. Sorgu iste alanında Evet'i seçin.
27. Tablo alanına 'LedgerJournalTable' yazın.
28. Tamam'a tıklayın.

## <a name="map-data-model-elements-to-added-data-sources"></a>Veri modeli öğelerini eklenen veri kaynaklarına eşleme
1. Ağaçta, 'Günlük' öğesini genişletin.
2. Ağaçta, 'Günlük\Hareket' öğesini genişletin.
3. Ağaçta, 'Günlük\Hareket\Boyut verileri' öğesini genişletin.
4. Ağaçta, 'Boyutlar ayarı' öğesini genişletin.
5. Ağaçta, 'LedgerJournal' öğesini genişletin.
6. Ağaçta, 'LedgerJournal\<İlişkiler' öğesini genişletin.
7. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans' öğesini genişletin.
8. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Fiş' öğesini seçin.
9. Ağaçta, 'Günlük\Hareket\Fiş' öğesini seçin.
10. Bağla'ya tıklayın.
11. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' öğesini seçin.
    * Örneğin LedgerDimension olarak ayarlanmış mali boyutlara yapılan tüm referansları için bunlara karşılık gelen bir veri kaynağının (LedgerDimension.Dimension) bulunduğuna dikkat edin. Bu veri kaynağı öğesi bu boyutlar kümesinin mali boyutlarını kaydın listesi olarak sunar.  
12. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' öğesini genişletin.
13. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar' öğesini genişletin.
14. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer' öğesini genişletin.
15. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Tanım' öğesini genişletin.
16. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Tanım\Ad' öğesini seçin.
17. Ağaçta, 'Günlük\Hareket\Boyut verileri\Ad' öğesini seçin.
18. Bağla'ya tıklayın.
19. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer\Açıklama' öğesini seçin.
20. Ağaçta, 'Günlük\Hareket\Boyut verileri\Açıklama' öğesini seçin.
21. Bağla'ya tıklayın.
22. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer\Kod' öğesini seçin.
23. Ağaçta, 'Günlük\Hareket\Boyut verileri\Kod' öğesini seçin.
24. Bağla'ya tıklayın.
25. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar' öğesini seçin.
26. Ağaçta, 'Günlük\Hareket\Boyut verileri' öğesini seçin.
27. Bağla'ya tıklayın.
28. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)' öğesini seçin.
29. Ağaçta, 'Günlük\Hareket\Borç' öğesini seçin.
30. Bağla'ya tıklayın.
31. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)' öğesini seçin.
32. Ağaçta, 'Günlük\Hareket\Tarih' öğesini seçin.
33. Bağla'ya tıklayın.
34. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)' öğesini seçin.
35. Ağaçta, 'Günlük\Hareket\Para Birimi' öğesini seçin.
36. Bağla'ya tıklayın.
37. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)' öğesini seçin.
38. Ağaçta, 'Günlük\Hareket\Alacak' öğesini seçin.
39. Bağla'ya tıklayın.
40. Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans' öğesini seçin.
41. Ağaçta, 'Günlük\Hareket' öğesini seçin.
42. Bağla'yı tıklatın.
43. Ağaçta, 'LedgerJournal\Günlük toplu iş numarası (JournalNum)' öğesini seçin.
44. Ağaçta, 'Günlük\Toplu İş' öğesini seçin.
45. Bağla'yı tıklatın.
46. Ağaçta, 'LedgerJournal' öğesini seçin.
47. Ağaçta, 'Günlük' öğesini seçin.
48. Bağla'yı tıklatın.
49. Ağaçta, 'Boyutlar' öğesini genişletin.
50. Ağaçta, 'Boyutlar\Ana hesap ve boyutlar' öğesini genişletin.
51. Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım' öğesini genişletin.
52. Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım\Ad' öğesini seçin.
53. Ağaçta, 'Boyutlar ayarı\Kod' öğesini seçin.
54. Bağla'yı tıklatın.
55. Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım\Rapor sütunu adı' öğesini seçin.
56. Ağaçta, 'Boyutlar ayarı\Ad' öğesini seçin.
57. Bağla'yı tıklatın.
58. Ağaçta, 'Boyutlar\Ana hesap ve boyutlar' öğesini seçin.
59. Ağaçta, 'Boyutlar ayarı' öğesini seçin.
60. Bağla'ya tıklayın.
61. Ağaçta, 'Şirket' öğesini seçin.
62. Düzenle öğesine tıklayın.
63. expressionAsStringText alanına 'Company.'find()'.'name()'' yazın.
    * Company.'find()'.'name()'  
64. Kaydet'e tıklayın.
65. Sayfayı kapatın.
66. Kaydet'e tıklayın.
67. Sayfayı kapatın.

## <a name="complete-this-draft-models-version"></a>Bu taslak modelin sürümünü tamamlama
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Durumu değiştir öğesine tıklayın.
4. Tamamla öğesine tıklayın.
5. Tamam'a tıklayın.


