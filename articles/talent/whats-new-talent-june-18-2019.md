---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (Haziran 18 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 06/18/2019
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
ms.search.validFrom: 2019-06-18
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a8b17fbeba591c20253bc4ec66767ac0dea64e6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528087"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-18-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (Haziran 18 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor

### <a name="job-approvals-appear-on-the-home-page"></a>Giriş sayfasında görünecek iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar, iş kodunu, başlığı, diğer onaylayanları ve atanan işi görüntüleyen, **size atanan** altında onayları gözden geçirebilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen** işi onaylaması gereken onaylayanları görüntüleyen, size ait işleri gözden geçirebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2347 için geçerlidir.

### <a name="confirmation-of-course-participants-causes-an-error"></a>Kurs katılımcılarının onayı hataya neden oluyor

Kurs katılımcıları hakkındaki raporu yazdırmak için iletişim kutusu kaldırıldı. Bu rapor, Talent tarafından desteklenmiyor.

### <a name="the-compensation-section-of-the-transfer-worker-page-isnt-available-in-some-scenarios"></a>Çalışan sayfasının Ücret bölümü bazı senaryolarda kullanılamaz

Bu değişiklik, kullanıcıların **Çalışanı transfer et** sayfasını doldururken maaş verilerini girmesini sağlar.

## <a name="in-preview"></a>Ön izlemede

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Önizleme özellikleri yalnızca korumalı alan ortamlarında etkinleştirilecek

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için, bkz [Talent sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün **Üretim** veya **Korumalı alan**. olduğunu belirtebilirsiniz. **Korumalı alan** türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Varolan tüm Talent örnekleri **Üretim** örneği türüne güncelleştirilecek. Varolan örneklerden birinin **Korumalı alan** örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için  [Destek](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) başvurun.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>İzin taleplerindeki izin türlerini kısıtlama

Kuruluşlar, çalışanlara birçok türde izin sunabilir. Ancak, çalışanların bazı izin türlerine zaman aşımı istekleri gönderebilmesi için uygun olmayabilir. Bu izin türleri İnsan kaynakları (İK) tarafından yönetiliyor olabilir. Bu sürümde çalışanların serbest bırakma taleplerini hangi izin türlerine gönderebilecekleri ile ilgili olarak ayarlayabilirsiniz. 

## <a name="coming-soon-in-core-hr"></a>Core HR'da yakında çıkacak

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği

Aşağıdaki varlıklar özel alanları destekleyecektir: Bordro kazanç kodu ve ücret referans noktası. 

### <a name="new-common-data-service-entities"></a>Yeni Common Data Service varlıkları

Neden kodları varlığı Common Data Service'e eklenecek.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Yönetici self-servisindeki doğrudan ve genişletilmiş raporlar için performans bilgilerini görüntüleyin

Yeni bir seçenek, yöneticilerin hem doğrudan raporların hem de genişletilmiş raporlarının performansını görüntülemesine olanak sağlar. Şu anda, satır yöneticileri performans hedeflerini atayabilir ve güncelleştirebilir ve yeni incelemeler yapabilir. Ek olarak, doğrudan yöneticiler ve bunların çalışanları performans gözden geçirme işleminin sorunsuz şekilde devam etmesine yardımcı olmak için performans günlüklerini koruyabilir ve güncelleştirebilir. Bu değişiklik uygulandığında, yöneticiler, kendi talimatlarına ek olarak, genişletilmiş raporlarının performansla ilgili bilgilerini görüntüleyebilir ve koruyabilirler.

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Çalışanlar, Yöneticiler ve İK, bir çalışanın performans incelemesini yazdırabileceklerdir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]