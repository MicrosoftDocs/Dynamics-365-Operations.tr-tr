---
title: Dynamics 365 for Talent'taki yenilikler veya değişiklikler (Haziran 11 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634492"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a>Dynamics 365 for Talent'taki yenilikler veya değişiklikler (Haziran 11 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="search-engine-optimization-for-job-posts"></a>İş gönderilerinin altyapısı iyileştirmeyi arama

Dynamics 365 for Talent'ta **Arama Altyapısı İyileştirmesi**'ni açtıktan sonra: Attract Yönetici merkezi, Attract, yeni bir işi etkinleştirip gönderdiğinizde veya mevcut bir işi güncellediğinizde web sayfasını taraması için Google Dizin Oluşturma uygulaması programlama arayüzünü (API) bilgilendirir. Bu şekilde, iş Google ve diğer arama alt yapılarının arama sonuçlarında görünecektir.

Benzer şekilde, bir işi deftere naklettiğinizde, işlemi deftere nakledilmeyen işin arama sonuçlarında görünmemesi için dizin oluşturma API'sine bildirilir.

> [!NOTE]
> Web gezginlerinin belirli bir zaman çerçevesinde Web sayfalarını gezmesi veya arama sonuçlarını güncelleştirmesi için tanımlı değildir.

## <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor

### <a name="job-approvals-appear-on-the-home-page"></a>Giriş sayfasında görünecek iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar, iş kodunu, başlığı, diğer onaylayanları ve atanan işi görüntüleyen, **size atanan** altında onayları gözden geçirebilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen** işi onaylaması gereken onaylayanları görüntüleyen, size ait işleri gözden geçirebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 for Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2337 için geçerlidir.

### <a name="platform-update-27"></a>Platform güncelleştirmesi 27

Platform güncelleştirmesi 27 hakkında daha fazla ayrıntı için bkz. [Dynamics 365 for Finance and Operations önizleme özellikle platform güncelleştirmesi 27 (Haziran 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Talent'ta özellik yönetimi çalışma alanı

**Sistem yönetimi**'nde bulunan **Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özellikleri görüntülemenizi, etkinleştirmenizi, devre dışı bırakmanızı ve zamanlamanızı sağlar. Varsayılan olarak, bu özellikler kapalıdır. **Özellik yönetimi** çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği

Veren kurum varlığı artık özel alanları destekliyor.

### <a name="new-common-data-service-entities"></a>Yeni Common Data Service varlıkları

Görev grubu varlığı eklendi.

## <a name="in-preview"></a>Ön izlemede

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Önizleme özellikleri yalnızca korumalı alan ortamlarında etkinleştirilecek

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için, bkz [Talent sağlama](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün Üretim veya Korumalı alan olduğunu belirtebilirsiniz. Korumalı alan türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Varolan tüm Talent örnekleri **Üretim** örneği türüne güncelleştirilecek. Varolan örneklerden birinin **Korumalı alan** örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için  [Destek](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) başvurun.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>İzin taleplerindeki izin türlerini kısıtlama

Kuruluşlar, çalışanlara birçok türde izin sunabilir. Ancak, çalışanların bazı izin türlerine zaman aşımı istekleri gönderebilmesi için uygun olmayabilir. Bu izin türleri İnsan kaynakları (İK) tarafından yönetiliyor olabilir. Bu sürümde çalışanların serbest bırakma taleplerini hangi izin türlerine gönderebilecekleri ile ilgili olarak ayarlayabilirsiniz. 

## <a name="coming-soon-in-core-hr"></a>Core HR'da yakında çıkacak

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Yönetim self servisinde rapor performansı hakkında genişletilmiş bilgileri görüntüle

Yeni bir seçenek, yöneticilerin hem doğrudan raporların hem de genişletilmiş raporlarının performansını görüntülemesine olanak sağlar. Şu anda, satır yöneticileri performans hedeflerini atayabilir ve güncelleştirebilir ve yeni incelemeler yapabilir. Ek olarak, doğrudan yöneticiler ve bunların çalışanları performans gözden geçirme işleminin sorunsuz şekilde devam etmesine yardımcı olmak için performans günlüklerini koruyabilir ve güncelleştirebilir. Bu değişiklik uygulandığında, yöneticiler, kendi talimatlarına ek olarak, genişletilmiş raporlarının performansla ilgili bilgilerini görüntüleyebilir ve koruyabilirler.

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Çalışanlar, Yöneticiler ve İK, bir çalışanın performans incelemesini yazdırabileceklerdir.
