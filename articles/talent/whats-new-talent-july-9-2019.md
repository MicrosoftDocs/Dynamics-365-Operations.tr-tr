---
title: Dynamics 365 for Talent'taki yenilikler veya değişiklikler (9 Temmuz 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e5bb02a7128cb920a79a5f04ac910be205aeed41
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856389"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-9-2019"></a>Dynamics 365 for Talent'taki yenilikler veya değişiklikler (9 Temmuz 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içerir.

### <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor
#### <a name="job-approvals-appear-on-the-home-page"></a>Giriş sayfasında görünecek iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar, iş kodunu, başlığı, diğer onaylayanları ve atanan işi görüntüleyen, **size atanan** altında onayları gözden geçirebilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen** işi onaylaması gereken onaylayanları görüntüleyen, size ait işleri gözden geçirebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2374 için geçerlidir.

### <a name="platform-update-28"></a>Platform güncelleştirmesi 28

Platform güncelleştirmesi 28 hakkında daha fazla ayrıntı için bkz. [Dynamics 365 for Finance and Operations önizleme özellikle platform güncelleştirmesi 28 (Temmuz 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Common Data Service'teki özel alanlar için varlık desteği 

Özel alanları destekleyen varlıklar aşağıdadır: 

- **Maaş sabit planı**
- **Ücret referans noktası ayarı**
- **Ücret referans noktalarını ayar çizgisi**
- **Bordro kazanç kodu**
- **Ödeme dönemi**
- **Sabit ücret etkinliği**
- **Ücret kılavuzu**

Talent içindeki tüm güncelleştirilmiş varlıkları görüntülemek için:

1. **Sistem Yönetimi**'ni seçin, **Bağlantılar**'ı seçin ve sonra **Common Data Service konfigürasyonu**'nu seçin.
2. **CD varlık adı** açılır menüsünü seçin. Listelenen tüm varlıklar en son sürümde. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Common Data Service içindeki çalışan varlığına tam ad eklendi

**Tam ad** alanı, **Çalışan** varlığına eklendi.

### <a name="full-time-equivalent-higher-than-10"></a>Tam zamanlı eşdeğer 1,0'dan fazla

Bir uyarı, bir pozisyondaki tam zamanlı çalışan için 1,0'dan büyük bir değer girilirse görüntülenir. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Çalışan gelecek tarihli çalışma olmadığında bir uyarı artık alt sayfada görüntülenmez

**Personel yönetimi** çalışma alanındaki **Çıkan çalışanlar** listesinden **Çalışan**  sayfasına giderken gelecekteki bir işe ait olduğunu belirten bir ileti almazsınız. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Talent'ta verilen iş süreci silinemiyor

Etkin iş süreçlerini **İş süreci** çalışma alanında silebilirsiniz.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Tahakkuk süresi boyunca bakiyeyi kullanırken, bakiyesi olmayan planlar için artık bakiyeyi sıfır görüntülemez

Sıfır tahakkuk ile ayarlanan planlar şimdi bir bakiye gösterebilir.

## <a name="in-preview"></a>Ön izlemede

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Önizleme özellikleri yalnızca korumalı alan örneklerinde etkinleştirilir

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün **Üretim** veya **Korumalı alan** olduğunu belirtebilirsiniz. **Korumalı alan** türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Varolan tüm Talent örnekleri **Üretim** örneği türüne güncelleştirilecek. Varolan örneklerden birinin **Korumalı alan** örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için  [Destek](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) başvurun.

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için, bkz [Talent sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>İzin taleplerindeki izin türlerini kısıtlama

Kuruluşlar, çalışanlara birçok farklı türde izin sunabilir. Ancak, çalışanların bazı izin türlerine zaman aşımı istekleri gönderebilmesi için uygun olmayabilir. Bu izin türleri İK tarafından yönetiliyor olabilir. Bu sürümde çalışanların serbest bırakma taleplerini hangi izin türlerine gönderebilecekleri ile ilgili olarak ayarlayabilirsiniz. 

## <a name="coming-soon-in-core-hr"></a>Core HR'da yakında çıkacak

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Yönetim self servisinde performans için genişletilmiş bilgileri görüntüle

Yeni bir seçenek, yöneticilerin hem doğrudan raporların hem de genişletilmiş raporlarının performansını görüntülemesine olanak sağlar. Şu anda, satır yöneticileri performans hedeflerini atayabilir ve güncelleştirebilir ve çalışanları birlikte yönetebilecek yeni incelemeler yapabilir. Ek olarak, doğrudan yöneticiler ve bunların çalışanları performans gözden geçirme işleminin sorunsuz şekilde devam etmesine yardımcı olmak için performans günlüklerini koruyabilir ve güncelleştirebilir. Bu değişiklik uygulandığında, yöneticiler, kendi talimatlarına ek olarak, genişletilmiş raporlarının performansla ilgili bilgilerini görüntüleyebilir ve koruyabilirler. 

### <a name="entities-supporting-custom-fields"></a>Özel alanları destekleyen varlıklar

Aşağıdaki varlıklar Common Data Service içindeki özel alanlar için etkinleştirilecek: 

- **İzin türü**
- **Çalışan banka hesabı**
- **İş takvimi**
