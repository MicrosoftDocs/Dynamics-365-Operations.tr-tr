--- 
title: "Elektronik raporlama (ER) için model eşleme yapılandırmalarını yönetme"
description: "Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 65db27e59ce5f9234eeb486efeb9bb6e9dad40f7
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için model eşleme yapılandırmalarını yönetme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar. Bu görev kılavuzunda bir örnek şirket olan Litware, Inc. için gerekli ER yapılandırmalarını oluşturacaksınız. Bu görev kılavuzunu tamamlamak için önce "ER Bir yapılandırma sağlayıcısı oluştur ve bunu etkin olarak işaretle" görev kılavuzundaki adımları tamamlamanız gerekir. 

ER yapılandırmalarının şirketler arasında paylaşılması nedeniyle, bu görev kılavuzunu istediğiniz şirketin veri kümesini kullanarak tamamlayabilirsiniz. Bu görev kılavuzunu işlevleri, aşağıdaki düzeltmelerden birini yüklediyseniz kullanılabilir: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 , Dynamics AX 7.0 sürümü için veya https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 Dynamics 365 for Operations sürümü için.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme görev kılavuzundaki adımları tamamlamanız gerekir.   

## <a name="add-a-new-er-model-configuration"></a>Yeni bir ER model yapılandırması ekleme
1. Raporlama konfigürasyonları'na tıklayın.
    * Yeni bir model yapılandırması ekleme. Adı, yapılandırma ağacında benzersiz olmalıdır.  
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. İsim alanında 'Örnek veri modeli' yazın.
    * Örnek veri modeli  
4. Konfigürasyon oluştur'u tıklatın.
5. Tasarımcı'yı tıklatın.
6. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
7. Ad alanına 'Kök' yazın.
    * Kök  
8. Ekle öğesini tıklatın.
9. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
10. İsim alanına 'Şirket' yazın.
    * Şirket  
11. Ekle öğesini tıklatın.
12. Açıklama alanında kullanıcın çalışma zamanında oturum açtığı metni, tüzel kişiliği veya şirketi girin. 
    * Kullanıcının çalışma zamanında oturum açmış olduğu tüzel kişinin veya şirketin açıklaması.  
13. Kök referansına tıklayın.
14. Tamam'a tıklayın.
15. Kaydet'e tıklayın.
16. Sayfayı kapatın.
17. Durumu değiştir öğesine tıklayın.
18. Tamamla öğesine tıklayın.
19. Tamam'a tıklayın.

## <a name="add-a-new-er-model-mapping-configuration"></a>Yeni bir ER modeli eşleme yapılandırması ekleme
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.
3. İsim alanına 'Örnek eşleme' yazın.
    * Örnek eşleme  
4. Konfigürasyon oluştur'u tıklatın.
5. Önkoşullar bölümünü genişletin.
    * Uygulama önkoşulları grubunun otomatik olarak eklenmiş olduğunu unutmayın. Grup, ana veri modeli yapılandırmasına referans gösteren önkoşul bileşenini içerir ve Uygulama olarak işaretlenmiştir. Bu, Örnek eşleme modeli eşleme yapılandırmasının, veri modeli, Örnek veri modelinin uygulaması olarak kabul edildiği anlamına gelir. Bu nedenle, bu bileşen ER'nin model yapılandırması, Örnek veri modeli indirildiğinde model eşleme yapılandırmasını, bir ER havuzundan indirmesini zorlayacaktır.   
6. Tasarımcı'yı tıklatın.
    * Oluşturulan model eşleme yapılandırmasının, oluşturulan yapılandırma ile aynı ada sahip bir boş eşlemeye sahip olduğunu unutmayın. Seçilen bir ana model yapılandırması, model eşlemeleri içeriyorsa, bunların yeni bir model eşleme yapılandırmasına kopyalanacağını göz önünde bulundurun.   
7. Tasarımcı'yı tıklatın.
8. Ağaçta, 'Dynamics 365 for Operations\Tablo' seçin.
9. Kök ekle'ye tıklayın.
10. İsim alanına 'Şirket' yazın.
    * Şirket  
11. Tablo alanına 'CompanyInfo' yazın.
    * CompanyInfo  
12. Tamam'a tıklayın.
13. Ağaçta, 'Şirket' metnini genişletin.
14. Ağaçta, 'Şirket\find()' öğesini genişletin.
15. Ağaçta, 'Şirket\find()\Ad' öğesini seçin.
16. Bağla'ya tıklayın.
17. Kaydet'e tıklayın.
18. Sayfayı kapatın.
19. Sayfayı kapatın.
20. Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.
21. Kullanıcı parametreleri'ne tıklayın.
22. Çalıştırma ayarları alanında Evet'i seçin.
23. Tamam'a tıklayın.
24. Düzenle öğesine tıklayın.
25. Taslak Çalıştır alanında Evet'e tıklayın.

## <a name="add-a-new-er-format-configuration"></a>Yeni bir ER biçim yapılandırması ekleme
1. Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. Yeni alanına, 'Örnek veri modeli veri modelini temel alan biçim' yazın.
4. İsim alanına 'Örnek biçim' yazın.
    * Örnek biçim  
5. Konfigürasyon oluştur'u tıklatın.
6. Tasarımcı'yı tıklatın.
7. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
8. Ağaçta seçin 'Text\String'.
9. Tamam'a tıklayın.
10. Eşleme sekmesini tıklatın.
11. Ağaçta, 'model'i genişletin.
12. Ağaçta, 'model\Şirket' metnini seçin.
13. Bağla'ya tıklayın.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.
    * Test amacıyla oluşturulan biçimin taslak sürümünü çalıştırın.  
16. Çalıştır öğesine tıklayın.
    * Sürümler hızlı sekmesinde, Çalıştır'ı tıklatın.  
17. Tamam'a tıklayın.
    * Bu biçim yapılandırmasını çalıştıran kullanıcının oturum açmış olduğu şirketin adını içeren çıktıyı gözden geçirin. Oluşturulan modelleme yapılandırmasının bu biçim yapılandırıcısı tarafından, gerekli model eşlemelerini içeren tek bir yapılandırma mevcut olduğu için kullanıldığını unutmayın.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Alternatif bir ER modeli eşleme yapılandırması ekleme
1. Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.
4. İsim alanında 'Örnek eşleme (alternatif)' yazın.
    * Örnek eşleme (alternatif)  
5. Konfigürasyon oluştur'u tıklatın.
6. Tasarımcı'yı tıklatın.
7. Tasarımcı'yı tıklatın.
8. Ağaçta, 'Dynamics 365 for Operations\Tablo' seçin.
9. Kök ekle'ye tıklayın.
10. İsim alanına 'Şirket' yazın.
    * Şirket  
11. Tablo alanına 'CompanyInfo' yazın.
    * CompanyInfo  
12. Tamam'a tıklayın.
13. Düzenle öğesine tıklayın.
14. Ağaçta 'String\CONCATENATE' seçin.
15. Fonksiyon ekle'ye tıklayın.
16. Ağaçta, 'Şirket' metnini genişletin.
17. Ağaçta, 'Şirket\find()' öğesini genişletin.
18. Ağaçta, 'Şirket\find()\Ad' öğesini seçin.
19. Veri kaynağı ekle'ye tıklayın.
20. Formül alanına bir değer yazın.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Ağaçta, 'Şirket\find()\Şirket(DataArea)' öğesini seçin.
22. Veri kaynağı ekle'ye tıklayın.
23. Formül alanına bir değer yazın.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Kaydet'e tıklayın.
25. Sayfayı kapatın.
26. Kaydet'e tıklayın.
27. Sayfayı kapatın.
28. Sayfayı kapatın.
29. Taslak Çalıştır alanında Evet'e tıklayın.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Mevcut bir ER model eşleme yapılandırmasının kullanın
1. Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.
2. Çalıştır öğesine tıklayın.
    * ER biçim yapılandırmasının, çalışan ER biçiminin veri kaynağı olarak seçilen belirtilmemiş veri modelinin birden fazla model eşlemesine sahip olduğu için ER biçim yapılandırmasının taslak sürümünün çalıştırılamayacağını unutmayın.   
    * Daha sonra, alternatif model eşleme yapılandırmasını, çalışan ER biçimi için veri kaynakları olarak kullanılacak model eşlemelerinin tanımlayacaksınız.   
3. Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.
4. Model eşleme varsayılanı alanında, Evet'i seçin.
5. Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.
6. Çalıştır öğesine tıklayın.
7. Tamam'a tıklayın.
    * Varsayılan model yapılandırasının, bu biçim yapılandırması tarafından elektronik belge oluşturmak için kullanıldığını unutmayın (oluşturulan çıktı şirket kodunu içerir).  


