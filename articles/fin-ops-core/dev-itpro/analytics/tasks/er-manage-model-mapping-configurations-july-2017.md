---
title: Ayrı ER yapılandırmalarında ER model eşlemesini yönetme
description: Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e59e9f2dd5a0fa6d5955e3d93d25759a478ede7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684439"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>Ayrı ER yapılandırmalarında ER model eşlemesini yönetme

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar. Bu görev kılavuzunda bir örnek şirket olan Litware, Inc. için gerekli ER yapılandırmalarını oluşturacaksınız. Bu görev kılavuzunu tamamlamak için önce "ER Bir yapılandırma sağlayıcısı oluştur ve bunu etkin olarak işaretle" görev kılavuzundaki adımları tamamlamanız gerekir. 

ER yapılandırmalarının şirketler arasında paylaşılması nedeniyle, bu görev kılavuzunu istediğiniz şirketin veri kümesini kullanarak tamamlayabilirsiniz. Bu görev kılavuzunu işlevleri, aşağıdaki düzeltmelerden birini yüklediyseniz kullanılabilir: Dynamics AX 7.0 sürümü için https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 veya Dynamics 365 for Operations sürümü için https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle görev kılavuzundaki adımları tamamlamanız, yapılandırma sağlayıcısı oluşturmanız ve sağlayıcı etkin olarak işaretlemeniz gerekir.   

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

## <a name="add-a-new-er-model-mapping-configuration"></a>Yeni bir ER model eşleme yapılandırması ekleme
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.
3. İsim alanına 'Örnek eşleme' yazın.
    * Örnek eşleme  
4. Konfigürasyon oluştur'u tıklatın.
5. Önkoşullar bölümünü genişletin.
    * Uygulama ön koşulları grubu, otomatik olarak eklenir. Grup, ana veri modeli yapılandırmasına referans gösteren önkoşul bileşenini içerir ve Uygulama olarak işaretlenmiştir. Bu drurum, Örnek eşleme model eşleme yapılandırmasının Örnek veri modelinin uygulaması kabul edildiği anlamına gelir. Bu nedenle, Örnek veri modeli model yapılandırılması indirildiğinde bu bileşen, ER'nin ER deposundan Örnek eşleme model eşleme yapılandırmasını indirmesini sağlayacaktır.   
6. Tasarımcı'ya tıklayın.
    * Oluşturulan model eşleme yapılandırması, oluşturulan yapılandırma ile aynı ada sahip bir boş eşleme içerir. Seçilen bir üst model yapılandırması, model eşlemeleri içeriyorsa bunlar yeni bir model eşleme yapılandırmasına kopyalanır.   
7. Tasarımcı'ya tıklayın.
8. Ağaçta, 'Dynamics 365 for Operations\Tablo' öğesini seçin.
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
    * Bu biçim yapılandırmasını çalıştıran kullanıcının oturum açmış olduğu şirketin adını içeren çıktıyı gözden geçirin. Gerekli model eşlemelerini içeren tek bir yapılandırma mevcut olduğundan, oluşturulan model eşleme yapılandırması bu biçim yapılandırması tarafından kullanılır.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Alternatif bir ER model eşleme yapılandırması ekleme
1. Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.
4. İsim alanında 'Örnek eşleme (alternatif)' yazın.
    * Örnek eşleme (alternatif)  
5. Konfigürasyon oluştur'u tıklatın.
6. Tasarımcı'yı tıklatın.
7. Tasarımcı'yı tıklatın.
8. Ağaçta, 'Dynamics 365 for Operations\Tablo' öğesini seçin.
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

## <a name="use-an-existing-er-model-mapping-configuration"></a>Mevcut bir ER model eşleme yapılandırmasının kullanma
1. Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.
2. Çalıştır'a tıklayın.
    * Çalıştırılan ER biçiminin veri kaynağı olarak seçilen tanımsız veri modeli için birden fazla model eşleme yapılandırması mevcut olduğundan, ER biçimi yapılandırmasının seçili taslak sürümü yürütülemez.   
    * Daha sonra, alternatif model eşleme yapılandırmasını, çalışan ER biçimi için veri kaynakları olarak kullanılacak model eşlemelerinden biri olarak tanımlayacaksınız.   
3. Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.
4. Model eşleme için varsayılan alanında Evet'i seçin.
5. Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.
6. Çalıştır'a tıklayın.
7. Tamam'a tıklayın.
    * Varsayılan model eşleme yapılandırması, bu biçim yapılandırması tarafından elektronik belge oluşturmak için kullanılır (oluşturulan çıktı şirket kodunu içerir).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]