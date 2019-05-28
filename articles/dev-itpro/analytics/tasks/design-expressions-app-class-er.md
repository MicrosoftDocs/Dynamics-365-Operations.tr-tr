---
title: Uygulama sınıfı yöntemlerini çağırmak için ER ifadeleri tasarlama
description: Bu kılavuz, ER ifadelerinde gerekli uygulama sınıfları yöntemlerini çağırarak Elektronik raporlama (ER) yapılandırmalarında mevcut uygulama mantığının nasıl yeniden kullanılabileceğiyle ilgili bilgiler sağlar.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544898"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Uygulama sınıfı yöntemlerini çağırmak için ER ifadeleri tasarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz, ER ifadelerinde gerekli uygulama sınıfları yöntemlerini çağırarak Elektronik raporlama (ER) yapılandırmalarında mevcut uygulama mantığının nasıl yeniden kullanılabileceğiyle ilgili bilgiler sağlar. Sınıfları çağırmak için bağımsız değişkenlerin değerleri, çalışma zamanında dinamik olarak (örneğin, doğruluğunu sağlamak için ayrıştırma belgesindeki bilgiye göre) tanımlanabilir. Bu kılavuzda, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. 

Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir. Ayrıca şu dosyayı indirmeniz ve yerel olarak kaydetmeniz gerekir: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Bu adımları tamamlamak için ilk olarak "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket Litware, Inc. için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.   
    * Bir uygulamanın veri güncelleştirmesi için gelen banka ekstrekerini ayrıştırmak üzere bir işlem tasarladığınızı varsayalım. Gelen banka ekstrelerini IBAN kodlarını içeren TXT dosyaları olarak alacaksınız. Banka ekstresi içe aktarma işleminin bir parçası olarak, halihazırda Dynamics 365 for Finance and Operations içinde bulunan mantığı kullanarak bu IBAN kodlarının doğru olduğunu doğrulamanız gerekir.   

## <a name="import-a-new-er-model-configuration"></a>Yeni bir ER modeli yapılandırmasını içe aktarma
1. Listede, istenen kaydı bulun ve seçin.
    * Microsoft sağlayıcısı kutucuğunu seçin.  
2. Depolar'a tıklayın.
3. Filtreleri göster'e tıklayın.
4. ‘Tür adı’ filtre alanını ekleyin. Ad alanında, "kaynaklar" değerini girin, "içerir" filtre işlecini seçin ve sonra Uygula'ya tıklayın.
5. Aç'a tıklayın.
6. Ağaçta 'Ödeme modeli' seçin.
    * Sürümler hızlı sekmesindeki İçe aktar düğmesi etkinleştirilmemişse, ER yapılandırma 'Ödeme modeli'nin bir sürüm 1'inin zaten içe aktarmışsınızdır. Bu alt görevdeki kalan adımları atlayabilirsiniz.   
7. İçe aktar'ı tıklatın.
8. Evet'i tıklatın.
9. Sayfayı kapatın.
10. Sayfayı kapatın.

## <a name="add-a-new-er-format-configuration"></a>Yeni bir ER biçim yapılandırması ekleme
1. Raporlama konfigürasyonları'na tıklayın.
    * TXT biçimindeki gelen banka ekstrelerini ayrıştırmak için yeni bir ER biçimi ekleyin.  
2. Ağaçta 'Ödeme modeli' seçin.
3. İletişim menüsünü açmak için Yapılandırma oluştur'a tıklayın.
4. Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.
5. Ad alanına, 'Banka ekstresi içe aktarma biçimi (örnek)' yazın.
    * Banka ekstresi içe aktarma biçimi (örnek)  
6. Veri içe aktarmayı destekler alanında Evet'i seçin.
7. Konfigürasyon oluştur'u tıklatın.

## <a name="design-the-er-format-configuration---format"></a>ER biçimi yapılandırması tasarlama - biçim
1. Tasarımcı'yı tıklatın.
    * Tasarlanan biçim, harici dosyanın TXT biçimindeki beklenen yapısını gösterir.  
2. İletişim kutusu menüsünü açmak için Kök ekle'ye tıklayın.
3. Ağaçta, "Metin\Sıra" öğesini seçin.
4. Ad alanına 'Kök' yazın.
    * Kök  
5. Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.
    * 'Özel karakterler' alanında 'Yeni satır - Windows (CR LF)' seçeneği seçilmiştir. Bu ayarı temel alarak, ayrıştırma dosyasındaki her satır ayrı bir kayıt olarak ele alınır.  
6. Tamam'a tıklayın.
7. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
8. Ağaçta, "Metin\Sıra" öğesini seçin.
9. Ad alanına 'Satırlar' yazın.
    * Satırlar  
10. Çokluluk alanında 'Bir fazla'yı seçin.
    * ‘Çok katlılık’ alanında 'Bir çok' seçeneği seçilmiştir. Bu ayara bağlı olarak, ayrıştırma dosyasında en az bir satır sunulması beklenir.  
11. Tamam'a tıklayın.
12. Ağaçta, 'Kök\Satırlar' öğesini seçin.
13. Sıra ekle'ye tıklayın.
14. Ad alanına 'Alanlar' yazın.
    * Alanlar  
15. Çokluluk alanında 'Tam bir'i seçin.
16. Tamam'a tıklayın.
17. Ağaçta, 'Kök\Satırlar\Alanlar' öğesini seçin.
18. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
19. Ağaçta seçin 'Text\String'.
20. İsim alanına 'IBAN' yazın.
    * IBAN  
21. Tamam'a tıklayın.
    * Ayrıştırma dosyasındaki her satırı yalnızca IBAN kodunu içerecek şekilde yapılandırıldı.  
22. Kaydet'e tıklayın.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>ER biçimi yapılandırması tasarlama – veri modeliyle eşleme
1. Biçimi modelle eşle'ye tıklayın.
2. Yeni'ye tıklayın.
3. Tanım alanına 'BankToCustomerDebitCreditNotificationInitiation' yazın.
    * BankToCustomerDebitCreditNotificationInitiation  
4. Tanımı ResolveChanges.
5. Ad alanına 'Veri modeliyle eşleme' yazın.
    * Veri modeline eşleme  
6. Kaydet'e tıklayın.
7. Tasarımcı'yı tıklatın.
8. Ağaçta 'Dynamics 365 for Operations\Sınıf' öğesini seçin.
9. Kök ekle'ye tıklayın.
    * IBAN kodları doğrulaması için mevcut uygulama mantığını çağırmak üzere yeni veri kaynağı ekleyin.  
10. Ad alanına, 'check_codes' yazın.
    * çek kodları  
11. Sınıf alanına 'ISO7064' yazın.
    * ISO7064  
12. Tamam'a tıklayın.
13. Ağaçta, 'biçim' metnini genişletin.
14. Ağaçta, 'biçim\Kök: Sıra(Kök)' öğesini seçin.
15. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)' öğesini seçin.
16. Bağla'ya tıklayın.
17. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)' öğesini genişletin.
18. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)' öğesini genişletin.
19. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)\IBAN: Dize(IBAN)' öğesini seçin.
20. Ağaçta 'Ödemeler = biçim.Kök.Satırlar' öğesini genişletin.
21. Ağaçta, 'Ödemeler = format.Root.Rows\Alacaklı Hesabı(CreditorAccount)' öğesini genişletin.
22. Ağaçta, 'Ödemeler = format.Root.Rows\Alacaklı Hesabı(CreditorAccount)\Kimlik Saptama' öğesini genişletin.
23. Ağaçta, 'Ödemeler = format.Root.Rows\Alacaklı Hesabı(CreditorAccount)\Kimlik Saptama\IBAN' öğesini seçin.
24. Bağla'ya tıklayın.
25. Doğrulamalar sekmesine tıklayın.
26. Yeni'ye tıklayın.
    * Geçersiz IBAN kodu içeren ayrıştırma dosyasındaki herhangi bir satır için bir hata görüntüleyen yeni bir doğrulama kuralı ekleyin.  
27. Koşulu düzenle'ye tıklayın.
28. Ağaçta 'check_codes' öğesini genişletin.
29. Ağaçta, 'check_codes\verifyMOD1271_36' öğesini seçin.
30. Veri kaynağı ekle'ye tıklayın.
31. Formül alanına 'check_codes.verifyMOD1271_36(' yazın.
    * check_codes.verifyMOD1271_36(  
32. Ağaçta, 'biçim' metnini genişletin.
33. Ağaçta, 'biçim\Kök: Sıra(Kök)' öğesini seçin.
34. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)' öğesini genişletin.
35. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)' öğesini genişletin.
36. Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)\IBAN: Dize(IBAN)' öğesini seçin.
37. Veri kaynağı ekle'ye tıklayın.
38. Formül alanına 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)' yazın.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Kaydet'e tıklayın.
40. Sayfayı kapatın.
    * Doğrulama koşulu herhangi bir geçersiz IBAN kodu için ‘ISO7064’ uygulama sınıfının mevcut ‘verifyMOD1271_36’ yöntemini çağırarak YANLIŞ değeri döndürecek şekilde yapılandırılmıştır. IBAN kodu değerinin çalışma zamanında çağırma yönteminin bağımsız değişkeni olarak ayrıştırma TXT dosyası içeri temel alınarak dinamik şekilde tanımlandığını unutmayın.   
41. İletiyi düzenle'ye tıklayın.
42. Formül alanına 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)' girin.
    * CONCATENATE("Geçersiz IBAN kodu bulundu:  ", format.Root.Rows.Fields.IBAN)  
43. Kaydet'e tıklayın.
44. Sayfayı kapatın.
45. Kaydet'e tıklayın.
46. Sayfayı kapatın.

## <a name="run-the-format-mapping"></a>Biçim eşlemeyi çalıştırma
Sınama amacıyla, daha önce yüklediğiniz SampleIncomingMessage.txt dosyasını kullanarak biçim eşlemesi yürütün. Oluşturulan çıktı, seçilen TXT dosyasından içeri aktarılacak verileri içerir ve gerçek içe aktarma sırasında özel veri modelini doldurur.   
1. Çalıştır öğesine tıklayın.
    * Gözat düğmesine tıklayın ve önceden indirdiğiniz SampleIncomingMessage.txt dosyasına gidin.  
2. Tamam'a tıklayın.
    * Seçili dosyadan içeri aktarılan ve veri modeline taşınan verileri temsil eden XML biçimindeki çıktıyı gözden geçirin. İçe aktarılan TXT dosyasındaki yalnızca 3 satırın işlendiğini unutmayın. Satır 4'teki geçersiz IBAN kodu atlandı ve Bilgi günlüğünde bir hata iletisi sağlandı.  

