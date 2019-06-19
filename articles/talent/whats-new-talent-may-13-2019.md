---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (13 Mayız 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591514"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (13 Mayız 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor

### <a name="job-approvals-on-home-page"></a>Giriş sayfasındaki iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar, iş kodunu, başlığı, diğer onaylayanları ve atanan tarihi görüntüleyen, **size atanan** altında onayları gözden geçirebilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen** işi onaylaması gereken onaylayanları görüntüleyen, size ait işleri gözden geçirebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2297 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="indicate-instance-type-when-provisioning-talent"></a>Talent'ta sağlarken örnek türünü gösterme

Talent'ın yeni bir örneğini sağlarken yeni özelliklerin erken sınanmasına izin vererek örnek türünün **Üretim** veya **Korumalı alan** olduğunu belirtebileceksiniz. Varolan tüm Talent örnekleri **Üretim** örneği türüne güncelleştirilecek. Varolan örneklerden birinin **Korumalı alan** örneği türüne güncelleştirilmesini istiyorsanız, lütfen değişiklik isteğini başlatmak için [Desteğe](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) başvurun.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği

Bu haftaki sürümde şu Common Data Service varlıkları artık özel alanları destekliyor: İş alım, Kazanç hesaplama sıklığı, Kazanç hesaplama oranı, İş takvimi tatili ve Kimlik saptama türü.

### <a name="common-data-service-integration-page"></a>Common Data Service tümleştirme sayfası

Bu sürüm, **Sistem Yönetimi > Bağlantılar > Tümleştirmeler Common Data Service yapılandırması** içinde yeni bir seçenek sağlar. **Common Data Service yapılandırması** seçeneği, bir yönetici veya veri yönetimi yöneticisinin Common Data Service ile esnekliğe sahip olmasını sağlar. Bu seçenekle, Common Data Service tümleştirmesini bir Talent kurulumuyla etkinleştirebilir veya devre dışı bırakabilir ve Talent kurulumu ve Common Data Service arasındaki eşitleme ayrıntılarını görebilirsiniz.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Son çalışan derecelendirmesine sahip performans verilerini içe aktar (316710)

Bu sürümde, geçmişteki çalışan derecelendirme verilerini içe aktarabilirsiniz. **FinalEmployeeRatingId** alanı artık yazma iznine sahiptir.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Common Data Service içinde Çalışan adresi oluşturulamıyor ve bu adres Talent ile eşitlenemiyor (317555)

Bu değişiklik, Common Data Service içinde oluşturulan adres verisinin Talent ile eşitlenmesini sağlar.

## <a name="in-preview"></a>Ön izlemede

### <a name="new-page-to-validate-position-hierarchy-data"></a>Konum hiyerarşisi verilerini doğrulamak için yeni sayfa

İnsan kaynakları (İK) ve yöneticiler yanlışlıkla içe aktarılmış olabilecek herhangi bir döngüsel referans için yönetim hiyerarşisini doğrulayabilir. Bu yeni sayfaya **Kuruluş yönetimi > Bağlantılar > Pozisyonlar > Pozisyon hiyerarşisi doğrulaması** üzerinden erişebilirsiniz.

### <a name="specify-reason-codes-on-leave-types"></a>İzin türlerinde neden kodları belirtme

Kuruluşlar izin istekleri hakkında ek bilgiler gerektirebilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki belirli izin türleri için sebep kodları gerektir

Kuruluşlar, bir çalışan izin talepleri gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Şirket ilkesi veya mevzuat gereksinimleri nedeniyle bu gereksinim bulunabilir. Hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlama

Çalışan iznini takip etme ve iznin nasıl hesaplandığını anlama özelliği, yalnızca İK'nın çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda çalışanlar için doğru izin ödülleri verilmesini sağlar. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece İK personeli, izin bakiyeleri arkasındaki nedenleri görebilir.
