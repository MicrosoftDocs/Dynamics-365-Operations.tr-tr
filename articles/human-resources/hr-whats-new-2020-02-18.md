---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (18 Şubat 2020)
description: Bu makalede, 18 Şubat 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e9e1f05de682b4fe29ec23f06099b2968ebe3df
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712000"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (18 Şubat 2020)

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.2903 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="platform-update-32"></a>Platform güncelleştirmesi 32 

32 platform güncelleştirmesi artık kullanılabilir durumdadır. Daha fazla bilgi için bkz. [Finance and Operations uygulamaları için Platform güncelleştirmesi 32'daki yenilikler veya değişiklikler (2020 Şubat)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Akıcı personel formundaki görünüm seçenekleri değiştirilirken arama değerleri hatırlanır (383833)

Görünüm seçeneklerini değiştirdiğinizde ve değişiklikler uyguladığınızda yeni **çalışan** formu artık arama değerlerini hatırlar.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Önizleme özelliğindeki maaş Yönetimi Özet kutucukları yanlış biçime yeniden yönlendir (401861)

Sabit ve değişken maaş yönetimi kutucukları şimdi yeni **çalışan** formunda doğru kayıtları görüntüler. Yalnızca, akıcı çalışan formu önizleme özelliği için geçerlidir. Bu önizleme özelliğini **Özellik yönetiminde** etkinleştirebilirsiniz. Daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Common Data Service'te bazı bırakma isteği için Boş Durum alanı kayıt kayıtları (414915)

Bu değişiklik, bir bırakma isteğindeki Common Data Service **durum** alanının **gözden geçirilmesi** için ayarlandığı durumlarda oluşan bir sorunu düzeltir. Common Data Service şimdi durumu yansıtır.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Yetenek eksikliği Analizi yalnızca atanan iş için mümkündür (411390)

İnsan Kaynakları tanımlı herhangi bir iş için artık bir yetenek eksikliği analizi yapabilirsiniz.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Sistem para birimi yeni ortamlarda Common Data Service'ten insan kaynaklarına eşitleme yapmıyor (418011)

Common Data Service'deki sistem para birimi şimdi insan kaynakları ile eşitlenebilir.

## <a name="in-preview"></a>Ön izlemede

- [İzin ve devamsızlık Önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Kazanç yönetimi önizleme özellikleri](hr-benefits-management-overview.md)

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

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)