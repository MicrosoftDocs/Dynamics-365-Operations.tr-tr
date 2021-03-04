---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (7 Şubat 2020)
description: Bu makalede, 7 Şubat 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fac6e34db10efb047b4cb0fc3c7752330e5bcf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526963"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (7 Şubat 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.2835 uygulanır. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Derslik boş ise, öğrenme analitiği kursu göstermez (388289)

Derslik boş ise, öğrenme Analizi sayfası kursu görüntüler.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Konum arama, saat dilimini hesaba götüremiyor (405344)

Açık pozisyonların aranması şimdi, bir pozisyon açık olduğunda doğrulama sırasında saat dilimini dikkate alır.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Geçerli bakiye analiz görünümü, saat kapalı istekler gönderdikten sonra doğru geçerli çıkış bakiyesiyle güncellemez (409756)

Geçerli bakiye şimdi teslim edilen zaman aşımı taleplerini içermektedir.

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki Önizleme özellikleri 3 Şubat 2020 ' da kullanılabilir:

- **İzin ve devamsızlık önizleme özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- **Kazançlar yönetimi önizleme özelliği** -bilinen sorunlar da dahil olmak üzere daha fazla bilgi için, bkz. [Kazançlar yönetimi önizleme özelliği](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Çok yakında

### <a name="platform-update-32"></a>Platform güncelleştirmesi 32 

Platform Güncelleştirmesi 32 yakında kullanıma sunulacaktır. [Platform Güncelleştirmesi 32 hakkında daha fazla bilgi edinin ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-common-data-service-solution"></a>Common Data Service Çözüm güncellendi

Aşağıdaki değişikliklerle , yeni bir Common Data Service çözüm yakında kullanıma sunulur:

| Tanım | Değiştirme |
| ----------------------------------------- | --- |
| **İş/pozisyon** varlığı değişiklikleri | **Ücret bölgesi** eklendi</br>**Mali boyutlar** eklende |
| **Çalışan varlığı** değişiklikleri | **Ad sırası** eklendi</br>**Evden çalışma** eklendi</br>**Dil** eklendi</br>**Kıdem tarihi** eklendi</br>**Yıldönümü tarihi** eklendi</br>**Orijinal işe alma tarihi** eklendi |
| **İstihdam** varlık değişiklikleri | **Mali boyutlar** eklende</br>**İşten çıkarma nedeni** eklendi</br>**Geçiş tarihinden** yeniden adlandırılan **sonlandırma tarihi**</br>**Deneme tarihleri** eklendi |
| **Çalışan adresi** varlık değişiklikleri | **Cadde Adresi** eklendi</br>**Adres satırı 1**, **Adres satırı 2** ve **Adres satırı 3** itiraz için işaretlenmiş. |
| Yeni değişken ücret kurulumu varlıkları | **Değişken Ücret Planı Türü**</br>**Maaş değişken planı**</br>**Hakediş ödeme kuralları**</br>**Değişken Ücret Planı Düzeyi** |
| Yeni **çalışan takvimi çalışan** varlığı | **İş takvimi varlığı** eklendi |
| Yeni **Bordro pozisyon ayrıntısı** varlığı | **Bordro pozisyon ayrıntısı** eklendi |
| Yeni **Başlık** varlığı | **Başlık** eklendi. Yeni **başlık** varlığı insan kaynakları ve Common Data Service eşitleme işlemine dahil edilecek. İlk olarak **iş pozisyonundan** veya **iş** varlıklarından başvurulmaz. |

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]