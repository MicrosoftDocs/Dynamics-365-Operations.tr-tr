---
title: "Elektronik raporlama yapılandırma yaşam döngüsünü yönetin"
description: "Bu konu, Microsoft Dynamics 365 for Operations çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Elektronik raporlama yapılandırma yaşam döngüsünü yönetin

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Operations çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.

<a name="overview"></a>Özet
--------

Elektronik raporlama (ER), Microsoft Dynamics 365 for Operations'da yasal olarak gerekli ve ülkeye özel elektronik belgeleri destekleyen bir motorudur. Genel olarak, ER tek bir elektronik belge için bir yeteneğin aşağıdaki görevleri gerçekleştirdiğini varsayar. Daha fazla bilgi için bkz: [Elektronik raporlamaya genel bakış](general-electronic-reporting.md).

-   Elektronik belge için bir şablon tasarlayın:
    -   Belgede sunulabilen gerekli veri kaynaklarını tanımlayın:
        -   Temel Dynamics 365 for Operations verileri (veri tabloları, veri varlıkları, sınıflar vb. gibi ).
        -   İşlem belirli özellikler (yürütme tarihi ve saati ve saat dilimi, vb. gibi).
        -   Kullanıcı giriş parametreleri (çalışma zamanı sırasında son kullanıcı tarafından belirtilen).
    -   Son belge biçimini belirtmek için gerekli belgele öğelerini ve topolojilerini tanımlayın.
    -   Seçili veri kaynaklarından istenen veri akışını (veri kaynağı bağlantıları aracılığıyla belge biçimi bileşenlerine) tanımlanan belge öğelerine yapılandırın ve işlem denetim mantığını belirtin.
-   Diğer Dynamics 365 for Operations örneklerinde de kullanılabilecek bir şablon hazırlayın:
    -   Dynamics 365 for Operations uygulamasında oluşturulmuş bir belge şablonunu ER yapılandırmasına dönüştürün ve yapılandırmayı geçerli Dynamics 365 for Operations örneğinden yerel olarak veya LCS içinde depolanabilen bir XML paketi halinde dışa aktarın.
    -   ER yapılandırmasını Dynamics 365 for Operations belge şablonuna dönüştürün.
    -   Yerel olarak ve LCS içinde depolanan bir XML paketini geçerli Dynamics 365 for Operations örneğine aktarın.
-   Bir elektronik belge şablonunu özelleştirin:
    -   LCS'den bir şablonu ER yapılandırması olarak geçerli Dynamics 365 for Operations örneğine getirin.
    -   Bir ER yapılandırmasının özel sürümünü tasarlayın ve taban sürüme bir referans verin.
-   Şablonu belirli bir iş süreciyle Dynamics 365 for Operations içinde kullanılabilir olacak şekilde tümleştirin:
    -   Dynamics 365 for Operations'ın işlemle ilgili bir parametrede ilgili yapılandırmaya başvurarak bir ER yapılandırmasını kullanmaya başlayabileceği şekilde ayarları yapılandırın. (Örneğin, faturaları işlemek için elektronik ödeme ileti oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde ER yapılandırmasına başvurun).
-   Belirli bir iş sürecinde şablon kullanın:
    -   Belirli bir iş işleminde ER yapılandırmasını çalıştırın. Örneğin, ER yapılandırmasına referans gösteren bir ödeme yöntemi seçildiğinde faturaları işlemek için bir ödeme yöntemi iletisi oluşturmak için.

## <a name="concepts"></a>Kavramlar
Aşağıdaki roller ve ilgili etkinlikler ER yapılandırma yaşam döngüsü ile ilişkilendirilmiştir.

| Rol                                       | Faaliyetler                                                      | Açıklama                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektronik raporlama işlev danışmanı | ER bileşenleri oluşturun ve yönetin (modeller ve biçimler).           | ER etki alanına özgü veri modellerini tasarlayan, elektronik belgeler için gerekli şablonları tasarlayan ve bunları uygun şekilde bağlayan işadamı.                                                                           |
| Elektronik raporlama geliştirici             | Veri modeli eşlemeleri oluşturun ve yönetin.                          | Gerekli Dynamics 365 for Operations veri kaynaklarını seçen ve bunları ER etki alanına özgü veri modellerine bağlayan bir Dynamics 365 for Operations uzmanı.                                                                 |
| Muhasebe gözetmeni                      | ER yapılarına başvuran süreçle ilgili ayarları yapılandırın. | Örneğin, bir ER yapılandırmasının ayarlarının faturaların işlenmesi için elektronik ödeme iletisi oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde kullanılmasına izin veren bir **Muhasebe gözetmeni** rolü. |
| Borç hesapları ödeme memuru            | ER yapılarını belirli bir iş sürecinde kullanın.                | Örneğin, belirli bir ödeme yöntemi için yapılandırılan ER biçimine göre faturaların işlenmesi için elektronik ödeme iletileri oluşturulmasına izin veren **Borç hesapları ödeme memuru** rolü.           |

## <a name="er-configuration-development-lifecycle"></a>ER yapılandırması geliştirme yaşam döngüsü
Aşağıdaki ER İle ilgili nedenlerden dolayı, geliştirme ortamı'ndaki ER yapılandırmalarını ayrı Dynamics 365 for Operations örnekleri olarak tasarlamanızı öneririz:

-   **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar yapılandırmaları düzenleyebilir ve sınama amacıyla bunları çalıştırabilir. Bu senaryo iş verilerine ve Dynamics 365 for Operations örneğinin performansına zararı olabilecek sınıflar ve tabloların çağrı yöntemlerine neden olabilir.
-   ER yapılandırmasının ER veri kaynağı olarak sınıflar ve tabloların çağrı yöntemleri Dynamics 365 for Operations giriş noktaları ve kayıtlı şirket içeriği ile sınırlı değildir. Bu nedenle, **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar iş açısından hassas verilere erişebilir.

Geliştirme ortamı içinde tasarlanan ER yapılandırmaları, yapılandırma değerlendirmesi (uygun işlem tümleştirme, sonuçların doğruluğu ve performans) ve kalite güvencesi (role dayalı erişim hakları doğruluğu ve görev ayrımı gibi) için test ortamı'na yüklenebilir. ER yapılandırması değişimi sağlayan özellikler bu amaçla kullanılabilir. Son olarak, kanıtlanan ER yapılandırmaları hizmet aboneleri ile paylaşılmak için LCS'ye veya iç kullanım için üretim ortamına yüklenebilir, aşağıdaki resimlerde gösterildiği gibi. ![ER yapılandırma yaşam döngüsü](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)




