---
title: "Project Service Automation'dan proje tahminlerini Finance and Operations'taki proje tahminlerine doğrudan eşitleme"
description: "Bu konu, proje saat tahminlerini ve proje gider tahminlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Project Service Automation'dan proje tahminlerini Finance and Operations'taki proje tahminlerine doğrudan eşitleme

Bu konu, proje saat tahminlerini ve proje gider tahminlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır.

> [!NOTE]
> Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation'dan Finance and Operations'a veri akışı

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje saat tahminleri ve proje gider tahminleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.

Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.

[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps Yönetim Merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.

Aşağıdaki şablon ve temel görevler, proje saat tahminlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

-  **Veri tümleştirmedeki şablonun adı:** Proje saat tahminleri (PSA'dan Fin and Ops'a)

-  **Projedeki görevlerin adı:** 
    - Hareket ilişkileri 
    - Gider tahminleri

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Proje görevleri                   | Proje saat tahminleri için tümleştirme varlığı   |

## <a name="entity-flow"></a>Varlık akışı

Proje saat tahminleri Project Service Automation'da yönetilir ve Finance and Operations'a proje saat tahminleri olarak eşitlenir.

## <a name="preconditions"></a>Ön koşullar

Proje saat tahminlerinin eşitlemesi gerçekleşmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.

## <a name="power-query"></a>Power Query

Proje saat tahminleri şablonunda şu işlemler için Microsoft Power Query kullanmanız gerekir:
- Tümleştirme yeni saat tahminleri oluştururken kullanılacak **Tahmin modeli kodunu** ayarlamak.
- Görev içinde, tümleştirmenin saat tahminlerini başarısız kılacak olan kaynağa özgü kayıtları filtrelemek.
- Tüm boş hareket kategorisi satırlarını filtrelemek. Bu yapılmadığı takdirde saat tahminleri yanlış çıkabilir.

### <a name="forecast-model-id"></a>Tahmin modeli kodu
Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Eşle** okuna tıklayarak eşlemeyi açın. Gelişmiş Sorgu ve Filtreleme'yi açmak için seçin.
- Varsayılan Microsoft Project saat tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, **Uygulanan Adımlar** bölümündeki **Eklenen Koşul**'u seçin. **İşlev** girişinde **O_forecast**'ı, tümleştirmeyle kullanılacak **Tahmin modeli kodunun** adıyla değiştirin. Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.
- Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir. **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin (örneğin ModelKodu). Sütun için şu koşulu girin: where if Proje görevi is not null, then<enter the forecast model ID>; else null.

### <a name="filter-out-resource-specific-records"></a>Kaynağa özgü kayıtları filtreleme
Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunda kaynağa özgü kayıtları kaldıran bir varsayılan filtre vardır. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir. Gelişmiş Sorgu ve Filtreleme formunda, **msdyn_islinetask** sütununda yalnızca **Yanlış** kayıtları içerecek filtre uygulamayı seçin.

### <a name="filter-out-empty-transaction-category-rows"></a>Boş hareket kategorisi satırlarını filtreleme
Boş hareket kategorileri içeren tüm satırları kaldırmak için bir filtre eklemeniz gerekir. Bu, varsayılan şablon kullanmanızdan veya kendi şablonunuzu oluşturmanızdan bağımsız olarak gereklidir. Bu filtre, Project Service Automation'dan gelen ve Finance and Operations'ta saat tahminlerinin yanlış çıkmasına neden olabilecek özet satırlarını kaldırır. Gelişmiş Sorgu ve Filtreleme formunda, **msdyn_transactioncategory_value** sütunundaki null kayıtları filtrelemeyi seçin.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor. Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Aşağıdaki şablon ve temel görev, proje gider tahminlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:

-  **Veri tümleştirmedeki şablonun adı:** Proje gider tahminleri (PSA'dan Fin and Ops'a)
-  **Projedeki görevlerin adı:** 
     - Hareket ilişkileri 
     - Gider tahminleri

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Hareket Bağlantıları         | Proje hareketi ilişkileri için tümleştirme varlığı.   |
| Tahmin Satırları                  | Proje gider tahminleri için tümleştirme varlığı.           |

## <a name="entity-flow"></a>Varlık akışı

Proje gider tahminleri Project Service Automation'da yönetilir ve Finance and Operations'a proje gider tahminleri olarak eşitlenir.

## <a name="prerequisites"></a>Ön koşullar

Proje gider tahminlerinin eşitlemesi gerçekleşmeden önce Projeleri, Proje görevlerini ve Proje gider hareketi kategorilerini eşitlemeniz gerekir.

## <a name="power-query"></a>Power Query

Proje gider tahminleri şablonunda şu işlemler için Microsoft Power Query kullanmanız gerekir:
- Yalnızca gider tahmini satır kayıtlarını içerecek filtre uygulamak
- Tümleştirme yeni saat tahminleri oluştururken kullanılacak **Tahmin modeli kodunu** ayarlamak.
- Faturalama türlerini dönüştürmek.
- Hareket türlerini dönüştürmek.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Yalnızca gider tahmini satırlarını içerecek filtre uygulama
Project gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirmede yalnızca gider satırlarını içerecek bir varsayılan filtre vardır. Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir. Hareket ilişkileri görevi'ni seçin ve **Eşle** okuna tıklayın. **Gelişmiş Sorgu ve Filtreleme**'yi seçin. **msdyn_transactiontype1** sütununa yalnızca **msdyn_estimateline**'ı içerecek filtre uygulayın.

### <a name="forecast-model-id"></a>Tahmin modeli kodu
Gider tahminleri görevine yönelik olarak şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Eşle** okuna tıklayarak eşlemeyi açın. Gelişmiş Sorgu ve Filtreleme'yi açmak için seçin.
- Varsayılan Microsoft Project gider tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, **Uygulanan Adımlar** bölümündeki ilk **Eklenen Koşul**'u seçin. **İşlev** girişinde **O_forecast**'ı, tümleştirmeyle kullanılacak **Tahmin modeli kodunun** adıyla değiştirin. Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.
- Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir. **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin (örneğin ModelKodu). Sütun için şu koşulu girin: where if Tahmin satırı kodu is not null, then < tahmin modeli kodunu girin >; else null.

### <a name="transform-the-billing-types"></a>Faturalama türlerini dönüştürme
Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan faturalama türlerini dönüştürmek için eklenen bir koşullu sütun vardır.
- Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir. Gelişmiş Sorgu ve Filtreleme formunda **Koşullu Sütun Ekle**'yi seçin. Sütuna bir ad verin (örneğin FaturalamaTürü). Girilecek koşul aşağıdaki gibidir:

    If **msdyn_billingtype** = 192350000, then **Masraflandırılamaz** else if **msdyn_billingtype** = 192350001, then **Masraflandırılabilir** else if **msdyn_billingtype** = 192350002, then **Karşılıksız** else **Yok**

### <a name="transform-the-transaction-types"></a>Hareket türlerini dönüştürme
Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan hareket türlerini dönüştürmek için eklenen bir koşullu sütun vardır.
- Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir. Gelişmiş Sorgu ve Filtreleme formunda **Koşullu Sütun Ekle**'yi seçin. Sütuna bir ad verin (örneğin HareketTürü). Girilecek koşul şöyledir: If **msdyn_transactiontypecode** = 192350000, then **Maliyet** else if **msdyn_transactiontypecode** = 192350005, then **Satış** else **null**

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor. Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşleme](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Şablon eşleme](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




