---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler 5 Nisan 2021
description: Bu konuda, 5 Nisan 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 04/05/2021
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
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d91ef244f8dd48baf65f5633357a7d81a68f84621b20d39d4e0ee771283a2bab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741369"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler 5 Nisan 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4074 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Çalışanların ilgili kişi bilgilerini düzenlemelerini kısıtlama | [Çalışanların ilgili kişi bilgilerini düzenlemesini kısıtlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Kişisel bilgilerin düzenlenmesini kısıtlama](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 550852 | **Onay** düğmesi, **İnceleme** formunda ayarlanmış zorunlu alanlar ile doğrulama yapmıyor. | **İnceleme** formunda bir alanı zorunlu olarak ayarlayıp değişiklikleri Yönetici rolü için yayımladığınızda, form beklendiği gibi doğrulama yapmıyor. |
| 559564 | Sabit maaş değişikliğiyle ilgili geçmişe ait çalışan eylemleri, işten çıkarılan kullanıcılar için hata veriyor. | Çıkarılan çalışanın maaşına ait çalışan eylemi hata veriyor. Bir çalışanın işine son verildikten sonra, işten çıkarılmadan önceki çalışan promosyon eylemi bir hata veriyor. |
| 560074 | İstihdam kategorisi açılır menüsü **Çalışan türü** için filtreleme yapmıyor ve personel ve yükleniciler için kategorileri gösteriyor. | **Personel** formunda, **İstihdam** kategorisi açılan menüsü, personelin çalışan türüne göre, personel veya yüklenici kategorilerini göstermelidir. |
| 567388 | Yeni oluşturulan personele ilişkin bazı bilgiler, Dataverse'deki **cdm_worker** tablosuyla hemen eşitlenmiyor. | Yeni bir personel kaydı oluştururken, yeni kayıt Dataverse'deki **cdm_worker** tablosuyla eşitlenir ancak tüm özellikler Dataverse kaydına dahil edilmiyor. |
| 563837 | Human Resources ekranında bulunmayan özellikler. | Human Resources için geçerli olmayan çeşitli özellikler Özellik yönetiminde görüntüleniyor. Bu özellikler şimdi Human Resources'ta etkinleştirilecek kullanılabilir özellikler listesinden kaldırıldı. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |
| Platform güncelleştirmesi 10.0.17 (41) | Platform Update 10.0.17, 19 Nisan 2021'deki bir sonraki sürüm ile kullanıma sunulmak üzere zamanlanmıştır. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.17 sürümü için platform güncelleştirmeleri (Nisan 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]