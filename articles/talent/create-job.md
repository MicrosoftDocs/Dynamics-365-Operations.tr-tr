---
title: "İşin bileşenlerini ayarlama"
description: "Bu konu, bir işin içerebileceği konsept öğelerini açıklar ve bu öğeleri kuruluşunuzda nasıl kullanabileceğiniz hakkında örnekler sağlar."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: b40b81fc24086e73b54cfe0cb5e6a81ec5838ab5
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="set-up-the-components-of-a-job"></a>İşin bileşenlerini ayarlama

[!include [banner](includes/banner.md)]


Bu konu, bir işin içerebileceği konsept öğelerini açıklar ve bu öğeleri kuruluşunuzda nasıl kullanabileceğiniz hakkında örnekler sağlar. 

Yeni işler oluşturabilmeden önce, bazı referans bilgileri ayarlamalısınız. Sadece bir isme sahip bir iş oluşturabilirsiniz. Ancak, örneğin bir iş unvanı gibi ek bilgiler ekleyerek, işe atanmış olan konumlara varsayılan değerler sağlarsınız. Ek olarak, girdiğiniz bazı bilgiler maaş planlarını belirli işlere filtrelemek için kullanılabilir. Maaş planlarını belirli bir işe filtrelemek için uygunluk ayarlamak istiyorsanız, iş işlevleri ve iş görevlerini, işleri ayarlamadan önce ayarlamalısınız. Bu varsayılan değerleri mevcut bulundurarak, işe konumlar eklerken zaman kazanırsınız. 

Bazı iş ayrıntıları, örneğin iş unvanı, türü ve işlevi, yürürlük tarihine sahiptir. Bugün bir iş oluşturursanız ancak bunları daha sonra bu ayrıntıları eklemezseniz ve daha sonra işe oluşturulma tarihinde bakarsanız, bu ayrıntılar görüntülenmez. Bu nedenle, bu başvuru bilgilerinin bazılarını, ihtiyaç duymadan oluşturmanız gerekir. Bu sayede, yeni işlere bilgileri, onları oluştururken ekleyebilirsiniz.

## <a name="job-titles"></a>İş başlıkları
İşler oluşturmadan önce, bu işler için unvanlar ayarlamanız gerekir. Pozisyonlar, iş unvanlarını, pozisyonların ilişkili olduğu işlerden devralır. 

Arama özelliğini kullanarak açabileceğiniz **Unvanlar** sayfasını kullanarak iş unvanlarını korumak. **Unvanlar** sayfasında, işlerinizde kullanmayı planladığınız unvanları girin.

## <a name="job-types"></a>İş tipleri
Benzer işleri kategorilere gruplamak için iş türlerini kullanın. İş türleri, zorunlu değildir. Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş türlerini kullanmayı planlıyorsanız, işleri ayarlamadan önce iş tiplerini ayarlamalısınız. İş türlerine bazı örnekler tam zamanlı ve yarı zamanlı veya maaşlı ve saatlik ödemelidir. **İş türleri** sayfasını kullanarak iş türlerini yönetirsiniz. **İş türleri** sayfası üzerinde, iş türü için kısa bir açıklama ve ad girin. **Muaf durumu** alanında, Adil İş Standartları Yasası (FLSA) muafiyet durumunu, şu iş durumuna sahip işler için belirtmek üzere aşağıdaki seçeneklerden birini işaretleyin:

-   **Muafiyet** – İşler, FLSA kapsamı altında fazla mesai dışında tutulurlar.
-   **Muaf olmayan** – İşler, FLSA kapsamı altında fazla mesai dışında tutulmaz.
-   **Geçerli değildir** – FLSA kapsamı için geçerli değildir.

## <a name="job-functions"></a>İş işlevleri
İş işlevleri, yüksek seviye işlevsellik kategorileri açıklar ve yüksek düzey görevleri ilişkilendirir. İş işlevleri, zorunlu değildir. Tazminat planlarını belirli işlere göre filtrelemek için iş işlevlerini iş tipleriyle birlikte kullanabilirsiniz. **Uygunluk kuralları** sayfasında uygunluk kuralları oluşturarak iş işlevlerini ve iş türlerini, maaş planları ile ilişkilendirebilirsiniz. Bir uygunluk kuralı aracılığıyla tanımlamış olduğunuz belirli bir iş türü ve iş işlevine uygulanacak bir diz seviyeyi bir ücret planına iliştirebilirsiniz. (Bu özellikler hem sabit maaş planları hem de değişken maaş planları için geçerlidir.) Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş işlevlerini kullanmayı planlıyorsanız, işleri ayarlamadan önce iş işlevlerini ayarlamalısınız. Aşağıdaki tablo iş işlevlerine bazı örnekleri gösterir.

| İş           | İş işlevi         |
|---------------|----------------------|
| Satış yöneticisi | Orta düzey Yönetici    |
| Muhasebeci    | Profesyoneller        |

İş işlevlerini, **İş işlevleri** sayfasını kullanarak yönetirsiniz. **İş işlevleri** sayfası üzerinde, bir kimlik saptama kodu ve iş işlevi için kısa bir açıklama girersiniz.

## <a name="job-tasks"></a>İş görevleri
İş görevleri, bir iş için bir konumda olan bir çalışanın tamamlaması gereken temel görevleri açıklar. Aynı iş görevi, birden fazla işe ve bu iş görevlerini kullanan iş pozisyonlarına eklenebilir. Aşağıdaki tablo iş görevlerinin bazı örneklerini gösterir.

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
<li><strong>Performans incelemesi</strong> – Her bir satış personelinin performansını gözden geçirin.</li>
<li><strong>Devamsızlık incelemesi</strong> – Her bir satış personelinin devamsızlık taleplerini veya kayıtlarını onaylayın veya reddedin.</li>
</ul></td>
</tr>
<tr class="even">
<td>Muhasebeci</td>
<td><strong>FIN-Report</strong> – Finans müdürüne haftalık mali raporlar sunun.</td>
</tr>
</tbody>
</table>

**İş görevleri** sayfasını kullanarak iş görevlerini yönetirsiniz. **İş görevleri** sayfası üzerinde, iş görevi için kısa bir açıklama ve ad girin. İsteğe bağlı olarak **Not** alanında ek bilgiler girebilirsiniz. Belirli bir iş için notlar, burada girmiş olduğunuz notları değiştirmeden güncelleştirilebilir.

## <a name="areas-of-responsibility"></a>Sorumluluk alanları
Bir pozisyondaki çalışanın o iş için sorumlu olacağı iş rollerini, süreçleri ve ürünleri belirtmek üzere sorumluluk alanlarını kullanırsınız. Örneğin, "Muhasebeci" olarak adlandırılan bir iş için, sorumluluk alanlarından biri "Ürün A için mali raporlama" olabilir. Arama işlevi ile bulabileceğiniz **Sorumluluk alanları** sayfasını kullanarak sorumluluk alanlarını yönetirsiniz. **Sorumluluk alanları** sayfasında, sorumluluk için bir isim ve açıklama girin. İsteğe bağlı olarak **Not** alanında ek bilgiler girebilirsiniz. Belirli bir iş için notlar, burada girmiş olduğunuz notları değiştirmeden güncelleştirilebilir.

## <a name="steps-for-creating-a-job"></a>Bir iş oluşturma adımları
Yeni bir iş oluşturmaya ilişkin adım adım yordam için [Yeni işler tanımlama](../fin-and-ops/hr/tasks/define-new-jobs.md) konusuna başvurun. 

