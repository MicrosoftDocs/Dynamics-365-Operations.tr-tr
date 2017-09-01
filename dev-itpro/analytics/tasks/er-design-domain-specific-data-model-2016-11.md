--- 
title: "Elektronik raporlama (ER) için etki alanına özel bir veri modeli tasarlama"
description: "Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bf727b63ed86e7cc26d4fca630d97af88abb1804
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için etki alanına özel bir veri modeli tasarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır. Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.



Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısını seçin. Bu yapılandırma sağlayıcısını göremiyorsanız, önce "Yapılandırma sağlayıcı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamalısınız.  
2. Raporlama konfigürasyonları'na tıklayın.
    * Bir elektronik ödeme belgeleri için veri modeli içeren bir yapılandırma oluşturacaksınız. Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.  

## <a name="create-a-new-data-model-configuration"></a>Yeni bir veri modeli yapılandırması oluşturun
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. İsim alanında, 'Ödemeler (Basitleştirilmiş model)' yazın.
    * Ödemeler (Basitleştirilmiş model)  
3. Açıklama alanına, 'Ödeme modeli yapılandırması' yazın.
    * Ödeme modeli konfigürasyonu  
    * Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir. Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır. Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.  
4. Yapılandırma oluşturma görevini tamamlamak için 'Konfigürasyon oluştur' düğmesini tıklatın

## <a name="create-a-data-model"></a>Bir veri modeli oluşturun
    * Seçili yapılandırma için yeni bir veri modeli oluşturuyorsunuz. Bu yapılandırma sürümü Taslak durumuna sahip.  
1. Tasarımcı'yı tıklatın.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Ödeme işlemine katılan bir tarafın yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. Ad alanına "Taraf" yazın.
    * Taraf  
3. Ekle öğesini tıklatın.
4. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
5. İsim alanında 'İsim' yazın.
    * Dosya Adı  
6. Madde türü alanında 'Dize' seçin.
7. Ekle öğesini tıklatın.
8. Bul alanına "Taraf" yazın.
    * Taraf  
9. Öncekini bul'a tıklayın.

## <a name="define-the-bank-structure-for-this-model"></a>Bu model için banka yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. İsim alanına 'Agent' yazın.
    * Temsilci  
3. Madde türü alanında 'Kayıt'ı seçin.
4. Ekle öğesini tıklatın.
5. Açıklama alanına "Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka)." yazın.
    * Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka).  
6. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
7. İsim alanında 'İsim' yazın.
    * Dosya Adı  
8. Madde türü alanında 'Dize' seçin.
9. Ekle öğesini tıklatın.
10. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
11. İsim alanına 'SWIFT' yazın.
    * SWIFT  
12. Ekle öğesini tıklatın.
13. Açıklama alanına, "Banka kimlik saptama kodu" yazın.
    * Banka kimlik saptama kodu  
14. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
15. İsim alanına 'RoutingNumber' yazın.
    * RoutingNumber  
16. Ekle öğesini tıklatın.
17. Açıklama alanına "Rota numarası" yazın.
    * Rota numarası  
18. Öncekini bul'a tıklayın.

## <a name="define-the-bank-account-structure-for-this-model"></a>Bu model için hesap yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. İsim alanına 'Hesap' yazın.
    * Hesap  
3. Madde türü alanında 'Kayıt'ı seçin.
4. Ekle öğesini tıklatın.
5. Açıklama alanına "Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği." yazın.
    * Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği.  
6. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
7. İsim alanına 'Para birimi' yazın.
    * Para birimi  
8. Madde türü alanında 'Dize' seçin.
9. Ekle öğesini tıklatın.
10. Açıklama alanına "Para birimi kodu" yazın.
    * Para birimi kodu  
11. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
12. İsim alanına 'Numara' yazın.
    * Sayı  
13. Ekle öğesini tıklatın.
14. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
15. İsim alanına 'IBAN' yazın.
    * IBAN  
16. Ekle öğesini tıklatın.
17. Açıklama alanına, "Uluslararası banka hesap numarası" yazın.
    * Uluslararası banka hesap numarası  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Kredi transferi ödeme türü için ödeme iletisi yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. Yeni düğüm biçimi alanına "Model kökü" girin.
3. İsim alanında 'CustomerCreditTransferInitiation' yazın.
    * CustomerCreditTransferInitiation  
4. Ekle öğesini tıklatın.
5. Bul alanına "CustomerCreditTransferInitiation" yazın.
    * CustomerCreditTransferInitiation  
6. Öncekini bul'a tıklayın.
7. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
8. İsim alanına 'MessageIdentification' yazın.
    * MessageIdentification  
9. Ekle öğesini tıklatın.
10. Açıklama alanına "Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans." yazın.
    * Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans.  
11. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
12. İsim alanına 'ProcessingDateTime' yazın.
    * ProcessingDateTime  
13. Madde türü alanında 'DateTime' seçin.
14. Ekle öğesini tıklatın.
15. Açıklama alanına, "Ödeme iletisinin oluşturulduğu tarih ve saat." yazın.
    * Ödeme iletisinin oluşturulduğu tarih ve saat.  
16. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
    * Bu model için ödeme hareketi yapısını tanımlayın.  
17. İsim alanına 'Ödemeler' yazın.
    * Ödemeler  
18. Madde türü alanında 'Kayıt listesi'ni seçin.
19. Ekle öğesini tıklatın.
20. Açıklama alanına, 'Geçerli iletinin ödeme satırları' girin.
    * Geçerli iletinin ödeme satırları  
21. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
22. İsim alanına 'Alacaklı' yazın.
    * Alacaklı  
23. Madde türü alanında 'Kayıt'ı seçin.
24. Ekle öğesini tıklatın.
25. Açıklama alanına "Belli bir tutardaki paranın ödenmesi gereken taraf." yazın.
    * Belli bir tutardaki paranın ödenmesi gereken taraf.  
26. Madde referansını değiştir'e tıklayın.
27. Bul alanına "Taraf" yazın.
    * Taraf  
28. Sonrakini bul'a tıklayın.
29. Tamam'a tıklayın.
30. Bul alanına "Ödemeler" yazın.
    * Ödemeler  
31. Sonrakini bul'a tıklayın.
32. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
33. İsim alanına 'Borçlu' yazın.
    * Borçlu  
34. Ekle öğesini tıklatın.
35. Açıklama alanına "Alacaklıya (son) belli bir tutarda para borçlu olan taraf." yazın.
    * Alacaklıya (son) belli bir tutarda para borçlu olan taraf.  
36. Madde referansını değiştir'e tıklayın.
37. Bul alanına "Taraf" yazın.
    * Taraf  
38. Sonrakini bul'a tıklayın.
39. Tamam'a tıklayın.
40. Sonrakini bul'a tıklayın.
41. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
42. İsim alanına 'Açıklama' yazın.
    * Açıklama  
43. Madde türü alanında 'Dize' seçin.
44. Ekle öğesini tıklatın.
45. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
46. İsim alanına 'Para birimi' yazın.
    * Para birimi  
47. Ekle öğesini tıklatın.
48. Açıklama alanına "Para birimi kodu" yazın.
    * Para birimi kodu  
49. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
50. İsim alanına, 'TransactionDate' yazın.
    * TransactionDate  
51. Madde türü alanında 'Tarih' seçin.
52. Ekle öğesini tıklatın.
53. Açıklama alanına, "Hareket tarihi" yazın.
    * Hareket tarihi  
54. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
55. İsim alanına 'InstructedAmount' yazın.
    * InstructedAmount  
56. Madde türü alanında 'Gerçek' seçin.
57. Ekle öğesini tıklatın.
58. Açıklama alanına "Masraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı" yazın. Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.
    * Tasraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı. Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.  
59. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
60. İsim alanına 'End2EndID' yazın.
    * End2EndID  
61. Madde türü alanında 'Dize' seçin.
62. Ekle öğesini tıklatın.
63. Açıklama alanına "Başlatan tarafça atanan benzersiz kimlik" yazın. Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.
    * Başlatan tarafça atanan benzersiz kimlik. Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.  
64. İsim alanında 'PaymentModel' yazın.
    * PaymentModel adı önceden tanımlanmış ödeme formları arabirimleriyle hizalanır.  
65. Kaydet'e tıklayın.
66. Sayfayı kapatın.


