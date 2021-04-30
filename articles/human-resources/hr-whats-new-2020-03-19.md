---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (19 Mart 2020)
description: Bu makalede, 19 Mart 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25214eafa2f2108f0b465a931cbb6995a0a4b553
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892093"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (19 Mart 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3014 uygulanır. Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>İnsan Kaynakları ortam sınırları Şimdi güncelleştirilmiş lisansa dayalıdır (394595)

Lifecycle Services (LCS) içindeki proje başına ortam sayısı sınırı değişti. Önceki sınır iki ortamlıda. LCS içindeki İnsan Kaynakları için oluşturabileceğiniz üretim ve korumalı alan ortamlarının sayısı sınırı Şimdi güncelleştirilmiş lisansa dayalıdır. Artık tüm LCS projesi başına gereken sayıda ortam satın alınan lisans sayısına bağlı olarak oluşturabilirsiniz. 1 Şubat 2020 tarihinde güncelleştirilen yeni lisans müşterilerin ek ortamlar satın almanıza olanak tanır. Ek ortamların lisans gereksinimleri hakkında daha fazla bilgi için bkz. [Dynamics 365 lisans Kılavuzu](https://dynamics.microsoft.com/pricing/#HumanResources)'na bakın.

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Çalışanlar ve yöneticiler için maaş verilerinin şirket içinde görüntülenmesini sağla (403904)

**Özellik yönetimi** çalışma alanında aşağıdaki özellikleri açın. Önizleme özellikleri hakkında daha fazla bilgi edinmek için bkz. [Önizleme özellikleri açma ve kapatma](hr-admin-manage-features.md#enable-or-disable-preview-features).

Bu özelliği etkinleştirdiğinizde, Yöneticiler çalışma şirketinde oturum açmadan doğrudan ve genişletilmiş rapor tazminatı görebilirler. Yöneticinin erişebileceği, oturum açmış tüm şirketlerdeki tam maaş geçmişi bulunabilir. Daha fazla bilgi için bkz [Çalışan ve yönetici self servise genel bakış](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Genel adres defteri birleştirme işlevini etkinleştir (427189)

Yinelenen adres defteri girişlerini, çoğaltılan kayıtları seçerek ve **Global adres defteri** sayfasından **Birleştir**'i seçerek birleştirebilirsiniz.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Çoklu izin türü özelliği ile oluşturulmuş tahakkukları olan bir plan için çıkış bakiyesi ayarlanamıyor (419635)

Artık, özellik yönetiminde etkinleştirilmiş **çoklu izin türü** önizleme özelliği ile oluşturulan bırakma planlarının bakiyelerini ayarlayabilirsiniz.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>WorkerPositionAssignmentEntity bir çalışan sonlandırıldığında birincil pozisyon alanı (420774)

İşten çıkarılan bir işe sahip çalışanlar için, işten çıkarma sırasında etkin olan birincil pozisyon varlıkta görüntülenir. Tümleştirmeler için, çalışanın çalışan pozisyon ataması için yinelenen bir kayıt oluşturulmayacaktır. 

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

### <a name="platform-update-33"></a>Platform update 33

- Tam sayfa uygulamalar (Önizleme) - Kaydedilmiş görünümler özelliğini etkinleştirmenizi sağlayan bu önizleme özelliği, Power Apps ve üçüncü taraf uygulamaların pano aracılığıyla tam sayfa deneyimleri olarak eklenmesine olanak tanır.

- Kaydedilmiş görünümler (Önizleme) - Bu önizleme özelliği, kişiselleştirme alt sisteminde belirgin bir iyileştirme olan kaydedilmiş görünümleri etkinleştirir. Bu özellik, kullanıcıların her sayfada birden çok adlandırılmış kişiselleştirme kümesine sahip olmasına olanak tanır. Ayrıca, görünümleri güvenlik rollerine yayımlayabilirsiniz.

- İyileştirilen "biri" filtreleme deneyimi - Bu özellik, en iyi duruma getirilmiş "biri" filtreleme deneyimini etkinleştirir; bu deneyim, birden fazla filtre değerinin kolaylıkla girilmesini sağlar, tek bir filtre değerini veya tüm filtre değerlerini kaldırmak için daha basit bir mekanizmaya sahiptir ve filtre değerleri için daha kompakt ve kullanışlı görselleştirme sağlar.

- Önerilen alanlar - Kullanıcıların sıklıkla bir kılavuza veya sayfaya alan eklemesi gerekir. Bu, birçok kullanılabilir çok alan bulunduğundan zor olabilir. Bu özellik, büyük bir liste içinde arama yapmak yerine sistemin benzer senaryolarda diğer kullanıcıların en sık eklediği alanları temel alarak önerilen alanlar kümesi sunmasına olanak tanır.

- Kılavuzlardaki yapışkan varsayılan eylemler - Bu özellik, bir kılavuzdaki varsayılan eylemin, söz konusu sütunun taşınmış veya gizlenmiş olmasına bakılmaksızın, kılavuzdaki belirli bir sütuna bağlanmasını sağlar.

## <a name="new-production-release-cadence"></a>Yeni üretim sürümü temposu

Nisandan başlayarak, İnsan Kaynakları sürüm temposu bir haftalık güncelleştirmeden iki haftada bir güncelleştirme olacak şekilde kayabilir. Bu, güvenli dağıtım uygulamalarıyla hizalamayı garanti altına alır ve hizmette yüksek kararlılık ve güvenilirlik standartlarını korur. İşlemin her aşamasında başarılı dağıtımı doğrulamak için yerine ek test ve izleyiciler koyuyoruz. Sürüm temposu hakkında daha fazla bilgi için [güncelleştirme işlemine](hr-admin-setup-update-process.md) bakın.

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki Önizleme özellikleri 3 Şubat 2020 ' da kullanılabilir:

- **İzin ve devamsızlık önizleme özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- **Kazançlar yönetimi önizleme özelliği** -bilinen sorunlar da dahil olmak üzere daha fazla bilgi için, bkz. [Kazançlar yönetimi önizleme özelliği](hr-benefits-management-overview.md).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]