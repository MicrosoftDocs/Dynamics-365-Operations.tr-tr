---
title: Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme
description: Bu konu, Microsoft Dynamics 365 Finance çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1a4741784103817c270c4c7f730753ba59a327d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682635"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Finance çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.

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

    - Uygulamada oluşturulmuş bir belge şablonunu ER yapılandırmasına dönüştürün ve yapılandırmayı geçerli örnekten yerel olarak veya LCS içinde depolanabilen XML paketi halinde dışa aktarın.
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

Geliştirme ortamı içinde tasarlanan ER yapılandırmaları, yapılandırma değerlendirmesi (uygun işlem tümleştirme, sonuçların doğruluğu ve performans) ve kalite güvencesi (role dayalı erişim hakları doğruluğu ve görev ayrımı gibi) için test ortamı'na yüklenebilir. ER yapılandırması değişimi sağlayan özellikler bu amaçla kullanılabilir. Son olarak, kanıtlanan ER yapılandırmaları hizmet aboneleri ile paylaşılmak için LCS'ye veya iç kullanım için üretim ortamına yüklenebilir, aşağıdaki resimlerde gösterildiği gibi.

![ER yapılandırma yaşam döngüsü](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
