---
title: Dynamics 365 Talent'deki yenilikler veya değişiklikler (9 Nisan 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462883"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Dynamics 365 Talent'deki yenilikler veya değişiklikler (9 Nisan 2019)

Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) ile 'bir problem raporla' entegrasyonu
Attract ve Onboard içinde, sorunlar son kullanıcılar tarafından, bir problem raporla özelliği tarafından kaydedilen sorunlar artık otomatik olarak müşterinin LCS projesinde destek talepleri oluşturur. Yöneticiler, sorunları daha sonra gözden geçirebilir ve ihtiyaç duyulursa Microsoft'a gönderebilir. Bu, Core HR'ın son kullanıcı sorunlarını nasıl el aldığıyla tutarlıdır.

### <a name="relevance-search"></a>İlgi araması
Yetenek havuzlarında, artık tüm aday veritabanınızı belirli yetenekler, adlar veya eğitim arka planı için arayabilirsiniz. Bir adayın profilinin hangi bölümünü aramak istediğinizi belirtmenize artık gerek yoktur. Attract, profilin tamamını arar ve bulunan tüm eşleşmeleri vurgular. Attract ayrıca bir aday için bir aday için mevcut olan tüm belgeleri arar ve arama sonuçlarını akıllıca sıralar. Ek olarak, sonuçları bir kaynak ve bir gümüş madalyalı olup olmadıklarına göre filtreleyebilirsiniz. Daha fazla bilgi için bkz. [Aday profillerini arayın ve görüntüleyin](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles)

### <a name="prospect-recommendations"></a>Aday önerileri
Attract, onu etkileştirmenizle birlikte, kuruluşun aday veri tabanından akıllı aday önerilerini sunarak bir iş için kaynak bulmanıza yardımcı olabilir. Öneriler, ilgili adayları ararken tanımlanmış yetenekleri ve eğitim bilgisinin içerir. Bu öneriler, bir iş altında **Öneriler** sekmesi altında belirir, eğer işin işe alım süreci boyunca etkinleştirirseniz. Daha fazla bilgi için bkz. [Aday önerileri](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Mülakatçı uygunluk durumları
Mülakat zamanlayıcıları yakında **Ofis dışında, başka yerde çalışıyor** durumlarını mülakatçılar için görüntüleyebileceklerdir, bu da mülakatılar için daha uygun zamanlamalar yapmalarına yardımcı olur.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Aday görüşme deneyimi: Takvim davetiyelerini kaydet
Adaylar şimdi mülakat etkinliklerini indirebilir ve kişisel takvimlerine adaya gönderilmiş mülakat özet e-postası .ics dosyası kullanarak kaydedebilirler.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) ile 'bir problem raporla' entegrasyonu
Attract ve Onboard içinde, sorunlar son kullanıcılar tarafından, bir problem raporla özelliği tarafından kaydedilen sorunlar artık otomatik olarak müşterinin LCS projesinde destek talepleri oluşturur. Yöneticiler, sorunları daha sonra gözden geçirebilir ve ihtiyaç duyulursa Microsoft'a gönderebilir. Bu, Core HR'ın son kullanıcı sorunlarını nasıl el aldığıyla tutarlıdır.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler
Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2225 için geçerlidir.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Temel değişken planları yük hatalı tutarı yüzdesi
Bu haftanın sürümü, temel planların yüzdesini kullanırken değişken ücret ikramiyelerini yüklerken bir sorunu giderir.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Son çalışılan gün üzerindeki tarih seçini düzgün çalışmıyor
Bu değişiklik, şu sorunu düzeltir: Kullanıcılar **Çalışma son günü**'nü düzenlediklerinde ve takvim denetimi kullanarak tarihi seçtiklerinde, bir gün seçimlerine eklenir.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Alınan eylem doğrultusunda personel eylemi türlerini sınırlama
Bu değişiklik, belirli spesifik eylemleri gerçekleştirirken eylem türlerini sınırlar. Örneğin, yeni bir pozisyon talep edildiğinde, yalnızca yeni pozisyon simgeleri eylemler listesinde seçilmek üzere belirir. Daha önce, hem yeni hem de düzenle eylemleri belirmekteydi. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Bir personeli bir ücret ile ikinci tüzel varlığa aktarmak
Bu sürüm, aktarma eğer şirketler arası bir aktarmaysa, ikinci tüzel varlıkta ücretlendirmenin sonlandırılmasını destekler.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Bir transfer sırasında gelecekteki çalışma için ücretlendirme seçilemiyor
Bir personel yeni bir tüzel varlığa aktarılırken, yeni tüzel varlık için transfer işlemi sırasında ücretlendirme ayarlayabilirsiniz.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Kullanıcı, pozisyon ataması sırasında ücretlendirme atayamıyor
Artık yeni bir pozisyon ataması eklemek, sabit ücret kayıtlarını ayarlamaya olanak sağlar. 

## <a name="in-preview"></a>Ön izlemede

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Sebep kodlarının izin türlerinde belirtilmesine izin ver
Kuruluşların izin istekleri hakkında ek bilgilere ihtiyacı olabilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki çeşitli izin türleri için sebep kodları gerektir
Kuruluşlar, bir çalışan izin talebi gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Bu, şirket ilkeleri veya düzenleme gereksinimleri nedeniyle olabilir. Artık hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlayın
Çalışan izni takip etmek ve iznin nasıl hesaplandığını anlamak, yalnızca İK'nı çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda, çalışanlar için doğru izin ödülleri verilmesini sağlar. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece bakiyeler arkasında nedenleri görebilir. 

## <a name="coming-soon"></a>Çok yakında

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Yinelenen çalışan denetimi için kullanıcı arabirimi iyileştirmeleri
Bu değişiklikle, isim alanlarını girdiğinizde yinelenenler tespit edilir ve yinelenenlerin sayısını görüntüleyen bir durum gösterilir. Sağlanan bağlantıyı tespit edilen eşleşmeyi kullanıp kullanmamak üzere yeni bir sayfa açmak için seçebilirsiniz. Veri girişinin kesilmesini engellemek için yinelenenler formu otomatik olarak açılmaz.

###  <a name="email-support-for-alerts"></a>Uyarılar için e-posta desteği
Finance and Operations Platform güncelleştirmesi 25 ile kullanıcılar otomatik olarak, bir etkinlik tarafından tetiklendiğinde e-posta bildirimlerini ilgili kişilere gönderen uyarı kuralları oluşturabilirler. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]