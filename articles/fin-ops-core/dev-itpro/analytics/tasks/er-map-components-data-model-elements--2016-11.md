---
title: ER Oluşturulan biçimin bileşenlerini veri modeli öğeleri ile eşleme (Kasım 2016)
description: Bu konuda, veri modeli öğelerinin oluşturulan Elektronik raporlama (ER) yapılandırmasının bileşenleriyle nasıl eşleneceği açıklanmaktadır.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae4b3123660d123fc5c06cbe0a69d5c66d306252ec2a117a1e6045505022f5a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776012"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>ER Oluşturulan biçimin bileşenlerini veri modeli öğeleri ile eşleme (Kasım 2016)

[!include [banner](../../includes/banner.md)]

Aşağıdaki yordam, Sistem yöneticisi veya Elektronik raporlama geliştirici rolüne sahip bir kullanıcının, veri modeli öğelerini ödemeler iş etki alanı için bir elektronik dosya biçimini tanımlayan, oluşturulmuş Elektronik raporlama (ER) yapılandırmasının bileşenlerine nasıl eşleyebileceğini gösterir. Bu biçim daha sonra ödeme işlemleri için elektronik belgeler oluşturmak üzere kullanılır. Bu örnekte, 'Litware, Inc.' örnek şirketi için bir biçim yapılandırması oluşturacaksınız. Bu adımlar, ER yapılandırmaları tüm şirketlerde paylaşıldığı için herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için öncelikle "Bir biçim yapılandırması oluşturma" görev kılavuzundaki adımları tamamlamalısınız.


## <a name="select-a-format-configuration"></a>Biçim yapılandırması seçme
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.
4. Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' seçin.
5. Tasarımcı'yı tıklatın.

## <a name="map-format-components-to-data-model-elements"></a>Format bileşenlerini veri modeli öğelerine eşleyin
1. Genişlet/daralt'a tıklayın.
2. Eşleme sekmesini tıklatın.
3. Ağaçta, 'model'i genişletin.
4. Ağaçta, "Xml\İleti\ProcessingDate\DateTime" öğesini seçin.
5. Ağaçta, "model\ProcessingDateTime" öğesini seçin.
6. Bağla'ya tıklayın.
7. Ağaçta, "Xml\İleti\MessageId\Dize" öğesini seçin.
8. Ağaçta, "model\MessageIdentification" öğesini seçin.
9. Bağla'ya tıklayın.
10. Ağaçta genişletin 'model\Payments'.
11. Ağaçta, "Xml\İleti\Ödemeler\Madde\Tutar\Dize" öğesini seçin.
12. Ağaçta, "model\Ödemeler\InstructedAmount" öğesini seçin.
13. Bağla'ya tıklayın.
14. Ağaçta, "Xml\İleti\Ödemeler\Madde\TransDate\DateTime" öğesini seçin.
15. Ağaçta, "model\Ödemeler\TransactionDate" öğesini seçin.
16. Bağla'ya tıklayın.
17. Ağaçta, "Xml\İleti\Ödemeler\Madde\Açıklama\Dize" öğesini seçin.
18. Ağaçta seçin 'model\Payments\Description'.
19. Bağla'ya tıklayın.
20. Ağaçta, "Xml\İleti\Ödemeler\Madde\Para Birimi\Dize" öğesini seçin.
21. Ağaçta seçin 'model\Payments\Currency'.
22. Bağla'ya tıklayın.
23. Ağaçta, "Xml\İleti\Ödemeler\Madde\Kimlik" öğesini seçin.
24. Ağaçta, "model\Ödemeler\End2EndID" öğesini seçin.
25. Bağla'ya tıklayın.
26. Ağaçta genişletin 'model\Payments\Creditor'.
27. Ağaçta genişletin 'model\Payments\Creditor\Account'.
28. Ağaçta genişletin 'model\Payments\Creditor\Agent'.
29. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad\Dize" öğesini seçin.
30. Ağaçta seçin 'model\Payments\Creditor\Name'.
31. Bağla'ya tıklayın.
32. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber\Dize" öğesini seçin.
33. Ağaçta, "model\Ödemeler\Alacaklı\Temsilci\RoutingNumber" öğesini seçin.
34. Bağla'ya tıklayın.
35. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber\Dize" öğesini seçin.
36. Ağaçta seçin 'model\Payments\Creditor\Account\Number'.
37. Bağla'ya tıklayın.
38. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Ad\Dize" öğesini seçin.
39. Ağaçta genişletin 'model\Payments\Debtor'.
40. Ağaçta genişletin 'model\Payments\Debtor\Account'.
41. Ağaçta genişletin 'model\Payments\Debtor\Agent'.
42. Ağaçta seçin 'model\Payments\Debtor\Name'.
43. Bağla'ya tıklayın.
44. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber\Dize" öğesini seçin.
45. Ağaçta, "model\Ödemeler\Borçlu\Temsilci\RoutingNumber" öğesini seçin.
46. Bağla'ya tıklayın.
47. Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber\Dize" öğesini seçin.
48. Ağaçta seçin 'model\Payments\Debtor\Account\Number'.
49. Bağla'ya tıklayın.
50. Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.
51. Ağaçta seçin 'model\Payments'.
52. Bağla'ya tıklayın.
53. Kaydet'e tıklayın.

## <a name="validate-format-mapping"></a>Biçim eşlemesini doğrulama
1. Doğrula'ya tıklayın.
    * Tüm bağlamaların doğru yapıldığından emin olmak için yeni eşlemeyi doğrulayın.  
2. Sayfayı kapatın.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Biçim yapılandırmasının geçerli sürümünün durumunu değiştirin
Sonraki adımlarda, biçim yapılandırmasının durumunu Taslak yerine Tamamlandı olarak değiştirerek ödeme belgesi oluşturmada kullanılabilir hale getirin.  
1. Durumu değiştir öğesine tıklayın.
2. Tamamla öğesine tıklayın.
3. Açıklama alanına bir değer girin.
    * Örneğin, "sürüm 1".  
4. Tamam'a tıklayın.
5. Geçerli yapılandırmanın tamamlanan sürümünü seçin.
    * Yapılandırmanın, tamamlanan sürüm 1.1 (veri modelinin sürüm 1'ini temel alan biçimin sürüm 1'i) olarak kaydedildiğine dikkat edin.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Tamamlanan biçiminin sürümü için yürürlük tarihi tanımla
Her biçimi sürümü belirli bir tarihten itibaren kullanılabilecek şekilde yapılandırılabilir. Belirli bir tarihte birden fazla biçim sürümü etkin olduğunda, kullanım için en son biçim (sürüm numarasına bağlı olarak) seçilir. Uygun sürüm seçimi için oturum tarihi değeri kullanılır.  

## <a name="restrict-access-to-created-format-from-companies"></a>Oluşturulan biçime şirketlerden erişimi kısıtlama
1. ISO Ülke/bölge kodları bölümünü genişletin.
    * Her biçim erişimi, biçimin geçerli olacağı ülke/bölgeleri tanımlayarak kısıtlanabilir. Belirli biçim için ülkeler/bölgeler listesi boş olduğunda, bu biçim herhangi bir şirkette kullanılabilir. Bazı ISO ülke/bölge kodları ülkeler/bölgeler listesine eklendiğinde, bu biçim yalnızca birincil adresi ülke/bölge listesinde olan şirketlerde kullanılabilir.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]