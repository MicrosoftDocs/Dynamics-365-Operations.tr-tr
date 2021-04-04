---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (2 Aralık 2020)
description: Bu konuda, 2 Aralık 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 89c5dbab58679dfe36f5eec0d6c5724f81c18523
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463466"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (2 Aralık 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya bakın](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3788 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Pozisyonlar için işe alma istekleri gönderebilme yöneticileri | [Pozisyonlar için işe alma istekleri gönderebilme yöneticileri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [İşe alma isteği Ekle](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Personel yönetiminde geliştirilmiş aday profili | [Personel yönetiminde geliştirilmiş aday profili](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Aday profili ekleme veya düzenleme](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir | [İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [İş adaylarını işe alma](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Yönetici self servisindeki özel bağlantılar | [Yönetici self servisindeki özel bağlantılar](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Yönetici self servisindeki özel bağlantılar](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış | Tanım |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult, işlemde kullanılan tarih/saati içermelidir. | BenefitEligibity işleme sonucu şimdi eksik olan son işleme için DateTimeStamp 'ı içeriyor. |
| 526903 | **İnsan kaynakları paylaşılan parametrelerinde** **Görevlileri otomatik olarak seç** açık olduğunda bağımlıları olan planlar için kazanç kaydı başarısız olur . | **Görevlileri otomatik olarak seç** seçeneği varsayılan olarak etkinleştirilmiş durumdayken, ayrıcalık kaydının bağımlı tehlikeleri için başarısız olduğu sorun düzeltildi. |
| 521922 | **Ayrıntı olmadan devamsızlığı göster** parametresi, ekip devamsızlık takviminde zaman aşımı isteklerinin ayrıntılarını gösterir. | **İzin ve devamsızlık parametrelerinde**, **ayrıntı olmadan izni göster**'i **Evet** olarak ayarladığınızda, izin türü, tür rengi ve gün ayrıntıları ekip devamsızlık takviminde gösteriliyor . Bu giderilmiştir ve şimdi bırakma türü görüntülenmez ve ekip devamsızlık takviminde tüm izin türleri için varsayılan bırakma türü rengi (koyu mavi) kullanılır. |
| 527316 | İş, konum ve çalışan bildirimleri için başlık değişiklikleri eşitlenmez. | Daha önceden İş, Pozisyon ve çalışan varlıklara eklenen bir başlık ilişkisi. Bu ilişkinin eşitlenmesi İnsan Kaynakları'ndan Dataverse'e itibaren eşitleme için çalışır ancak Dataverse'den bildirimler için çalışmadı. Bu giderildi. |
| 512275 | **İzin ve devamsızlık parametrelerinden** renk seçeneklerini kaldırın. | Artık izin türü üzerinde renkler tanımlanmış olduğundan, **izin ve devamsızlık parametrelerinde** renkler seçeneklerinin kaldırılmış olması için artık gerekli değildir . |
| 437112 | Çalışan pozisyonu ataması sırasında yanıltıcı hata iletisi metni. | Bir çalışanı işe alırken ve çalışanı etkin olmayan bir konuma atamaya çalışırken hata iletisi güncelleştirildi. Güncelleştirilmiş ileti **Belirtilen pozisyon işe başlangıç tarihi itibariyle etkin değil. Lütfen bu pozisyonun süresini denetleyin.** |
| 527816 | **İzin** sayfası ile ilgili performans sorunları. | **İzin** sayfası zamanı geçen zamanda artırıldı. |
| 523158 | BenefitPeriodMigrationUpgrade ve BenefitPlanMigrationUpgrade çalışmıyor. | **Dönem** ve **plan** doğru olarak yürütülmediğinden ilgili kazanç geçişi işlerine yönelik sabit sorunlar. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| Geliştirilmiş iş akışı istekleri ve onaylar | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| LinkedIn Talent Hub ile tümleştirme | [LinkedIn Talent Hub ile tümleştirme](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub ile tümleştirme](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Şirketler arası Yöneticiler şirket içi görünümü | [Şirketler arası Yöneticiler şirket içi çalışan izni görünümü](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [İzin ve devamsızlık parametrelerini yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Denge görünümü konusunda ek bilgiler sunma| [Denge görünümü konusunda ek bilgiler sunma](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Personel iznini yönetme](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Pozisyonlar için işe alma istekleri gönderebilme yöneticileri | [Pozisyonlar için işe alma istekleri gönderebilme yöneticileri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [İşe alma isteği Ekle](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Personel yönetiminde geliştirilmiş aday profili | [Personel yönetiminde geliştirilmiş aday profili](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Aday profili ekleme veya düzenleme](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir | [İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [İş adaylarını işe alma](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]