---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (10 Mart 2020)
description: Bu makalede, 10 Mart 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
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
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526939"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (10 Mart 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.2985 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Yetenek eksikliği analiz raporuna erişilemiyor (394460)

Bu rapor, Dynamics 365 Human Resources'ta desteklenmiyor. SSRS raporunu yazdıran menü öğesi kaldırıldı.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Başlarken sayfasına erişirken yanlış ileti (417950)

Bu değişiklikle, forma erişiminiz yoksa güvenlik bu menü öğesini gizler.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Personel için sorunsuz görev bakımı (380538)

Çalışan görev bakım formu işe alım süreci, işten çıkarma süreci, geçişler ve iş süreçleri konusunda personelin tüm görevlerini listeler. Görevleri silebilir, yeniden atayabilir veya durumunu güncelleştirebilirsiniz.

Örnek: Benjamin Martin bir ek kazançlar yöneticisidir. Personel işe alım süreci sırasında, Benjamin'in yeni personelin kazanç seçimini incelemesi için görevler oluşturulur. Benjamin tamamlandığı geçmiş görevleri ve tamamlanması gereken gelecekteki görevleri bulunur. Benjamin şirketten ayrılmaya karar verir; bu nedenle görevlerinin yeniden atanması veya kaldırılması gerekir. Görev bakım formu ( **Çalışan** formunun eylem bölmesinde), Benjamin'in tüm görevlerinin başka bir çalışana yeniden atanmasına veya kaldırılmasına olanak tanır.  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service çözümü şimdi aşağıdaki değişikliklerle kullanılabilir:

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
| Yeni **Başlık** varlığı | <ul><li>**Unvan** eklendi</li></ul> Common Data Service'a yeni **Unvan** varlığı eklendi ancak bu varlığa şu an için  **İş Pozisyonu** veya **İş** varlıklarından başvurulamamaktadır. |

> [!NOTE]
> Pozisyonlar ve istihdam için mali boyutlar, Human Resources'tan Common Data Service'a güncelleştirmeler için tek yönlü tümleştirme sağlar. Mali boyut güncelleştirmeleri şu an için Common Data Service'tan Human Resources ile eşitlenmez.

Gelecek birkaç hafta içinde bu varlık değişiklikleri tüm ortamlarda kullanılabilir olacaktır. Human Resources için en son Common Data Service çözümünü el ile yüklemek için:

1.  [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ne gidin.

2.  **Ortamlar**'ı seçin.

3.  Yükseltmek istediğiniz ortamı bulun. Ortam, Human Resources'taki **Hakkında** formunun **Common Data Service bilgileri** bölümündeki **Ortam adı**'na karşılık gelmelidir.

4.  Ortam ayrıntılarını görüntülemek için ortamı seçin.

5.  Üstteki eylem çubuğunda **Çözümleri Yönet**'i seçin. Yeni bir tarayıcı penceresi açılır ve ortamınızın bağlamında **Dynamics 365 Yönetim Merkezi**'ne gider.

6.  **Çözüm** listesinde, **Dynamics 365 Human Resources Bağlayıcısını** seçin.

7.  En son çözümü uygulamak için **Yükselt**'i seçin.

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki Önizleme özellikleri 3 Şubat 2020 ' da kullanılabilir:

- **İzin ve devamsızlık önizleme özellikleri** - Daha fazla bilgi için bkz. [İzin ve devamsızlık önizleme özellikleri](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- **Kazançlar yönetimi önizleme özelliği** -bilinen sorunlar da dahil olmak üzere daha fazla bilgi için, bkz. [Kazançlar yönetimi önizleme özelliği](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Çok Yakında

### <a name="platform-update-33"></a>Platform update 33

- Tam sayfa uygulamalar (Önizleme) - Kaydedilmiş görünümler özelliğini etkinleştirmenizi sağlayan bu önizleme özelliği, Power Apps ve üçüncü taraf uygulamaların pano aracılığıyla tam sayfa deneyimleri olarak eklenmesine olanak tanır.

- Kaydedilmiş görünümler (Önizleme) - Bu önizleme özelliği, kişiselleştirme alt sisteminde belirgin bir iyileştirme olan kaydedilmiş görünümleri etkinleştirir. Bu özellik, kullanıcıların her sayfada birden çok adlandırılmış kişiselleştirme kümesine sahip olmasına olanak tanır. Ayrıca, görünümleri güvenlik rollerine yayımlayabilirsiniz.

- İyileştirilen "biri" filtreleme deneyimi - Bu özellik, en iyi duruma getirilmiş "biri" filtreleme deneyimini etkinleştirir; bu deneyim, birden fazla filtre değerinin kolaylıkla girilmesini sağlar, tek bir filtre değerini veya tüm filtre değerlerini kaldırmak için daha basit bir mekanizmaya sahiptir ve filtre değerleri için daha kompakt ve kullanışlı görselleştirme sağlar.

- Önerilen alanlar - Kullanıcıların sıklıkla bir kılavuza veya sayfaya alan eklemesi gerekir. Bu, birçok kullanılabilir çok alan bulunduğundan zor olabilir. Bu özellik, büyük bir liste içinde arama yapmak yerine sistemin benzer senaryolarda diğer kullanıcıların en sık eklediği alanları temel alarak önerilen alanlar kümesi sunmasına olanak tanır.

- Kılavuzlardaki yapışkan varsayılan eylemler - Bu özellik, bir kılavuzdaki varsayılan eylemin, söz konusu sütunun taşınmış veya gizlenmiş olmasına bakılmaksızın, kılavuzdaki belirli bir sütuna bağlanmasını sağlar.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)