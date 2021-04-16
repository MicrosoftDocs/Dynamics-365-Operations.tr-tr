---
title: ER model eşlemelerini tanımlama ve bunlar için veri kaynaklarını seçme
description: Bu konuda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi'nin bir Elektronik raporlama veri modeli için veri kaynaklarını nasıl seçebileceği açıklanmaktadır.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d88aaa24d61d6768801a84c81002d7a6ab2f316
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755094"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>ER model eşlemelerini tanımlama ve bunlar için veri kaynaklarını seçme

[!include [banner](../../includes/banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının bir Elektronik Raporlama (ER) veri modeli için veri kaynaklar seçebilir. Veri kaynakları, tasarım zamanında seçilen veri modelinin ayrı ayrı bileşenlerine bağlanır ve çalışma süresinde bu veri modeli için iş verilerini doldurur. Bu örnekte, Litware, Inc. örnek şirketi için oluşturulan, mevcut bir veri modeli için veri kaynaklarını seçeceksiniz. Bu adımları tamamlamak için öncelikle "Yeni veri modeli oluştur" prosedürü altındaki adımları tamamlamanız gerekir.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Elektronik Raporlama yapılandırmaları ağacını açın
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.

## <a name="insert-a-new-model-mapping"></a>Yeni bir model eşlemesi ekle
1. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.
2. Tasarımcı'yı tıklatın.
3. Modeli veri kaynağına eşle'yi tıklayın.
4. Yeni'ye tıklayın.
    * Bu, veri kaynaklarına bir veri modeli eşlemek için yeni bir kayıt oluşturur. Bu örnekte tercih edilen ödeme türü olan Kredi transferi için veri kaynaklarına veri modelinin eşlemesin yapacaksınız.     Belirli bir veri modeli için birden fazla eşleme tasarlamak mümkündür. Örneğin, doğrudan borç veya kredi transferi gibi farklı ödeme türleri için eşlemeler oluşturacaktınız. Bu örnekte, kredi transferleri için bir eşleme oluşturacaksınız.  
5. İsim alanına 'CT eşleme' yazın.
    * CT eşleme  
6. Açıklama alanına, 'ödeme modeli CT eşleme' yazın.
    * Ödeme modeli CT eşleme  
7. Tanım alanına, "CustomerCreditTransferInitiation" yazın.
    * CustomerCreditTransferInitiation  
8. Tanımı ResolveChanges.
9. Kaydet'e tıklayın.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Geçerli model eşleme için gereken veri kaynaklarını tanımlama
1. Tasarımcı'yı tıklatın.
2. Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' öğesini seçin.
3. Kök ekle'ye tıklayın.
    * Ödeme hareketlerine erişmek için bu veri kaynağı girin.  
4. İsim alanına, 'Hareketler' yazın.
    * Hareketler  
5. Etiket alanına "Hareketler" girin.
    * Hareketler  
6. Yardım alanına 'Genel muhasebe günlük satırları' girin.
    * Genel muhasebe günlüğü satırları  
7. Sorgu iste alanında Evet'i seçin.
    * Evet'i seçin.  
8. Tablo alanına 'LedgerJournalTrans' yazın.
    * LedgerJournalTrans  
9. Tamam'a tıklayın.
    * Geçerli veri modeli için bir veri kaynağı olarak LedgerJournalTrans tablosunu seçin.  
10. Ağaçta, 'Functions\Calculated field' seçin.
11. Ekle öğesini tıklatın.
    * Yeni bir hesaplanmış alan eklemek için Ekle'yi tıklatın.  
12. İsim alanına '$EndToEndID' yazın.
    * $EndToEndID  
13. Formülü düzenle'ye tıklayın.
14. Ağaçta 'String\CONCATENATE' seçin.
15. Fonksiyon ekle'ye tıklayın.
16. Ağaçta, 'Hareketler'i genişletin.
17. Ağaçta, 'Transactions\Voucher' seçin.
18. Veri kaynağı ekle'ye tıklayın.
19. Formül alanına "CONCATENATE(Transactions.Voucher, "-", " yazın.
    * Förmülün sonuna, [ , “-“, ] yazın.  
20. Ağaçta 'String\TEXT' seçin.
21. Fonksiyon ekle'ye tıklayın.
22. Ağaçta, 'Transactions\Record-ID(RecId)' seçin.
23. Veri kaynağı ekle'ye tıklayın.
24. Formül alanına "CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))" yazın.
    * Formülün sonuna, [))] yazın.  
25. Kaydet'e tıklayın.
    * Oluşturulan formülde herhangi bir hata tespit edilmediğinden emin olun. Formül düzenleyici denetimin altındaki HATALAR sekmesine bakın.  
26. Sayfayı kapatın.
27. Tamam'a tıklayın.
    * Bu veri kaynağına hesaplanan alan ekleyin.  
28. Ekle öğesini tıklatın.
    * Yeni bir hesaplanmış alan eklemek için Ekle'yi tıklatın.  
29. İsim alanına '$Amount' yazın.
    * $Amount  
30. Formülü düzenle'ye tıklayın.
31. Ağaçta, 'Hareketler'i genişletin.
32. Ağaçta, 'Transactions\Debit(AmountCurDebit)' seçin.
33. Veri kaynağı ekle'ye tıklayın.
34. Formül alanına "Transactions.AmountCurDebit - " yazın.
    * Formün sonuna [ - ] yazın.  
35. Ağaçta, 'Transactions\Credit(AmountCurCredit)' seçin.
36. Veri kaynağı ekle'ye tıklayın.
37. Kaydet'e tıklayın.
38. Sayfayı kapatın.
39. Tamam'a tıklayın.
    * Bu, $Amount hesaplanan alanını, mevcut veri modeli için seçilen veri kaynağına ekleyecektir.  
40. Ağaçta, 'Transactions\$Amount' seçin.
41. Ağaçta, 'Hareketler'i genişletin.
42. Ağaçta, "Hareketler\$Tutar" öğesini genişletin veya daraltın.
43. Ağaçta, "Hareketler" öğesini genişletin veya daraltın.
44. Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' öğesini seçin.
45. Kök ekle'ye tıklayın.
    * Şirketin banka hesap ayrıntılarına erişmek için bu veri kaynağı girin.  
46. İsim alanına 'BankAccount' yazın.
    * BankAccount  
47. Etiket alanına "Banka Hesabı" girin.
    * Banka Hesabı  
48. Yardım alanına "Banka Hesabı" girin.
    * Banka Hesabı  
49. Sorgu iste alanında Evet'i seçin.
    * Evet'i seçin.  
50. Tablo alanına 'BankAccountTable' yazın.
    * BankAccountTable  
51. Tamam'a tıklayın.
    * Geçerli veri modeli için bir veri kaynağı olarak BankAccountTable tablosunu seçin.  
52. Kök ekle'ye tıklayın.
    * Şirketin koşullarına erişmek için bu veri kaynağı girin.  
53. İsim alanına 'Şirket' yazın.
    * Şirket  
54. Etiket alanına bir değer yazın.
    * Şirket bilgileri  
55. Yardım alanına 'Şirket bilgisi' girin.
    * Şirket bilgileri  
56. Sorgu iste alanında Evet'i seçin.
    * Evet'i seçin.  
57. Tablo alanına 'CompanyInfo' yazın.
    * CompanyInfo  
58. Tamam'a tıklayın.
    * Geçerli veri modeli için bir veri kaynağı olarak CompanyInfo tablosunu seçin.  
59. Ağaçta, 'Functions\Calculated field' seçin.
60. Kök ekle'ye tıklayın.
    * Hesaplanan bir alanı yeni bir veri kaynağı olarak ekleyin.  
61. İsim alanına 'ProcessingDateTime' yazın.
    * ProcessingDateTime  
62. Etiket alanına 'İşleme tarihi ve saati'ni girin.
    * İşleme tarihi ve saati  
63. Formülü düzenle'ye tıklayın.
64. Ağaçta, "Tarih saat\SESSIONNOW" öğesini seçin.
65. Fonksiyon ekle'ye tıklayın.
66. Kaydet'e tıklayın.
67. Sayfayı kapatın.
68. Tamam'a tıklayın.
    * Geçerli veri modeli için bir veri kaynağı olarak ProcessingDateTime hesaplanmış alanı ekleyin.  
69. Kaydet'e tıklayın.
70. Sayfayı kapatın.
71. Sayfayı kapatın.
72. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]