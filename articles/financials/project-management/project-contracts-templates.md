---
title: "Proje sözleşmelerini ve projeleri doğrudan Project Service Automation'dan Finance and Operations'a eşitleme"
description: "Bu konu, proje sözleşmelerini ve projeleri Microsoft Dynamics 365 for Project Service Automation'dan Microsoft Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonu ve temel görevleri açıklamaktadır."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 65a274323a2d95c9c76727c9e40aa7e649e6350a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Proje sözleşmelerini ve projeleri doğrudan Project Service Automation'dan Finance and Operations'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, proje sözleşmelerini ve projeleri Microsoft Dynamics 365 for Project Service Automation'dan Microsoft Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonu ve temel görevleri açıklamaktadır.

> [!NOTE] 
> Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation'dan Finance and Operations'a veri akışı

> [!NOTE]
> Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmadan önce Microsoft Dynamics 365 Veri tümleştirme özelliği hakkında bilgi sahibi olmanız gerekir.

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje sözleşmeleri, projeler, proje sözleşme satırları ve proje sözleşme satırı kilometre taşları hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için Microsoft PowerApps yönetim merkezinde **Projeler**'i seçin ve ardından sağ üst köşede **Yeni proje**'yi seçerek genel şablonları seçin.

Aşağıdaki şablon ve temel görevler, proje sözleşmelerini ve projeleri Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Projeler ve sözleşmeler (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Proje sözleşmeleri - PSA'dan Fin and Ops'a
    - Projeler - PSA'dan Fin and Ops'a
    - Proje sözleşme satırları - PSA'dan Fin and Ops'a
    - Proje sözleşme satırı kilometre taşları - PSA'dan Fin and Ops'a

Proje sözleşmelerinin ve projelerin eşitlemesinin yapılabilmesi için hesapları eşitlemeniz gerekir.

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Siparişler                           | Proje sözleşmesi için tümleştirme varlığı                |
| Projeler                         | Proje için tümleştirme varlığı                         |
| Sipariş satırları                      | Proje sözleşme satırı için tümleştirme varlığı           |
| Proje sözleşme satırı kilometre taşları | Proje sözleşme satırı kilometre taşı için tümleştirme varlığı |

## <a name="entity-flow"></a>Varlık akışı

Proje sözleşmeleri Project Service Automation'da yönetilir ve Finance and Operations'a proje sözleşmeleri olarak eşitlenir. Tümleştirme şablonun bir parçası olarak, proje sözleşmesi için Finance and Operations'ta tümleştirme kaynağını ayarlayabilirsiniz.

Zaman ve malzeme projesi ve Sabit fiyatlı projeler, Project Service Automation'da yönetilir ve Finance and Operations'a proje olarak eşitlenir. Tümleştirme şablonunun bir parçası olarak, proje için Finance and Operations'ta tümleştirme kaynağını ayarlayabilirsiniz.

Proje sözleşme satırları Project Service Automation'da yönetilir ve Finance and Operations'a proje sözleşmesi faturalama kuralları olarak eşitlenir. Faturalama yöntemi varsayılan proje türünden farklıysa eşitleme işlemi sözleşme satırı projesinin proje türünü ve proje grubunu güncelleştirir.

Proje sözleşme satırı kilometre taşları Project Service Automation'da yönetilir ve Finance and Operations'a proje sözleşmesi faturalama kuralı kilometre taşları olarak eşitlenir.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Project Service Automation'dan Finance and Operations'a tümleştirme çözümü

**Proje sözleşmesi kodu** alanı **Proje sözleşmeleri** sayfasındadır. Tümleştirmeyi desteklemek için, bu alan doğal ve benzersiz anahtar yapılmıştır.

Yeni bir proje sözleşmesi oluşturulduğunda, bir **Proje sözleşmesi kodu** değeri önceden mevcut değilse, bu numara serisiyle otomatik olarak oluşturulur. Değer **ORD** ve onun ardından gelen artımlı bir numara serisi ve altı karakterlik bir sonekten oluşur. Örneğin: **ORD-01022-Z4M9Q0**.

**Proje Numarası** alanı, **Projeler** sayfasındadır. Tümleştirmeyi desteklemek için, bu alan doğal ve benzersiz anahtar yapılmıştır.

Yeni bir proje oluşturulduğunda, bir **Proje Numarası** değeri önceden mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur. Değer **PRJ** ve onun ardından gelen artımlı bir numara serisi ve altı karakterlik bir sonekten oluşur. Örneğin: **PRJ-01049-CCNID0**.

Project Service Automation'dan Finance and Operations'a tümleştirme çözümü uygulanırken<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, bir yükseltme komut doyası, Project Service Automation'da mevcut proje sözleşmeleri için **Proje sözleşmesi kodunu** ve mevcut projeler için **Proje Numarası** alanını ayarlar.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- Proje sözleşmelerinin ve projelerin eşitlemesinin yapılabilmesi için hesapları eşitlemeniz gerekir.
- Bağlantı kümenizde**msdyn\_organizationalunits**'ten **msdyn\_name \[Ad\]**'a bir tümleştirme anahtarı alan eşlemesi ekleyin. Bağlantı kümesine önce bir proje eklemeniz gerekebilir. Tümleştirme anahtarları hakkında daha fazla bilgi için bkz. [Dynamics 365 Veri tümleştirme](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).
- Bağlantı kümenizde **msdyn\_projects**'ten **msdynce\_projectnumber \[Proje Numarası\]**'na bir tümleştirme anahtarı alan eşlemesi ekleyin. Bağlantı kümesine önce bir proje eklemeniz gerekebilir. Tümleştirme anahtarları hakkında daha fazla bilgi için bkz. [Dynamics 365 Veri tümleştirme](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).
- Proje sözleşmeleri ve projeler için **SourceDataID** (Kaynak Veri Kodu), farklı bir değerle güncelleştirilebilir veya eşlemeden kaldırılabilir. Varsayılan şablon değeri **Project Service Automation**'dır.
- **PaymentTerms** (Ödeme Koşulları) eşlemesinin, Finance and Operations'ta geçerli ödeme koşullarını yansıtacak şekilde güncellenmesi gerekir. Ayrıca, eşlemeyi proje görevinden kaldırabilirsiniz. Varsayılan değer eşlemesinde, tanıtım verileri için varsayılan değerler vardır. Aşağıdaki tabloda Project Service Automation'daki değerler gösterilmektedir.

    | Değer | Tanım   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | %2 10, Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power Query

Aşağıdaki koşullar karşılanırsa verilere filtre uygularken Excel için Microsoft Power Query kullanmanız gerekir:

- Microsoft Dynamics 365 for Sales'de satış siparişleriniz vardır.
- Project Service Automation'da birden fazla kuruluş biriminiz vardır ve bu kuruluş birimleri Finance and Operations'ta birden fazla tüzel kişilikle eşlenecektir.

Power Query kullanmanız gerekiyorsa şu yönergeleri takip edin:

- Projeler ve sözleşmeler (PSA'dan Fin and Ops'a) şablonunda yalnızca **Çalışma öğesi (msdyn\_ordertype = 192350001)** türünde satış siparişleri içeren bir varsayılan filtre vardır. Bu filtre Finance and Operations'taki satış siparişleri için proje sözleşmeleri oluşturulmadığından emin olmanıza yardımcı olur. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.
- Yalnızca, tümleştirme bağlantı kümesinin tüzel kişiliğine eşitlenecek sözleşme kuruluşlarını içeren bir Power Query filtresi oluşturmanız gerekir. Örneğin Contoso ABD'nin sözleşme kuruluş birimiyle aranızdaki proje sözleşmelerinin USSI tüzel kişiliğine eşitlenmesi gerekirken, Contoso Global'in sözleşme kuruluş birimiyle aranızdaki proje sözleşmelerinin USMF tüzel kişiliğine eşitlenmesi gerekiyor. Bu filtreyi görev eşlemenize eklemezseniz tüm proje sözleşmeleri, sözleşmenin kuruluş birimine bakılmaksızın bağlantı kümesi için tanımlanan tüzel kişiliğe eşitlenir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE] 
> **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ve **AddressZipCode** alanları, proje sözleşmeleri için varsayılan eşlemeye dahil değildir. Proje sözleşmeleri için bu verilerin eşitlenmesini zorunlu kılarsanız eşlemeleri ekleyebilirsiniz.
>
> **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ve **ProjectType** alanları projeler için varsayılan eşlemeye dahil değildir. Projeler için bu verilerin eşitlenmesini zorunlu kılarsanız eşlemeleri ekleyebilirsiniz.

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Şablon eşleme](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Şablon eşleme](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Şablon eşleme](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

