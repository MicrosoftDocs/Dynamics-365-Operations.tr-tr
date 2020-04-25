---
title: Dynamics 365 Talent'deki yenilikler veya değişiklikler (16 Nisan 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa61a70e14b7997258376beaf389129a4ad2fa73
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197279"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Dynamics 365 Talent'deki yenilikler veya değişiklikler (16 Nisan 2019)

Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="process-auditing"></a>İşlem denetimi

Artık adaylar, açılan işler veya iş başvurularında yapılan değişiklikleri izleyebilirsiniz. Daha fazla bilgi için bkz. [İşe alım verilerindeki değişiklikleri izleme](process-auditing.md).

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2239 için geçerlidir. Parantez içindeki numaralar Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Common Data Service'taki Ücret bölgesi, Ücret düzeyi, Kazanç seçeneği ve Yetenek türü varlıkları müşteri alanı desteğini içerecek şekilde güncelleştirildi

Bu sürümde, bu Common Data Service varlıkları, Talent: Core HR üzerinden eklenen özel alanı dahil etme yeteneğini içerecek şekilde güncelleştirilmiştir.

### <a name="powerbi-refresh-issues-314342"></a>PowerBI yenileme sorunları (314342)

Bu değişiklik, PowerBI raporlarının doğru şekilde yenilenmesiyle ilişkili bir sorunu düzeltir.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Çalışan self servis'teki geçiş görevleri üzerinden doğrudan tıklama yapılamıyor (303309)

Bu değişiklik, çalışan rolüne sahip kullanıcıların Talent yapılacaklar listesindeki geçiş görevlerini seçmesini ve güncelleştirmesini sağlar.

### <a name="performance-feedback-email-message-updated-309615"></a>Performans geri bildirimi e-posta iletisi güncelleştirildi (309615)

Bu değişiklikle, geribildirim başarıyla gönderildiğinde bir onay iletisi görüntülenir.

### <a name="missing-tables-in-word-template-308048"></a>Word şablonunda eksik tablolar (308048)

Bu değişiklikle, çalışan ve beceri bilgileri içeren bir Word şablonu oluştururken, Word belgesinde yalnızca seçilen çalışanın becerileri görünür.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>İşten çıkarma denetim listesi uygularken bir hata görüntülenir. (299877)

Bu değişiklik, doğrudan çalışan formundan çıkarma denetim listesi uygularken oluşan bir sorunu düzeltir.

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

### <a name="email-support-for-alerts"></a>Uyarılar için e-posta desteği

Finance and Operations Platform güncelleştirmesi 25 ile kullanıcılar otomatik olarak, bir etkinlik tarafından tetiklendiğinde e-posta bildirimlerini ilgili kişilere gönderen uyarı kuralları oluşturabilirler.


