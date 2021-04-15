---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (21 Ocak 2021)
description: Bu konuda, 21 Ocak 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 01/21/2021
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
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14df61a68ed402365bd26257cfc5e9b6b4c14db3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803381"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (21 Ocak 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya bakın](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3866 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Platform güncelleştirmesi 10.0.16(40) | -- | [Finance and Operations uygulamaların 10.0.16 sürümü için platform güncelleştirmeleri (Şubat 2021)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16) |
| Geliştirilmiş iş akışı istekleri ve onaylar | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| 1095-C, Form 1095-B ve eski Yan Haklar'da elektronik raporlama için Uygun Fiyatlı Bakım uyumluluk güncelleştirmeleri | -- | -- | 
| Yan Haklar yönetimi artık ABD merkezlik tüzel kişilikler için ACA uyumluluk raporlamasını desteklemektedir | -- | [Yan Haklar Yönetiminde ACA raporları oluşturma](hr-benefits-management-aca-reports.md) |
| Yan Haklar yönetiminde artık Yan Hak oranı katmanları ve Yan Hak oranı çift katman varlıkları bulunmaktadır  | -- | -- |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 533079 | Kesintilere bakmaya çalıştığımda, gezinti hatası "Form hatalı olarak çağrıldı" alıyorum. | Sosyal haklar kesintilerine **Tarih itibarıyla** görünümünde bakarken oluşan hata düzeltildi. |
| 543641 | Posta Kodu elektronik raporlamada doldurulmuyor.  | Kapsama kodu M ile Q arasında olduğunda, Yan haklar yönetimi için ACA elektronik raporlarında Posta Kodunun görünmediği bir dahili hata düzeltildi. |
| 542815 | Employee Self-Service'teki kişisel ilgili kişi ekranı, çalışanların başkalarının kişisel ilgili kişilerini görmesini sağlar. | Employee Self-Service kişisel ilgili kişileri için **Düzenle** formunun, yalnızca tek bir kişisel ilgili kişinin alınmasını garanti edecek kadar sorguyu kısıtlamadığı ve kullanıcının diğer kişilerin ilgili kişilerini görüntülemek için klavye kısayollarını kullanmasına izin verdiği hata düzeltildi. |
| 536157 | IsVirtualEntityPackageInstalled() çağrısı edeniyle Sistem yönetiminde **Microsoft Dataverse tümleştirmesi** sayfası açılamıyor. | Sorun, **Microsoft Dataverse tümleştirmesi** sayfasının Human Resources'da yüklenmesini engelliyor. |
| 533079 | Kesintilere bakmaya çalıştığımda, gezinti hatası "Form hatalı olarak çağrıldı" alıyorum. | **Şu tarihten itibaren** görüntülendiğinde Yan haklar yönetimi için **Kesintiler** formunda oluşan hata düzeltildi. |
| 537264 | Aday kaydında **kişisel bilgiler** hızlı sekmesi eksik. | Aday için kişisel bilgiler artık aday kaydı üzerinde kullanılabilir. |
| 537267 | **Profesyonel deneyim**, dahili aday kayıtlarında görüntülenmiyor. | **Profesyonel deneyim** hızlı sekmesi artık dahili aday kayıtlarında görüntülenmektedir. Önceden aday şirket içinden ise **Profesyonel deneyim**, adayın kuruluştaki çalışma geçmişi olan **Çalışma geçmişi** ile değiştiriliyordu. Her ikisi de uygulanabilir ve şirket içi adaylar için görüntünmelidir. |
| 537067 | **İşverenle iletişime izin veriliyor** ayarı görüntülenmiyor. | **İşverenle iletişime izin veriliyor** denetimi, aday kaydı için **Profesyonel deneyimi düzenle** bölmesine eklendi. |
| 525957 | Aktarım tamamlandığında, **Aday durumu**, şirket içi adaylarda güncelleştirilmiyor. | Transfer tamamlandığında (**Transfer çalışanını yeni bir pozisyon atama** sayfasında **Pozisyon değiştir** veya **Devam Et** düğmesi seçilidir), aday kaydındaki **Durum**, **İşe Alındı** olarak değiştirilmelidir. |
| 537051 | Hindistan rupisi ve Türk lirası için para birimi simgeleri Dataverse'e doğru olarak eşitlenmiyor | Hindistan rupisi ve Türk lirası simgeleri artık Dataverse'e doğru olarak eşitlenmektedir. |
| 534846 | İşe alma tabloları, Veri Yönetimi için etkinleştirilmelidir. | İşe alma istekleri ve adaylar için oluşturulan yeni tablolar artık Veri Yönetimi için etkindir. Bu, tablolar için değişiklik izlemenin etkinleştirilmesine izin verir ve Dataverse sanal tablolarında OData değişiklik izlemeyi etkinleştirir. |
| 533474 | Eksik Microsoft.SqlServer.XEvent.dll referansı düzeltildi. | Microsoft.SqlServer.XEvent.dll için derleme yükleme özel durumları, bazı ortamlarda Dataverse sanal tabloların ayarlanmalarını engelliyordu. |
| 481122 | **Kişi** çalışma alanı, kullanım dışı pozisyonları gösteriyor. | Kullanımdan kaldırılan pozisyonlar, **Kişiler** çalışma alanında açık pozisyonlar olarak görüntüleniyordu. Kullanımdan kaldırılan pozisyonlar artık görüntülenmemektedir. | 
| 541978 | BaseWorker varlığına birincil e-posta adresi ekleyin. | Bu değişiklik, çalışanın birincil e-posta adresini HcmWorkerBaseEntity varlığına ekledi. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| LinkedIn Talent Hub ile tümleştirme | [LinkedIn Talent Hub ile tümleştirme](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub ile tümleştirme](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Şirketler arası Yöneticiler şirket içi görünümü | [Şirketler arası Yöneticiler şirket içi çalışan izni görünümü](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [İzin ve devamsızlık parametrelerini yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Denge görünümü konusunda ek bilgiler sunma| [Denge görünümü konusunda ek bilgiler sunma](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Personel iznini yönetme](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Pozisyonlar için işe alma istekleri gönderebilme yöneticileri | [Pozisyonlar için işe alma istekleri gönderebilme yöneticileri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [İşe alma isteği Ekle](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Personel yönetiminde geliştirilmiş aday profili | [Personel yönetiminde geliştirilmiş aday profili](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Aday profili ekleme veya düzenleme](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir | [İşe alma sağlayıcılarıyla Basitleştirilmiş tümleştirmeleri etkinleştir](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [İş adaylarını işe alma](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Çok yakında
| Özellik | Ayrıntılı |
| --- | --- |
| Yan hak kayıtları için e-posta onayı | Bu özellik, Employee Self-Service'deki sosyal haklar kayıt deneyiminden çıktığında çalışanlara bir onay e-postası gönderme seçeneği sunar. Daha fazla bilgi için bkz. [Şirket başına Yan haklar yönetimi parametrelerini yapılandırma](hr-benefits-setup-parameters-per-company.md). |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse için terminoloji güncelleştirmeleri

Kasım 2020'den itibaren geçerli olacak şekilde, Common Data Service [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro) olarak yeniden adlandırıldı. Daha fazla bilgi edinmek için Power Apps blogundaki [resmi duyuruya](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) bakın. Bu ad değişikliğiyle birlikte, Dataverse'te bazı terimler güncelleştirildi. Örneğin, artık *varlık* yerine *tablo* ve *alan* yerine *sütun* kullanılmaktadır. Daha fazla bilgi için bkz. [Terminoloji güncelleştirmeleri](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Bu sürümde, Dataverse ile Dynamics 365 Human Resources tümleştirmesine dair terminoloji, bu değişiklikleri yansıtacak şekilde uygulamanın tamamında güncelleştirilmiştir. Örneğin, **Common Data Service tümleştirme** formu artık **Microsoft Dataverse tümleştirme** adını almıştır.

Microsoft Dataverse ile Dynamics 365 Human Resources tümleştirmesi hakkında daha fazla bilgi için bkz. [Microsoft Dataverse tümleştirmesini yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) ve [Microsoft Dataverse sanal tablolarını yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]