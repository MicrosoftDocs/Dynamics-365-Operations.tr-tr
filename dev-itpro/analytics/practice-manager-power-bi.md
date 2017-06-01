---
title: "Uygulama yöneticisi Power BI içeriği"
description: "Bu konu, Power BI Uygulama yöneticisi nelerin bulunduğunu açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Uygulama yöneticisi Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Power BI **Uygulama yöneticisi** nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Uygulama yöneticisi** Power BI içeriği, uygulama yöneticileri ve proje yöneticileri için oluşturulmuştur. Kuruluşun üzerinde çalışmakta olduğu projelerle ilgili önemli ölçümler sağlar. Pano, projeler ve ilgili müşterilerle ilgili bir genel bakış sağlar. Bir rapor seviyesi filtresi, çeşitli tüzel kişiliklerin raporlaması için kullanılabilir. Bu Power BI içeriği, Microsoft Dynamics 365 for Operations için proje muhasebe toplama ölçümlerinden verileri çeker.

**Uygulama yöneticisi** Power BI içeriği, beş rapor sayfası içerir: bir genel bakış sayfası ve proje maliyetleri, gelirler, kazanılan değer yönetimi ve saatlik ölçümlerin ayrıntılarını sağlayan ve çeşitli boyutlara bölünmüş olan dört sayfa.

İçerikteki tüm tutarlar sistem para birimi cinsinden gösterilir. Sistem para birimini **Sistem parametreleri** sayfasından ayarlayabilirsiniz.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek

**Uygulama yöneticisi** Power BI içeriğini, Microsoft Dynamics Lifecycle Services (LCS) içindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçerik paketini indirmek ve Dynamics 365 for Operations verinize bağlamak hakkında daha fazla bilgi için bkz. [Microsoft ve ortaklarınızdan LCS içerisindeki Power BI içeriği](power-bi-content-microsoft-partners.md).

Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office mix.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan raporlar

Aşağı tablo, **Uygulama yöneticisi** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor sayfası                                          | Ölçümler               |
|------------------------------------------------------|-----------------------------------------------|
| Pano  | Oluşturulan projeler<br>Tahmin edilen projeler<br>İşlemi devam eden projeler<br>Aşamaya göre projelerin sayısı<br>Şehre göre projelerin sayısı<br>Müşteriye göre gerçek gelir<br>Projeye göre bütçe brüt karı<br>Kazanılan değer yönetimi genel bakış |
| Maliyet                                                 | Aya göre fiili - bütçe maliyeti karşılaştırması<br>Yıla göre fiili - bütçe maliyeti karşılaştırması<br>Kategoriye göre fiili - bütçe maliyet karşılaştırması<br>Hareket türüne göre fiili maliyet       |
| Gelir                                              | Aya göre gerçek gelir<br>Posta koduna göre gerçek gelir<br>Kategoriye göre fiili - bütçe maliyeti karşılaştırması<br>Müşteri endüstrisine göre gerçek gelir        |
| EVM                                                  | Projeye göre maliyet ve planlama performans endeksi                 |
| Saatler                                                | Gerçek faturalanabilir çalışılan saatleri - gerçek faturalanabilen yük saatleri - bütçe saatleri karşılaştırması<br>Projeye göre gerçek faturalanabilir çalışılan saatleri - gerçek faturalanabilen yük saatleri karşılaştırması<br>Kaynağa göre gerçek faturalanabilir çalışılan saatleri - gerçek faturalanabilen yük saatleri karşılaştırması<br>Projeye göre gerçek faturalanabilir saatlerin oranı<br>Kaynağa göre gerçek faturalanabilir saatlerin oranı |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir pano oluşturma ve yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Altta yatan veriyi dışa aktar işlevini de görselleştirme içerisinde özetlenen altta yatan veriyi dışa aktarmak için kullanabilirsiniz.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Dynamics 365 for Operations verisi, **Uygulama yöneticisi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, analytics için en iyi duruma getirilen bir Microsoft SQL veritabanı olan Varlık mağazasında hazırlanmış toplam ölçümler olarak temsil edilir. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).

Aşağıdaki bölümler, her bir varlıkta kullanılan toplanan ölçümleri açıklar.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Varlık: ProjectAccountingCube_ActualHourUtilization
**Veri kaynağı**: ProjEmplTrans

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Gerçek faturalanabilir kullanılan saatlerin toplamı |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Gerçek yük oranının toplamı             |

### <a name="entity-projectaccountingcubeactuals"></a>Varlık: ProjectAccountingCube_Actuals
**Veri kaynağı**: ProjTransPosting

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Tüm hareket için deftere nakledilen gelirin toplamı |   
| ActualCost   |                             Sum(ActualCost)           |    Tüm hareket türleri için deftere nakledilen maliyetin toplamı    |

### <a name="entity-projectaccountingcubecustomer"></a>Varlık: ProjectAccountingCube_Customer
**Veri kaynağı**: CustTable

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Projelerin sayısı        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Kullanılabilir Projelerin sayısı    |


### <a name="entity-projectaccountingcubeforecasts"></a>Varlık: ProjectAccountingCube_Forecasts
**Veri kaynağı**: ProjTransBudget

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Tüm hareket türleri için tahmin edilen maliyetin toplamı     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Tahmin edilen tahakkuk edilen/faturalanan gelir toplamı         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Toplam tahmin edilen gelir toplamı ve toplam tahmin edilen maliyet toplamının farkı

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Varlık: ProjectAccountingCube_ProjectPlanCostsView
**Veri kaynağı**: Proje

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Planlanan görevlere sahip tüm proje hareket türleri için toplam maliyet fiyatı tahmini |

### <a name="entity-projectaccountingcubeprojects"></a>Varlık: ProjectAccountingCube_Projects
**Veri kaynağı**: Proje

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Maliyet performansı endeksi  |ProjectAccountingCube_Projects[Kazanılan değer] / ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam fiili maliyeti] |     Toplam kazanılan değerin toplam fiili maliyete bölümünün hesaplanması|
|  Performans planla endeksi |ProjectAccountingCube_Projects[Kazanılan değer] / ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam planlanan maliyeti]|Toplam kazanılan değerin toplam planlanan maliyete bölümünün hesaplanması |
|Tamamlanan iş yüzdesi |Tamamlanan işin yüzdesi = ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam fiili maliyeti] / (ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam fiili maliyeti] + ProjectAccountingCube_Projects[Projenin toplam planlanan maliyeti] - ProjectAccountingCube_Projects[Tamamlanan görevlerin toplam planlanan maliyeti])|Tamamlanan görev ve projenin planlanan maliyetinin toplam fiili maliyetine dayalı olarak tamamlanan işin toplam yüzdesi|
|Proje gerçek faturalanabilir Saatler oranı|ProjectAccountingCube_Projects[Proje toplam gerçek faturalanabilir kullanılan saatleri] / (ProjectAccountingCube_Projects[Proje toplam gerçek faturalanabilir kullanılan saatleri] + ProjectAccountingCube_Projects[Proje toplam gerçek faturalanabilir yük saatleri])|Kullanılan + yüke dayanan toplam gerçek faturalanabilir saatler|
|Kazanılan değer|ProjectAccountingCube_Projects[Projenin toplam planlanan maliyeti] * ProjectAccountingCube_Projects[Tamamlanan işin yüzdesi]|Tamamlanan işin yüzdesine göre toplam planlanan maliyet çarpanı|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Varlık: ProjectAccountingCube_TotalEstimatedCosts 
**Veri kaynağı**: ProjTable

| Kilit toplam ölçüm                | Alan                                | Açıklama                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Tamamlanan görevlere sahip tüm proje hareket türleri için toplam maliyet fiyatı tahmini|

## <a name="additional-resources"></a>Ek kaynaklar

Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

- [Veri varlıkları](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Çalışma alanları için Power BI tümleştirmesini yapılandır](configure-power-bi-integration.md)

