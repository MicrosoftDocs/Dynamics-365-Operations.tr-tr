---
title: Proje sözleşmelerini ve projeleri doğrudan Project Service Automation'dan Finance and Operations'a eşitleme
description: Bu konuda, proje sözleşmelerini ve projeleri doğrudan Microsoft Dynamics 365 Project Service Automation'dan Dynamics 365 Finance'a eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 76c62f3a503ff2a8c93143390fc91ef81fbf7d0f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250473"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Proje sözleşmelerini ve projeleri doğrudan Project Service Automation'dan Finance and Operations'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu projeleri Dynamics 365 Project Service Automation üzerinden Dynamics 365 Finance üzerine proje sözleşmelerini ve projeleri doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.

> [!NOTE] 
> Enterprise edition 7.3.0'ı kullanıyorsanız KB 4074835'i yüklemeniz gerekir.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation'dan Finance'e veri akışı

> [!NOTE]
> Project Service Automation'dan Finance'e tümleştirme çözümünü kullanabilmeniz için Dynamics 365 Veri tümleştirme özelliği hakkında bilgi sahibi olmanız gerekir.

Project Service Automation ile Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu; proje sözleşmeleri, projeler, proje sözleşme satırları ve proje sözleşme satırı kilometre taşları hakkındaki verilerin Project Service Automation'dan Finance'e akışına olanak tanır.

Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.

[![Project Service Automation ile Finance tümleştirmesi için veri akışı](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görevler, proje sözleşmelerini ve projeleri Project Service Automation'dan Finance'e eşitlemek için kullanılır:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Dynamics 365 Project Service Automation v2.x ile tümleştirme
- **Veri tümleştirmedeki şablonun adı:** Projeler ve sözleşmeler (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Proje sözleşmeleri - PSA'dan Fin and Ops'a
    - Projeler - PSA'dan Fin and Ops'a
    - Proje sözleşme satırları - PSA'dan Fin and Ops'a
    - Proje sözleşme satırı kilometre taşları - PSA'dan Fin and Ops'a
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Dynamics 365 Project Service Automation v3.x ile tümleştirme
Project Service Automation'da Proje sözleşme satırı kilometre taşı şablonunu etkileyen bir şema değişikliği vardır ve Project Service Automation v3.x'i Dynamics 365 ile tümleştirmek için şablonun v2 sürümünün kullanılması gerekmektedir.

- **Veri tümleştirmedeki şablonun adı:** Projeler ve Sözleşmeler (PSA 3.x'ten Fin and Ops'a) - v2
- **Projedeki görevlerin adı:**

    - Proje sözleşmeleri - PSA'dan Fin and Ops'a
    - Projeler - PSA'dan Fin and Ops'a
    - Proje sözleşme satırları - PSA'dan Fin and Ops'a
    - Proje sözleşme satırı kilometre taşları - PSA'dan Fin and Ops'a

Proje sözleşmelerinin ve projelerin eşitlemesinin yapılabilmesi için hesapları eşitlemeniz gerekir.

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation       | Finans                                                |
|----------------------------------|--------------------------------------------------------|
| Siparişler                           | Proje sözleşmesi için tümleştirme varlığı                |
| Projeler                         | Proje için tümleştirme varlığı                         |
| Sipariş satırları                      | Proje sözleşme satırı için tümleştirme varlığı           |
| Proje sözleşme satırı kilometre taşları | Proje sözleşme satırı kilometre taşı için tümleştirme varlığı |

## <a name="entity-flow"></a>Varlık akışı

Proje sözleşmeleri, Project Service Automation'da yönetilir ve Finance ile proje sözleşmeleri olarak eşitlenir. Tümleştirme şablonunun bir parçası olarak, proje sözleşmesi için Finance'te tümleştirme kaynağını ayarlayabilirsiniz.

Zaman ve malzeme projesi ile Sabit fiyatlı projeler, Project Service Automation'da yönetilir ve Finance ile proje olarak eşitlenir. Şablon tümleştirmesinin bir parçası olarak, proje sözleşmesi için Finance'te tümleştirme kaynağını ayarlayabilirsiniz.

Proje sözleşme satırları, Project Service Automation'da yönetilir ve Finance ile proje sözleşmesi faturalama kuralları olarak eşitlenir. Faturalama yöntemi varsayılan proje türünden farklıysa eşitleme işlemi sözleşme satırı projesinin proje türünü ve proje grubunu güncelleştirir.

Proje sözleşme satırı kilometre taşları, Project Service Automation'da yönetilir ve Finance ile proje sözleşmesi faturalama kuralı kilometre taşları olarak eşitlenir.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation'dan Finance'e tümleştirme çözümü

**Proje sözleşmesi kodu** alanı **Proje sözleşmeleri** sayfasındadır. Tümleştirmeyi desteklemek için, bu alan doğal ve benzersiz anahtar yapılmıştır.

Yeni bir proje sözleşmesi oluşturulduğunda, bir **Proje sözleşmesi kodu** değeri önceden mevcut değilse, bu numara serisiyle otomatik olarak oluşturulur. Değer **ORD** ve onun ardından gelen artımlı bir numara serisi ve altı karakterlik bir sonekten oluşur. Örneğin: **ORD-01022-Z4M9Q0**.

**Proje Numarası** alanı, **Projeler** sayfasındadır. Tümleştirmeyi desteklemek için, bu alan doğal ve benzersiz anahtar yapılmıştır.

Yeni bir proje oluşturulduğunda, bir **Proje Numarası** değeri önceden mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur. Değer **PRJ** ve onun ardından gelen artımlı bir numara serisi ve altı karakterlik bir sonekten oluşur. Örneğin: **PRJ-01049-CCNID0**.

Project Service Automation'dan Finance'e tümleştirme çözümü uygulanırken yükseltme komut doyası, Project Service Automation'da mevcut proje sözleşmeleri için **Proje sözleşmesi kimliği** ve mevcut projeler için **Proje Numarası** alanlarını ayarlar.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- Proje sözleşmelerinin ve projelerin eşitlemesinin yapılabilmesi için hesapları eşitlemeniz gerekir.
- Bağlantı kümenizde**msdyn\_organizationalunits**'ten **msdyn\_name \[Ad\]**'a bir tümleştirme anahtarı alan eşlemesi ekleyin. Bağlantı kümesine önce bir proje eklemeniz gerekebilir. Daha fazla bilgi için bkz. [Common Data Service for Apps'e veri entegre edin](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Bağlantı kümenizde **msdyn\_projects**'ten **msdynce\_projectnumber \[Proje Numarası\]**'na bir tümleştirme anahtarı alan eşlemesi ekleyin. Bağlantı kümesine önce bir proje eklemeniz gerekebilir. Daha fazla bilgi için bkz. [Common Data Service for Apps'e veri entegre edin](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Proje sözleşmeleri ve projeler için **SourceDataID** (Kaynak Veri Kodu), farklı bir değerle güncelleştirilebilir veya eşlemeden kaldırılabilir. Varsayılan şablon değeri **Project Service Automation**'dır.
- **PaymentTerms** (Ödeme Koşulları) eşlemesinin Finance'te geçerli ödeme koşullarını yansıtacak şekilde güncelleştirilmesi gerekir. Ayrıca, eşlemeyi proje görevinden kaldırabilirsiniz. Varsayılan değer eşlemesinde, tanıtım verileri için varsayılan değerler vardır. Aşağıdaki tabloda Project Service Automation'daki değerler gösterilmektedir.

    | Değer | Tanım   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | %2 10, Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power Query

Aşağıdaki koşullar karşılanırsa verilere filtre uygularken Excel için Microsoft Power Query kullanmanız gerekir:

- Dynamics 365 Sales'da satış siparişleriniz bulunur.
- Project Service Automation'da birden fazla kuruluş biriminiz vardır ve bu kuruluş birimleri Finance'te birden fazla tüzel kişilikle eşlenir.

Power Query kullanmanız gerekiyorsa şu yönergeleri takip edin:

- Projeler ve sözleşmeler (PSA'dan Fin and Ops'a) şablonunda yalnızca **Çalışma öğesi (msdyn\_ordertype = 192350001)** türünde satış siparişleri içeren bir varsayılan filtre vardır. Bu filtre, Finance'teki satış siparişleri için proje sözleşmeleri oluşturulmamasını sağlamaya yardımcı olur. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.
- Yalnızca, tümleştirme bağlantı kümesinin tüzel kişiliğine eşitlenecek sözleşme kuruluşlarını içeren bir Power Query filtresi oluşturmanız gerekir. Örneğin Contoso ABD'nin sözleşme kuruluş birimiyle aranızdaki proje sözleşmelerinin USSI tüzel kişiliğine eşitlenmesi gerekirken, Contoso Global'in sözleşme kuruluş birimiyle aranızdaki proje sözleşmelerinin USMF tüzel kişiliğine eşitlenmesi gerekiyor. Bu filtreyi görev eşlemenize eklemezseniz tüm proje sözleşmeleri, sözleşmenin kuruluş birimine bakılmaksızın bağlantı kümesi için tanımlanan tüzel kişiliğe eşitlenir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE] 
> **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ve **AddressZipCode** alanları, proje sözleşmeleri için varsayılan eşlemeye dahil değildir. Proje sözleşmeleri için bu verilerin eşitlenmesini zorunlu kılarsanız eşlemeleri ekleyebilirsiniz.
>
> **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ve **ProjectType** alanları projeler için varsayılan eşlemeye dahil değildir. Projeler için bu verilerin eşitlenmesini zorunlu kılarsanız eşlemeleri ekleyebilirsiniz.

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Şablon eşleme](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Şablon eşleme](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Şablon eşleme](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projeler ve Sözleşmelerdeki proje sözleşme satırı kilometre taşı eşlemesi (PSA 3.x'den Dynamics'e) - v2 şablonu:

[![Şablon eşleme](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
