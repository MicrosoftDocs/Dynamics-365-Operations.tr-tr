---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (18 Şubat 2020)
description: Bu makalede, 18 Şubat 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec7d8dbc73dce57d3968c4d239a51d27673a2493
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066298"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (18 Şubat 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.2903 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="platform-update-32"></a>Platform güncelleştirmesi 32 

32 platform güncelleştirmesi artık kullanılabilir durumdadır. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamaları için Platform güncelleştirmesi 32'deki yenilikler veya değişiklikler (Şubat 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Akıcı personel formundaki görünüm seçenekleri değiştirilirken arama değerleri hatırlanır (383833)

Görünüm seçeneklerini değiştirdiğinizde ve değişiklikler uyguladığınızda yeni **çalışan** formu artık arama değerlerini hatırlar.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Önizleme özelliğindeki maaş Yönetimi Özet kutucukları yanlış biçime yeniden yönlendir (401861)

Sabit ve değişken maaş yönetimi kutucukları şimdi yeni **çalışan** formunda doğru kayıtları görüntüler. Yalnızca, akıcı çalışan formu önizleme özelliği için geçerlidir. Bu önizleme özelliğini **Özellik yönetiminde** etkinleştirebilirsiniz. Daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Dataverse'te bazı bırakma isteği için Boş Durum alanı kayıt kayıtları (414915)

Bu değişiklik, bir bırakma isteğindeki Dataverse **durum** alanının **gözden geçirilmesi** için ayarlandığı durumlarda oluşan bir sorunu düzeltir. Dataverse şimdi durumu yansıtır.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Yetenek eksikliği Analizi yalnızca atanan iş için mümkündür (411390)

İnsan Kaynakları tanımlı herhangi bir iş için artık bir yetenek eksikliği analizi yapabilirsiniz.

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>Sistem para birimi yeni ortamlarda Dataverse'ten insan kaynaklarına eşitleme yapmıyor (418011)

Dataverse'deki sistem para birimi şimdi insan kaynakları ile eşitlenebilir.

## <a name="in-preview"></a>Ön izlemede

- [İzin ve devamsızlık Önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Kazanç yönetimi önizleme özellikleri](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Çok yakında

### <a name="updated-dataverse-solution"></a>Güncellenen Dataverse çözümü

Aşağıdaki değişikliklerle , yeni bir Dataverse çözüm yakında kullanıma sunulur:

| Tanım | Değiştirme |
| ----------------------------------------- | --- |
| **İş/pozisyon** varlığı değişiklikleri | **Ücret bölgesi** eklendi</br>**Mali boyutlar** eklende |
| **Çalışan varlığı** değişiklikleri | **Ad sırası** eklendi</br>**Evden çalışma** eklendi</br>**Dil** eklendi</br>**Kıdem tarihi** eklendi</br>**Yıldönümü tarihi** eklendi</br>**Orijinal işe alma tarihi** eklendi |
| **İstihdam** varlık değişiklikleri | **Mali boyutlar** eklende</br>**İşten çıkarma nedeni** eklendi</br>**Geçiş tarihinden** yeniden adlandırılan **sonlandırma tarihi**</br>**Deneme tarihleri** eklendi |
| **Çalışan adresi** varlık değişiklikleri | **Cadde Adresi** eklendi</br>**Adres satırı 1**, **Adres satırı 2** ve **Adres satırı 3** itiraz için işaretlenmiş. |
| Yeni değişken ücret kurulumu varlıkları | **Değişken Ücret Planı Türü**</br>**Maaş değişken planı**</br>**Hakediş ödeme kuralları**</br>**Değişken Ücret Planı Düzeyi** |
| Yeni **çalışan takvimi çalışan** varlığı | **İş takvimi varlığı** eklendi |
| Yeni **Bordro pozisyon ayrıntısı** varlığı | **Bordro pozisyon ayrıntısı** eklendi |
| Yeni **Başlık** varlığı | **Başlık** eklendi. Yeni **başlık** varlığı insan kaynakları ve Dataverse eşitleme işlemine dahil edilecek. İlk olarak **iş pozisyonundan** veya **iş** varlıklarından başvurulmaz. |

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
