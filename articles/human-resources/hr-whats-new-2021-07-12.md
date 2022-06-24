---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 12 Temmuz 2021
description: Bu makalede, 12 Temmuz 2021 için Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 259004773c4e5a7d8865d563da9bcfea3a116632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870972"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 12 Temmuz 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources'da yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4353 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
|  Hizmet yılı görüntüleme geçişi | |Bu özellik, **Kolaylaştırılmış çalışan girişi** sayfasında ve **Kişiler** sayfasında görüntülenen hizmet yılını hesaplamak için farklı tarihler kullanma seçeneği sunar.  Bu, [Human Resources parametreleri](/dynamics365/human-resources/hr-setup-parameters) bölümünde mevcuttur. |


### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası | Sorun |  Açıklama |
| --- | --- | --- |
| 595871 | Human Resources'taki Hakkında bölmesinde yanlış Dataverse terminolojisi var | Common Data Service'in Dataverse olarak yeniden markalanması nedeniyle, Microsoft Dynamics 365 Human Resources bilgi bölmesindeki terminoloji güncelleştirildi (**Yardım ve Destek > Hakkında**). |
| 598676 | Kolaylaştırılmış çalışan giriş formu geçersiz kılma görevi, Kaydedilmiş Görünüm ile kullanıldığında hata oluşturabilir| **Çalışan** sayfasında, "Kolaylaştırılmış Çalışan girişi" özelliği açıksa kaydedilen görünümde **Her zaman düzenleme için açık** ayarlanmışsa uygulama hata verebilir. |
| 592344 |Pozisyondaki çalışan maaşı bölümü yan hak yönetimi etkinleştirildiğinde salt okunur olmalıdır | Çalışan maaşı bilgileri, eski yan hak işlevi kullanılarak oluşturulmuştur.  Yan hak yönetimi etkinleştirildiğinde, alanlar salt okunur olur. Yan hak yönetimi açıldığında ve paylaşılan HR parametrelerinde **Eski yan hak formlarını gizle** **Evet** olarak ayarlandığında, **Çalışan maaşı** sekmesi gizlenir. |
| 598617 | **HcmDiscussion** formu etkinleştirme sekmesi, kişiselleştirmeler uygulandığında sonsuz döngüye neden oluyor | Hem kılavuz hem de ayrıntılar görünümünde **her zaman düzenleme için açık** özelliği açık olduğunda, geçersiz kılınan görev yönteminde sekmeyi etkinleştiren kod, hangi denetime odaklanılması gerektiği konusunda kişiselleştirmeyle çakışır ve sonsuz bir döngü oluşturur. |
| 593553 | Performans günlüğündeki Günlük Tarihi alanı UTC'de gösteriliyor | Performans günlüklerinin **Günlük Tarihi** alanı, sistem tarihi kurulumunda tanımlanan saat dilimi yerine UTC saat diliminde görüntülenir ve bu da bazı saat dilimleri için tarihin yanlış olmasına neden olur. |
| 586930 | Performans hedefleri için açılış etkinlikleri tamamen farklı bir kayıt açıyor | Özellik Yönetimi'nde "Performans Günlükleri genişletilmiş raporlar görünümü" özelliği etkinleştirildiğinde, **Çalışan Self Servisi**'ndeki **Ekibim** sekmesinde genişletilmiş raporlar için performans hedeflerini seçmek, seçili personel yerine bir personelin hedeflerini açıyor. |
| 569959 |  HcmPositionWorkerAssignmentV2 varlığı bir çalışanı pozisyona atamıyor | Varlık üzerinden bir pozisyon atama kaydı eklenirken kullanıcılar hata alır ve yayınlama başarısız olur. |
| 582259 | VETS 4212 raporu 2020 formu yerine 2017 formunu kullanıyor | 2020 biçimine güncelleştirildi.  Yeni biçimi yüklemek için **Rapor yapılandırmaları**'na gidin ve sol sütundaki VETS-4212 raporunu silin. **Elektronik raporlama - Depolar- İK kaynakları**'na gidin ve **Aç**'ı seçin.  **VETS-4212 PDF çıktısı**'nı ve ardından **İçeri Aktar**'ı seçin.|


## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|
|  Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Devamsızlık yöneticisi rolünü yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  İzin türü başına ek gereksinimini yapılandırma | [İzin türü başına ek gereksinimini yapılandırma](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  İzin birimlerini izin türüne göre yapılandır | [İzin birimlerini izin türüne göre yapılandır](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Ödemeye hazır](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Platform güncelleştirmesi 10.0.20 (44) | Platform güncellemesi 10.0.20, 26 Temmuz 2021'de hizmet sürümüyle birlikte kullanıma sunulmaya başlanacak. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.20 sürümü için platform güncelleştirmeleri (Ağustos 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
