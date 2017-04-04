---
title: "Bir iş bileşenlerini kurma"
description: "Bu konuda bir proje içerebilir ve bu öğeleri, kuruluşunuzda nasıl kullanabileceğinizi örnekler sağlayan kavramsal öğeleri açıklar."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Bir iş bileşenlerini kurma

Bu konuda bir proje içerebilir ve bu öğeleri, kuruluşunuzda nasıl kullanabileceğinizi örnekler sağlayan kavramsal öğeleri açıklar. 

İşleri oluşturmadan önce bazı başvuru bilgileri ayarlamanız gerekir. Yalnızca bir ada sahip bir proje oluşturabilirsiniz. Ancak, bir Unvan gibi ek bilgileri dahil olmak üzere, varsayılan değerler için projeye atanan pozisyonların sağlar. Ayrıca, bazı girdiğiniz bilgilerin belirli projelere maaş planları filtrelemek için kullanılabilir. Maaş planları belirli bir projeye filtre uygulamak için kullanabileceğiniz uygunluk ayarlamak istiyorsanız, işler ayarlamak önce bir iş işlevlerini ve proje türleri ayarlamanız. Bu varsayılan değerler kullanılabilir sağlayarak, pozisyonları projeye eklediğiniz zaman zaman kazandırır. 

İş Unvanı, türü ve işlev, gibi bazı iş ayrıntıları etkin tarih. Bugün bir iş oluşturmak, ancak daha sonra bu ayrıntıları ekleme ve sonra işin oluşturulma tarihi itibariyle gözden geçirmeniz, bu ayrıntıları görüntülenmez. Bu nedenle, önce onu gerektiren bazı bu başvuru bilgileri oluşturmanız gerekir. Bu yolla oluşturduğunuzda, yeni işler için bilgi ekleyebilirsiniz.

## <a name="job-titles"></a>İş unvanları
İşleri oluşturmadan önce bu işler için başlıkları ayarlamanız gerekir. Pozisyonların iş unvanları pozisyonları ile ilişkili işleri devralması. 

İş unvanları kullanarak korumak **başlıkları** sayfası, arama işlevini kullanarak açabilirsiniz. Üzerinde ** başlıkları ** sayfasında, işleriniz için kullanmayı planladığınız bir başlık girin.

## <a name="job-types"></a>İş tipleri
İş türleri, benzer işleri kategorilerde gruplandırmak için kullanın. İş türleri, gerekli değildir. Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş tiplerini kullanmayı planlıyorsanız, işler ayarlamak için önce iş tiplerini ayarlamanız gerekir. Tam zamanlı ve yarı zamanlı iş tiplerinin bazı örnekler veya maaş ve saatlik ödemesi. İş tiplerini kullanarak korumak **proje türleri** sayfa. Üzerinde **proje türleri** sayfasında, ad ve iş tipi için kısa bir açıklama girin. İçinde **muaf durumu** alanında, bu iş türü içeren işlerin adil işçi standartları Yasası (FLSA) muafiyet durumu belirtmek için aşağıdaki seçeneklerden birini seçin:

-   **Muafiyet** – işleri FLSA altında fazla mesai dışında.
-   **Muafiyet dışı** – işleri FLSA altında fazla mesai dışında değildir.
-   **Geçerli değildir** – FLSA kapsamı geçerli değildir.

## <a name="job-functions"></a>İş işlevleri
İşi kavşakları üst düzey işlev kategorileri açıklar ve üst düzey görevleri ilişkilendirebilirsiniz. İş işlevlerini gerekli değildir. İşi İşlevler, iş türleri, maaş planları belirli projeler için filtre uygulamak için kullanabilirsiniz. Görev ve proje türleri ile maaş planları üzerinde uygunluğu kurallar ayarlayarak ilişkilendirmenize **uygunluk kuralları** sayfa. Sonra iş türü ve bir Uygunluk kuralı ile tanımladığınız iş işlevi belirli birleşimi için geçerli bir tazminat planı çevreleyen düzeyler kümesi ekleyebilirsiniz. (Bu özellikler sabit maaş planları ve değişken maaş planları için geçerlidir.) Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş işlevlerini kullanmayı planlıyorsanız, işler ayarlamak için önce iş işlevlerini ayarlamanız gerekir. Aşağıdaki tabloda bazı örnekler iş işlevlerini gösterir.

| İş           | İş işlevi      |
|---------------|-------------------|
| Satış yöneticisi | Orta düzey yönetici |
| Muhasebeci    | Uzmanları     |

İş işlevlerini kullanarak korumak **iş işlevleri** sayfa. Üzerinde **iş işlevleri** sayfasında, bir kimlik kodu ve iş işlevine ilişkin kısa bir açıklama girin.

## <a name="job-tasks"></a>İş görevleri
Proje görevleri bir iş için bir pozisyonda olan işçi tamamlaması gereken temel görevler açıklanmıştır. Aynı proje görevi birden fazla işi ve bu proje görevleri kullanın işleri pozisyonlar için eklenebilir. Aşağıdaki tabloda bazı örnekler proje görevleri gösterir.

<table>
<thead>
<tr class="header">
<th>İş</th>
<th>İş görevi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Satış yöneticisi</td>
<td><ul>
<li><strong>Yapılarındaki İnceleme</strong> – her satış temsilcisinin iş performansı gözden geçirin.</li>
<li><strong>Abs İnceleme</strong> – onaylama veya reddetme her satış temsilcisinin devamsızlık istekleri veya kayıtları.</li>
</ul></td>
</tr>
<tr class="even">
<td>Muhasebeci</td>
<td><strong>FIN rapor</strong> – Finans Müdürü haftalık finansal raporlar sunmak.</td>
</tr>
</tbody>
</table>

Proje görevleri kullanarak korumak **proje görevleri** sayfa. Üzerinde **proje görevleri** sayfasında, ad ve proje görevi için açıklama girin. İçinde **Not** alan, ek bilgi isteğe bağlı olarak girebilirsiniz. Not belirli bir proje için buraya girdiğiniz notları değiştirmeden güncelleştirilebilir.

## <a name="areas-of-responsibility"></a>Sorumluluk alanları
Sorumluluk alanları, iş rolleri, işlemler ve bir proje için bir konum olan işçi sorumlu olduğu ürünleri göstermek için kullanın. Örneğin, "Muhasebeci" adlı bir proje için bir sorumluluk alanı "mali raporlama için ürün A." olabilir Sorumluluk alanları kullanarak korumak **sorumluluk alanlarının** sayfası, arama işlevini kullanarak bulabilirsiniz. Üzerinde **sorumluluk alanlarının** sayfasında, ad ve Sorumluluk için açıklama girin. İçinde **Not** alan, ek bilgi isteğe bağlı olarak girebilirsiniz. Not belirli bir proje için buraya girdiğiniz notları değiştirmeden güncelleştirilebilir.


