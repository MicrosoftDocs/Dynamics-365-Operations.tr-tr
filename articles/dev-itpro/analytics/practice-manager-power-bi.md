---
title: "Uygulama yöneticisi Power BI içeriği"
description: "Bu konu, Power BI Uygulama yöneticisi nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 44f017fc3460b83b730f2f7c909c6b88480dd918
ms.contentlocale: tr-tr
ms.lasthandoff: 12/18/2017

---

# <a name="practice-manager-power-bi-content"></a>Uygulama yöneticisi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Power BI **Uygulama yöneticisi** nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Uygulama yöneticisi** Power BI içeriği, uygulama yöneticileri ve proje yöneticileri için oluşturulmuştur. Kuruluşun üzerinde çalışmakta olduğu projelerle ilgili önemli ölçümler sağlar. Pano, projeler ve ilgili müşterilerle ilgili bir genel bakış sağlar. Bir rapor seviyesi filtresi, çeşitli tüzel kişiliklerin raporlaması için kullanılabilir. Bu Power BI içeriği verileri proje muhasebe toplama ölçümlerinden çeker.

**Uygulama yöneticisi** Power BI içeriği, beş rapor sayfası içerir: bir genel bakış sayfası ve proje maliyetleri, gelirler, kazanılan değer yönetimi ve saatlik ölçümlerin çeşitli boyutlara göre ayrıntılarını sağlayan dört sayfa.

İçerikteki tüm tutarlar sistem para birimi cinsinden gösterilir. Sistem para birimini **Sistem parametreleri** sayfasından ayarlayabilirsiniz.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek

**Uygulama yöneticisi** Power BI içeriği **Proje yönetimi** çalışma alanında gösterilir.


## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan raporlar

Aşağı tablo, **Uygulama yöneticisi** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor sayfası       | Ölçümler |
|-------------------|---------|
| Projeler genel bakışı | <ul><li>Oluşturulan projeler</li><li>Tahmin edilen projeler</li><li>İşlemi devam eden projeler</li><li>Müşteriye göre gerçek gelir</li><li>Projeye göre bütçe brüt karı</li><li>Kazanılan değer yönetimi genel bakış</li></ul> |
| Maliyet              | <ul><li>Aya göre fiili maliyet- bütçe maliyeti karşılaştırması</li><li>Yıla göre fiili maliyet - bütçe maliyeti karşılaştırması</li><li>Kategoriye göre fiili maliyet - bütçe maliyet karşılaştırması</li><li>Hareket türüne göre fiili maliyet</li></ul> |
| Gelir           | <ul><li>Aya göre gerçek gelir</li><li>Posta koduna göre gerçek gelir</li><li>Kategoriye göre fiili gelir - bütçe geliri karşılaştırması</li><li>Müşteri endüstrisine göre gerçek gelir</li></ul> |
| EVM               | Projeye göre maliyet ve planlama performans endeksi |
| Saatler             | <ul><li>Fiili faturalanabilir çalışılan saatler - fiili faturalanabilir yük saati sayısı - bütçe saatleri karşılaştırması</li><li>Projeye göre fiili faturalanabilir çalışılan saatler - fiili faturalanabilir yük saati sayısı karşılaştırması</li><li>Kaynağa göre fiili faturalanabilir çalışılan saatler - fiili faturalanabilir yük saatleri karşılaştırması</li><li>Projeye göre gerçek faturalanabilir saatlerin oranı</li><li>Kaynağa göre gerçek faturalanabilir saatlerin oranı</li></ul> |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir pano oluşturma ve yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Altta yatan veriyi dışa aktar işlevini de görselleştirme içerisinde özetlenen altta yatan veriyi dışa aktarmak için kullanabilirsiniz.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Aşağıdaki veriler **Uygulama yöneticisi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).

Aşağıdaki bölümler, her bir varlıkta kullanılan toplanan ölçümleri açıklar.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Varlık: ProjectAccountingCube\_ActualHourUtilization
**Veri kaynağı:** ProjEmplTrans

| Kilit toplam ölçüm      | Alan                              | Açıklama |
|--------------------------------|------------------------------------|-------------|
| Fiili faturalanabilir kullanılan saat sayısı | Sum(ActualUtilizationBillableRate) | Fiili faturalanabilir çalışılan saatlerin toplamı. |
| Fiili faturalanabilir yük saat sayısı   | Sum(ActualBurdenBillableRate)      | Fiili yük oranının toplamı. |

### <a name="entity-projectaccountingcubeactuals"></a>Varlık: ProjectAccountingCube\_Actuals
**Veri kaynağı:** ProjTransPosting

| Kilit toplam ölçüm | Alan              | Açıklama |
|---------------------------|--------------------|-------------|
| Gerçek gelir            | Sum(ActualRevenue) | Tüm hareketler için deftere nakledilen gelirin toplamı. |
| Gerçek maliyet               | Sum(ActualCost)    | Tüm hareket türleri için deftere nakledilen maliyetin toplamı. |

### <a name="entity-projectaccountingcubecustomer"></a>Varlık: ProjectAccountingCube\_Customer
**Veri kaynağı:** CustTable

| Kilit toplam ölçüm | Alan                                             | Tanım |
|---------------------------|---------------------------------------------------|-------------|
| Projelerin sayısı        | COUNTA(ProjectAccountingCube\_Projects[PROJECTS]) | Kullanılabilir projelerin sayısı. |


### <a name="entity-projectaccountingcubeforecasts"></a>Varlık: ProjectAccountingCube\_Forecasts
**Veri kaynağı:** ProjTransBudget

| Kilit toplam ölçüm | Alan                  | Açıklama |
|---------------------------|------------------------|-------------|
| Bütçe maliyeti               | Sum(BudgetCost)        | Tüm hareket türleri için tahmin edilen maliyetin toplamı. |
| Bütçe geliri            | Sum(BudgetRevenue)     | Tahmini tahakkuk eden/faturalanan gelir toplamı. |
| Bütçedeki brüt kar       | Sum(BudgetGrossMargin) | Toplam tahmin edilen gelir toplamı ve toplam tahmin edilen maliyet toplamının farkı. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Varlık: ProjectAccountingCube\_ProjectPlanCostsView
**Veri kaynağı:** Proje

| Kilit toplam ölçüm | Alan                    | Açıklama |
|---------------------------|--------------------------|-------------|
| Planlanan maliyet              | Sum(SumOfTotalCostPrice) | Planlanan görevlere sahip tüm proje hareket türleri için toplam maliyet fiyatı tahmini. |

### <a name="entity-projectaccountingcubeprojects"></a>Varlık: ProjectAccountingCube\_Projects
**Veri kaynağı:** Proje

| Kilit toplam ölçüm    | Alan | Tanım |
|------------------------------|-------|-------------|
| Maliyet performansı endeksi       | ProjectAccountingCube\_Projects[Kazanılan değer] ÷ ProjectAccountingCube\_Projects[Tamamlanan görevlerin toplam fiili maliyeti] | Toplam kazanılan değerin toplam fiili maliyete bölümünün hesaplanması. |
| Performans planla endeksi   | ProjectAccountingCube\_Projects[Kazanılan değer] ÷ ProjectAccountingCube\_Projects[Tamamlanan görevlerin toplam planlanan maliyeti] | Toplam kazanılan değerin toplam planlanan maliyete bölümünün hesaplanması. |
| Tamamlanan iş yüzdesi | Tamamlanan görev yüzdesi = ProjectAccountingCube\_Projects[Tamamlanan görevlerin toplam fiili maliyeti] ÷ (ProjectAccountingCube\_Projects[Tamamlanan görevlerin toplam fiili maliyeti] + ProjectAccountingCube\_Projects[Projenin toplam planlanan maliyeti] – ProjectAccountingCube\_Projects[Tamamlanan görevlerin toplam planlanan maliyeti]) | Tamamlanan görevler ve projenin planlanan maliyetinin toplam fiili maliyetine dayalı olarak tamamlanan işin toplam yüzdesi. |
| Fiili faturalanabilir saat oranı  | ProjectAccountingCube\_Projects[Projedeki toplam fiili faturalanabilir çalışılan saat sayısı] ÷ (ProjectAccountingCube\_Projects[Projedeki toplam fiili faturalanabilir çalışılan saat sayısı] + ProjectAccountingCube\_Projects[Projedeki toplam fiili faturalanabilir yük saati sayısı]) | Çalışılan saat ve yük saati sayısını temel alan toplam fiili faturalanabilir saat. |
| Kazanılan değer                 | ProjectAccountingCube\_Projects[Projenin toplam planlanan maliyeti] × ProjectAccountingCube\_Projects[Tamamlanan işin yüzdesi] | Tamamlanan işin yüzdesiyle çarpılan toplam planlanan maliyet. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Varlık: ProjectAccountingCube\_TotalEstimatedCosts 
**Veri kaynağı:** ProjTable


|    Kilit toplam ölçüm    |        Alan        |                                          Açıklama                                           |
|---------------------------------|---------------------|------------------------------------------------------------------------------------------------|
| Tamamlanan faaliyetin planlanan maliyeti | Sum(TotalCostPrice) | Tamamlanan görevlere sahip tüm proje hareket türleri için toplam maliyet fiyatı tahmini. |


