---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (24 Mart 2020)
description: Bu makalede, 24 Mart 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3607e09935928a079a3f7e60cde1017e69875dea
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694781"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (24 Mart 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3073 uygulanır. Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>İnsan Kaynakları ortam sınırları Şimdi güncelleştirilmiş lisansa dayalıdır (394595)

Lifecycle Services (LCS) içindeki proje başına ortam sayısı sınırı değişti. Önceki sınır iki ortamlıda. LCS içindeki İnsan Kaynakları için oluşturabileceğiniz üretim ve korumalı alan ortamlarının sayısı sınırı Şimdi güncelleştirilmiş lisansa dayalıdır. Artık tüm LCS projesi başına gereken sayıda ortam satın alınan lisans sayısına bağlı olarak oluşturabilirsiniz. 1 Şubat 2020 tarihinde güncelleştirilen yeni lisans müşterilerin ek ortamlar satın almanıza olanak tanır. Ek ortamların lisans gereksinimleri hakkında daha fazla bilgi için bkz. [Dynamics 365 lisans Kılavuzu](https://dynamics.microsoft.com/pricing/#HumanResources)'na bakın.

## <a name="platform-changes"></a>Platform değişiklikleri

- Tam sayfa uygulamalar (Önizleme) - Kaydedilmiş görünümler özelliğini etkinleştirmenizi sağlayan bu önizleme özelliği, Power Apps ve üçüncü taraf uygulamaların pano aracılığıyla tam sayfa deneyimleri olarak eklenmesine olanak tanır.

- Kaydedilmiş görünümler (Önizleme) - Bu önizleme özelliği, kişiselleştirme alt sisteminde belirgin bir iyileştirme olan kaydedilmiş görünümleri etkinleştirir. Bu özellik, kullanıcıların her sayfada birden çok adlandırılmış kişiselleştirme kümesine sahip olmasına olanak tanır. Ayrıca, görünümleri güvenlik rollerine yayımlayabilirsiniz.

- İyileştirilen "biri" filtreleme deneyimi - Bu özellik, en iyi duruma getirilmiş "biri" filtreleme deneyimini etkinleştirir; bu deneyim, birden fazla filtre değerinin kolaylıkla girilmesini sağlar, tek bir filtre değerini veya tüm filtre değerlerini kaldırmak için daha basit bir mekanizmaya sahiptir ve filtre değerleri için daha kompakt ve kullanışlı görselleştirme sağlar.

- Önerilen alanlar - Kullanıcıların sıklıkla bir kılavuza veya sayfaya alan eklemesi gerekir. Bu, birçok kullanılabilir çok alan bulunduğundan zor olabilir. Bu özellik, büyük bir liste içinde arama yapmak yerine sistemin benzer senaryolarda diğer kullanıcıların en sık eklediği alanları temel alarak önerilen alanlar kümesi sunmasına olanak tanır.

- Kılavuzlardaki yapışkan varsayılan eylemler - Bu özellik, bir kılavuzdaki varsayılan eylemin, söz konusu sütunun taşınmış veya gizlenmiş olmasına bakılmaksızın, kılavuzdaki belirli bir sütuna bağlanmasını sağlar.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>"Çoklu izin türü" özelliği ile oluşturulmuş tahakkukları olan bir plan için çıkış bakiyesi ayarlanamıyor (419635)

Bu değişiklikle, özellik yönetiminde etkinleştirilmiş Çoklu izin türü (Önizleme) özelliği ile oluşturulmuş olan izin planlarının bakiyelerini ayarlayabilirsiniz.

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki önizleme özellikleri 3 Şubat 2020'de kullanılabilir duruma gelmiştir:

- **İzin ve devamsızlık önizleme özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- **Kazançlar yönetimi önizleme özelliği** -bilinen sorunlar da dahil olmak üzere daha fazla bilgi için, bkz. [Kazançlar yönetimi önizleme özelliği](hr-benefits-management-overview.md).

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse çözümü şimdi aşağıdaki değişikliklerle kullanılabilir:

| Tanım | Değiştirme |
| --- | --- |
| **İş/pozisyon** varlığı değişiklikleri | <ul><li>**Ücret bölgesi** eklendi</li>|
| **İş pozisyonu boyutu** varlığı eklendi | <ul><li>**Mali boyutlar** eklende</li>
| **Çalışan varlığı** değişiklikleri | <ul><li>**Ad sırası** eklendi</li><li>**Evden çalışma** eklendi</li><li>**Dil** eklendi</li><li>**Kıdem tarihi** eklendi</li><li>**Yıldönümü tarihi** eklendi</li><li>**Orijinal işe alma tarihi** eklendi</li></ul> |
| **İstihdam** varlık değişiklikleri | <ul><li>**Mali boyutlar** eklende</li><li>**İşten çıkarma nedeni** eklendi</li><li>**Geçiş tarihinden** yeniden adlandırılan **sonlandırma tarihi**</li><li>**Deneme tarihleri** eklendi</li></ul> |
| **Çalışan adresi** varlık değişiklikleri | <ul><li>**Cadde Adresi** eklendi</li><li>**Adres satırı 1**, **Adres satırı 2** ve **Adres satırı 3** itiraz için işaretlenmiş.</li></ul> |
| Yeni değişken ücret kurulumu varlıkları | <ul><li>**Değişken Ücret Planı Türü**</li><li>**Maaş değişken planı**</li><li>**Hakediş ödeme kuralları**</li><li>**Değişken Ücret Planı Düzeyi**</li></ul> |
| Yeni **çalışan takvimi çalışan** varlığı | <ul><li>**İş takvimi varlığı** eklendi</li></ul> |
| Yeni **Bordro pozisyon ayrıntısı** varlığı | <ul><li>**Bordro pozisyon ayrıntısı** eklendi</li></ul> |
| Yeni **Başlık** varlığı | <ul><li>**Unvan** eklendi</li></ul>Dataverse'a yeni **Unvan** varlığı eklendi ancak bu varlığa şu an için  **İş Pozisyonu** veya **İş** varlıklarından başvurulamamaktadır. |

> [!NOTE]
> Pozisyonlar ve istihdam için mali boyutlar, Human Resources'tan Dataverse'a güncelleştirmeler için tek yönlü tümleştirme sağlar. Mali boyut güncelleştirmeleri şu an için Dataverse'tan Human Resources ile eşitlenmez.

Gelecek birkaç hafta içinde bu varlık değişiklikleri tüm ortamlarda kullanılabilir olacaktır. Human Resources için en son Dataverse çözümünü el ile yüklemek için:

1.  [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ne gidin.

2.  **Ortamlar**'ı seçin.

3.  Yükseltmek istediğiniz ortamı bulun. Ortam, Human Resources'taki **Hakkında** formunun **Common Data Service bilgileri** bölümündeki **Ortam adı**'na karşılık gelmelidir.

4.  Ortam ayrıntılarını görüntülemek için ortamı seçin.

5.  Üstteki eylem çubuğunda **Çözümleri Yönet**'i seçin. Yeni bir tarayıcı penceresi açılır ve ortamınızın bağlamında **Dynamics 365 Yönetim Merkezi**'ne gider.

6.  **Çözüm** listesinde, **Dynamics 365 Human Resources Bağlayıcısını** seçin.

7.  En son çözümü uygulamak için **Yükselt**'i seçin.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint Önizleme bazı ortamlarda çalışmıyor

SharePoint'te depolanan belgelere ait belge önizlemesi çalışmazsa, aşağıdaki yordamı deneyin:

1. Yönetici Kullanıcı hesabının kullanıcı kaydıyla ilişkili bir e-posta olduğunu doğrulayın. Bu bilgileri **Kullanıcı** sayfasında görüntüleyebilirsiniz. E-posta ayarlanmamışsa, OData Excel eklentisi ile e-posta ve sağlayıcı eklemeniz gerekir. Varsayılan olarak, e-posta adresi Excel tasarımında bulunmaz. Excel tasarımını düzenlemeniz, tüm alanları eklemeniz, uygulamanız ve yenilemeniz gerekir. Bu adımları tamamladıktan sonra, yönetici hesabını güncelleştirebilirsiniz.

2. Yönetici hesabının ilişkili bir e-posta hesabı varsa, yönetici kimlik bilgileriyle İnsan Kaynakları için oturum açın.

3. Belge önizlemesini başlatmak için SharePoint ' deki bir eke erişin.

4. Eklere erişimi olan başka bir kullanıcı hesabıyla oturum açın ve önizlemenin beklendiği gibi çalıştığını doğrulayın.

## <a name="coming-soon"></a>Çok Yakında

## <a name="new-production-release-cadence"></a>Yeni üretim sürümü temposu

Nisan ayından başlayarak, Human Resources sürüm temposu bir haftalık güncelleştirme yerine iki haftalık güncelleştirme olacak şekilde değiştirilecektir. Güvenli dağıtım uygulamalarıyla uyumu sağlamak ve hizmette yüksek kararlılık ve güvenilirlik standartlarını korumak için, tüm bölgelere hizmet güncelleştirmelerini dağıtma işlemi iki haftalık bir dağıtım olacaktır. İşlemin her aşamasında başarılı dağıtımı doğrulamak için ek test ve izleyiciler olacaktır. Sürüm temposu hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Bilinen sorunlar

## <a name="employment-detail-entity"></a>İstihdam Ayrıntısı varlığı

**İstihdam Ayrıntısı** varlığı aşağıdaki alanlarla güncelleştirildi: **PayFrequency**, **İstihdam Kategorisi Kodu**, **İstihdam Türü**, **EmploymentType Kodu** ve **Kazanç İstihdam Durumu**. Bu alanların kurulum verileri, Özellik yönetiminde etkinleştirilen kazanç yönetimine bağlıdır. İçe aktarma sırasında hatalara neden olacağından, bu alanlar **İstihdam Ayrıntısı** varlığında doldurulmamalı veya güncelleştirilmemelidir.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]