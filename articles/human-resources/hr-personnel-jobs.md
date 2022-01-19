---
title: İşin bileşenlerini ayarlama
description: Bu konu, bir işin içerebileceği konsept öğelerini açıklar ve bu öğeleri kuruluşunuzda nasıl kullanabileceğiniz hakkında örnekler sağlar.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4aa7369c84836154b8217a5b70267021f4028b1
ms.sourcegitcommit: 4f84540e6121ca3d5ae52ee07e414116d423cefa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/03/2022
ms.locfileid: "7948487"
---
# <a name="set-up-the-components-of-a-job"></a>İşin bileşenlerini ayarlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, bir işin içerebileceği konsept öğelerini açıklar ve bu öğeleri kuruluşunuzda nasıl kullanabileceğiniz hakkında örnekler sağlar. 

Yeni işler oluşturabilmeden önce, bazı referans bilgileri ayarlamalısınız. Sadece bir isme sahip bir iş oluşturabilirsiniz. Ancak, örneğin bir iş unvanı gibi ek bilgiler ekleyerek, işe atanmış olan konumlara varsayılan değerler sağlarsınız. Ek olarak, girdiğiniz bazı bilgiler maaş planlarını belirli işlere filtrelemek için kullanılabilir. Maaş planlarını belirli bir işe filtrelemek için uygunluk ayarlamak istiyorsanız, iş işlevleri ve iş görevlerini, işleri ayarlamadan önce ayarlamalısınız. Bu varsayılan değerleri mevcut bulundurarak, işe konumlar eklerken zaman kazanırsınız. 

Bazı iş ayrıntıları, örneğin iş unvanı, türü ve işlevi, yürürlük tarihine sahiptir. Bugün bir iş oluşturursanız ancak bunları daha sonra bu ayrıntıları eklemezseniz ve daha sonra işe oluşturulma tarihinde bakarsanız, bu ayrıntılar görüntülenmez. Bu nedenle, bu başvuru bilgilerinin bazılarını, ihtiyaç duymadan oluşturmanız gerekir. Bu sayede, yeni işlere bilgileri, onları oluştururken ekleyebilirsiniz.

## <a name="job-titles"></a>İş başlıkları
İşler oluşturmadan önce, bu işler için unvanlar ayarlamanız gerekir. Pozisyonlar, iş unvanlarını, pozisyonların ilişkili olduğu işlerden devralır. 

Arama özelliğini kullanarak açabileceğiniz **Unvanlar** sayfasını kullanarak iş unvanlarını korumak. **Unvanlar** sayfasında, işlerinizde kullanmayı planladığınız unvanları girin.

## <a name="job-types"></a>İş türleri
Benzer işleri kategorilere gruplamak için iş türlerini kullanın. İş türleri, zorunlu değildir. Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş türlerini kullanmayı planlıyorsanız, işleri ayarlamadan önce iş tiplerini ayarlamalısınız. İş türlerine bazı örnekler tam zamanlı ve yarı zamanlı veya maaşlı ve saatlik ödemelidir. **İş türleri** sayfasını kullanarak iş türlerini yönetirsiniz. **İş türleri** sayfası üzerinde, iş türü için kısa bir açıklama ve ad girin. **Muaf durumu** alanında, Adil İş Standartları Yasası (FLSA) muafiyet durumunu, şu iş durumuna sahip işler için belirtmek üzere aşağıdaki seçeneklerden birini işaretleyin:

-   **Muafiyet** – İşler, FLSA kapsamı altında fazla mesai dışında tutulurlar.
-   **Muaf olmayan** – İşler, FLSA kapsamı altında fazla mesai dışında tutulmaz.
-   **Geçerli değildir** – FLSA kapsamı için geçerli değildir.

## <a name="job-family"></a>İş ailesi
Bir iş ailesi, benzer bir iş içeren ve benzer eğitim, beceriler, bilgi ve uzmanlığa gereksinim duyan bir iş grubudur. İş ailesi, **İşler** sayfasının **İş sınıflandırması** hızlı sekmesinde ve **Tüm pozisyonlar** sayfasının **Genel** hızlı sekmesinde bir işle bağlantılı olabilir. İş aileleri, işletmeniz ve raporlama gereksinimlerinize bağlı olarak geniş veya özel olabilir. Geniş çaplı iş ailelerine örnek olarak, **Nitelikli işçilik** ve **Yetenek gerektirmeyen işçilik** verilebilir. Özel iş ailelerine örnek olarak **Muhasebe**, **Üretim** ve **Satış** verilebilir.

Arama özelliğini kullanarak açabileceğiniz **İş ailesi** sayfasını kullanarak iş ailelerini yönetin. **İş ailesi** sayfasında, aile için benzersiz bir ad girin ve işleriniz için kullanmayı planladığınız ayrıntılı açıklamayı girin.

## <a name="job-functions"></a>İş işlevleri
İş işlevleri, yüksek seviye işlevsellik kategorileri açıklar ve yüksek düzey görevleri ilişkilendirir. İş işlevleri, zorunlu değildir. Tazminat planlarını belirli işlere göre filtrelemek için iş işlevlerini iş tipleriyle birlikte kullanabilirsiniz. **Uygunluk kuralları** sayfasında uygunluk kuralları oluşturarak iş işlevlerini ve iş türlerini, maaş planları ile ilişkilendirebilirsiniz. Bir uygunluk kuralı aracılığıyla tanımlamış olduğunuz belirli bir iş türü ve iş işlevine uygulanacak bir diz seviyeyi bir ücret planına iliştirebilirsiniz. (Bu özellikler hem sabit maaş planları hem de değişken maaş planları için geçerlidir.) Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş işlevlerini kullanmayı planlıyorsanız, işleri ayarlamadan önce iş işlevlerini ayarlamalısınız. Aşağıdaki tablo iş işlevlerine bazı örnekleri gösterir.

| İş           | İş işlevi         |
|---------------|----------------------|
| Satış yöneticisi | Orta düzey Yönetici    |
| Muhasebeci    | Profesyoneller        |

İş işlevlerini, **İş işlevleri** sayfasını kullanarak yönetirsiniz. **İş işlevleri** sayfası üzerinde, bir kimlik saptama kodu ve iş işlevi için kısa bir açıklama girersiniz.

## <a name="compensation"></a>Maaş
Bir projede pozisyona sahip bir çalışana sabit ücret planı atamak için, iş üzerinde ücret düzeylerini ayarlamanız gerekir. Ücret yapısında (ücret ızgarası) minimum, orta nokta ve maksimum tutarlar ayarlandığında, **Ücret düzeyi** kullanılır. Sabit ücret planı oluşturulduğunda, ücret yapısı seçilir. Ücret yapısı ücret düzeyini de içerir. Bir çalışan için sabit bir ücret planı seçerken, seçim için kullanılabilen ücret düzeyleri, çalışanın pozisyonunun ilişkili olduğu işe bağlıdır. Ücret ayarlama hakkında daha fazla bilgi için bkz. [Ücret planları](hr-compensation-overview.md).

## <a name="job-skills"></a>İş yetenekleri
İş yetenekleri, bir işi gerçekleştirmek için gerekli olan yetenekleri açıklar. Yetenek düzeyinin her iş yeteneğiyle ilişkilendirilmesi gerekir. Yetenek düzeyleri kullanıcı tanımlıdır. Bunlar yetenek için gerekli olan bilgi düzeyini veya yeterliliği gösterir. Örneğin, şirketler 1-5 gibi sayısal düzeyler ayarlayabilir, burada **1** acemi ve **5** uzman düzeyi belirtir. Alternatif olarak, şirketler **Acemi**, **Orta** veya **Uzman** etiketli düzeyler ayarlayabilir. Yetenek düzeyi ayarlandıktan sonra, yeteneğin önem derecesi de ayarlanabilir. Örneğin, bir muhasebecinin güçlü Microsoft Excel bilgisine sahip olması gerekiyorsa, **Excel bilgisi** olarak adlandırılan bir yetenek oluşturulabilir. Yetenek düzeyi daha sonra **Orta** olarak ve önem derecesi **En çok** olarak ayarlanabilir.

Bir işteki yetenekler yetenek eşlemede kullanılabilir. Yetenek eşleme, bir iş için gerekli olan yetenek kümesini ve bir çalışanla ilişkili yetenekleri karşılaştırabilir. Daha sonra, örtüşen yetenekleri temel alan bir yüzde eşleşmesi belirleyebilir. Yetenek eşleme hakkında daha fazla bilgi edinmek için, bkz [Yetenekleri yapılandırma](hr-develop-skills.md). 

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
<li><strong>Perf-review</strong> – Her bir satış personelinin performansını gözden geçirin.</li>
<li><strong>Abs-review</strong> – Her bir satış personelinin devamsızlık taleplerini veya kayıtlarını onaylayın veya reddedin.</li>
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
Yeni bir iş oluşturmaya ilişkin adım adım yordam için [Yeni işler tanımlama](./hr-personnel-define-jobs.md) konusuna başvurun. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
