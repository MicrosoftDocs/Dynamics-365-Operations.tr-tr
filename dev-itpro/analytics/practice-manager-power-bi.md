---
title: "Uygulama yöneticisi Power BI içeriği"
description: "Bu konu, Power BI Uygulama yöneticisi nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017


---

# <a name="practice-manager-power-bi-content"></a>Uygulama yöneticisi Power BI içeriği

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Power BI **Uygulama yöneticisi** nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Uygulama yöneticisi** Power BI içeriği, uygulama yöneticileri ve proje yöneticileri için oluşturulmuştur. Kuruluşun üzerinde çalışmakta olduğu projelerle ilgili önemli ölçümler sağlar. Pano, projeler ve ilgili müşterilerle ilgili bir genel bakış sağlar. Bir rapor seviyesi filtresi, çeşitli tüzel kişiliklerin raporlaması için kullanılabilir. Bu Power BI içeriği verileri proje muhasebe toplama ölçümlerinden çeker.

**Uygulama yöneticisi** Power BI içeriği, beş rapor sayfası içerir: bir genel bakış sayfası ve proje maliyetleri, gelirler, kazanılan değer yönetimi ve saatlik ölçümlerin çeşitli boyutlara göre ayrıntılarını sağlayan dört sayfa.

İçerikteki tüm tutarlar sistem para birimi cinsinden gösterilir. Sistem para birimini **Sistem parametreleri** sayfasından ayarlayabilirsiniz.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü Temmuz 2017 güncelleştirmesini kullanıyorsanız, **Uygulama yöneticisi** Power BI içeriği **Proje yönetimi** çalışma alanında görüntülenir.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan raporlar

Aşağı tablo, **Uygulama yöneticisi** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor sayfası       | Ölçümler |
|-------------------|---------|
| Projeler genel bakışı | <ul><li>Oluşturulan projeler</li><li>Tahmin edilen projeler</li><li>İşlemi devam eden projeler</li><li>Aşamaya göre projelerin sayısı</li><li>Şehre göre projelerin sayısı</li><li>Müşteriye göre gerçek gelir</li><li>Projeye göre bütçe brüt karı</li><li>Kazanılan değer yönetimi genel bakış</li></ul> |
| Maliyet              | <ul><li>Aya göre fiili maliyet- bütçe maliyeti karşılaştırması</li><li>Yıla göre fiili maliyet - bütçe maliyeti karşılaştırması</li><li>Kategoriye göre fiili maliyet - bütçe maliyet karşılaştırması</li><li>Hareket türüne göre fiili maliyet</li></ul> |
| Gelir           | <ul><li>Aya göre gerçek gelir</li><li>Posta koduna göre gerçek gelir</li><li>Kategoriye göre fiili gelir - bütçe geliri karşılaştırması</li><li>Müşteri endüstrisine göre gerçek gelir</li></ul> |
| EVM               | Projeye göre maliyet ve planlama performans endeksi |
| Saatler             | <ul><li>Fiili faturalanabilir çalışılan saatler - fiili faturalanabilir yük saati sayısı - bütçe saatleri karşılaştırması</li><li>Projeye göre fiili faturalanabilir çalışılan saatler - fiili faturalanabilir yük saati sayısı karşılaştırması</li><li>Kaynağa göre fiili faturalanabilir çalışılan saatler - fiili faturalanabilir yük saatleri karşılaştırması</li><li>Projeye göre gerçek faturalanabilir saatlerin oranı</li><li>Kaynağa göre gerçek faturalanabilir saatlerin oranı</li></ul> |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir pano oluşturma ve yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Altta yatan veriyi dışa aktar işlevini de görselleştirme içerisinde özetlenen altta yatan veriyi dışa aktarmak için kullanabilirsiniz.

## <a name="extending-the-power-bi-content"></a>Power BI içeriğini genişletmek
Microsoft Dynamics Lifecycle Services (LCS) içinde kullanılabilir durumda olan içerik paketlerini kullanarak, Microsoft Dynamics 365'e oturum açmayan kişilere harika analizler sunabilirsiniz. Bu içerik paketlerini diğer raporları veya görsel öğeleri içerecek şekilde değiştirebilir ve analiz için Power BI.com kiracınıza yayınlayabilirsiniz. 

**Uygulama yöneticisi** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](power-bi-content-microsoft-partners.md). Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.

Kullanmakta olduğunuz Dynamics 365 sürümü için geçerli **Uygulama yöneticisi** içeriğini indirdiğinizden emin olun.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Aşağıdaki veriler **Uygulama yöneticisi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).

Aşağıdaki bölümler, her bir varlıkta kullanılan toplanan ölçümleri açıklar.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Varlık: ProjectAccountingCube_ActualHourUtilization
**Veri kaynağı:** ProjEmplTrans

| Kilit toplam ölçüm      | Alan                              | Açıklama | 
|--------------------------------|------------------------------------|-------------|
| Fiili faturalanabilir kullanılan saat sayısı | Sum(ActualUtilizationBillableRate) | Fiili faturalanabilir çalışılan saatlerin toplamı. |
| Fiili faturalanabilir yük saat sayısı   | Sum(ActualBurdenBillableRate)      | Fiili yük oranının toplamı. |

### <a name="entity-projectaccountingcubeactuals"></a>Varlık: ProjectAccountingCube_Actuals
**Veri kaynağı:** ProjTransPosting

| Kilit toplam ölçüm | Alan              | Açıklama | 
|---------------------------|--------------------|-------------|
| Gerçek gelir            | Sum(ActualRevenue) | Tüm hareketler için deftere nakledilen gelirin toplamı. |   
| Gerçek maliyet               | Sum(ActualCost)    | Tüm hareket türleri için deftere nakledilen maliyetin toplamı. |

### <a name="entity-projectaccountingcubecustomer"></a>Varlık: ProjectAccountingCube_Customer
**Veri kaynağı:** CustTable

| Kilit toplam ölçüm | Alan                                            | Açıklama | 
|---------------------------|--------------------------------------------------|-------------|
| Projelerin sayısı        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Kullanılabilir projelerin sayısı. |


### <a name="entity-projectaccountingcubeforecasts"></a>Varlık: ProjectAccountingCube_Forecasts
**Veri kaynağı:** ProjTransBudget

| Kilit toplam ölçüm | Alan                  | Açıklama | 
|---------------------------|------------------------|-------------|
| Bütçe maliyeti               | Sum(BudgetCost)        | Tüm hareket türleri için tahmin edilen maliyetin toplamı. |
| Bütçe geliri            | Sum(BudgetRevenue)     | Tahmini tahakkuk eden/faturalanan gelir toplamı.  |
| Bütçedeki brüt kar       | Sum(BudgetGrossMargin) | Toplam tahmin edilen gelir toplamı ve toplam tahmin edilen maliyet toplamının farkı. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Varlık: ProjectAccountingCube_ProjectPlanCostsView
**Veri kaynağı:** Proje

| Kilit toplam ölçüm | Alan                    | Açıklama | 
|---------------------------|--------------------------|-------------|
| Planlanan maliyet              | Sum(SumOfTotalCostPrice) | Planlanan görevlere sahip tüm proje hareket türleri için toplam maliyet fiyatı tahmini. |

### <a name="entity-projectaccountingcubeprojects"></a>Varlık: ProjectAccountingCube_Projects
**Veri kaynağı:** Proje

| Kilit toplam ölçüm    | Alan | Açıklama | 
|------------------------------|-------|-------------|
| Maliyet performansı endeksi       | ProjectAccountingCube_Projects[Kazanılan değer] / ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam fiili maliyeti] | Toplam kazanılan değerin toplam fiili maliyete bölümünün hesaplanması. |
| Performans planla endeksi   | ProjectAccountingCube_Projects[Kazanılan değer] / ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam planlanan maliyeti] | Toplam kazanılan değerin toplam planlanan maliyete bölümünün hesaplanması. |
| Tamamlanan iş yüzdesi | Tamamlanan işin yüzdesi = ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam fiili maliyeti] / (ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam fiili maliyeti] + ProjectAccountingCube_Projects[Projenin toplam planlanan maliyeti] - ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam planlanan maliyeti]) | Tamamlanan görevler ve projenin planlanan maliyetinin toplam fiili maliyetine dayalı olarak tamamlanan işin toplam yüzdesi. |
| Fiili faturalanabilir saat oranı  | ProjectAccountingCube_Projects[Proje toplam gerçek faturalanabilir kullanılan saatleri] / (ProjectAccountingCube_Projects[Proje toplam gerçek faturalanabilir kullanılan saatleri] + ProjectAccountingCube_Projects[Proje toplam gerçek faturalanabilir yük saatleri]) | Çalışılan saat ve yük saati sayısını temel alan toplam fiili faturalanabilir saat. |
| Kazanılan değer                 | ProjectAccountingCube_Projects[Projenin toplam planlanan maliyeti] * ProjectAccountingCube_Projects[Tamamlanan işin yüzdesi] | Tamamlanan işin yüzdesiyle çarpılan toplam planlanan maliyet. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Varlık: ProjectAccountingCube_TotalEstimatedCosts 
**Veri kaynağı:** ProjTable

| Kilit toplam ölçüm       | Alan               | Açıklama | 
|---------------------------------|---------------------|-------------|
| Tamamlanan faaliyetin planlanan maliyeti | Sum(TotalCostPrice) | Tamamlanan görevlere sahip tüm proje hareket türleri için toplam maliyet fiyatı tahmini. |

