---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (16 Temmuz 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cd7f288e5c1015f4266db527adfcd62a5dbbc95f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528115"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (16 Temmuz 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler
Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

### <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor
#### <a name="job-approvals-appear-on-the-home-page"></a>Giriş sayfasında görünecek iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar, iş kodunu, başlığı, diğer onaylayanları ve atanan işi görüntüleyen, **size atanan** altında onayları gözden geçirebilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen** işi onaylaması gereken onaylayanları görüntüleyen, size ait işleri gözden geçirebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler
Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler
Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2390 için geçerlidir.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Şu anda özel alanları destekleyen Common Data Service varlıklar

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Yönetici Self Serviste hedefler ve incelemeler denetlenemiyor

Bu haftanın değişiklikleri şimdi yönetim Self Servisteki atlama düzeyi yöneticileri için hedeflerin görüntülenmesine ve düzenlenmesine izin veriyor.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Kullanıcı herhangi bir hedef alanını düzenledikten sonra hedef form kapatılamıyor

Bu sürüm, **Kapat**'ı seçerken hedef formun kapanmayan bir sorunu düzeltir.

### <a name="creating-new-goals-and-saving-displays-error"></a>Yeni hedefler oluşturma ve kaydetme görüntüler hatası

Bu sürüm, hedefleri çalışan ve yönetici self servise kaydederken bir sorunu düzeltir.

### <a name="unable-to-add-a-field-to-position-details"></a>Pozisyon ayrıntılarına alan eklenemiyor 

Bu sürümde, özel alanlar şimdi pozisyon ayrıntılarında desteklenir.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Veri yönetimi aracılığıyla, işitme kodunda kullanım süresi sonu tarihi ayarlanamıyor

Değişiklikler şimdi veri yönetiminde, hazır kodlar üzerinde sona erme tarihleri ayarlamanıza olanak tanır.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Yeni özel alanlar yeterince hızlı eşitlenmedi

Özel alan eşitleme Common Data Service performansı bu haftaki sürümle geliştirilmiştir.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Veritabanı işlerine varlık aktarma şu hata iletisiyle başarısız oldu: "Başlatma dizesinin biçimi 0 dizininde başlayan belirtime uymuyor."

Bu sürüm veritabanı toplu işlerin başarısız olduğu sorunu düzeltir. Manuel olarak güncellemek için:

1. **Veri Yönetimi**'ne gidin.
2. **Varlığı veritabanına aktarmayı yapılandır**'ı seçin.
3. Bağlantı dizesini hedef veritabanına yeniden girin ve **Kaydet**'i seçin.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP e-posta yapılandırması aniden şu hata iletisiyle başarısız oluyor: "SMTP sunucusu güvenli bir bağlantı gerektiriyor veya istemcinin kimliği doğrulanmadı."

Bu sürüm, aniden başarısız olan bir SMTP e-posta yapılandırmasını düzeltir. Manuel olarak güncellemek için:

1. **Sistem yönetimi**'ne gidin.
2. **E-posta parametreleri**'ni seçin.
3. **SMTP ayarları**'nı seçin. 
4. SMTP sunucusu için kullanılan kullanıcı adı ve parolayı yeniden girin ve **Kaydet**'i seçin.

## <a name="in-preview"></a>Ön izlemede

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Önizleme özellikleri yalnızca korumalı alan örneklerinde etkinleştirilir

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün **Üretim** veya **Korumalı alan** olduğunu belirtebilirsiniz. **Korumalı alan** türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Varolan tüm Talent örnekleri **Üretim** örneği türüne güncelleştirilecek. Varolan örneklerden birinin **Korumalı alan** örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için  [Destek](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) başvurun.

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için, bkz [Talent sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>İzin taleplerindeki izin türlerini kısıtlama

Kuruluşlar, çalışanlara birçok farklı türde izin sunabilir. Ancak, çalışanların bazı izin türlerine zaman aşımı istekleri gönderebilmesi için uygun olmayabilir. Bu izin türleri İK tarafından yönetiliyor olabilir. Bu sürümde çalışanların serbest bırakma taleplerini hangi izin türlerine gönderebilecekleri ile ilgili olarak ayarlayabilirsiniz. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Yönetici self-servisindeki doğrudan ve genişletilmiş raporlar için performans bilgilerini görüntüleyin

Yeni bir seçenek, yöneticilerin hem doğrudan raporların hem de genişletilmiş raporlarının performansını görüntülemesine olanak sağlar. Şu anda, satır yöneticileri performans hedeflerini atayabilir ve güncelleştirebilir ve yeni incelemeler yapabilir. Ek olarak, doğrudan yöneticiler ve bunların çalışanları performans gözden geçirme işleminin sorunsuz şekilde devam etmesine yardımcı olmak için performans günlüklerini koruyabilir ve güncelleştirebilir. Bu değişiklik uygulandığında, yöneticiler, kendi talimatlarına ek olarak, genişletilmiş raporlarının performansla ilgili bilgilerini görüntüleyebilir ve koruyabilirler.


[!INCLUDE[footer-include](../includes/footer-banner.md)]