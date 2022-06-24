---
title: Dynamics 365 Human Resources uygulamasındaki yenilikler veya değişiklikler (9 Ağustos 2021)
description: Bu makalede, 9 Ağustos 2021 için Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad1397084dd3eb210065fe6d8c20c5b8253cd206
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882880"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Dynamics 365 Human Resources uygulamasındaki yenilikler veya değişiklikler (9 Ağustos 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Microsoft Dynamics 365 Human Resources'daki yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4393 uygulanır.

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası | Sorun | Açıklama |
| --- | --- | --- |
| 558385 | Varsayılan görevli için **Görevlileri otomatik olarak seç** seçeneği etkinleştirildiğinde varsayılan görevli seçilmiyor. | Bu sorun artık düzeltildi. **Human Resources paylaşılan parametreleri** sayfasındaki **Görevlileri otomatik olarak seç** seçeneği etkinleştirildiğinde birden çok varsayılan görevli uygun planlarda otomatik olarak seçilir. |
| 589617 | Erişim belirli bir şirketle sınırlandırıldığında **İzin süresi** sayfasındaki **Satın alınabilir** ve **Satılabilir** bakiyeleri boş oluyor. | Bu sorun artık düzeltildi. Kullanıcı, belirli bir şirketle sınırlandırıldığında **İzin süresi** sayfası, doğru **Satın alınabilir** ve **Satılabilir** bakiyelerini gösterir. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özelliklerin nasıl açılıp kapatılacağı hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|
| Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Bu sürümde, devamsızlık yöneticisi çalışma alanı görünümünü güncelleştiriyoruz. Daha fazla bilgi için bkz. [Devamsızlık yöneticisi rolünü yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168107). |
| İzin türü başına ek gereksinimini yapılandırma | [İzin türü başına ek gereksinimini yapılandırma](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168108)|
| İzin birimlerini izin türüne göre yapılandır | [İzin birimlerini izin türüne göre yapılandır](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Ödemeye hazır](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Özellik | Ayrıntılı |
| --- | --- |
| Platform güncelleştirmesi 10.0.21 (45) | Platform güncelleştirmesi 10.0.21'in kullanıma sunulmasının, 4 Ekim 2021'deki hizmet sürümüyle başlaması planlanıyor. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.21 sürümü için platform güncelleştirmeleri (Ekim 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 2'ye genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
