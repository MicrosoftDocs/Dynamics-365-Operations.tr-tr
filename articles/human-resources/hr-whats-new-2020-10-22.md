---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 22 Ekim 2020
description: Bu makalede, 22 Ekim 2020 için Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b183ea08a2decc2696ca3bc3997b5cf7f04652d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068076"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 22 Ekim 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu makalede, Dynamics 365 Human Resources'da yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır. Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3680 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Platform güncelleştirmesi 10.0.14(38) | -- | [Finans ve operasyon uygulamalarının 10.0.14 sürümü için platform güncelleştirmeleri (Kasım 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| Kuruluş ve personel yönetimi iş akışları deneyimi geliştirmeleri | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası| Sorun  | Açıklama|
| --- | --- | --- |
| 437922 | DMF varlığı kullanılarak FMLA saatlerinin aktarılması salt okunur bir hatayla sonuçlanır. | Bir FMLA servis talebiyle ilişkilendirilmiş saatleri içe aktarmak için FMLA saat varlığını kullanma başarısız oldu. İçe aktarılan saatlerin servis talebi için kalan saatleri aşmamasını sağlamak amacıyla mantık ekledik. |
| 512019 | Yanlış **son ileri taşıma** miktarı. | **İzin** sayfasında **Başlangıç tarihini** sonraki mali dönemin ilk günü olarak değiştirmek **Yıllık izin** türü için yanlış **son ileri taşıma** tutarı görüntülüyordu. Şimdi doğru tutarı görüntülüyor. |
| 458639 | **Çalışan ilgili kişiler** varlığı değişiklik izleme modunu desteklemiyor. | **Çalışan ilgili kişiler** varlığını kendi veritabanınızı getirin (BYOD) senaryolarında kullanabilmeniz için güncelleştirdik.|
| 505347 | Eğitim yöneticileri, kolay çalışan özelliği etkinleştirildiğinde bir çalışan için izin isteği gönderebilir. | HR asistanı ve HR müdürü dışındaki rollerin çalışanlar için izin istekleri göndermesine izin verilmez. |
| 513490 | Kazanç yönetimi günlüğü: Kapsam seçenekleri olmayan planlar için günlük kaydı ekleyin. | **Kapsam seçeneği olmayan plan** için günlük tutma sonuçları etkinleştirildi. Bunlar artık **işlem sonuçları** tablosunda görüntülenir ve en üstte görüntülenmek üzere doğru sıralanır. |
| 517021 | **Plan türü** her tür için bir kayıt içeriyorsa, aynı **plan türü** koduna sahip birden fazla plan seçilemez. | Yalnızca bir kayda izin verilen planların seçilmesiyle ilgili sınırlamaları değiştirdik. Sınırlamalar, **plan türü** yerine şimdi **plan türü kodu** düzeyindedir. Bu değişiklik, aynı türden olan HSA ve FSA gibi planlara izin verir, ancak bunlara ayrı bir **plan türü kodu** verebilirsiniz. Böylece, aynı kayıt dönemi için her ikisini de seçebilirsiniz. |
| 444791 | Ücret planında **erişimi kısıtla** özelliği açık olduğunda, çalışan self servisinde maaş görüntülenemiyor. | Çalışan self servisi **Ücret** kartında, çalışan **erişimi kısıtla** özelliğinin açık olduğu ve belirli rollere atandığı bir plana kayıtlıysa geçerli ücret tutarı ve zam yüzdesi "0" görünüyordu. Bu sorunu çözdük; böylece çalışan ve yönetici kendilerinin ve bağlı çalışanlarının ücret ayrıntılarını her zaman görebilir. |
| 457542 | Kurs kapatıldıktan sonra kurs ayrıntılarını güncelleştirme, kursu alan çalışan için aynı bilgileri güncelleştirmez. | Kurs ayrıntılarını değiştirdiğinizde artık kurs kapatılıp yeniden açıldığında çalışan bilgileri doğru şekilde güncelleştirilir. |
| 515342 | **CDSLeaveRequestDetailEntity** üzerinden veri eklenemiyor. Şirket bulunamadı veya yok. | Artık **CDSLeaveRequestDetailEntity** üzerinden veri ekleyebilirsiniz. |
| 514743 | Microsoft Exchange kullanılırken **e-posta parametresi** formunda hata oluştu. | E-posta sağlayıcısı **Exchange** olarak ayarlandığında **e-posta parametreleri** sayfasında "Dosyalar veya derleme yüklenemedi..." görüntüleniyordu. Bu düzeltme **e-posta parametreleri** sayfasının beklendiği gibi yüklenmesine ve kaydedilmesine de olanak tanır. |


## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| Geliştirilmiş iş akışı istekleri ve onaylar | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Human Resources için Dataverse'te sanal varlıklar | [Dataverse'te Dynamics 365 Human Resources temel verilerini genişletme](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse sanal varlıklarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md) |
| LinkedIn Talent Hub ile tümleştirme | [LinkedIn Talent Hub ile tümleştirme](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub ile tümleştirme](./hr-admin-integration-linkedin.md) |
| Yönetici self servisindeki özel bağlantılar | [Yönetici self servisindeki özel bağlantılar](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Yönetici self servisindeki özel bağlantılar](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için bkz. [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 sürüm 2'ye genel bakış](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
