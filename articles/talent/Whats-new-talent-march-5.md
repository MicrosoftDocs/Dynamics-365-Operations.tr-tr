---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (5 Mart 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 561b6fad0facad86e9a7bc8f36218ab98fcec73c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773277"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (5 Mart 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="extending-option-sets-in-attract"></a>Attract'te seçenek kümelerini genişletmek

Attract, Common Data Service içinde seçenek kümesi olan birden çok alan vardır. Yeni yeterlilikler, seçenek kümelerini genişletmek için sunulmuştur, **Reddetme** sebep alanı, **İstihdam türü** alanı ve **Kıdem türü** alanı.

> [!IMPORTANT]
> LinkedIn'e iş ilanı verme özelliği, **İstihdam türü** ve **Kıdem türü** alanlarının **İş ayrıntıları** sayfasında kullanılmasını gerektirir. Bu alanlardaki varsayılan değerler, LinkedIn tarafından desteklenir ve iş ilanı verildiğinde görüntülenir. LinkedIn'e iş ilanları veriyorsanız ve mevcut seçenek kümesi değerlerini bu alanlar için değiştiriyorsanız, iş ilanı yine de verilecektir ancak LinkedIn, özel **İstihdam türü** ve **Kıdem türü** değerlerini görüntülemez.

## <a name="changes-in-onboarding"></a>İş almadaki değişiklikler

### <a name="private-preview-for-onboard-teams"></a>İşe alma ekipleri için özel önizleme
Artık şablonları kuruluşunuzun tamamında paylaşabilir ve birlikte çalışabilirsiniz. Daha fazla bilgi için bkz. [İşe Alma Ekipleri kullanarak kuruluşunuzda en iyi deneyimleri paylaşın](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Atama yer tutucuları için özel önizlemeler
Şablonlarınızı etkinlikleri kişilere değil rollere atayarak zenginleştirebilirsiniz. Roller daha sonra kılavuz oluşturma sırasında kişilere atanır. Daha fazla bilgi için bkz. [Kılavuz yönetimini etkinlikleri rollere atayarak hızlandırmak](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

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

### <a name="upgrade-to-common-data-service"></a>Common Data Service'a yükseltin
Common Data Service'e yükseltme için son tarihler hızla yaklaşmaktadır. Power Apps Yönetim Merkezi'nde oturum açarak veritabanınızın yükseltilmeye gereksinimi olup olmadığını belirleyin. Son tarihler ve yükseltme için gerekli adımlar hakkında daha fazla bilgi için bkz. [Common Data Service'e yükseltme](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Çok yakında

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Gelişmiş ücret güvenliği (sabit ve değişken)
Pek çok kuruluşta, ücret ve kazanç yöneticileri yalnızca belirli ücret kayıtlarına erişebilirler; örneğin yöneticiler için kayıtlar veya yerel tabanlı personeller gibi. Bu değişiklik ile yönetimini değiştirebilir ve ücret planlarını kuruluş içindeki farklı personel popülasyonları için korur. Sabit ve değişken planlar, güvenlik rollerine atanabilir, bunlar planlara ve planlarla ilişkili personel verisine erişimi belirler, örneğin maaş veya ikramiye kayıtları gibi. Yalnızca belirli erişime sahip roller bu çalışanlar için ücreti işleyebilirler.

###  <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operations için Platform güncelleştirmesi 24
Finance and Operations için Platform güncelleştirmesi 24 hakkında daha fazla bilgi için bkz. [Finance and Operations platform güncelleştirmesi 24'teki yenilikler veya değişiklikler (Mart 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
