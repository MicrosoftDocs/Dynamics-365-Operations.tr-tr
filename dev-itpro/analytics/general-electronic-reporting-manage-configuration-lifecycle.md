---
title: "Elektronik raporlama yapılandırma yaşam döngüsünü yönetin"
description: "Bu konu, kullanım ömrü boyunca elektronik işlemler çözüm için Microsoft Dynamics 365 (ER) yapılandırmaları raporlama yönetme yöntemi açıklanmıştır."
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

Bu konu, kullanım ömrü boyunca elektronik işlemler çözüm için Microsoft Dynamics 365 (ER) yapılandırmaları raporlama yönetme yöntemi açıklanmıştır.

<a name="overview"></a>Özet
--------

Elektronik raporlama (ER), Microsoft Dynamics 365 for Operations'da yasal olarak gerekli ve ülkeye özel elektronik belgeleri destekleyen bir motorudur. Genel olarak, ER tek bir elektronik belge için bir yeteneğin aşağıdaki görevleri gerçekleştirdiğini varsayar. Daha fazla bilgi için bkz: [elektronik bildirimine genel bakış](general-electronic-reporting.md).

-   Elektronik belge için bir şablon tasarlayın:
    -   Belgede sunulabilen gerekli veri kaynaklarını tanımlayın:
        -   İşlem verileri, veri tabloları, veri varlıkları ve sınıfları gibi temel Dynamics 365.
        -   Yürütme tarih ve saati ve saat dilimi gibi özel işlem özellikleri.
        -   Çalıştırma sırasında son kullanıcı tarafından belirtilen kullanıcı giriş parametreleri.
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
    -   Dynamics 365 for Operations'ın işlemle ilgili bir parametrede ilgili yapılandırmaya başvurarak bir ER yapılandırmasını kullanmaya başlayabileceği şekilde ayarları yapılandırın. Örneğin, faturalar işlemek için bir elektronik Ödeme iletisi oluşturmak için belirli bir hesap borç ödeme yöntemi ER yapılandırmasında bakın.
-   Belirli bir iş sürecinde şablon kullanın:
    -   Belirli iş sürecinde ER yapılandırma çalıştırın. Örneğin, faturalar ER yapılandırma başvuran bir ödeme yöntemi zaman işlemek için bir elektronik Ödeme iletisi oluşturmak için seçilir.

## <a name="concepts"></a>Kavramlar
Aşağıdaki roller ve ilgili etkinlikler ER yapılandırma ömrü ile ilişkilidir.

| Rol                                       | Faaliyetler                                                      | Açıklama                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektronik raporlama işlev danışmanı | ER bileşenleri oluşturun ve yönetin (modeller ve biçimler).           | ER etki alanına özgü veri modelleri, elektronik belgeler için gerekli şablon tasarımları tasarlayan ve buna uygun olarak bağlayan bir iş kişi.                                                                           |
| Elektronik raporlama geliştirici             | Veri modeli eşlemeleri oluşturun ve yönetin.                          | İşlemler veri kaynakları için gerekli Dynamics 365 seçer ve bunları ER etki alanına özgü veri modelleri için bağlar işlemleri uzmanı için Dynamics 365.                                                                 |
| Muhasebe gözetmeni                      | ER yapılarına başvuran süreçle ilgili ayarları yapılandırın. | Örneğin, bir **hesap yönetici** ER yapılandırma ayarlarını belirli bir hesap borç ödeme yönteminde faturaları işlemek için bir elektronik Ödeme iletisi oluşturmak için kullanılacak veren rol. |
| Borç hesapları ödeme memuru            | ER yapılarını belirli bir iş sürecinde kullanın.                | Örneğin, bir **hesaplarına borç ödemeleri memuru** elektronik Ödeme iletileri işleme faturalar için oluşturulacak veren rol tabanlı özel bir ödeme yöntemi için yapılandırılmış ER biçimini.           |

## <a name="er-configuration-development-lifecycle"></a>ER yapılandırması geliştirme yaşam döngüsü
Aşağıdaki ER İle ilgili nedenlerden dolayı, geliştirme ortamı'ndaki ER yapılandırmalarını ayrı Dynamics 365 for Operations örnekleri olarak tasarlamanızı öneririz:

-   **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar yapılandırmaları düzenleyebilir ve sınama amacıyla bunları çalıştırabilir. Bu senaryo iş verilerine ve Dynamics 365 for Operations örneğinin performansına zararı olabilecek sınıflar ve tabloların çağrı yöntemlerine neden olabilir.
-   ER yapılandırmasının ER veri kaynağı olarak sınıflar ve tabloların çağrı yöntemleri Dynamics 365 for Operations giriş noktaları ve kayıtlı şirket içeriği ile sınırlı değildir. Bu nedenle, **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar iş açısından hassas verilere erişebilir.

Yapılandırma değerlendirme (uygun işlem tümleştirme, sonuçları ve performans doğruluk) ve rol tabanlı erişim haklarının doğruluğu ve harçlar, segregation gibi kalite güvencesi için test ortamı geliştirme ortamında tasarlanan ER yapılandırmaları yüklenebilir. ER yapılandırma değişim sağlayan özellikler bu amaçla kullanılabilir. Son olarak, kanıtlanmış ER yapılandırmaları nerede hizmet aboneleri ile paylaşılabilir, LCS, veya gibi aşağıdaki çizimde gösterildiği dahili kullanım için üretim ortamına yüklenemez. ![ER yapılandırma ömrü](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)


