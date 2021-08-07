---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (20 Mayıs 2021)
description: Bu konuda, 20 Mayıs 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c7b7f71cf084a05bb0278f5df4ddb022ef3d640f
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560062"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (20 Mayıs 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4189 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Platform güncelleştirmesi 10.0.18 (42) | -- | [Finance and Operations uygulamaların 10.0.18 sürümü için platform güncelleştirmeleri (Mayıs 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Microsoft Teams için İnsan Kaynakları uygulaması artık yarı gün ve günü bölme özelliği tanımlarını destekliyor | -- | [Teams'de izin isteklerini yönetme](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Sorun |  Tanım |
| --- | --- | --- |
| 583776 | Çalışanlara ait toplu kayıtlar yinelenen kayıt hatasına neden oluyor | Bu hata en son sürüm düzeltildi ve toplu izin planı kayıtları başarıyla işleniyor olmalı. |
| 582263 | Tüm çalışanlar için ömür olayı işleme aynı anda çalıştırılamaz | Bir **çalışan** alanı, bir ömür olayı işlemesi için boş bırakıldığında tüm çalışanlar işleme alınır. |
| 558383 | Varsayılan görevli seçilmezse birincil lehdar %100 olarak işaretlenmemiş | Kullanıcının yalnızca birincil lehdarı seçmeniz gerekiyor şekilde hata düzeltildi.|
| 509404 | Departman Kişi sayısı analizi, departman arasındaki çalışanların hareketini dikkate almaz |Analiz, Departmanlar arasında çalışan transferlerini içerecek şekilde güncelleştirilmiştir|
| 579420 | Kılavuzlar özelliğindeki sütunları dondurma özelliği henüz kullanılabilir değildir | **Izgaralar içinde sütunları dondurma** özelliği, İnsan Kaynakları uygulamasında yoktur ve Özellik yönetimi'nde kullanılabilir olarak listeleniyor. Özellik etkinleştirilecek özellikler listesinden kaldırıldı. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazançlar yönetimi uygunluğu kurallarında özel alanlar desteği | [Uygunluk işleme için özel alan desteği](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Uygunluk kurallarını yapılandırma](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| İzin ve devamsızlık iş akışı deneyiminde geliştirmeler | [İzin ve devamsızlık iş akışı deneyiminde geliştirmeler](https://go.microsoft.com/fwlink/?linkid=2147528) | [İzin iste](hr-employee-self-service-request-time-off.md)|
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|
| İzin tahakkuku hareketi denetleme | - | [İzin tahakkuku hareketi denetleme](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
|  Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
