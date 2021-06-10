---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 22 Şubat 2021
description: Bu konuda, 22 Şubat 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cac3c188e372521a1f63833cd0032f0e9ff7ebe3
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052397"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 22 Şubat 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3988 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams için Dynamics 365 Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 529994 | **Çalışan** formunda **Bilinen** alanını değiştirmek, bir Dataverse güncelleştirmesini tetiklemez | **Çalışan** formunda **Bilinen** alanı güncelleştirildiğinde Dataverse'ün güncelleştirilmediği bir sorun giderildi. |
| 532651 | Ücret analizi PBI raporu, tüm şirket için ölçümleri hesaplarken para birimi dönüştürmeyi kullanmıyor | Ücret analizi PBI raporunun para birimi dönüşümlerini doğru şekilde yapmadığı bir sorun giderildi. |
| 552226 | Yaşam olayı işleme, tek yaşam olayı için planları birden çok kez kapatır ve yeniden açar  | Bir çalışanın birden çok tüzel kişilikte olduğu ve bir yaşam olayının gerçekleşmesine neden olan sorun giderildi, çalışanın içinde bulunduğu her tüzel kişilik için bir yaşam olayı kaydı oluşturulur. Yaşam olaylarını işlerken, işlenecek tüzel kişilik seçilmelidir. Ancak işleme mantığı kendisini bu tüzel kişilikle sınırlamaz. Bunun yerine, tüm tüzel kişilikler için işler ve seçili tüzel kişilikteki planları kapatır ve yeniden açar. Bu eylem, aynı tüzel kişilikte birden çok kez işlenecek bir yaşam olayıdır ve yaşam olayından etkilenen her planın birden çok kez kapatılmasına/yeniden açılmasına neden olabilir. |
| 518064 | Birden fazla bağımlı, varsayılan görevli olarak işaretlendiğinde uygun planlarda yalnızca bir bağımlı seçiliyor | Uygun planlarda birden çok varsayılan görevlinin otomatik olarak seçilmemesine neden olan sorun çözüldü. Artık kişisel bir ilgili kişi için birincil lehdar da belirleyebilirsiniz. Birden fazla lehdar olduğunda, birincil lehdar uygun planlarda %100 olarak listelenir. |
| 552365 | Platform güncelleştirmesi 40'a yükselttikten sonra kendi veritabanınızı getirme (BYOD) dışa aktarma işleri başarısız oluyor | Platform güncelleştirmesi 40 ortama uygulandıktan sonra BYOD dışarı aktarmalarının başarısız olmasına neden olan sorun çözüldü. |
| 547123 | Panodaki Yapılacaklar listesinde sorgulanacak görev sayısını sınırlama | Yüklenmeye çalışan aşırı sayıda görevin neden olduğu performans sorununu gidermek için Yapılacaklar listesinde gösterilen görev sayısı artık 15 ile sınırlıdır. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Şirketler arası Yöneticiler şirket içi görünümü | [Şirketler arası Yöneticiler şirket içi çalışan izni görünümü](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [İzin ve devamsızlık parametrelerini yapılandırma](./hr-leave-and-absence-parameters.md) |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Çalışanların ilgili kişi bilgilerini düzenlemelerini kısıtlama | [Çalışanların ilgili kişi bilgilerini düzenlemesini kısıtlama](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Kişisel bilgilerin düzenlenmesini kısıtlama](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse için terminoloji güncelleştirmeleri

Kasım 2020'den itibaren geçerli olacak şekilde, Common Data Service [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro) olarak yeniden adlandırıldı. Daha fazla bilgi edinmek için Power Apps blogundaki [resmi duyuruya](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) bakın. Bu ad değişikliğiyle birlikte, Dataverse'te bazı terimler güncelleştirildi. Örneğin, artık *varlık* yerine *tablo* ve *alan* yerine *sütun* kullanılmaktadır. Daha fazla bilgi için bkz. [Terminoloji güncelleştirmeleri](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Bu sürümde, Dataverse ile Dynamics 365 Human Resources tümleştirmesine dair terminoloji, bu değişiklikleri yansıtacak şekilde uygulamanın tamamında güncelleştirilmiştir. Örneğin, **Common Data Service tümleştirme** formu artık **Microsoft Dataverse tümleştirme** adını almıştır.

Microsoft Dataverse ile Dynamics 365 Human Resources tümleştirmesi hakkında daha fazla bilgi için bkz. [Microsoft Dataverse tümleştirmesini yapılandırma](./hr-admin-integration-common-data-service.md) ve [Microsoft Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Hizmet dağıtımı güncelleştirmeleri

22 Şubat 2021 sürümünden itibaren bölgesel hizmet güncelleştirmesi dağıtımımızı düzenliyoruz. Düzenlemeler, global bölgelerin Human Resources hizmeti için güncelleştirmeleri alma sırasını döndürmeyi ve güncelleştirme aşamaları arasındaki bekleme süresinde değişiklikleri içerir. Bu değişiklikler, hizmet kararlılığını, kalitesini ve desteklenebilirliğini artırmak için Güvenli Dağıtım Uygulamaları (SDP) ile daha uyumlu olmamızı sağlar.

İki haftalık dağıtım temposunu uygulamaya devam edeceğiz. Ancak müşteriler güncelleştirmelerin genellikle iki haftalık döngünün önceki sürümlerden farklı bir gününde Human Resources ortamlarına uygulandığını fark edebilir.

Hizmet güncelleştirme işlemi hakkında daha fazla bilgi için [Güncelleştirme işlemi](./hr-admin-setup-update-process.md)'ne bakın.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]