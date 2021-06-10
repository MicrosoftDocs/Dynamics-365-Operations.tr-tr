---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (3 Mart 2020)
description: Bu makalede, 3 Mart 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e39e0c55fddffa99b0a86dba52da120b1ba0d1b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051149"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (3 Mart 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.2955 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse çözümü şimdi aşağıdaki değişikliklerle kullanılabilir:

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

Gelecek birkaç hafta içinde bu varlık değişiklikleri tüm ortamlarda kullanılabilir olacaktır. Human Resources için en son Dataverse çözümünü el ile yüklemek için:

1.  [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ne gidin.

2.  **Ortamlar**'ı seçin.

3.  Yükseltmek istediğiniz ortamı bulun. Ortam, Human Resources'taki **Hakkında** formunun **Common Data Service bilgileri** bölümündeki **Ortam adı**'na karşılık gelmelidir.

4.  Ortam ayrıntılarını görüntülemek için ortamı seçin.

5.  Üstteki eylem çubuğunda **Çözümleri Yönet**'i seçin. Yeni bir tarayıcı penceresi açılır ve ortamınızın bağlamında **Dynamics 365 Yönetim Merkezi**'ne gider.

6.  **Çözüm** listesinde, **Dynamics 365 Human Resources Bağlayıcısını** seçin.

7.  En son çözümü uygulamak için **Yükselt**'i seçin.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>İzin kaydı veri varlığıyla ilgili içe aktarma sorunları (406082)

Yeni kayıt tarihi önceki planın sona eren kayıt tarihinden sonra olduğu sürece, artık bir personeli aynı türden yeni bir izin kaydına kaydedebilirsiniz.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>DMF'deki 401k payrollWorkerEnrolledBenefitDetail varlığında katkı oranlarını dışa aktarma sorunu (420700)

Bu değişiklik, **payrollWorkerEnrolledBenefitDetail** varlığı için dışa aktarma işlevini, iş veren katkısı geçerli değerlerini yansıtacak şekilde düzeltir.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Kullanışlı Çalışan formunda arama yapmak Kişi alanı doldurulmalıdır iletisine neden oluyor (402525)

Bir personel aradığınızda, artık **Kişi** alanını doldurmanız gerektiğini söyleyen bir ileti almayacaksınız.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Not alan değeri Daha fazla yetenek ekle formunda işlenmiyor (380134)

Bu değişiklik, Personel self servisinde **Daha fazla yetenek ekle** formu kişiselleştirirken oluşan bir sorunu düzeltir.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Çalışanların transferi sırasında çoklu sabit ücret planlarının süresi sona ermiyor (389466)

Bu değişiklikle, eski pozisyon için tüm etkin sabit ücret kayıtları geçiş tarihinde sona erecektir.

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki önizleme özellikleri 3 Şubat 2020'de kullanılabilir duruma gelmiştir:

- **İzin ve devamsızlık önizleme özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- **Kazançlar yönetimi önizleme özelliği** -bilinen sorunlar da dahil olmak üzere daha fazla bilgi için, bkz. [Kazançlar yönetimi önizleme özelliği](hr-benefits-management-overview.md).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]