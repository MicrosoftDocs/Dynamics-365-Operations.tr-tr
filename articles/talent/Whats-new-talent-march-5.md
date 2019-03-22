---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (5 Mart 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/08/2019
ms.locfileid: "783037"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (5 Mart 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Talent'daki yeni veya değişen özellikler açıklanmaktadır

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="extending-option-sets-in-attract"></a>Attract'te seçenek kümelerini genişletmek

Attract, Common Data Service (CDS) içinde seçenek kümesi olan birden çok alan vardır. Yeni yeterlilikler, seçenek kümelerini genişletmek için sunulmuştur, **Reddetme** sebep alanı, **İstihdam türü** alanı ve **Kıdem türü** alanı.

> [!IMPORTANT]
> LinkedIn'e iş ilanı verme özelliği, **İstihdam türü** ve **Kıdem türü** alanlarının **İş ayrıntıları** sayfasında kullanılmasını gerektirir. Bu alanlardaki varsayılan değerler, LinkedIn tarafından desteklenir ve iş ilanı verildiğinde görüntülenir. LinkedIn'e iş ilanları veriyorsanız ve mevcut seçenek kümesi değerlerini bu alanlar için değiştiriyorsanız, iş ilanı yine de verilecektir ancak LinkedIn, özel **İstihdam türü** ve **Kıdem türü** değerlerini görüntülemez.

## <a name="changes-in-onboarding"></a>İş almadaki değişiklikler

### <a name="private-preview-for-onboard-teams"></a>İşe alma ekipleri için özel önizleme
Artık şablonları kuruluşunuzun tamamında paylaşabilir ve birlikte çalışabilirsiniz. Daha fazla bilgi için bkz. [İşe Alma Ekipleri kullanarak kuruluşunuzda en iyi deneyimleri paylaşın](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Atama yer tutucuları için özel önizlemeler
Şablonlarınızı etkinlikleri kişilere değil rollere atayarak zenginleştirebilirsiniz. Roller daha sonra kılavuz oluşturma sırasında kişilere atanır. Daha fazla bilgi için bkz. [Kılavuz yönetimini etkinlikleri rollere atayarak hızlandırmak](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler
**Derleme 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>İş akışını, bir İK veya hat yöneticisi izin taleplerini gönderdiğinde veya güncelleştirdiğinde iş akışını otomatik onaylamak ve izlemek için yapılandırın
Yeni iş akışı koşulları, izin taleplerinin bir personel yöneticisi veya İK tarafından otomatik olarak onaylanmasına izin vermek için eklenmiştir. Bir iş akışı üzerinde otomatik onayı başarmanın bir yolu, iş akışı onayı üzerinde otomatik eylemi etkinleştirmektir.

Eklenmiş koşullara şunlar dahildir:

- Gönderen - Talebi iş akışına gönderen kullanıcının sistem kullanıcı kodunu değerlendirmekte kullanılır.
- Adına gönderildi - İzin talebinin, talep ile ilişkili bir çalışan adına mı gönderildiğini değerlendirmekte kullanılır.
- İnsan kaynakları tarafından gönderildi - İş akışına talebi gönderen kullanıcının bir İnsan Kaynakları rolüne sahip olup olmadığını değerlendirmekte kullanılır.
- Yönetici tarafından gönderildi - İzin talebini iş akışına gönderen kullanıcının, talep ile ilişkili çalışanın bir hat hiyerarşi yöneticisi olup olmadığını değerlendirmekte kullanılır.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Gelecekteki konum atamaları için personel sabit ücreti etkinleştir
Personellerin kuruluşa gelecekteki bir başlangıç tarihiyle katılması normaldir. Bu değişiklik, gelecekteki konum atamalarına sahip çalışanlar için sabit ücreti tanımlamaya olanak verir.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Konum Bordro alanları bu konumu düzenlerken boştur
Bu değişiklikle, mevcut konumlara bir değişiklik talebi yapılırsa, bordro alanları şimdi geçerli değerlere varsayılana döner.

### <a name="other-miscellaneous-bug-fixes"></a>Diğer çeşitli hata düzeltmeleri
Bu sürüm ile diğer küçük hata gidermeleri vardır.

### <a name="upgrade-to-cds-for-apps"></a>CDS for Apps'e yükseltin
CDS for Apps'e yükseltme için son tarihler hızla yaklaşmaktadır. PowerApps Yönetim Merkezine oturum açarak veritabanınızın yükseltilmeye ihtiyacı olup olmadığını görün. Son tarihler ve yükseltme için gerekli adımlar hakkında daha fazla bilgi için bkz. [Common Data Service for Apps'e yükseltme](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Çok yakında

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Gelişmiş ücret güvenliği (sabit ve değişken)
Pek çok kuruluşta, ücret ve kazanç yöneticileri yalnızca belirli ücret kayıtlarına erişebilirler; örneğin yöneticiler için kayıtlar veya yerel tabanlı personeller gibi. Bu değişiklik ile yönetimini değiştirebilir ve ücret planlarını kuruluş içindeki farklı personel popülasyonları için korur. Sabit ve değişken planlar, güvenlik rollerine atanabilir, bunlar planlara ve planlarla ilişkili personel verisine erişimi belirler, örneğin maaş veya ikramiye kayıtları gibi. Yalnızca belirli erişime sahip roller bu çalışanlar için ücreti işleyebilirler.

###  <a name="platform-update-24"></a>Platform güncelleştirmesi 24
Platform güncelleştirmesi 24 hakkında daha fazla bilgi için bkz. [Finance and Operations platform güncelleştirmesi 24'te (Mart 2019) neler yeni veya değişti](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
