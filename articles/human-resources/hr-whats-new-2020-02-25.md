---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (25 Şubat 2020)
description: Bu makalede, Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092764"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (25 Şubat 2020)

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.2927 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Servis Talebi Yönetimi gezintisini ve veri yönetimi çerçevesi (DMF) varlığını etkinleştirme (414754)

Bu önizleme özelliği, servis talebi yönetimi servis taleplerine ek gezinti olanağı sağlar. Bu önizleme özelliğini **Özellik Yönetimi** çalışma alanında etkinleştirebilirsiniz. Bu menü öğeleri Dynamics 365 Human Resources'ın **Uyumluluk** çalışma alanında görünür. Bu değişiklikle Human Resources şunlara erişebilir:

- Tüm servis talepleri
- Servis taleplerim
- Açık servis taleplerim
- Vadesi geçen servis taleplerim
- İş akışı üzerinden bana atanan servis talepleri

Servis taleplerindeki bu yeni görünümlerin yanı sıra **Servis talebi ayrıntısı** DMF varlığı da kullanılabilir.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Genel adres defterinde İlişki tanımlarını etkinleştirme (414762)

İlişkiler, artık genel adres defterinde etkin durumdadır. Bu haftanın sürümünden **İlişki** bilgi kutusu sistem tanımlı tüm ilişkilerde gösteriliyordu. Artık bu ilişkileri genel adres defteri sayfası içinde tanımlayabilirsiniz.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Pozisyon için etkin ücret kayıtları olduğunda pozisyon kaldırılabilir (414568)

Bu değişiklikle, bir pozisyonu ve aynı pozisyon için etkin ücret kaydı bulunan bir çalışanı silmeye çalıştığınızda bir uyarı görüntülenir. Bu durumda, pozisyonu kaldırmadan önce personel sabit ücret kaydını güncelleştirmeniz gerekir.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Performans gözden geçirme iş akışı bazen işlemin parçası olmayan kişilerden kapatma işlemleri ekliyor (414171)

Bu değişiklik, ek kapatma katılımcılarının performans incelemesine eklenme sorununu düzeltir.

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a>Yeni Çalışan iletişim kutusunda seçildiğinde çalışan pozisyonu ataması Common Data Service'ta oluşturulmuyor (413479)

Bu değişiklik, yeni bir çalışan işe alınırken ve yeni işe alınan kişi **Yeni çalışan** iletişim kutusu aracılığıyla bir pozisyona atanırken oluşan bir sorunu düzeltir. Şimdi pozisyon ataması Common Data Service'ta yansıtılır.

## <a name="coming-soon"></a>Çok yakında

### <a name="updated-common-data-service-solution"></a>Güncellenen Common Data Service çözümü

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

Gelecek birkaç hafta içinde bu varlık değişiklikleri tüm ortamlarda kullanılabilir olacaktır. Human Resources için en son Common Data Service çözümünü el ile yüklemek için:

1.  [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ne gidin.

2.  **Ortamlar**'ı seçin.

3.  Yükseltmek istediğiniz ortamı bulun. Bu, Human Resources'taki **Hakkında** formunun **Common Data Service bilgileri** bölümündeki **Ortam adı**'na karşılık gelmelidir.

4.  Ortam ayrıntılarını görüntülemek için ortamı seçin.

5.  Üstteki eylem çubuğunda **Çözümleri Yönet**'i seçin. Yeni bir tarayıcı penceresi açılır ve ortamınızın bağlamında **Dynamics 365 Yönetim Merkezi**'ne gider.

6.  **Çözüm** listesinde, **Dynamics 365 Human Resources Bağlayıcısını** seçin.

7.  En son çözümü uygulamak için **Yükselt**'i seçin.

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki önizleme özellikleri 3 Şubat 2020'de kullanılabilir duruma gelmiştir:

- **İzin ve devamsızlık önizleme özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- **Kazançlar yönetimi önizleme özelliği** -bilinen sorunlar da dahil olmak üzere daha fazla bilgi için, bkz. [Kazançlar yönetimi önizleme özelliği](hr-benefits-management-overview.md).
