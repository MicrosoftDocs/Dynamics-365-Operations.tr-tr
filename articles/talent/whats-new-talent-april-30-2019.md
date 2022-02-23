---
title: Dynamics 365 Talent'deki yenilikler veya değişiklikler (30 Nisan 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2539baba84bffeb21d351cc307191eea3e940515
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528207"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Dynamics 365 Talent'deki yenilikler veya değişiklikler (30 Nisan 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2270 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="provide-feedback"></a>Geribildirim gönder

Geri bildirim sağlama seçeneği Talent'taki **Yardım** menüsünde (**?**) bulunur. Bu menü aşağıdaki kaynaklara erişim sağlar:

- Bildirim
- Yardım
- Başlayın
- Destek
- Fikirler
- Hakkında

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Yinelenen çalışan tespiti için kullanıcı arabirimi iyileştirmeleri

Bu değişiklik nedeniyle, yinelenen öğeler artık ad alanları ayarladığınız algılanır ve durum göstergesi algılanan yinelenen sayısını gösterir. Sağlanan bağlantı, yinelemelerin birini kullanmanız gerekip gerekmediğini değerlendirilebileceğiniz bir sayfa açar. Veri girişinin kesilmesini engellemek için yinelenenler sayfası otomatik olarak açılmaz. Sayfayı açmak için bağlantıyı seçmeniz gerekir.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği

Bu haftanın sürümünde şu varlıklar artık özel alanları destekliyor: İstihdam, Kazanç türü ve Ödeme döngüsü.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Çıkarma denetim listesi atandığında hata oluşuyor (299877)

Bu değişiklik, bir çalışanı sonlandırma süreci dışında işten çıkarma denetim listesi atadığınızda görüntülenen hata iletisini düzeltir.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Çıkarılan çalışanlar bağlantısı yanlış çalışanı açıyor (309939)

Bu değişiklik, bir çalışanı başka bir tüzel kişilikte yeniden işe aldığınızda ve daha sonra çıkarılan çalışanlar listesinden çalışana gitmeye çalıştığınızda oluşan bir sorunu düzeltir.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Gelişmiş güvenlik özelliği etkinleştirildiğinde, çalışan self servis ücret kartı özet değerleri göstermiyor (315231)

Bu değişiklik, gelişmiş ücret güvenliğini kullandığınızda oluşan bir sorunu düzeltir. Gelişmiş güvenlik açık olduğunda, çalışan self servisi artık hem çalışanlar hem de yöneticiler için özet ücret tutarlarını gösterir. Bu değişiklikten önce, özet değerler 0 (sıfır) olarak görünürdü.

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Common Data Service içinde başlıksız bir pozisyon oluşturulduysa, Talent'ta hiçbir pozisyon oluşturulmuyor (314562)

Bu haftanın değişiklikleri, Common Data Service'ta pozisyonlar oluşturduğunuzda ancak bunlara başlık girmediğinizde oluşan bir sorunu düzeltir.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Çalışan self servis'deki performans günlüğü girişlerinde hata iletisi (314134)

Bu değişiklik, çalışan self servis'deki performans günlüğü girişlerine performans hedefleri iliştirdiğinizde oluşan bir sorunu düzeltir.

## <a name="in-preview"></a>Ön izlemede

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Sebep kodlarının izin türlerinde belirtilmesine izin ver

Kuruluşlar izin istekleri hakkında ek bilgiler gerektirebilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki belirli izin türleri için sebep kodları gerektir

Kuruluşlar, bir çalışan izin talepleri gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Şirket ilkesi veya mevzuat gereksinimleri nedeniyle bu gereksinim bulunabilir. Artık hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlama

Çalışan iznini takip etme ve iznin nasıl hesaplandığını anlama özelliği, yalnızca İnsan kaynaklarının (İK) çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda çalışanlar için doğru izin ödülleri verilmesine yardımcı olur. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece İK personeli bakiyeler arkasındaki nedenleri görebilir.

## <a name="coming-soon"></a>Çok yakında

### <a name="email-support-for-alerts"></a>Uyarılar için e-posta desteği

Finance and Operations için Platform güncelleştirmesi 26'da kullanıcılar otomatik olarak, bildirimler bir etkinlik tarafından tetiklendiğinde e-posta bildirimlerini ilgili kişilere gönderen uyarı kuralları oluşturabilirler.
