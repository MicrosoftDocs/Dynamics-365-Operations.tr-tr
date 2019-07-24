---
title: Dynamics 365 for Talent'deki yenilikler veya değişiklikler (23 Nisan 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5ec10820761cb22cbff6229babe8a250848214b7
ms.sourcegitcommit: 15154b0aa86110ce5fad6f63e6763103a676a1d2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624593"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-23-2019"></a>Dynamics 365 for Talent'deki yenilikler veya değişiklikler (23 Nisan 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler
Bu sürüm, Dynamics 365 for Talent: Attract için küçük hata düzeltmeleri içerir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler
Bu sürüm, Dynamics 365 for Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler
Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2253 için geçerlidir. Parantez içindeki numaralar Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği
Bu haftaki sürümle, aşağıdaki varlıklar özel alanları destekler: Ücret düzeyi, Kazanç seçeneği, Yetenek türü ve Ücret bölgesi.

### <a name="additional-odata-entities-302992"></a>Ek OData varlıkları (302992)
Şu varlıklar artık OData içinde desteklenir: Çalışanın profesyonel deneyimi ve Çalışan eğitimi.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Yöneticiler ve çalışanlar için performans günlüğü ekleri (308248)
Bu sürümle birlikte artık performans günlüğü girişlerini oluştururken ve güncelleştirirken, Yöneticiler ve çalışanlar için ekler kullanılabilir.

### <a name="employee-rehire-flag-always-available-310047"></a>Çalışan yeniden işe alma bayrağı her zaman kullanılabilir (310047)
Çalışan yeniden işe alma seçeneği artık sonlandırma işleminin dışında güncelleştirme için kullanılabilir. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>**Ödeme yöntemim**'in adı değiştirilemiyor (308815)
**Ödeme yöntemim** etiketinin Çalışan self serviste değiştirilmesine izin vermek üzere kişiselleştirme etkinleştirildi.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Bir Pozisyona karşı Finansal boyutlar silinemiyor (293908)
Mali boyutlar artık varolan bir pozisyon ve şirket sınırları arasındaki mali boyutlar için bir değişiklik talep edildiğinde kaldırılabiliyor. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Müşteri verileri Excel'den açtığında Verileri Talent'a geri yayımlayamıyor (302955)
Bu değişiklik, ilişkili tablolar kullanılırken oluşan bir yayımlama sorununu düzeltir.

## <a name="in-preview"></a>Ön izlemede

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Sebep kodlarının izin türlerinde belirtilmesine izin ver
Kuruluşların izin istekleri hakkında ek bilgilere ihtiyacı olabilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki çeşitli izin türleri için sebep kodları gerektir
Kuruluşlar, bir çalışan izin talebi gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Bu, şirket ilkeleri veya düzenleme gereksinimleri nedeniyle olabilir. Artık hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlayın
Çalışan izni takip etmek ve iznin nasıl hesaplandığını anlamak, yalnızca İK'nın çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda, çalışanlar için doğru izin ödülleri verilmesini sağlar. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece bakiyeler arkasında nedenleri görebilir.

## <a name="coming-soon"></a>Çok yakında

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Yinelenen çalışan denetimi için kullanıcı arabirimi iyileştirmeleri
Bu değişiklikle, isim alanlarını girdiğinizde yinelenenler tespit edilir ve yinelenenlerin sayısını görüntüleyen bir durum gösterilir. Sağlanan bağlantıyı tespit edilen eşleşmeyi kullanıp kullanmamak üzere yeni bir sayfa açmak için seçebilirsiniz. Veri girişinin kesilmesini engellemek için yinelenenler formu otomatik olarak açılmaz.
## <a name="known-issues"></a>Bilinen sorunlar

### <a name="email-support-for-alerts"></a>Uyarılar için e-posta desteği
Platform güncelleştirmesi 26 ile kullanıcılar otomatik olarak, bir etkinlik tarafından tetiklendiğinde e-posta bildirimlerini ilgili kişilere gönderen uyarı kuralları oluşturabilirler.
