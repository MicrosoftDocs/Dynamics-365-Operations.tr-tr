---
title: Maliyet yönetimi Power BI içeriği
description: Bu makalede, Maliyet yönetimi Power BI içeriğinde nelerin bulunduğu açıklanmaktadır.
author: JennySong-SH
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom:
- "270314"
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.industry: Manufacturing
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
ms.openlocfilehash: 7dcc8b2df62b250c59e343e0def5840f1b4f5432
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205713"
---
# <a name="cost-management-power-bi-content"></a>Maliyet yönetimi Power BI içeriği

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Genel bakış

**Maliyet yönetimi** Microsoft Power BI içeriği stok muhasebecileri veya kuruluş içinde stok durumundan veya süren işten (WIP) sorumlu olan veya bunlarla ilgilenen veya standart maliyet farklarından sorumlu kişilere yöneliktir.

Bu Power BI içeriği stokların performansını izlemenize ve maliyetin bunlar üzerinde nasıl akış sağladığını görselleştirmenize yardımcı olan kategorilere ayrılmış bir biçim sağlar. Ciro oranı, stoğun elde olduğu gün sayısı, doğruluk, tercih ettiğiniz toplama düzeyinde "ABC sınıflandırması" (şirket, madde, madde grubu veya tesis) gibi yönetimsel öngörüler de elde edebilirsiniz. Kullanıma sunulan bu bilgiler, mali tabloya detaylı bir destekleyici olarak da kullanılabilir.

Power BI içeriği birincil veri kaynağı olarak **CostObjectStatementCache** tablosunu kullanan **CostObjectStatementCacheMonthly** toplam ölçümüne yerleşiktir. Bu tablo Veri kümesi önbelleğini çerçevesi tarafından yönetilir. Tablo varsayılan olarak her 24 saatte bir güncelleştirilir, ancak güncelleştirme sıklığını değiştirebilir veya veri kümesi önbelleği yapılandırmasında el ile güncelleştirmeyi etkinleştirebilirsiniz. El ile güncelleştirmeler **Maliyet yönetimi** çalışma alanı veya **Maliyet analizi** çalışma alanından çalıştırılabilir.

**CostObjectStatementCache** tablosunun her güncelleştirilmesinden sonra, **CostObjectStatementCacheMonthly** toplama ölçümünün Power BI görselleştirmelerindeki veriler güncelleştirilmeden önce güncelleştirilmesi gerekir.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim

**Maliyet yönetimi** Power BI içeriği **Maliyet yönetimi** ve **Maliyet analizi** çalışma alanında gösterilir.

**Maliyet yönetimi** çalışma alanı aşağıdaki sekmeleri içerir:

- **Genel Bakış**: Bu sekme, uygulama verilerini gösterir.
- **Stok muhasebesi durumu** - Bu sekme Power BI içeriğini gösterir.
- **Üretim muhasebesi durumu** - Bu sekme Power BI içeriğini gösterir.

**Maliyet analizi** çalışma alanı aşağıdaki sekmeleri içerir:

- **Genel Bakış**: Bu sekme, uygulama verilerini gösterir.
- **Stok muhasebesi analizi** - Bu sekme Power BI içeriğini gösterir.
- **Üretim muhasebesi analizi** - Bu sekme Power BI içeriğini gösterir.
- **Standart maliyet farkı analizi** - Bu sekme Power BI içeriğini gösterir.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil edilen rapor sayfaları

**Cost management** Power BI içeriği, bir dizi ölçümden oluşan bir rapor sayfaları kümesi içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. 

Aşağıdaki tablolar **Yönetim maliyeti** Power BI içeriğindeki görselleştirmelere bir bakış sağlar.

### <a name="inventory-accounting-status"></a>Stok muhasebesi durumu

| Rapor sayfası                               | Gözde canlandırma                                   |
|-------------------------------------------|-------------------------------------------------|
| Stok özeti                        | Başlangıç bakiyesi                               |
|                                           | Net değişiklik                                      |
|                                           | Net değişiklik %                                    |
|                                           | Kapanış bakiyesi                                  |
|                                           | Stok doğruluğu                              |
|                                           | Stok devir hızı oranı                        |
|                                           | Eldeki stok günleri                          |
|                                           | Dönemdeki etkin ürün                        |
|                                           | Dönemdeki etkin maliyet nesneleri                   |
|                                           | Madde grubuna göre bakiye                           |
|                                           | Tesise göre bakiye                                 |
|                                           | Kategoriye göre ekstre                           |
|                                           | Üç aylık dönem başına net değişiklik                           |
| Tesis ve madde grubuna göre stoğa genel bakış | Tesise göre stok doğruluğu                      |
|                                           | Tesise göre stok ciro oranı                |
|                                           | Tesise göre stok bitiş bakiyesi                |
|                                           | Madde grubuna göre stok doğruluğu                |
|                                           | Madde grubuna göre stok ciro oranı          |
|                                           | Tesise ve madde grubuna göre stok bitiş bakiyesi |
| Stok ekstresi                       | Stok ekstresi                             |
| Tesise göre stok ekstresi               | Tesise göre stok ekstresi                     |
| Ürün hiyerarşisine göre stok ekstresi  | Stok ekstresi                             |
| Ürün hiyerarşisine göre stok ekstresi  | Tesise göre stok ekstresi                     |

### <a name="manufacturing-accounting-status"></a>Üretim muhasebesi durumu

| Rapor sayfası                | Gözde canlandırma                       |
|----------------------------|-------------------------------------|
| Süren işe genel bakış YTD           | Başlangıç bakiyesi                   |
|                            | Net değişiklik                          |
|                            | Net değişiklik %                        |
|                            | Kapanış bakiyesi                      |
|                            | Süren iş ciro oranı                  |
|                            | Süren iş eldeki stok günleri                    |
|                            | Dönemdeki etkin maliyet nesnesi        |
|                            | Kaynak grubuna göre net değişim        |
|                            | Tesise göre bakiye                     |
|                            | Kategoriye göre ekstre               |
|                            | Üç aylık dönem başına net değişiklik               |
| süren iş raporu              | Başlangıç bakiyesi                   |
|                            | Kapanış bakiyesi                      |
|                            | Kategoriye göre süren iş ekstresi           |
| Tesise göre süren iş ekstresi      | Başlangıç bakiyesi                   |
|                            | Kapanış bakiyesi                      |
|                            | Kategori ve tesise göre süren iş ekstresi  |
| Hiyerarşiye göre süren iş ekstresi | Başlangıç bakiyesi                   |
|                            | Kapanış bakiyesi                      |
|                            | Kategori hiyerarşisine göre süren iş ekstresi |

### <a name="inventory-accounting-analysis"></a>Stok muhasebesi analizi

| Rapor sayfası        | Gözde canlandırma                                                                |
|--------------------|------------------------------------------------------------------------------|
| Stok ayrıntıları  | Kapanış bakiyesine göre en iyi 10 kaynak                                           |
|                    | Net değişim artışına göre en iyi 10 kaynak                                      |
|                    | Net değişim düşüşüne göre en iyi 10 kaynak                                      |
|                    | Stok ciro oranına göre en iyi 10 kaynak                                 |
|                    | Düşük stok ciro oranı ve eşik üzerindeki kapanış bakiyesine göre kaynaklar |
|                    | Düşük doğruluğa göre en iyi 10 kaynak                                             |
| ABC sınıflandırması | Stok bitiş bakiyesi                                                     |
|                    | Tüketilen malzeme                                                            |
|                    | Satılan (SMM)                                                                  |
| Stok eğilimleri   | Stok bitiş bakiyesi                                                     |
|                    | Stok net değişimi                                                         |
|                    | Stok devir hızı oranı                                                     |
|                    | Stok doğruluğu                                                           |

### <a name="manufacturing-accounting-analysis"></a>Üretim muhasebesi analizi

| Rapor sayfası | Gözde canlandırma      |
|-------------|--------------------|
| Süren iş eğilimleri  | Süren iş kapanış bakiyesi |
|             | Süren iş net değişim     |
|             | Süren iş ciro oranı |

### <a name="std-cost-variance-analysis"></a>Standart maliyet farkı analizi

| Rapor sayfası                             | Gözde canlandırma                                        |
|-----------------------------------------|------------------------------------------------------|
| Satınalma fiyatı farkı (Std. maliyet) YTD | Sağlanan bakiye                                     |
|                                         | Satınalma fiyat farkı                              |
|                                         | Satınalma fiyat farkı oranı                        |
|                                         | Madde grubuna göre fark                               |
|                                         | Tesise göre fark                                     |
|                                         | Üç aylık döneme göre satınalma fiyatı                            |
|                                         | Üç aylık dönem ve madde grubuna göre satınalma fiyatı             |
|                                         | Uygun olmayan satınalma fiyatı oranına göre en iyi 10 kaynak |
|                                         | Uygun satınalma fiyatı oranına göre en iyi 10 kaynak   |
| Üretim farkı (Std. maliyet) YTD     | Üretim maliyeti                                    |
|                                         | Üretim farkı                                  |
|                                         | Üretim farkı oranı                            |
|                                         | Madde grubuna göre fark                               |
|                                         | Tesise göre fark                                     |
|                                         | Üç aylık döneme göre üretim farkı                       |
|                                         | Üç aylık dönem ve fark türüne göre üretim farkı     |
|                                         | Uygun olmayan üretim farkına göre en iyi 10 kaynak  |
|                                         | Uygun üretim farkına göre en iyi 10 kaynak    |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Uygulamadan alınan veriler, **Maliyet yönetimi** Power BI içeriğinin rapor sayfalarını doldurmak için kullanılır. Bu veri, analytics için en iyi duruma getirilen bir Microsoft SQL Server olan varlık mağazasında hazırlanmış toplam ölçümler olarak temsil edilir. Daha fazla bilgi için bkz. [Varlık mağazası ile Power BI tümleştirmesi](power-bi-integration-entity-store.md).

Aşağıdaki nesnelerin başlıca toplama ölçümleri Power BI içeriğinin temeli olarak kullanılır.

| Nesne                          | Önemli toplam ölçümler | Finans ve operasyon uygulamaları için veri kaynağı | Alan               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Tutar                     | CostObjectStatementCache               | Tutar              |
| CostObjectStatementCacheMonthly | Miktar                   | CostObjectStatementCache               | Miktar                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Aşağıdaki tabloda Power BI içeriğinde hesaplanan temel ölçümler gösterilir.

| Ölçü                            | Hesaplama |
|------------------------------------|-------------|
| Başlangıç bakiyesi                  | Başlangıç bakiyesi = \[Bitiş bakiyesi\]-\[Net değişiklik\] |
| Başlangıç bakiyesi miktarı             | Başlangıç bakiyesi miktarı = \[Bitiş bakiyesi miktarı\]-\[Net değişiklik miktarı\] |
| Kapanış bakiyesi                     | Bitiş bakiyesi = (CALCULATE(SUM(\[Tutar\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Bitiş bakiyesi miktarı                | Bitiş bakiyesi miktarı = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Net değişiklik                         | Net değişiklik = SUM(\[AMOUNT\]) |
| Net değişiklik miktarı                    | Net değişiklik miktarı = SUM(\[QTY\]) |
| Tutara göre stok ciro oranı | Tutara göre stok ciro oranı = if(OR(\[Stok ortalama bakiyesi\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Stok satılan veya tüketilen çıkışlar\])/\[Stok ortalama bakiyesi\]) |
| Stok ortalama bakiye          | Stok ortalama bakiyesi = ((\[Bitiş bakiyesi\] + \[Başlangıç bakiyesi\]) / 2) |
| Eldeki stok günleri             | Eldeki stok günleri = 365 / CostObjectStatementEntries\[Tutara göre stok ciro oranı\] |
| Stok doğruluğu                 | Tutara göre stok doğruluğu = IF (\[Bitiş bakiyesi\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Bitiş bakiyesi\] \< 0), 0, 1), MAX(0, (\[Bitiş bakiyesi\] - ABS(\[Stok sayılan tutar\]))/\[Bitiş bakiyesi\])) |

Aşağıda belirtilen temel boyutlar daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.


| Varlık                                                  | Öznitelik örnekleri                          |
|---------------------------------------------------------|-------------------------------------------------|
| Ürünler                                                | Ürün numarası, Ürün adı, Birim, Madde grupları |
| Kategori hiyerarşileri (Maliyet yönetimi rolüne atanan) | Kategori hiyerarşisi, Kategori düzeyi              |
| Tüzel kişilikler                                          | Tüzel kişilik adları                              |
| Mali takvimler                                        | Mali yıl, Yıl, Üç aylık dönem, Dönem, Ay   |
| Tesis                                                    | Kod, Ad, Adres, Eyalet, Ülke               |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

