---
title: Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.
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
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5724ba62bfb2c6e75ae895dc9285966c25f387a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553854"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Finance and Operations çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.

## <a name="overview"></a>Genel bakış

Elektronik raporlama (ER), Microsoft Dynamics 365 for Finance and Operations'te gerekli yasal ve ülkeye özel elektronik belgeleri destekleyen bir motorudur. Genel olarak, ER tek bir elektronik belge için bir yeteneğin aşağıdaki görevleri gerçekleştirdiğini varsayar. Daha fazla bilgi için bkz: [Elektronik raporlamaya genel bakış](general-electronic-reporting.md).

- Elektronik belge için bir şablon tasarlayın:

    - Belgede sunulabilen gerekli veri kaynaklarını tanımlayın:

        - Temel Finance and Operations verileri (veri tabloları, veri varlıkları, sınıflar vb. gibi ).
        - İşlem belirli özellikler (yürütme tarihi ve saati ve saat dilimi, vb. gibi).
        - Kullanıcı giriş parametreleri (çalışma zamanı sırasında son kullanıcı tarafından belirtilen).

    - Son belge biçimini belirtmek için gerekli belgele öğelerini ve topolojilerini tanımlayın.
    - Seçili veri kaynaklarından istenen veri akışını (veri kaynağı bağlantıları aracılığıyla belge biçimi bileşenlerine) tanımlanan belge öğelerine yapılandırın ve işlem denetim mantığını belirtin.

- Diğer Finance and Operations örneklerinde de kullanılabilecek bir şablon hazırlayın:

    - Finance and Operations uygulamasında oluşturulmuş bir belge şablonunu ER yapılandırmasına dönüştürün ve yapılandırmayı geçerli Finance and Operations örneğinden yerel olarak veya LCS içinde depolanabilen XML paketi halinde dışa aktarın.
    - ER yapılandırmasını Finance and Operations belge şablonuna dönüştürün.
    - Yerel olarak ve LCS içinde depolanan bir XML paketini geçerli Finance and Operations örneğine aktarın.

- Bir elektronik belge şablonunu özelleştirin:

    - LCS'den bir şablonu ER yapılandırması olarak geçerli Finance and Operations örneğine getirin.
    - Bir ER yapılandırmasının özel sürümünü tasarlayın ve taban sürüme bir referans verin.

- Şablonu belirli bir iş süreciyle Finance and Operations içinde kullanılabilir olacak şekilde tümleştirin:

    - Finance and Operations'ın işlemle ilgili bir parametrede ilgili yapılandırmaya başvurarak bir ER yapılandırmasını kullanmaya başlayabileceği şekilde ayarları yapılandırın. (Örneğin, faturaları işlemek için elektronik ödeme ileti oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde ER yapılandırmasına başvurun).

- Belirli bir iş sürecinde şablon kullanın:

    - Belirli bir iş işleminde ER yapılandırmasını çalıştırın. Örneğin, ER yapılandırmasına referans gösteren bir ödeme yöntemi seçildiğinde faturaları işlemek için bir ödeme yöntemi iletisi oluşturmak için.

## <a name="concepts"></a>Kavramlar
Aşağıdaki roller ve ilgili etkinlikler ER yapılandırma yaşam döngüsü ile ilişkilendirilmiştir.

| Rol                                       | Faaliyetler                                                      | Açıklama |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Elektronik raporlama işlev danışmanı | ER bileşenleri oluşturun ve yönetin (modeller ve biçimler).           | ER etki alanına özgü veri modellerini tasarlayan, elektronik belgeler için gerekli şablonları tasarlayan ve bunları uygun şekilde bağlayan işadamı. |
| Elektronik raporlama geliştirici             | Veri modeli eşlemeleri oluşturun ve yönetin.                          | Gerekli Finance and Operations veri kaynaklarını seçen ve bunları ER etki alanına özgü veri modellerine bağlayan bir Finance and Operations uzmanı. |
| Muhasebe gözetmeni                      | ER yapılarına başvuran süreçle ilgili ayarları yapılandırın. | Örneğin, bir ER yapılandırmasının ayarlarının faturaların işlenmesi için elektronik ödeme iletisi oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde kullanılmasına izin veren bir **Muhasebe gözetmeni** rolü. |
| Borç hesapları ödeme memuru            | ER yapılarını belirli bir iş sürecinde kullanın.                | Örneğin, belirli bir ödeme yöntemi için yapılandırılan ER biçimine göre faturaların işlenmesi için elektronik ödeme iletileri oluşturulmasına izin veren **Borç hesapları ödeme memuru** rolü. |

## <a name="er-configuration-development-lifecycle"></a>ER yapılandırması geliştirme yaşam döngüsü
Aşağıdaki ER İle ilgili nedenlerden dolayı, geliştirme ortamı'ndaki ER yapılandırmalarını ayrı Finance and Operations örnekleri olarak tasarlamanızı öneririz:

- **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar yapılandırmaları düzenleyebilir ve sınama amacıyla bunları çalıştırabilir. Bu senaryo iş verilerine ve Finance and Operations örneğinin performansına zararı olabilecek sınıflar ve tabloların çağrı yöntemlerine neden olabilir.
- ER yapılandırmasının ER veri kaynağı olarak sınıflar ve tabloların çağrı yöntemleri Finance and Operations giriş noktaları ve kayıtlı şirket içeriği ile sınırlı değildir. Bu nedenle, **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar iş açısından hassas verilere erişebilir.

Geliştirme ortamı içinde tasarlanan ER yapılandırmaları, yapılandırma değerlendirmesi (uygun işlem tümleştirme, sonuçların doğruluğu ve performans) ve kalite güvencesi (role dayalı erişim hakları doğruluğu ve görev ayrımı gibi) için test ortamı'na yüklenebilir. ER yapılandırması değişimi sağlayan özellikler bu amaçla kullanılabilir. Son olarak, kanıtlanan ER yapılandırmaları hizmet aboneleri ile paylaşılmak için LCS'ye veya iç kullanım için üretim ortamına yüklenebilir, aşağıdaki resimlerde gösterildiği gibi.

![ER yapılandırma yaşam döngüsü](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)
