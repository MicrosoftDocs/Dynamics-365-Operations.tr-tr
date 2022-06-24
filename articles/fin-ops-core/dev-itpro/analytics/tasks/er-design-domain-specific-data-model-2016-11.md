---
title: ER Tasarım etki alanına özel veri modeli
description: Bu makalede, elektronik ödeme belgeleri için bir veri modeli içeren yeni bir Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı açıklanmaktadır.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c923ed6ec817d1f4ae6cd956c06b2156a6a61311
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908456"
---
# <a name="er-design-domain-specific-data-model"></a>ER Tasarım etki alanına özel veri modeli

[!include [banner](../../includes/banner.md)]

Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır. Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.

Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.

    Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısını seçin. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.  
    
2. Raporlama konfigürasyonları'na tıklayın.

    Bir elektronik ödeme belgeleri için veri modeli içeren bir yapılandırma oluşturacaksınız. Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.  

## <a name="create-a-new-data-model-configuration"></a>Yeni bir veri modeli yapılandırması oluşturun
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. İsim alanında, 'Ödemeler (Basitleştirilmiş model)' yazın.
3. Açıklama alanına, 'Ödeme modeli yapılandırması' yazın.

    Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir. Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır. Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.  

4. Yapılandırma oluşturma görevini tamamlamak için 'Konfigürasyon oluştur' düğmesini tıklatın

## <a name="create-a-data-model"></a>Bir veri modeli oluşturun
Seçili yapılandırma için yeni bir veri modeli oluşturuyorsunuz. Bu yapılandırma sürümü Taslak durumuna sahip.  
1. Tasarımcı'yı tıklatın.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Ödeme işlemine katılan bir tarafın yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. Ad alanına "Taraf" yazın.
3. Ekle öğesine tıklayın.
4. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
5. İsim alanında 'İsim' yazın.
6. Madde türü alanında 'Dize' seçin.
7. Ekle öğesine tıklayın.
8. Bul alanına "Taraf" yazın.
9. Öncekini bul'a tıklayın.

## <a name="define-the-bank-structure-for-this-model"></a>Bu model için banka yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. İsim alanına 'Agent' yazın.
3. Madde türü alanında 'Kayıt'ı seçin.
4. Ekle öğesine tıklayın.
5. Açıklama alanına "Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka)." yazın.

    Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka).  

6. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
7. İsim alanında 'İsim' yazın. 
8. Madde türü alanında 'Dize' seçin.
9. Ekle öğesine tıklayın.
10. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
11. İsim alanına 'SWIFT' yazın.
12. Ekle öğesine tıklayın.
13. Açıklama alanına, "Banka kimlik saptama kodu" yazın. 
14. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
15. İsim alanına 'RoutingNumber' yazın.
16. Ekle öğesine tıklayın.
17. Açıklama alanına "Rota numarası" yazın.
18. Öncekini bul'a tıklayın.

## <a name="define-the-bank-account-structure-for-this-model"></a>Bu model için hesap yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. İsim alanına 'Hesap' yazın. 
3. Madde türü alanında 'Kayıt'ı seçin.
4. Ekle öğesine tıklayın.
5. Açıklama alanına "Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği." yazın.

    Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği.  

6. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
7. İsim alanına 'Para birimi' yazın. 
8. Madde türü alanında 'Dize' seçin.
9. Ekle öğesine tıklayın.
10. Açıklama alanına "Para birimi kodu" yazın.
11. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
12. İsim alanına 'Numara' yazın. 
13. Ekle öğesine tıklayın.
14. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
15. İsim alanına 'IBAN' yazın. 
16. Ekle öğesine tıklayın.
17. Açıklama alanına, "Uluslararası banka hesap numarası" yazın.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Kredi transferi ödeme türü için ödeme iletisi yapısını tanımlama
1. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
2. Yeni düğüm biçimi alanına "Model kökü" girin.
3. İsim alanında 'CustomerCreditTransferInitiation' yazın.
4. Ekle öğesine tıklayın.
5. Bul alanına "CustomerCreditTransferInitiation" yazın. 
6. Öncekini bul'a tıklayın.
7. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
8. İsim alanına 'MessageIdentification' yazın. 
9. Ekle öğesine tıklayın.
10. Açıklama alanına "Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans." yazın.

    Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans.  

11. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
12. İsim alanına 'ProcessingDateTime' yazın.
13. Madde türü alanında 'DateTime' seçin.
14. Ekle öğesine tıklayın.
15. Açıklama alanına, "Ödeme iletisinin oluşturulduğu tarih ve saat." yazın. 
16. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.

    Bu model için ödeme hareketi yapısını tanımlayın.  

17. İsim alanına 'Ödemeler' yazın.
18. Madde türü alanında 'Kayıt listesi'ni seçin.
19. Ekle öğesine tıklayın.
20. Açıklama alanına, 'Geçerli iletinin ödeme satırları' girin.
21. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
22. İsim alanına 'Alacaklı' yazın. 
23. Madde türü alanında 'Kayıt'ı seçin.
24. Ekle öğesine tıklayın.
25. Açıklama alanına "Belli bir tutardaki paranın ödenmesi gereken taraf." yazın. 
26. Madde referansını değiştir'e tıklayın.
27. Bul alanına "Taraf" yazın.
28. Sonrakini bul'a tıklayın.
29. Tamam'a tıklayın.
30. Bul alanına "Ödemeler" yazın.
31. Sonrakini bul'a tıklayın.
32. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
33. İsim alanına 'Borçlu' yazın. 
34. Ekle öğesine tıklayın.
35. Açıklama alanına "Alacaklıya (son) belli bir tutarda para borçlu olan taraf." yazın.
36. Madde referansını değiştir'e tıklayın.
37. Bul alanına "Taraf" yazın.
38. Sonrakini bul'a tıklayın.
39. Tamam'a tıklayın.
40. Sonrakini bul'a tıklayın.
41. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
42. İsim alanına 'Açıklama' yazın.
43. Madde türü alanında 'Dize' seçin.
44. Ekle öğesine tıklayın.
45. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
46. İsim alanına 'Para birimi' yazın.
47. Ekle öğesine tıklayın.
48. Açıklama alanına "Para birimi kodu" yazın.
49. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
50. İsim alanına, 'TransactionDate' yazın. 
51. Madde türü alanında 'Tarih' seçin.
52. Ekle öğesine tıklayın.
53. Açıklama alanına, "Hareket tarihi" yazın. 
54. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
55. İsim alanına 'InstructedAmount' yazın.  
56. Madde türü alanında 'Gerçek' seçin.
57. Ekle öğesine tıklayın.
58. Açıklama alanına "Masraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı" yazın. Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.

    Tasraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı. Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.  

59. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
60. İsim alanına 'End2EndID' yazın. 
61. Madde türü alanında 'Dize' seçin.
62. Ekle öğesine tıklayın.
63. Açıklama alanına "Başlatan tarafça atanan benzersiz kimlik" yazın. Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir. 
64. İsim alanında 'PaymentModel' yazın.

    PaymentModel adı önceden tanımlanmış ödeme formları arabirimleriyle hizalanır.  

65. Kaydet'e tıklayın.
66. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
