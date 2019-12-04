---
title: Proje tahminlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme
description: Bu konuda, doğrudan Microsoft Dynamics 365 Project Service Automation'dan alınaqn proje saati tahminlerini ve proje gider tahminlerini Dynamics 365 Finance ile eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770301"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Proje tahminlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu projeleri Dynamics 365 Project Service Automation üzerinden Dynamics 365 Finance üzerine proje saat tahminleri ve proje maliyet tahminlerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.

> [!NOTE]
> - Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme gibi özellikler sürüm 8.0'da bulunmaktadır.
> - Fiili değerlerin tümleştirmesi sürüm 8.0.1 veya sonrasında kullanılabilir.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation'dan Finance'e veri akışı

Project Service Automation ile Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje saat tahminleri ve proje gider tahminleri hakkındaki verilerin Project Service Automation'dan Finance'e akışına olanak tanır.

Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.

[![Project Service Automation ile Finance tümleştirmesi için veri akışı](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Proje saat tahminleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft Power Apps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görevler, Project Service Automation'dan alınan proje saat tahminlerini Finance ile eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje saat tahminleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Hareket ilişkileri
    - Gider tahminleri

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                                       |
|----------------------------|-----------------------------------------------|
| Proje görevleri              | Proje saat tahminleri için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje saat tahminleri, Project Service Automation'da yönetilir ve Finance ile proje saat tahminleri olarak eşitlenir.

### <a name="prerequisites"></a>Önkoşullar

Proje saat tahminlerinin eşitlemesi gerçekleşmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje saat tahminleri şablonunda şu görevleri tamamlamak için Excel için Microsoft Power Query kullanmanız gerekir:

- Tümleştirme yeni saat tahminleri oluştururken kullanılacak varsayılan tahmin modeli kodunu ayarlamak.
- Görev içinde, tümleştirmenin saat tahminlerini başarısız kılacak olan kaynağa özgü kayıtları filtrelemek.
- Tüm boş hareket kategorisi satırlarını filtrelemek. Bu görev tamamlanmadığı takdirde saat tahminleri yanlış çıkabilir.

#### <a name="set-the-default-forecast-model-id"></a>Varsayılan tahmin modeli kodunu ayarlama

Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Eşle** okuna tıklayarak eşlemeyi açın. Ardından **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.

- Varsayılan Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** listesindeki **Eklenen Koşul**'u seçin. **İşlev** girişinde **O\_forecast** öğesini tümleştirmeyle kullanılacak tahmin modeli kodunun adıyla değiştirin. Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.
- Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir. Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin, örneğin **ModelKodu**. Sütun için şu koşulu girin: where, if Project task is not null, then \<tahmin modeli kodunu girin\>; else null.

#### <a name="filter-out-resource-specific-records"></a>Kaynağa özgü kayıtları filtreleme

Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunda kaynağa özgü kayıtları kaldıran bir varsayılan filtre vardır. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçerek **msdyn\_islinetask** sütununda yalnızca **Yanlış** kayıtları içerecek filtreyi uygulayın.

#### <a name="filter-out-empty-transaction-category-rows"></a>Boş hareket kategorisi satırlarını filtreleme

Boş hareket kategorilerine sahip tüm satırları kaldırmak için bir filtre eklemeniz gerekir. Bu görev, varsayılan şablon kullanmanızdan veya kendi şablonunuzu oluşturmanızdan bağımsız olarak gereklidir. Bu filtre, Project Service Automation'dan alınan ve Finance'te saat tahminlerinin yanlış çıkmasına neden olabilecek özet satırlarını kaldırır. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçerek **msdyn\_transactioncategory\_value** sütunundaki null kayıtları filtreleyin.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor. Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Proje gideri tahminleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablon ve temel görevler, Project Service Automation'dan alınan proje gider tahminlerini Finance ile eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider tahminleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Hareket ilişkileri 
    - Gider tahminleri

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                                                  |
|----------------------------|----------------------------------------------------------|
| Hareket Bağlantıları    | Proje hareketi ilişkileri için tümleştirme varlığı |
| Tahmin Satırları             | Proje gider tahminleri için tümleştirme varlığı         |

### <a name="entity-flow"></a>Varlık akışı

Proje gider tahminleri, Project Service Automation'da yönetilir ve Finance ile proje gider tahminleri olarak eşitlenir.

### <a name="prerequisites"></a>Önkoşullar

Proje gider tahminleri eşitlenmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje gider tahminleri şablonunda aşağıdaki görevleri tamamlamak için Power Query kullanmanız gerekir:

- Yalnızca gider tahmini satır kayıtlarını içerecek şekilde filtreleyin.
- Tümleştirme yeni saat tahminleri oluştururken kullanılacak varsayılan tahmin modeli kodunu ayarlamak.
- Faturalama türlerini dönüştürmek.
- Hareket türlerini dönüştürmek.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Yalnızca gider tahmini satırlarını içerecek filtre uygulama

Project gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirmede yalnızca gider satırlarını içeren bir varsayılan filtre vardır. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir. **Hareket ilişkileri** görevini seçin ve ardından eşlemeyi açmak için **Eşle** okuna tıklayın. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin. **msdyn\_transactiontype1** sütununu yalnızca **msdyn\_estimateline** öğesini içerecek şekilde filtreleyin.

#### <a name="set-the-default-forecast-model-id"></a>Varsayılan tahmin modeli kodunu ayarlama

Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Gider tahminleri** görevini seçin ve ardından eşlemeyi açmak için **Eşle** okuna tıklayın. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.

- Power Query'de varsayılan Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** bölümünden ilk **Eklenen Koşul**'u seçin. **İşlev** girişinde **O\_forecast** öğesini tümleştirmeyle kullanılacak tahmin modeli kodunun adıyla değiştirin. Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.
- Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir. Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin, örneğin **ModelKodu**. Sütun için şu koşulu girin: where, if Estimate line ID is not null, then \<tahmin modeli kodunu girin\>; else null.

#### <a name="transform-the-billing-types"></a>Faturalama türlerini dönüştürme

Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan faturalama türlerini dönüştürmek için kullanılan bir koşullu sütun vardır. Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin ve ardından **Koşullu Sütun Ekle**'yi seçin. Yeni sütun için **Faturalama Türü** gibi bir ad girin. Ardından aşağıdaki koşulu girin:

If **msdyn\_billingtype** = 192350000, then **Masraflandırılamaz**  
else if **msdyn\_billingtype** = 192350001, then **Masraflandırılabilir**  
else if **msdyn\_billingtype** = 192350002, then **Karşılıksız**  
else **Yok**

#### <a name="transform-the-transaction-types"></a>Hareket türlerini dönüştürme

Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan hareket türlerini dönüştürmek için kullanılan bir koşullu sütun vardır. Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin ve ardından **Koşullu Sütun Ekle**'yi seçin. Yeni sütun için **Hareket Türü** gibi bir ad girin. Ardından aşağıdaki koşulu girin:

If **msdyn\_transactiontypecode** = 192350000, then **Maliyet**  
else if **msdyn\_transactiontypecode** = 192350005, then **Satış**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.

[![Şablon eşleme](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Şablon eşleme](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
