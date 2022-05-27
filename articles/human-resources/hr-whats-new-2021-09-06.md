---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 6 Eylül 2021
description: Bu konuda, 6 Eylül 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 314d836db9b7560c2ed95ad1b9d2eba753e39d2b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690596"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 6 Eylül 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasındaki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4443 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
|---|---|---|
| Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Bu sürümde, devamsızlık yöneticisi çalışma alanı görünümünü güncelleştiriyoruz. Daha fazla bilgi için bkz. [Devamsızlık yöneticisi rolünü yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168107). |
| İzin türü başına ek gereksinimini yapılandırma | [İzin türü başına ek gereksinimini yapılandırma](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168108) |
| İzin birimlerini izin türüne göre yapılandır | [İzin birimlerini izin türüne göre yapılandır](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Sorun | Tanım |
|---|---|---|
| 610128 | HcmDiscussionOverallCommentEntity varlığını kullanırken veri yayımlama hatası oluştu | Veriler bir Excel çalışma kitabından HcmDiscussionOverralCommentEntity varlığına yayımlandığında aşağıdaki hata oluşuyor: "HcmTopicOverrall veri kaynağı kayıt türü bulunamıyor" |
| 589073 | EEO-1 raporunda, **Cinsiyet** alanı için "Belirsiz" ve boş değerler "Kadın" değeri olarak sayılır. | **Cinsiyet** alanı için **Erkek** belirtilmezse EEO-1 raporunda varsayılan **Kadın** değeri oluşturulur. |
| 589617 | İzin kartı bakiyesi ve Satın alınabilir ve Satılabilir bakiyeleri, kullanıcı rolleri belirli bir tüzel kişilik için kısıtlandığında görüntülenmez. | Kullanıcı (personel rolü) belirli bir tüzel kişilik için kısıtlanırsa bakiyeler, **İzin Bakiyeleri** kartında ve **Satın alınabilir** ve **Satılabilir** alanlarında doğru şekilde görüntülenmez. |
| 604310 | Kullanıcıya devamsızlık hiyerarşisi atanmadığında Devamsızlık yöneticisi sekmesi gizli olmalıdır. | Belirli bir tüzel kişilik için, şirketler arası parametresi etkinleştirilmedikçe ve kullanıcıyla en az bir devamsızlık hiyerarşisi ilişkilendirilmedikçe self servis portalında **Devamsızlık yöneticisi** sekmesi gizlenmelidir. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özelliklerin nasıl açılıp kapatılacağı hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
|---|---|---|
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md) |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Ödemeye hazır](/dynamics365/human-resources/hr-compensation-payroll) |
| Uygunluk'taki özel alanlar |[Uygunluk işlemede özel alanlar desteği](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Uygunluk işlemede özel alanları kullanma](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Özellik | Ayrıntılı |
|---|---|
| Platform güncelleştirmesi 10.0.21 (45) | Platform güncelleştirmesi 10.0.21'in kullanıma sunulmasının, 4 Ekim 2021'deki hizmet sürümüyle başlaması planlanıyor. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.21 sürümü için platform güncelleştirmeleri (Ekim 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Kazanç beyanı | Personelin geçerli kazanç seçimlerini görüntülemek için kazanç beyanı. Daha fazla bilgi için Sürüm dalgası belgesindeki [Kazanç Beyanı](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) bölümüne bakın. |

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 2'ye genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
