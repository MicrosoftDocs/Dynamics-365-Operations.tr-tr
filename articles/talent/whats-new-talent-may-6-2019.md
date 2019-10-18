---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (6 Mayız 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a4571abdb0e104af0a0657c75bf5a6b5764345a
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023873"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (6 Mayız 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="select-optional-documents-upon-offer-creation"></a>Teklif oluşturma üzerine isteğe bağlı belgeleri seçme

Bir teklif paketi şablonu seçtiğinizde, Attract artık o paket şablonundan uygun, isteğe bağlı belgeleri seçmenizi ister. Teklifi hazırlarken başka isteğe bağlı belgeleri de ekleyebilirsiniz.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2282 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="platform-update-26-for-finance-and-operations"></a>Finance and Operations için Platform güncelleştirmesi 26

Finance and Operations için Platform güncelleştirmesi 26 hakkında daha fazla ayrıntı için bkz. [Dynamics 365 Finance and Operations platform güncelleştirmesi 26'daki (Mayıs 2019) önizleme özellikleri](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği

Bu haftaki sürümde şu varlık artık özel alanları destekliyor: Kazanç hesaplama sıklığı, Kazanç hesaplama oranı, Kazanç türü, İş takvimi, İş takvimi tatili, Ödeme döngüsü ve Çalışan tanımlama tipleri.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>İzin toplu kaydı, katman temeli "Kıdem tarihi" olarak değiştirildiğinde başlangıçtaki tahakkuk oranını yenilemiyor (318526)

Çalışanları toplu kaydedip katman temelini değiştirdiğinizde, başlangıç tahakkuku artık seçmiş olduğunuz katman temelini yansıtıyor.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Yinelenen yer tutucuları gösteren iş akışı (313636)

Bu sürümdeki değişiklikler iş akışı bildirimleri gönderildiğinde yer tutucuların yinelenmesini ortadan kaldırır.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>"Excel 'de aç" kullanılırken boyut alanları güncelleştirilmiyor (176261)

Bu sürümle birlikte artık mali boyutları **Çalışan** sayfasından **Excel'de Aç**'ı kullanarak güncelleştirebilirsiniz. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Common Data Service'te oluşturulan çalışan adresi Talent ile eşitlenmiyor (317555)

Bu değişiklikle, Common Data Service'te oluşturulan adresler Talent: Core HR'da güncelleştiriliyor.


## <a name="in-preview"></a>Ön izlemede

### <a name="new-page-to-validate-position-hierarchy-data"></a>Konum hiyerarşisi verilerini doğrulamak için yeni sayfa

İnsan kaynakları (İK) ve yöneticiler artık yanlışlıkla içe aktarılmış olabilecek herhangi bir döngüsel referans için yönetim hiyerarşisini doğrulayabilir. Bu yeni sayfaya **Kuruluş yönetimi > Bağlantılar > Pozisyonlar > Pozisyon hiyerarşisi doğrulaması** üzerinden erişebilirsiniz.

### <a name="specify-reason-codes-on-leave-types"></a>İzin türlerinde neden kodları belirtme

Kuruluşlar izin istekleri hakkında ek bilgiler gerektirebilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki belirli izin türleri için sebep kodları gerektir

Kuruluşlar, bir çalışan izin talepleri gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Şirket ilkesi veya mevzuat gereksinimleri nedeniyle bu gereksinim bulunabilir. Artık hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlama

Çalışan iznini takip etme ve iznin nasıl hesaplandığını anlama özelliği, yalnızca İK'nın çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda çalışanlar için doğru izin ödülleri verilmesini sağlar. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece İK personeli bakiyeler arkasındaki nedenleri görebilir.

## <a name="coming-soon"></a>Çok yakında

### <a name="indicate-instance-type-when-provisioning-talent"></a>Talent'ta sağlarken örnek türünü gösterme

Talent'ın yeni bir örneğini sağlarken yeni özelliklerin erken sınanmasına izin vererek örnek türünün **Üretim** veya **Korumalı alan** olduğunu belirtebileceksiniz. Varolan tüm Talent örnekleri Üretim örneği türüne güncelleştirilecek. Varolan örneklerden birinin Korumalı alan örneği türüne güncelleştirilmesini istiyorsanız, lütfen değişiklik isteğini başlatmak için Desteğe başvurun.
