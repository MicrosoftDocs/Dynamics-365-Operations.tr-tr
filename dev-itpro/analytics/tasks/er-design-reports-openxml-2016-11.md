--- 
title: "Elektronik raporlama (ER) için OpenXML biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama"
description: "Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının OPENXML biçiminde elektronik ödeme belgeleri oluşturmak için bir şablon içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d552dbcf932813de4d060b4f2190cf388eddb1bf
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için OpenXML biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının OPENXML biçiminde elektronik ödeme belgeleri oluşturmak için bir şablon içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır. Bu yapılandırma, satıcı ödemelerini işlemek için kullanılacaktır.



Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir GBSI şirketinde gerçekleştirilebilir.



Bu adımları tamamlamak için, öncelikle "Bir yapılandırma sağlayıcı oluşturun ve etkin olarak işaretleyin" yordamındaki adımları tamamlamanız gerekir. Ayrıca, şablonu oluştururken, alınacak olan bir Excel dosyası olmalıdır. Bu dosyaya şu adresten erişilebilir: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx


## <a name="upload-the-payments-data-model-configuration"></a>Ödemeler veri modeli konfigürasyonunu yükleme
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Listede, seçili satırı işaretleyin.
    * Örnek şirket Litware, Inc. için yapılandırma sağlayıcısını seçin. Bu yapılandırma sağlayıcısını göremiyorsanız, önce "Yapılandırma sağlayıcı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamalısınız.  
3. Etkin olarak ayarla'ya tıklayın.
4. Depolar'a tıklayın.
    * Varsa, Operations Kaynakları türü için bir depo seçin. Kullanılabiliyorsa, yeni bir havuz oluşturmak hakkındaki aşağıdaki adımları atlayın.  
5. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
6. Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.
7. Havuz oluştur'a tıklayın.
8. Tamam'a tıklayın.
9. Aç'a tıklayın.
10. Ağaçta 'Ödeme modeli' seçin.
11. İçe aktar'ı tıklatın.
    * Bu veri modelini içeri alın. Yeni bir biçim yapılandırılmasında veri kaynağı olarak kullanılır. Bu yapılandırmayı zaten içe aktardıysanız, bu adımı atlayın.  
12. Evet'i tıklatın.
13. Sayfayı kapatın.
14. Sayfayı kapatın.

## <a name="create-a-new-format-configuration"></a>Yeni bir biçim yapılandırması oluşturma
1. Raporlama konfigürasyonları'na tıklayın.
2. Ağaçta 'Ödeme modeli' seçin.
3. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
4. Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.
    * Bir biçimi, PaymentModel veri modeline dayalı olarak oluşturun.  
5. Ad alanında 'Örnek çalışma sayfası raporu' yazın.
    * Örnek çalışma sayfası raporu  
6. Açıklama alanında, 'Satıcıların ödemeleri için örnek çalışma sayfası raporu' yazın.
    * Satıcıların ödemeleri için örnek çalışma sayfası raporu.  
7. Veri modeli tanımı alanına bir değer girin veya seçin.
    * 'CustomerCreditTransferInitiation' tanımını seçin.  
8. Konfigürasyon oluştur'u tıklatın.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>OPENXML çalışma sayfası biçiminde yeni bir belge tasarlama
1. Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.
2. Tasarımcı'yı tıklatın.
3. Eylem Bölmesinde, İçeri Al'a tıklayın.
4. Microsoft Excel'den içe aktar'a tıklayın.
5. Ekler'e tıklayın.
    * Şablon olarak mevcut Excel belgesini iliştirin.  
6. Yeni'ye tıklayın.
7. Dosya'ya tıklayın.
    * Mevcut Excel dosyasına yönlendirin.  
8. Sayfayı kapatın.
9. Şablon alanına bir değer girin veya seçin.
    * Şablon olarak kullanılmak üzere ekli Excel dosyasını seçin.  
10. Tamam'a tıklayın.
    * ER biçim bileşenlerinin, başvurulan MS Excel belgesinin (adlandırılmış aralıklar) yapısına dayalı bir tasarım biçiminde oluşturulduğunu unutmayın.  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Para birimi kodlarına göre toplamları hesaplamak için yeni bir veri kaynağı oluşturma
1. Eşleme sekmesini tıklatın.
2. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
3. Ağaçta 'İşleveler\Grupla'yı seçin.
4. Ad alanında 'PaymentByCurrency' yazın.
    * PaymentByCurrency  
5. Grubu buna göre düzenle'ye tıklatın.
6. Ağaçta, 'model'i genişletin.
7. Ağaçta seçin 'model\Payments'.
8. Alanı buna ekle'yi tıklatın.
9. Neler gruplanacak'ı tıklayın.
10. Ağaçta genişletin 'model\Payments'.
11. Ağaçta seçin 'model\Payments\Currency'.
12. Alanı buna ekle'yi tıklatın.
13. Gruplandırılmış alanlar'ı tıklatın.
14. Ağaçta seçin: 'model\Payments\Instructed Amount(InstructedAmount)'.
15. Alanı buna ekle'yi tıklatın.
16. Toplam alanları'nı tıklatın.
17. Yöntem alanında bir seçenek belirtin.
    * SUM toplama işlevini seçin.  
18. Ad alanında 'TotalInstructuredAmount' yazın.
    * TotalInstructuredAmount  
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.
21. Tamam'a tıklayın.

## <a name="map-format-components-to-data-sources"></a>Biçim bileşenlerini veri kaynaklarına eşleme
1. Ağaçta, 'model'i genişletin.
2. Ağaçta genişletin 'model\Payments'.
3. Ağaçta, 'model\Payments\Initiating Party(InitiatingParty)' seçeneğini genişletin.
4. Ağaçta 'model\Payments\Initiating Party(InitiatingParty)\Name' seçeneğini seçin.
5. Ağaçta, "Excel\ReportHeader" öğesini genişletin.
6. Ağaçta, "Excel\ReportHeader\CompanyName" öğesini seçin.
7. Bağla'ya tıklayın.
8. Ağaçta genişletin 'model\Payments\Creditor'.
9. Ağaçta genişletin 'model\Payments\Creditor\Identification'.
10. Ağaçta seçin: 'model\Payments\Creditor\Identification\Source ID(SourceID)'.
11. Ağaçta, "Excel\PaymLines" öğesini genişletin.
12. Ağaçta, "Excel\PaymLines\VendAccountName" öğesini seçin.
13. Bağla'ya tıklayın.
14. Ağaçta seçin 'model\Payments\Creditor\Name'.
15. Ağaçta, "Excel\PaymLines\VendName" öğesini seçin.
16. Bağla'ya tıklayın.
17. Ağaçta genişletin: 'model\Payments\Creditor Agent(CreditorAgent)'.
18. Ağaçta seçin: 'model\Payments\Creditor Agent(CreditorAgent)\Name'.
19. Ağaçta, "Excel\PaymLines\Banka" öğesini seçin.
20. Bağla'ya tıklayın.
21. Ağaçta seçin 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.
22. Ağaçta, "Excel\PaymLines\RoutingNumber" öğesini seçin.
23. Bağla'ya tıklayın.
24. Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.
25. Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.
26. Ağaçta seçin 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.
27. Ağaçta, "Excel\PaymLines\AccountNumber" öğesini seçin.
28. Bağla'ya tıklayın.
29. Ağaçta seçin: 'model\Payments\Instructed Amount(InstructedAmount)'.
30. Ağaçta, "Excel\PaymLines\Borç" öğesini seçin.
31. Bağla'ya tıklayın.
32. Ağaçta genişletin 'model\Payments\Creditor'.
33. Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.
34. Ağaçta genişletin: 'model\Payments\Creditor Agent(CreditorAgent)'.
35. Ağaçta seçin 'model\Payments\Currency'.
36. Ağaçta, "Excel\PaymLines\Para Birimi" öğesini seçin.
37. Bağla'ya tıklayın.
38. Ağaçta 'PaymentByCurrency' öğesini genişletin.
39. Ağaçta genişletin: 'PaymentByCurrency\grouped'.
40. Ağaçta seçin 'PaymentByCurrency\grouped\Currency'.
41. Ağaçta, "Excel\SummaryLines" öğesini genişletin.
42. Ağaçta, "Excel\SummaryLines\SummaryCurrency" öğesini seçin.
43. Bağla'ya tıklayın.
44. Ağaçta genişletin 'PaymentByCurrency\aggregated'.
45. Ağaçta seçin 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.
46. Ağaçta, "Excel\SummaryLines\SummaryAmount" öğesini seçin.
47. Bağla'ya tıklayın.
48. Ağaçta 'PaymentByCurrency' seçin.
49. Ağaçta, "Excel\SummaryLines" öğesini seçin.
50. Bağla'ya tıklayın.
51. Ağaçta seçin 'model\Payments'.
52. Ağaçta, "Excel\PaymLines" öğesini seçin.
53. Bağla'ya tıklayın.
54. Kaydet'e tıklayın.
55. Sayfayı kapatın.

## <a name="use-the-created-configuration-for-payments-processing"></a>Ödemeleri işlemek için oluşturulan yapılandırmayı kullanın
1. Durumu değiştir öğesine tıklayın.
2. Tamamla öğesine tıklayın.
3. Tamam'a tıklayın.
4. Sayfayı kapatın.
5. Sayfayı kapatın.
6. Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.
7. Ödeme yöntemi alanına "Elektronik" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
    * Elektronik  
8. Düzenle öğesine tıklayın.
9. Dosya biçimleri bölümünü genişletin.
10. Genel elektronik raporlama alanında Evet'i seçin.
11. Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.
    * 'Örnek çalışma sayfası raporu yapılandırması'nı seçin.  
12. Kaydet'e tıklayın.
13. Sayfayı kapatın.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Oluşturulan yapılandırmayı ödeme günlüklerini işleme için kullanma
1. Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
2. Yeni'ye tıklayın.
    * Yeni bir ödeme günlüğü oluşturun.  
3. İsim alanına VendPay' yazın.
    * VendPay  
4. Satırlar seçeneğine tıklayın.
5. Hesap alanında, 'GB_SI_000001' değerlerini belirtin.
    * GB_SI_000001  
6. Borcu '1000' olarak ayarlayın.
7. Yeni'ye tıklayın.
8. Hesap alanında, 'GB_SI_000005' değerlerini belirtin.
    * GB_SI_000005  
9. Borcu '2000' olarak ayarlayın.
10. Para birimi alanına 'EUR' yazın.
    * Euro  
11. Mahsup hesabı alanında, 'GBSI OPER' değerlerini belirtin.
    * GBSI OPER  
12. Ödeme yöntemi alanına 'Elektronik' girin.
    * Elektronik  
13. Kaydet'e tıklayın.
14. Ödemeler oluştur'u tıklatın.
15. Ödeme yöntemi alanına 'Elektronik' girin.
    * Elektronik  
16. Ad alanına, "Ödemeler" yazın.
    * Örneğin 'Ödemeler' yazın.  
17. Banka hesabı alanında 'GBSI OPER' yazın.
    * GBSI OPER  
18. Tamam'a tıklayın.
19. Tamam'a tıklayın.
    * Oluşturulan çalışma sayfasını gözden geçirin; ödeme ayrıntı satırları ve bu ödeme iletisinde kullanılacak her bir para birimi kodu için toplamlar da dahil olmak üzere.  


