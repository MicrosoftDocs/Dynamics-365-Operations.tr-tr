---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 19 Kasım 2021
description: Bu makalede, 19 Kasım 2021 için tek başına çalışan Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886087"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 19 Kasım 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Microsoft Dynamics 365 Human Resources'daki yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için [Dynamics 365 Human Resources 2021 sürümü 2. dalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)'ya bakın.

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4591 uygulanır.

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası | Sorun | Açıklama |
|---|---|---|
| 626178 | **Yönetici self servisinde**, çalışan kutucuğunda gezinti eksik | Bu sorun artık düzeltildi. **Yönetici self servisinde** rapor ayrıntılarını görmek için navigasyon mevcuttur. |
| 632573 | **Kurs** kaydedilirken doğrulama hatası yok | Bu sorun artık düzeltildi. **Minimum katılımcı sayısı** 0'ın üzerinde olan bir kurs oluştururken, **Maksimum katılımcı sayısı** 0 olsa bile kaydedilmesine izin verilir. |
| 615955 | Yeni işe alma isteği konumu oluşturulurken "**Amaç** alanı doldurulmalıdır" hatası. | Yeni bir işe alma isteği konumu için adres oluştururken şu hatayı alırsınız: "'Amaç' alanı doldurulmalıdır." Ancak, **Amaç** alanı sayfada kullanılamaz. |
| 620797 | Boş **Cinsiyet** alan hatası yanıltıcıdır | Kişisel bir ilgili kişi için cinsiyet girilmediğinde, raporda "Metin girmek için buraya tıklayın veya dokunun" ifadesi görüntülenir. Bu, alana hiçbir şey girilemeyeceği için yanıltıcıdır. |
| 620800 | Yan haklar deyim bağlantısı gizli | Yan haklar deyimi, **Employee Self-Service**'te varsayılan olarak görüntülenemez.  **Bağlantılar** bölümünün altında **Employee Self-Service**'in sağ tarafına bir bağlantı eklendi |
| 629778 | CDS tümleştirmesi ile ilgili performans sorunu. | Yetkilendirmeyle ilgili istek performans sorununa neden oldu. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özelliklerin nasıl açılıp kapatılacağı hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
|---|---|---|
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Çok yakında
Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [ Dynamics 365 ve sektör bulutları: 2021 sürümü 2. dalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
