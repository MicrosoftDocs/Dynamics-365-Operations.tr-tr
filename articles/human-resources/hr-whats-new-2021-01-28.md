---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (28 Ocak 2021)
description: Bu konuda, 28 Ocak 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fbf3034805146c3900b46f5ccce76e63b0805a4
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893089"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (28 Ocak 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3906 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Yan hak neden kodlarını **Personel yönetimi** çalışma alanına tümleştirme | -- | [Neden kodlarını ayarla](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.


| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 539456 | Takvim, **Ayrıntılar olmadan yalnızca devamsızlığı göster** parametresi etkinleştirildiğinde vurgulu metinde izin türünü gösterir. | **Ayrıntı olmadan yalnızca devamsızlığı göster** seçeneği etkinleştirildiğinde, isteğin tarihi artık vurgulu olarak görüntülenir. |
| 528907 | Çalışan rolündeki bir tüzel kişiliğe erişim izni verilmesi, yöneticilerin Employee Self-Service'in **Takımım** alanında çalışanlar için kalan izin sayısı etkinliğini görememelerine neden olur. |Bu seçeneğin ayarlanması artık yöneticilerin kalan izin etkinliğini görmeye devam etmelerini sağlar. |
| 526280 | HcmWorkerEntity, HcmEmployeeEntity ve HcmContractorEntity varlığında izin hatası. | Sistem dışı yönetici rolündeki kullanıcılar, NationalityCountryRegion alanındaki izin hatası nedeniyle listelenen varlıkları dışarı aktaramadı. Kullanıcılar bu bilgileri vermek için aşağıdaki ayrıcalıklara ihtiyaç duymaya devam edecektir: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain ve HCMContractorEntityView. |
| 542147 | Employee Self-Service aracılığıyla banka hesabı eklerken **Banka hesap numarası** ve **Yönlendirme numarası** alanları zorunludur. | Çalışanların banka hesap bilgilerini eklerken **Banka hesap numarası** ve **Yönlendirme numarası** alanlarını girmelerini gerektiren hatayı düzelttik. Yeni banka hesabı bilgileri kaydedilirken bu alanlar artık zorunlu değildir. |
| 543641 | Posta Kodu elektronik raporlamada doldurulmuyor. | Posta Kodunun L ile Q arasındaki kapsam kodları için ACA raporunda doldurulmadığı hata düzeltildi. |
| 545402 | 404 hatasını kaldırmak için UserBranding.js dosyasına yönelik yönlendirme değişikliği eklendi. | Kullanıcı artık konsolda 404 hatası görmemelidir. |

## <a name="in-preview"></a>Ön izlemede   

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| Şirketler arası Yöneticiler şirket içi görünümü | [Şirketler arası Yöneticiler şirket içi çalışan izni görünümü](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [İzin ve devamsızlık parametrelerini yapılandırma](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Yan hak kayıtları için e-posta onayı | Bu özellik, Employee Self-Service'deki sosyal haklar kayıt deneyiminden çıktığında çalışanlara bir onay e-postası gönderme seçeneği sunar. Bu özellik 1 Şubat'ta kullanıma sunulacak. Daha fazla bilgi için bkz. [Şirket başına Yan haklar yönetimi parametrelerini yapılandırma](hr-benefits-setup-parameters-per-company.md). |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse için terminoloji güncelleştirmeleri

Kasım 2020'den itibaren geçerli olacak şekilde, Common Data Service [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro) olarak yeniden adlandırıldı. Daha fazla bilgi edinmek için Power Apps blogundaki [resmi duyuruya](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) bakın. Bu ad değişikliğiyle birlikte, Dataverse'te bazı terimler güncelleştirildi. Örneğin, artık *varlık* yerine *tablo* ve *alan* yerine *sütun* kullanılmaktadır. Daha fazla bilgi için bkz. [Terminoloji güncelleştirmeleri](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Bu sürümde, Dataverse ile Dynamics 365 Human Resources tümleştirmesine dair terminoloji, bu değişiklikleri yansıtacak şekilde uygulamanın tamamında güncelleştirilmiştir. Örneğin, **Common Data Service tümleştirme** formu artık **Microsoft Dataverse tümleştirme** adını almıştır.

Microsoft Dataverse ile Dynamics 365 Human Resources tümleştirmesi hakkında daha fazla bilgi için bkz. [Microsoft Dataverse tümleştirmesini yapılandırma](./hr-admin-integration-common-data-service.md) ve [Microsoft Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]