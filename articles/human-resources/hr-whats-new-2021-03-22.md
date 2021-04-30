---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (22 Mart 2021)
description: Bu konuda, 22 Mart 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b973be365b3afa8461f7709c1ecee835c5dcf2f1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890663"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (22 Mart 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4049 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Takılı toplu işleri iptal etmeye ve sıfırlamaya yönelik seçenek (560976) | NA | [Takılı toplu işleri Sıfırlama](./hr-admin-troubleshooting-batch-execution.md) |
| Yeni kazançlar planı oluşturmak için küçük UX güncelleştirmeleri (419941) | NA | [Bir kazanç planı oluştur](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 554239 | **BusinessProcessTaskAssignment** tablosuyla ilgili varlıklar için performans iyileştirmeleri | Tabloya önerilen dizinleri ekleyerek **BusinessProcessTaskAssignment** tablosuyla ilgili varlıkların performansını artırın. |
| 566061 | Gece eşitlemesinden v2 varlığı geri dönüş kodunu kaldırma | Gecelik Dataverse eşitlemesi için v2 geri dönüş kodunu kaldırın. Geri dönüş artık gerekli değildir ve filtrelenmiş eşitlemenin beklendiği gibi çalışmasını engeller. Bu değişiklik Dataverse veri eşitleme işleminin tutarlılığını geliştirir. |
| 538024 | Çalışan kazanç planları > Hata veren ödemeyi kaldır | Çalışan kazançları formundaki kazanç planı seçeneği için ödeme kaldırılırken oluşan hata giderildi. |
| 557965 | **Kazançlar** çalışma alanı: **etkin yaşam olayları** bağlantısı her zaman **Bağlantılar** bölümünde görünür olmalıdır | **Etkin yaşam olayları** bağlantısının **Bağlantılar** bölümünde görünür olduğu ancak **(Önizleme) kazançlar yönetimi çalışma alanı** özelliğinin etkin olmadığı durumlarda gezinmeye çalışılırken hata oluşturan bir sorun giderildi. Çalışma alanını etkinleştirme hakkında daha fazla bilgi için bkz [Kazançlar yönetimi çalışma alanı](hr-benefits-management-workspace.md). |
| 556672 | Özellik yönetiminde **kolaylaştırılmış çalışan girişi** etkinleştirildiğinde, işi sonlandırılan bir çalışan için tahakkuklar işlenemiyor | İzin ve devamsızlık planlarını tahakkuk etme seçeneği, özellik yönetiminde **kolaylaştırılmış çalışan girişi** etkinleştirildiğinde çalışanlar için **çalışma geçmişi** altındaki **diğer seçeneklere** eklenmiştir. |
| 562656 | **SysRecordChangeLogValidTimeState** menü öğesi **SystemExternalBasicMaintain** güvenlik görevinin bir güvenlik ayrıcalığına ve uzantısına eklenmelidir | Sistem dışı yönetici rollerinde Tarih Yöneticisi formlarındaki **değişiklikleri görüntüle** düğmesi eksik. |
| 505989 | Yaşam olayları işleme: Kullanılan Tarih nedeniyle uygunluk değişikliği doğru işlenmiyor | Uygunluk değişikliğinin işlenmesinin yalnızca geçerli pozisyona değil, başlangıç tarihine de bağlı olduğu sorun giderildi. |
| 562286 | Çalışanın işten çıkarılması, Dataverse'e birden fazla güncelleştirme gönderiyor | Bir çalışan işten çıkarıldığında Dataverse'e birden fazla güncelleştirme işlemi gönderiliyor ve aynı değişiklik için iki güncelleştirme bildiriminin gönderilmesine neden oluyor. Bir Power Automate akışı, eylemden tetiklenecek şekilde yapılandırılmışsa birden fazla tetikleyiciye neden olabilir. |
| 527340 | İzin ve devamsızlık kayıtlarını açarken "gösterilemeyen DateTime" hatası görüntüleniyor | Bir İzin ve Devamsızlık kaydı seçerken, hata artık görüntülemez. |
| 561663 | Küme sağlama için bekleme zaman aralığını artırma | Altyapı kararlılığını ve sağlama tutarlılığını, Küme sağlama güncelleştirmeleriyle geliştirin. |
| 486129 | **Konumlar > Değişiklikleri yönet** özel alanları düzenlenemiyor | **Konumlar** için **değişiklikleri Yönet** sekmesinde özel alanların düzenlenemediği bir sorun düzeltildi. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Çalışanların ilgili kişi bilgilerini düzenlemelerini kısıtlama | [Çalışanların ilgili kişi bilgilerini düzenlemesini kısıtlama](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Kişisel bilgilerin düzenlenmesini kısıtlama](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]