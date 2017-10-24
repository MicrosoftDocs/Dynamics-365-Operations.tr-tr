--- 
title: "Elektronik raporlama (ER) için biçim oluştururken veri modeli tanımını seçme"
description: "Bu yordamdaki adımları tamamlamak için öncelikle \"ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme\" yordamını tamamlamanız gerekir."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 70d928b0f0807731a5f96ef5497fb6060fbfebf5
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için biçim oluştururken veri modeli tanımını seçme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlamanız gerekir. 

Bu yordam, elektronik belgeler oluşturmak için tasarlanmış bir Elektronik raporlama (ER) biçimi yapılandırması olarak nasıl bir modeli kök öğesinin bir veri modeli tanımı olarak nasıl seçilebileceğini gösterir. Bu yordamda, 'Litware, Inc.' örnek şirketi için bir ER biçim yapılandırması ekleyeceksiniz. 

Bu yordam Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar içindir. Adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.  
2. Raporlama konfigürasyonları'na tıklayın.

## <a name="add-a-new-er-data-model-configuration"></a>Yeni bir ER veri modeli yapılandırması ekleme
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
    * ER raporları oluşturma için bir veri modeli olarak kullanılacak bir veri modeli içeren yeni bir ER model yapılandırması ekliyoruz.  
2. İsim alanında, 'Ödeme modeli (hayali)' yazın.
    * Ödeme modeli (hayali)  
3. Konfigürasyon oluştur'u tıklatın.
4. Tasarımcı'yı tıklatın.
    * Bu yapılandırmanın veri modelinin yapısını belirtmek için ER tasarımcısını açın.  
    * 2 ödeme yöntemini desteklemek için iş etki alanı için veri modelini tasarladığımızı varsayalım – alacak transferi ve otomatik ödemeler.  
5. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
6. İsim alanında 'Ödemeler – alacak transferi' yazın.
    * Ödemeler – kredi transferi  
7. Ekle öğesini tıklatın.
8. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
9. Yeni düğüm biçimi alanına "Model kökü" girin.
10. İsim alanında 'Ödemeler – hesaptan ödeme' yazın.
    * Ödemeler – otomatik ödeme  
11. Ekle öğesini tıklatın.
12. Kaydet'e tıklayın.
13. Sayfayı kapatın.
14. Durumu değiştir öğesine tıklayın.
    * Yeni model eşlemeleri ve biçimlerinde kullanılabilir hale getirmek için modelin taslak sürümünü tamamlayın.  
15. Tamamla öğesine tıklayın.
16. Tamam'a tıklayın.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Yeni bir ER biçimi yapılandırması girmeye başlayın
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. Yeni alanına, 'Ödemeler modeli (hayali) veri modelini temel alan biçim' yazın.
3. Veri modeli tanımı alanına bir değer girin veya seçin.
    * Seçilen veri modelinin tüm kök maddelerinin bir veri modeli tanımı olarak şu anda kullanılabilir olduğuna dikkat edin. Biçiminizi, veri modelinin gereken maddelerinin herhangi birini kullanarak tasarlamaya devam edebilirsiniz. Seçilen kök maddesi için eksik bir model eşlemesi, çalışmaya devam etmenizi engellemez.  
4. Sayfayı kapatın.

## <a name="add-a-new-er-model-mapping-configuration"></a>Yeni bir ER modeli eşleme yapılandırması ekleme
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. Yeni alanına, 'Ödemeler modeli (hayali) veri modelini temel alan Model Eşleme' yazın.
3. İsim alanında, 'Ödeme modeli eşlemeleri (hayali)' yazın.
    * Ödeme modeli eşlemeleri (hayali)  
4. Veri modeli tanımı alanına bir değer girin veya seçin.
5. Konfigürasyon oluştur'u tıklatın.

## <a name="design-er-model-mappings"></a>ER model eşlemeleri tasarlayın
1. Tasarımcı'yı tıklatın.
    * Gerekli kök maddeleri için model eşlemelerini belirtmek için ER tasarımcısını kullanın.  
2. Tasarımcı'yı tıklatın.
    * Seçilen modelin kök maddesi için seçilen model eşlemesinin ayarının benzetimini yapın.  
3. Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' seçin.
4. Kök ekle'ye tıklayın.
5. Ad alanına 'Genel muhasebe defteri' yazın.
6. Tablo alanına 'LedgerJournalTrans' yazın.
    * LedgerJournalTrans  
7. Tamam'a tıklayın.
8. Kaydet'e tıklayın.
9. Sayfayı kapatın.
10. Sayfayı kapatın.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Başka bir ER biçimi yapılandırması girmeye başlayın
1. Ağaçta 'Ödeme modeli (hayali)' seçin.
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. Yeni alanına, 'Ödemeler modeli (hayali) veri modelini temel alan biçim' yazın.
4. Veri modeli tanımı alanına bir değer girin veya seçin.
    * Şimdi uygulama veri kaynaklarına yalnızca bir kök maddenin kullanılabilir olduğuna dikkat edin. En az bir model eşlemesi eklendiğinde, yalnızca uygulama veri kaynaklarına eşleşmiş olan modelin kök maddelerinin bir ER biçimi eklendiğinde bir model tanımı olarak seçilebileceğini unutmayın.   
5. Sayfayı kapatın.


