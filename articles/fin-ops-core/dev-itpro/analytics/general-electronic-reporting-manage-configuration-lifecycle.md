---
title: Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme
description: Bu konu, Dynamics 365 Finance için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8b61082cf17707c952b6e07613769a671c349bb8fa92c21e3fe8524ef62dcb2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767791"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme

[!include [banner](../includes/banner.md)]

Bu konu, Dynamics 365 Finance için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.

## <a name="overview"></a>Genel bakış

Elektronik raporlama (ER), gerekli yasal ve ülkeye özel elektronik belgeleri destekleyen bir motorudur. Genel olarak, ER tek bir elektronik belge için bir yeteneğin aşağıdaki görevleri gerçekleştirdiğini varsayar. Daha fazla bilgi için bkz. [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md).

- Elektronik belge için bir şablon tasarlayın:

    - Belgede sunulabilen gerekli veri kaynaklarını tanımlayın:

        - Temel veriler (veri tabloları, veri varlıkları, sınıflar vb. gibi ).
        - İşlem belirli özellikler (yürütme tarihi ve saati ve saat dilimi, vb. gibi).
        - Kullanıcı giriş parametreleri (çalışma zamanı sırasında son kullanıcı tarafından belirtilen).

    - Son belge biçimini belirtmek için gerekli belgele öğelerini ve topolojilerini tanımlayın.
    - Seçili veri kaynaklarından istenen veri akışını (veri kaynağı bağlantıları aracılığıyla belge biçimi bileşenlerine) tanımlanan belge öğelerine yapılandırın ve işlem denetim mantığını belirtin.

- Diğer örneklerde de kullanılabilecek bir şablonu kullanılır hale getirin:

    - Uygulamada oluşturulmuş bir belge şablonunu ER yapılandırmasına dönüştürün ve yapılandırmayı geçerli örnekten yerel olarak veya Lifecycle Services (LCS) içinde depolanabilen XML paketi halinde dışa aktarın.
    - ER yapılandırmasını uygulama belge şablonuna dönüştürün.
    - Yerel olarak ve LCS içinde depolanan bir XML paketini geçerli örneğe aktarın.

- Bir elektronik belge şablonunu özelleştirin:

    - Bir LCS şablonunu ER yapılandırması olarak geçerli örneğe getirin.
    - Bir ER yapılandırmasının özel sürümünü tasarlayın ve taban sürüme bir referans verin.

- Bir şablonu belirli bir iş süreciyle uygulama içinde kullanılabilir olacak şekilde tümleştirin:

    - Uygulamanın işlemle ilgili bir parametrede ilgili yapılandırmaya başvurarak bir ER yapılandırmasını kullanmaya başlayabileceği şekilde ayarları yapılandırın. (Örneğin, faturaları işlemek için elektronik ödeme ileti oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde ER yapılandırmasına başvurun).

- Belirli bir iş sürecinde şablon kullanın:

    - Belirli bir iş işleminde ER yapılandırmasını çalıştırın. Örneğin, ER yapılandırmasına referans gösteren bir ödeme yöntemi seçildiğinde faturaları işlemek için bir ödeme yöntemi iletisi oluşturmak için.

## <a name="concepts"></a>Kavramlar
Aşağıdaki roller ve ilgili etkinlikler ER yapılandırma yaşam döngüsü ile ilişkilendirilmiştir.

| Rol                                       | Faaliyetler                                                      | Açıklama |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Elektronik raporlama işlev danışmanı | ER bileşenleri oluşturun ve yönetin (modeller ve biçimler).           | ER etki alanına özgü veri modellerini tasarlayan, elektronik belgeler için gerekli şablonları tasarlayan ve bunları uygun şekilde bağlayan işadamı. |
| Elektronik raporlama geliştirici             | Veri modeli eşlemeleri oluşturun ve yönetin.                          | Gerekli Finance veri kaynaklarını seçen ve bunları ER etki alanına özgü veri modellerine bağlayan uzman. |
| Muhasebe gözetmeni                      | ER yapılarına başvuran süreçle ilgili ayarları yapılandırın. | Örneğin, bir ER yapılandırmasının ayarlarının faturaların işlenmesi için elektronik ödeme iletisi oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde kullanılmasına izin veren bir **Muhasebe gözetmeni** rolü. |
| Borç hesapları ödeme memuru            | ER yapılarını belirli bir iş sürecinde kullanın.                | Örneğin, belirli bir ödeme yöntemi için yapılandırılan ER biçimine göre faturaların işlenmesi için elektronik ödeme iletileri oluşturulmasına izin veren **Borç hesapları ödeme memuru** rolü. |

## <a name="er-configuration-development-lifecycle"></a>ER yapılandırması geliştirme yaşam döngüsü
Aşağıdaki ER ile ilgili nedenlerden dolayı, ER yapılandırmalarını geliştirme ortamında ayrı Finance and Operations kurulumları olarak tasarlamanızı öneririz:

- **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar yapılandırmaları düzenleyebilir ve sınama amacıyla bunları çalıştırabilir. Bu senaryo iş verilerine ve örneğin performansına zararı olabilecek sınıflar ve tabloların çağrı yöntemlerine neden olabilir.
- ER yapılandırmasının ER veri kaynağı olarak sınıflar ve tabloların çağrı yöntemleri giriş noktaları ve oturum açan şirket içeriği ile sınırlı değildir. Bu nedenle, **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar iş açısından hassas verilere erişebilir.

Geliştirme ortamı içinde tasarlanan ER yapılandırmaları, yapılandırma değerlendirmesi (uygun işlem tümleştirme, sonuçların doğruluğu ve performans) ve kalite güvencesi (role dayalı erişim hakları doğruluğu ve görev ayrımı gibi) için test ortamına [yüklenebilir](#data-persistence-consideration). ER yapılandırması değişimi sağlayan özellikler bu amaçla kullanılabilir. Kanıtlanan ER yapılandırmaları hizmet aboneleri ile paylaşılmak için LCS'ye veya dahili kullanım için üretim ortamına [aktarılabilir](#data-persistence-consideration).

![ER yapılandırma yaşam döngüsü.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Veri kalıcılığının dikkate alınması

Bir ER [yapılandırmasının](general-electronic-reporting.md#Configuration) farklı [sürümlerini](general-electronic-reporting.md#component-versioning) Finance kurulumunuza ayrı ayrı [aktarabilirsiniz](tasks/er-import-configuration-lifecycle-services.md). ER yapılandırmasının yeni bir sürümü içeri aktarıldığında sistem, bu yapılandırmanın taslak sürümünün içeriğini denetler:

- Geçerli Finance kurulumunda içe aktarılan sürüm bu yapılandırmanın en yüksek sürümünden daha düşükse, bu yapılandırmanın taslak sürümünün içeriği değişmeden kalır.
- İçeri aktarılan sürüm bu yapılandırmanın geçerli Finance kurulumundaki diğer herhangi bir sürümünden daha yüksek olduğunda, içeri aktarılan sürümün içeriği bu yapılandırmanın taslak sürümüne kopyalanır ve son tamamlanan sürümü düzenlemeye devam etmenize olanak tanır.

Bu yapılandırmanın sahibi etkinleştirilmiş olan yapılandırma [sağlayıcısıysa](general-electronic-reporting.md#Provider), bu yapılandırmanın taslak sürümü **Yapılandırmalar** sayfasının **Sürümler** hızlı sekmesinde size gösterilir (**Kuruluş yönetimi** > **Elektronik raporlama** > **Yapılandırmalar**). Yapılandırmanın taslak sürümünü seçebilir ve ilgili ER tasarımcısını kullanarak içeriğini [değiştirebilirsiniz](er-quick-start2-customize-report.md#ConfigureDerivedFormat). Bir ER yapılandırmasının taslak sürümünü düzenlediğinizde içeriği artık geçerli Finance kurulumundaki yapılandırmanın en yüksek sürümünün içeriğiyle eşleşmez. Değişikliklerinizin kaybolmasını önlemek için sistem, bu yapılandırmanın sürümünün geçerli Finance kurulumundaki yapılandırmanın en yüksek sürümünden yüksek olduğundan, içeri aktarmanın devam edemediğine ilişkin bir hata görüntüler. Bu durumda, örneğin **X** biçim yapılandırmasıyla **'X' biçimi sürümü tamamlanmadı** hatası görüntülenir.

Taslak sürümünde yaptığınız değişiklikleri geri almak için, **Sürümler** hızlı sekmesinde, Finance içindeki en yüksek tamamlanmış veya paylaşılan sürümü ve ardından **Bu sürümü al** seçeneğini belirleyin. Seçili sürümün içeriği taslak sürümüne kopyalanır.

## <a name="applicability-consideration"></a>Uygulanabilirlik değerlendirmesi

ER yapılandırmasının yeni bir sürümünü tasarladığınızda diğer yazılım bileşenlerinde bunun [bağımlılığını](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) tanımlayabilirsiniz. Bu adım, bu yapılandırmanın sürümünü bir ER havuzundan veya harici bir XML dosyasından indirmeyi ve bu sürümün daha fazla kullanımını denetlemek için bir önkoşul olarak kabul edilir. ER yapılandırmasının yeni bir sürümünü içeri aktarmayı denediğinizde sistem, sürümün içeri aktarılıp aktarılamayacağını denetlemek için yapılandırılmış önkoşulları kullanır.

Bazı durumlarda, ER yapılandırmalarının yeni sürümlerini içeri aktardığınızda sistemin yapılandırılmış önkoşulları yok sayması gerekebilir. İçeri aktarma sırasında sistemin önkoşulları yok sayması için şu adımları izleyin.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **İçeri aktarma sırasında ürün güncelleştirmeleri ve sürüm önkoşulu denetimini atla** seçeneğini **Evet** olarak ayarlayın.

    > [!NOTE]
    > Bu parametre kullanıcıya özel ve şirkete özeldir.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[ER yapılandırmalarının diğer bileşenlere bağımlılığını tanımlama](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
