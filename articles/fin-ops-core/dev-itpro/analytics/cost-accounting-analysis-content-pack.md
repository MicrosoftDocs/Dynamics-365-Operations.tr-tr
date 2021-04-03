---
title: Maliyet muhasebesi analizi Power BI içeriği
description: Bu konu, Power BI Maliyet muhasebesi analizinde nelerin bulunduğunu açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1290cf971e7702affa325640a2b28ac64d74744e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563012"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Maliyet muhasebesi analizi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **Maliyet muhasebesi analizi** Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Maliyet muhasebesi analizi** Power BI içeriği, maliyet denetleyicileri veya bir kuruluşun maliyet kontrolünü yapmaktan sorumlu olan herkes için tasarlanmıştır. Bu, maliyet, büyüklük ve gerçek maliyete dayalı maliyet oranı, bütçe maliyeti ve esnek bütçe maliyeti gibi kilit ölçümleri içerir. **Maliyet muhasebesi** modülü içerisindeki hareket verilerini kullanır ve tüm organizasyonun maliyetlerinin toplam görünümünü tek bir raporlama para birimi cinsinden sağlar. Yöneticiler veriyi maliyet nesnelerine dayalı olarak kendi kuruluş birimlerinde maliyet denetimi gerçekleştirmek için filtreleyebilir, kuruluş çok sayıda tüzel varlığa sahip olsa bile.

**Maliyet muhasebesi analizi** içeriği gerçek maliyetler ve bütçe maliyetleri arasındaki farkları vurguladığı için, yöneticiler kendi operasyonel birimleri hakkında pozitif veya negatif trendler hakkında bilgilendirilebilirler. Yöneticiler maliyet öğesi hiyerarşilerinin veya tek tek maliyet öğelerinin ayrıntısına inebilir. Yöneticiler böylece maliyet farklarının nasıl oluştuğuna dair bilgi edinebilir ve etkili eylemlerde bulunabilir.

**Maliyet muhasebesi analizi** içeriği, maliyet muhasebecilerinin maliyet akışlarının, tüm kuruluşun maliyet öğelerinin arasında nasıl aktığını görmelerine olanak sağlar.

Maliyet muhasebesi hakkında daha fazla bilgi için bkz: [Maliyet muhasebesi giriş sayfası](../../../finance/cost-accounting/cost-accounting-home-page.md).

Maliyet muhasebesi erişim seviyesi güvenliğini tanımlayarak ve bunu satır düzeyi güvenlik ile Power BI içerisinde birleştirerek tüm maliyet öğesi sahiplerine **Maliyet muhasebesi analizi** Power BI içeriğine erişim sağlayabilirsiniz. Görsellerdeki tüm veri daha sonra Maliyet muhasebesi içinde denetlenen erişim seviyesinde filtrelenir. Erişim düzeyi güvenliği ve satır düzeyi güvenliği hakkında daha fazla bilgi için bkz. [Maliyet muhasebesi analizi Power BI içeriğinin güvenliğini ayarlama](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**Maliyet muhasebesi analizi** Power BI içeriğini, Microsoft Dynamics Lifecycle Services (LCS) içindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).

Kullanmakta olduğunuz Microsoft Dynamics 365 sürümü için geçerli **Maliyet muhasebesi analizi** içeriğini indirdiğinizden emin olun.

> [!NOTE]
> KB 4011327 bu Power BI içeriği için bir önkoşuldur. LCS'de oturum açtıktan sonra BB'ye buradan erişebilirsiniz: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler
İçerik bir dizi rapor sayfası içermektedir. Her sayfa grafikler, döşemeler ve tablolar ile görselleştirilen bir dizi ölçüm kümesinden oluşur. Aşağıdaki tablo **Yönetim maliyeti analizi** Power BI içeriğindeki görselleştirmelere bir bakış sağlar.

| Rapor sayfası                      | Grafik                                                                                                                         | Kutucuk                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Mali döneme göre maliyeti denetimi    | Maliyet öğesi hiyerarşi düzeyine göre fiili maliyet ve bütçe maliyeti                                                                   | Fiili maliyet - Bütçe maliyeti karşılaştırması                    |
|                                  | Maliyeti öğesi hiyerarşi düzeyine göre bütçe farkı                                                                               | Fiili maliyet oranı - Bütçe maliyet oranı karşılaştırması          |
|                                  | Maliyet öğesine göre İlk 10 Bütçe farkı                                                                          | Gerçek büyüklük - Bütçe büyüklüğü karşılaştırması          |
| Yıldan bugüne kadar maliyet denetimi     | Takvim Yılı Dönemine göre Fiili maliyet ve Bütçe maliyeti                                                                           | Fiili maliyet - Bütçe maliyeti karşılaştırması                    |
|                                  | Takvim Yılı Dönemine göre Bütçe farkı                                                                                       | Fiili maliyet oranı - Bütçe maliyet oranı karşılaştırması          |
|                                  | Maliyet öğesine göre İlk 10 Bütçe farkı                                                                          | Gerçek büyüklük - Bütçe büyüklüğü karşılaştırması          |
| Mali yıla göre Maliyet oranı         | Maliyet davranışına göre Fiili maliyet oranı                                                                                             | Fiili maliyet oranı - Bütçe maliyet oranı karşılaştırması          |
|                                  | Maliyet öğesi hiyerarşi seviyesine göre Fiili maliyet oranı, Bütçe maliyet oranı farkı, Bütçe maliyeti oranı yüzdesi ve Bütçe maliyeti oranı | Gerçek büyüklük - Bütçe büyüklüğü karşılaştırması          |
|                                  | Maliyeti öğesi hiyerarşi düzeyine göre bütçe farkı                                                                               |                                               |
|                                  | Maliyet öğesine göre İlk 10 Bütçe farkı                                                                          |                                               |
| Mali döneme göre Esnek bütçe | Maliyet öğesi hiyerarşi seviyesine göre Fiili maliyet, Bütçe maliyeti ve Esnek bütçe maliyeti                                             | Gerçek büyüklük - Bütçe büyüklüğü karşılaştırması          |
|                                  | Maliyet öğesi hiyerarşi seviyesine göre Bütçe farkı ve Esnek bütçe farkı                                                  | Fiili maliyet - Esnek bütçe maliyeti karşılaştırması           |
|                                  | Maliyet davranışı ve Maliyet öğesi hiyerarşi seviyesine göre Fiili maliyet, Bütçe maliyeti ve Esnek maliyet                                  | Fiili maliyet oranı - Esnek bütçe maliyet oranı karşılaştırması |
| Mali döneme göre maliyet raporu  | Maliyet öğesi hiyerarşi seviyesi ve Maliyet nesnesi boyut üye adına göre Fiili maliyet                                             |                                               |
|                                  | Maliyet nesnesi boyut üye adına ve Maliyeti öğesi boyut üye adına göre Fiili maliyet                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Aşağıdaki veriler **Maliyet muhasebesi analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesi](power-bi-integration-entity-store.md).

Aşağıdaki önemli toplam ölçümler, içeriğin temeli olarak kullanılır.

| Varlık                  | Kilit toplam ölçüm | Dynamics 365 için Veri kaynağı      | Alan     | Açıklama                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Maliyet muhasebesi girdileri | SUM(Tutar)               | CAMDATAAggregatedCostEntry        | Tutar    | Maliyet muhasebesi genel muhasebe para birimindeki tutar. |
| İstatistiksel girişler     | SUM(Büyüklük)            | CAMDATAAggregatedStatisctialEntry | Büyüklük |                                                    |

Aşağıdaki tablo önemli toplam ölçümlerin çok sayıda hesaplanmış ölçümünü içerik veri kümesini oluşturmak için nasıl kullanıldığını gösterir.

| Ölçü                                       | Ölçümün hesaplanması                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Gerçek maliyet                                   | CALCULATE('Maliyet muhasebesi girişleri'\[Ölçüm\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Bütçe maliyeti                                   | CALCULATE('Maliyet muhasebesi girişleri'\[Ölçüm\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Bütçe maliyet farkı                          | \[Bütçe maliyeti\] - \[Fiili maliyet\]                                                                                      |
| Bütçe farkı yüzdesi                    | IF(\[Bütçe maliyeti\] = 0, blank(), \[Bütçe farkı\] / \[Bütçe maliyeti\])                                                |
| Gerçek büyüklük                              | CALCULATE('İstatistiki girişler'\[FullMagnitude\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Bütçe büyüklüğü                              | CALCULATE(\[FullMagnitude\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| İstatistiksel bütçe farkı                   | \[Bütçe büyüklüğü\] - \[Gerçek büyüklük\]                                                                            |
| İstatistiksel bütçe farkı yüzdesi        | IF(\[Bütçe büyüklüğü\] = 0, blank(), \[İstatistiksel bütçe farkı\] / \[Bütçe büyüklüğü\])                          |
| Gerçek maliyet oranı                              | IF(\[Gerçek büyüklük\] = 0, BLANK(), \[Fiili maliyet\] / \[Gerçek büyüklük\])                                          |
| Bütçe maliyet oranı                              | IF(\[Bütçe büyüklüğü\] = 0, BLANK(), \[Bütçe maliyeti\] / \[Bütçe büyüklüğü\])                                          |
| Bütçe maliyet oranı farkı                     | \[Bütçe maliyet oranı\] - \[Fiili maliyet oranı\]                                                                            |
| Bütçe maliyet oranı farkı yüzdesi          | IF(\[Bütçe maliyeti\] = 0, blank(), \[Bütçe maliyeti oranı farkı\] / \[Bütçe maliyeti oranı\])                                 |
| Sabit bütçe maliyeti                             | CALCULATE(\[Bütçe maliyeti\], 'Maliyet muhasebesi girişleri'\[COSTBEHAVIOR\] = 1)                                              |
| Değişken bütçe maliyeti                          | CALCULATE(\[Bütçe maliyeti\], 'Maliyet muhasebesi girişleri'\[COSTBEHAVIOR\] = 2)                                              |
| Sabit esnek bütçe maliyeti                    | \[Sabit bütçe maliyeti\]                                                                                                  |
| Değişken esnek bütçe maliyeti                 | IF(\[Bütçe büyüklüğü\] = 0, BLANK(), (\[Değişken bütçe maliyeti\] / \[Bütçe büyüklüğü\]) \* \[Gerçek büyüklük\])       |
| Esnek bütçe maliyeti                          | \[Sabit esnek bütçe maliyeti\] + \[Değişken esnek bütçe maliyeti\]                                                     |
| Esnek bütçe farkı                      | \[Esnek bütçe maliyeti\] - \[Fiili maliyet\]                                                                             |
| Esnek bütçe farkı yüzdesi           | IF(\[Esnek bütçe maliyeti\] = 0, BLANK(), \[Esnek bütçe farkı\] / \[Esnek bütçe maliyeti\])                     |
| Esnek bütçe maliyeti oranı                     | IF(\[Gerçek büyüklük\] = 0, BLANK(), \[Esnek bütçe maliyeti\] / \[Gerçek büyüklük\])                                 |
| Esnek bütçe maliyet oranı farkı            | \[Esnek bütçe maliyeti oranı\] - \[Gerçek maliyet oranı\]                                                                   |
| Esnek bütçe maliyet oranı farkı yüzdesi | IF(\[Esnek bütçe maliyet oranı\] = 0, BLANK(), \[Esnek bütçe maliyet oranı farkı\] / \[Esnek bütçe maliyet oranı\]) |

Aşağıdaki anahtar boyutlar, daha büyük hassasiyet elde etmek ve daha derin analitik bilgiler edinmek için toplam ölçümleri bölmek amaçlı filtreler olarak kullanılır.

| Varlık                             | Öznitelik örnekleri                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Maliyet muhasebesi defterleri            | Maliyet muhasebesi defteri                                                                                               |
| Maliyet kontrolü birimleri                 | Maliyet kontrolü birimi adı                                                                                               |
| Maliyet öğesi boyutları            | Maliyet öğeleri boyutu adı, Maliyeti öğesi boyut üye adı, Maliyet öğesi boyut üye açıklaması          |
| Maliyet nesnesi boyutları             | Maliyet nesnesi boyutu adı, Maliyeti nesnesi boyutu üye adı, Maliyet nesnesi boyut üye açıklaması              |
| İstatistiksel boyutlar             | İstatistiksel boyut adı, İstatistiksel boyut üye adı, İstatistiksel boyut üye açıklaması              |
| Maliyet nesnesi boyut hiyerarşileri  | Maliyet nesnesi boyutu hiyerarşi adı, Maliyet nesnesi boyutu hiyerarşi seviyesi, Maliyet nesnesi boyutu hiyerarşi ağacı    |
| Maliyet öğesi boyut hiyerarşileri | Maliyet öğesi boyutu hiyerarşi adı, Maliyet öğesi boyutu hiyerarşi seviyesi, Maliyet öğesi boyutu hiyerarşi ağacı |
| İstatistiksel boyut hiyerarşileri  | İstatistiksel boyut hiyerarşi adı, İstatistiksel boyut hiyerarşi seviyesi, İstatistiksel boyut hiyerarşi ağacı    |
| Hareket sürümleri               | Sürüm adı                                                                                                         |
| Mali takvimler                   | Takvim, Takvim açıklaması                                                                                       |
| Mali yıllar                       | Takvim yılı                                                                                                        |
| Mali dönemler                     | Takvim yılı dönemi                                                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]