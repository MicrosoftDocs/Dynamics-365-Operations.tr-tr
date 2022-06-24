---
title: Performans incelemeleri oluşturma
description: Bu konu bir performans gözden geçirmenin nasıl oluşturulacağını ve gözden geçirmenin her bölümünün amacını açıklar.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2de087f4e345ba826ddbe8a65f917476bd6894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872195"
---
# <a name="create-performance-reviews"></a>Performans incelemeleri oluşturma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Bu konu bir performans gözden geçirmenin nasıl oluşturulacağını ve gözden geçirmenin her bölümünün amacını açıklar. Bu yordam, USMF demo veri şirketi kullanılarak oluşturulmuştur.

1. Giriş sayfasında **Personel self servisi** çalışma alanını seçin.
2. Yeni bir gözden geçirme oluşturmak için **Yeni inceleme**'yi seçin.
3. **Gözden geçirme türü** alanına bir değer girin veya seçin.
4. **Performans dönemi** alanına bir değer girin veya seçin.
5. **Bitiş tarihi** alanına bir tarih girin.
6. **Tamam**'ı seçin. Gözden geçirmeyi bir şablondan da oluşturabilirsiniz. Her bölüm gözden geçirmeyi başlatmak için gereken bilgileri içereceğinden bu, bir gözden geçirme oluşturmanın en iyi yoludur.  
7. Ekler sekmesi gibi sekmeleri gösterebilir veya gizleyebilirsiniz:

    1. Eylem Bölmesinde, iletişim kutusu menüsünü açmak için **Bölümleri göster**'i seçin.
    1. Ekler sekmesini göstermek veya gizlemek için **Ekleri göster** alanındaki **Evet** ya da **Hayır**'ı seçin.
    1. **Kaydet**'i seçin.

8. Hedef eklemek için **İncelemeye hedef ekle**'yi seçin. Tamamlanınca **Tamam**'ı seçin.
9. Açılır iletişim kutusunu açmak için **Uzmanlık ekle**'yi seçin.
10. **Başlık** alanına bir değer yazın.
11. **Tanım** alanına `Increase customer skills by working with the support team` girin.
12. **Tamam**'ı seçin.
13. **Tümünü daralt**'ı seçin.
14. **Tümünü genişlet**'i seçin.
15. **Yorum ekle**'yi seçin.
16. **Naklet**'i seçin.
17. **Ölçüm** sekmesini seçin.
18. İletişim kutusu menüsünü açmak için **Ölçüm ekle**'yi seçin.
19. **Ölçüm** alanına bir değer girin veya seçin.
26. **Hedef tutar** alanına bir sayı girin.
20. **Tamam**'ı seçin.
21. **Faaliyetler** sekmesini seçin.
22. **Ekle**'yi seçin.
23. **Başlık** alanına bir değer yazın.
24. **Tanım** alanına bir değer girin.
25. **Başlangıç tarihi** alanına bir tarih girin.
26. **Tamamlanma tarihi** alanına bir tarih girin.
27. **Geliştirme planı** alanında **Evet**'i seçin.
28. **Anahtar sözcükler** alanına bir değer yazın.
29. **Kaydet**'i seçin.
30. **Derecelendirmeler** sekmesini seçin.  

    - **Derecelendirme ayrıntıları** Hızlı Sekmesi, çalışanların kendilerini derecelendirmelerini ve yöneticinin çalışanı derecelendirmesini sağlar. Ağırlıklar kullanılırsa puanların ağırlık değeri otomatik olarak hesaplanır.  
    - Bu bölümü görüntülemek için **İnsan kaynakları paylaşılan parametreleri** sayfasında çalışan derecelendirmelerini göstermek üzere parametre ayarlarını etkinleştirin.  

31. **Oturum kapatma işlemleri** sekmesini seçin. Oturumu kapatma işlemleri yalnızca iş akışı tamamlandıktan sonra görüntülenir. İş akışı kullanılmazsa çalışan ve yönetici burada listelenir. Gözden geçirme türü ayarlarına göre **Oturum kapatma işlemleri** için **Gerekli** onay kutusu seçilir.  
32. **Genel** sekmesini seçin.

    - Performans dönemi varsayılan başlangıç ve bitiş tarihlerini oluşturur. Bu tarihler düzenlenebilir.  
    - Durumlar gözden geçirmeye erişimi kontrol eder. **Başlatılmadı** durumu gözden geçirmeyi herkesin görmesine olanak tanır. **İşlemde** durumunu gözden geçirmeyi yalnızca çalışanların görüntülemesine ve düzenlemesine olanak tanır. **Gözden geçirme için hazır**, gözden geçirmeyi yalnızca yöneticinin görüntülemesine ve düzenlemesine olanak tanır. **Son gözden geçirme** durumu, gözden geçirme türünde **Son gözden geçirmede düzenlemeye izin ver** seçeneği belirlenirse çalışanın ve yöneticinin gözden geçirmeyi görüntülemesine ve düzenlemesine olanak tanır. **Tamamlandı** ve **İptal Edildi** durumları gözden geçirmeyi salt okunur hale getirir. Bir gözden geçirme **Reddedildi** durumundaysa ve çalışana geri gönderilirse, hem çalışan hem de yönetici, çalışanın yeniden gönderebilmesi için gerekli düzenlemeleri yapabilir.

33. **Özet** alanına bir değer yazın.
34. **Gözden geçirme** sekmesini seçin. Gözden geçirme durumlar arasında ilerledikçe çalışan ve yönetici her bir hedef veya uzmanlık için yorumlar ekleyebilir.  
35. **Oturum kapatma işlemleri** sekmesini seçin. Çalışan ve yönetici gözden geçirmeyi kapatabilir. Tüm gerekli oturum kapatma işlemleri tamamlandığında durum **Tamamlandı** olarak değişir ve başka değişiklik yapılamaz.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
