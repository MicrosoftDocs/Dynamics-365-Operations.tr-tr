---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (2 Aralık 2020)
description: Bu makalede, 2 Aralık 2020 için Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cecef6d2e73b42126b1be100dca52ebd8d9270fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848121"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (2 Aralık 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources'da yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3788 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Pozisyonlar için işe alma istekleri gönderebilme yöneticileri | [Pozisyonlar için işe alma istekleri gönderebilme yöneticileri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [İşe alma isteği Ekle](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Personel yönetiminde geliştirilmiş aday profili | [Personel yönetiminde geliştirilmiş aday profili](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Aday profili ekleme veya düzenleme](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir | [İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [İş adaylarını işe alma](./hr-personnel-recruit.md) |
| Yönetici self servisindeki özel bağlantılar | [Yönetici self servisindeki özel bağlantılar](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Yönetici self servisindeki özel bağlantılar](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası | Sorun | Açıklama |
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
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| Geliştirilmiş iş akışı istekleri ve onaylar | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| LinkedIn Talent Hub ile tümleştirme | [LinkedIn Talent Hub ile tümleştirme](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub ile tümleştirme](./hr-admin-integration-linkedin.md) |
|Şirketler arası Yöneticiler şirket içi görünümü | [Şirketler arası Yöneticiler şirket içi çalışan izni görünümü](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [İzin ve devamsızlık parametrelerini yapılandırma](./hr-leave-and-absence-parameters.md) |
|Denge görünümü konusunda ek bilgiler sunma| [Denge görünümü konusunda ek bilgiler sunma](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Personel iznini yönetme](./hr-leave-and-absence-manage-employee-leave.md) |
| Pozisyonlar için işe alma istekleri gönderebilme yöneticileri | [Pozisyonlar için işe alma istekleri gönderebilme yöneticileri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [İşe alma isteği Ekle](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Personel yönetiminde geliştirilmiş aday profili | [Personel yönetiminde geliştirilmiş aday profili](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Aday profili ekleme veya düzenleme](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir | [İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [İş adaylarını işe alma](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 sürüm 2'ye genel bakış](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]