---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 26 Temmuz 2021
description: Bu makalede, 26 Temmuz 2021 için Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
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
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14041dfc753b508a0d68b90ee99d79510d07e622
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070095"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 26 Temmuz 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources'da yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4384 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Platform update 10.0.20 | -- | [Finans ve operasyon uygulamalarının 10.0.20 sürümü için platform güncelleştirmeleri (Ağustos 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası | Sorun |  Açıklama |
| --- | --- | --- |
| 600422 | Ödemeye Hazır seçeneği için bordro adresi doğrulaması başarısız. | Doğrulama, yalnızca "Bordro ikamet konumu" türünde bir adres ve "Bordro iş konumu" türünde bir adres gerektirecek şekilde güncelleştirildi. |
| 601226 | Veri Tümleştirme sorunu: Bordro tümleştirmesi dışarı aktarma projesinde tam gönderim seçeneği yoktur | Ceridian DayForce için bordro tümleştirmesi, tam gönderim yerine artımlı gönderim yapıyordu. Ceridian için her zaman tam yenileme olması gerekir. Bu sorun artık düzeltildiğinden veri dışarı aktarma projesindeki varlıklar artık artımlı gönderime döndürülmeyecektir. |
| 602272 | Çalışan Self Servisi çalışma alanına eklenen kutucuklar şu anda eksik ve kutucuklar artık bu alana eklenemez | Çalışan self servisi için kişiselleştirme sorununu düzelttik. Yeni kutucuklar görünüme eklenebilir ve mevcut kişiselleştirmeler kullanıcılar tarafından görülebilir |
| 600711 | Yarım gün tanımı seçim alanı, tam gün izin istekleri için etkinleştirildi | Bu sorun artık düzeltildi ve yarım gün tanımı alanı yalnızca çalışanlar yarım gün tanımının etkinleştirildiği bir izin türü ve seçilen miktar değeri olarak yarım günü seçtiğinde etkinleştirilir |
| 602208 | Gün yerine saatleri görüntüleyen tahakkuk oranı birimleri | Bu sorun artık düzeltildi. **İzin** formunda, **Tahakkuk oranı** sütunu için doğru izin birimi (saat veya gün) gösterilir. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|
|  Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Bu sürümle, devamsızlık yöneticisi çalışma alanı görünümünü güncelleştiriyoruz. Daha fazla bilgi için bkz. [Devamsızlık yöneticisi rolünü yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  İzin türü başına ek gereksinimini yapılandırma | [İzin türü başına ek gereksinimini yapılandırma](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  İzin birimlerini izin türüne göre yapılandır | [İzin birimlerini izin türüne göre yapılandır](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Ödemeye hazır](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için bkz. [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 2'ye genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

