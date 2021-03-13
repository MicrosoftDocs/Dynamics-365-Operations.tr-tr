---
title: Üretim performansı Power BI içeriği
description: Bu konu, Üretim performansı Power BI içeriğinde nelerin bulunduğunu açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c815a2e37f9882d695bf170a806301a3145d0f06
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094224"
---
# <a name="production-performance-power-bi-content"></a>Üretim performansı Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **Üretim performansı** Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Üretim performansı** Power BI içeriği, üretim müdürlerine veya kuruluşta üretim denetiminden sorumlu kişilere yöneliktir.

Dahil edilen raporlar Power BI'yı üretim işlemlerinin performansını zamanında yürütme, kalite ve maliyet açısından izlemek üzere kullanmanıza olanak tanır. Raporlar üretim emirlerinden ve toplu iş emirlerinden gelen hareket verilerini kullanır ve hem şirket genelindeki ölçümlerin toplam görünümünü hem de ürün ve kaynağa göre ölçümlerin dökümünü verir.

Power BI içeriği kuruluşun üretimi zamanında ve tam olarak tamamlama yeteneğini vurgular. Üretim planları temel alınarak gelecekteki performans yansıtılır. Kapsamlı raporlar üretimden kaynaklanan ürün kusurları hakkında ayrıntılı görüşler sağlar ve ayrıca kaynaklar ve operasyonlar için hata oranlarını sunar.

Bu Power BI içeriği aynı zamanda üretimdeki farkları analiz etmenizi sağlar. Üretim farkları gerçekleşmiş maliyet ve tahmini maliyet arasındaki fark olarak hesaplanır. Üretim farkları üretim emirleri veya toplu iş emirleri **Bitti** durumuna ulaştığında hesaplanır.

**Üretim performansı** Power BI içeriği üretim emirlerinden ve toplu iş emirlerden gelen verileri içerir. Raporlar kanban üretimlerle ilgili verileri içermez.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**Üretim performansı** Power BI içeriği, **Üretim performansı** sayfasında gösterilir (**Üretim denetimi** \> **Sorgulamalar ve raporlar** \> **Üretim performansı analizi** \> **Üretim performansı**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler

**Üretim performansı** Power BI içeriği bir dizi rapor sayfası içerir. Her sayfa grafikler, döşemeler ve tablolar ile görselleştirilen bir dizi ölçüm kümesinden oluşur.

Aşağıdaki tabloda, dahil edilen görsellere yönelik genel bakış sunulur.

| Rapor sayfası                                | Grafikler | Kutucuklar |
|--------------------------------------------|--------|-------|
| Üretim performansı                     | <ul><li>Tarihe göre üretim sayısı</li><li>Ürün ve madde grubuna göre üretim sayısı</li><li>Tarihe göre planlı üretim sayısı</li><li>Zamanında &amp; tam olarak ölçütüne göre en alttaki 10 ürün</li></ul> | <ul><li>Toplam sipariş</li><li>Zamanında &amp; tam olarak yüzdesi</li><li>Eksik yüzdesi</li><li>Erken yüzdesi</li><li>Geç yüzdesi</li></ul> |
| Ürüne göre hatalar                         | <ul><li>Tarihe göre hasar oranı (ppm)</li><li>Ürün ve madde grubuna göre hasar oranı (ppm)</li><li>Tarihe göre üretilen miktar</li><li>Geçerli orana göre ilk 10 ürün</li></ul> | <ul><li>Hasar oranı (ppm)</li><li>Bozuk miktar</li><li>Toplam miktar</li></ul> |
| Ürüne göre hasar eğilimi                   | Üretilen miktara göre hasar oranı (ppm) | Hasar oranı (ppm) |
| Kaynağa göre hasarlar                        | <ul><li>Tarihe göre hasar oranı (ppm)</li><li>Kaynak ve tesise göre hasar oranı (ppm)</li><li>Operasyona göre hasar oranı (ppm)</li><li>Hasar oranına göre en iyi 10 kaynak</li></ul> | Bozuk miktar |
| Kaynağa göre hasar eğilimi                  | İşlenen miktara göre hasar oranı (ppm) | |
| İş emri maliyetlendirme için üretim farkları | <ul><li>Tarih ve maliyet grubu türüne göre üretim farkı</li><li>Tesis ve maliyet grubu türüne göre üretim farkı</li><li>İstenmeyen üretim farkıyla en iyi 10 ürün</li><li>Kaynağa göre ilk 10 istenmeyen üretim farkı </li></ul> | <ul><li>Gerçekleşen maliyet</li><li>Üretim farkı</li><li>Üretim farkı yüzdesi</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Aşağıdaki veriler **Üretim performansı** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır. Varlık deposu hakkında daha fazla bilgi için bkz. [Varlık deposu ile Power BI tümleştirmesi](power-bi-integration-entity-store.md).

Aşağıdaki tabloda Power BI içeriğinin temeli olarak kullanılan başlıca toplama ölçümleri gösterilmektedir.

| Varlık                   | Önemli toplam ölçümler  | Finance and Operations uygulamaları için veri kaynağı | Alan              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Aşağıdaki tablo önemli toplam ölçümlerin çok sayıda hesaplanmış ölçümünü içerik veri kümesini oluşturmak için nasıl kullanıldığını gösterir.

| Ölçü                  | Ölçümün hesaplanması |
|--------------------------|-------------------------------|
| Üretim farkı, %   | TOPLA('Üretim farkı'\[Üretim farkı\]) / TOPLA('Üretim farkı'\[Tahmini maliyet\]) |
| Tüm planlanan siparişler       | COUNTROWS('Planlanan üretim emri') |
| Erken                    | COUNTROWS(FILTER('Planlanan üretim emri', 'Planlanan üretim emri'\[Planlanan bitiş tarihi\] \< 'Planlanan üretim emri'\[Gereksinim tarihi\])) |
| Geç                     | COUNTROWS(FILTER('Planlanan üretim emri', 'Planlanan üretim emri'\[Planlanan bitiş tarihi\] \> 'Planlanan üretim emri'\[Gereksinim tarihi\])) |
| Zamanında                  | COUNTROWS(FILTER('Planlanan üretim emri', Planlanan üretim emri'\[Planlanan bitiş tarihi\] = 'Planlanan üretim emri'\[Gereksinim tarihi\])) |
| Zamanında %                | IF ('Planlanan üretim emri'\[Zamanında\] \<\> 0, 'Planlanan üretim emri'\[Zamanında\], IF ('Planlanan üretim emri'\[Tüm planlanan siparişler\] \<\> 0, 0, BLANK()) ) / 'Planlanan üretim emri'\[Tüm planlanan siparişler\] |
| Tamamlandı                | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Is RAF'ed\] = TRUE)) |
| Hasar oranı (ppm)     | IF( 'Üretim emri'\[Toplam miktar\] = 0, BLANK(), (SUM('Üretim emri'\[Hasarlı miktar\]) / 'Üretim emri'\[Toplam miktar\]) \* 1000000) |
| Ertelenen üretim oranı  | 'Üretim emri'\[Geç \#\] / 'Üretim emri'\[Tamamlandı\] |
| Erken ve tam          | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Tam\] = TRUE && 'Üretim emri'\[Erken\] = TRUE)) |
| Erken \#                 | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Erken\] = TRUE)) |
| Erken yüzdesi                  | IFERROR( IF('Üretim emri'\[Early \#\] \<\> 0, 'Üretim emri'\[Erken \#\], IF('Üretim emri'\[Toplam sipariş\] = 0, BLANK(), 0)) / 'Üretim emri'\[Toplam sipariş\], BLANK()) |
| Eksik               | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Tam\] = FALSE && 'Üretim emri'\[Is RAF'ed\] = TRUE)) |
| Eksik yüzdesi             | IFERROR( IF('Üretim emri'\[Incomplete\] \<\> 0, 'Üretim emri'\[Incomplete\], IF('Üretim emri'\[Toplam sipariş\] = 0, BLANK(), 0)) / 'Üretim emri'\[Toplam sipariş\], BLANK()) |
| Gecikmiş               | 'Üretim emri'\[Is RAF'ed\] = TRUE && 'Üretim emri'\[Gecikmiş değer\] = 1 |
| Erken                 | 'Üreim emri'\[Is RAF'ed\] = TRUE && 'Üretim emri'\[Geciken gün\] \< 0 |
| Tam               | 'Üretim emri'\[Sağlam miktar\] \>= 'Üretim emri'\[Planlanan miktar\] |
| RAF'ed                | 'Üretim emri'\[Üretim durumu değeri\] = 5 \|\| 'Üretim emri'\[Üretim durumu değeri\] = 7 |
| Geç ve tam           | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Tam\] = TRUE && 'Üretim emri'\[Gecikmiş\] = TRUE)) |
| Geç \#                  | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Gecikmiş\] = TRUE)) |
| Geç yüzdesi                   | IFERROR( IF('Üretim emri'\[Geç \#\] \<\> 0, 'Üretim emri'\[Geç \#\], IF('Üretim emri'\[Toplam sipariş\] = 0, BLANK(), 0)) / 'Üretim emri'\[Toplam sipariş\], BLANK()) |
| Zamanında ve tam        | COUNTROWS(FILTER('Üretim emri', 'Üretim emri'\[Tam\] = TRUE && 'Üretim emri'\[Gecikmiş\] = FALSE && 'Üretim emri'\[Erken\] = FALSE)) |
| Zamanında ve tam olarak yüzdesi      | IFERROR( IF('Üretim emri'\[Zamanında ve tam\] \<\> 0, 'Üretim emri'\[Zamanında ve tam\], IF('Üretim emri'\[Tamamlandı\] = 0, BLANK(), 0)) / 'Üretim emri'\[Tamamlandı\], BLANK()) |
| Toplam sipariş             | COUNTROWS('Üretim emri') |
| Toplam miktar           | SUM('Üretim emri'\[Sağlam miktar\]) + SUM('Üretim emri'\[Hasarlı miktar\]) |
| Hasar oranı (ppm)        | IF( 'Rota hareketleri'\[İşlenen miktar\] = 0, BLANK(), (SUM('Rota hareketleri'\[Hasarlı miktar\]) / 'Rota hareketleri'\[İşlenen miktar\]) \* 1000000) |
| Hata oranı karma (ppm) | IF( 'Rota hareketleri'\[Toplam karışım miktarı\] = 0, BLANK(), (SUM('Rota hareketleri'\[Hasarlı miktar\]) / 'Rota hareketleri'\[Toplam karışık miktarı\]) \* 1000000) |
| İşlenen miktar       | SUM('Rota hareketleri'\[Sağlam miktar\]) + SUM('Rota hareketleri'\[Hasarlı miktar\]) |
| Toplam karışık miktar     | SUM('Üretim emri'\[Sağlam miktar\]) + SUM('Rota hareketleri'\[Hasarlı miktar\]) |

Aşağıdaki tablo, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılan temel boyutları gösterir.

| Varlık                    | Öznitelik örnekleri                                        |
|---------------------------|---------------------------------------------------------------|
| Tamamlandığı bildirilen tarih | Tamamlanma tarihi (RAF), Ay ve Yıl denkleştirme                 |
| Bitiş tarihi                | Biten ay denkleştirme ve Ay                                  |
| Gereksinim tarihi          | Gereksinim tarihi ay denkleştirme ve Gereksinim tarihi            |
| Rota hareketi tarihi    | Rota hareketi ay denkleştirme ve Tarih                       |
| Tesisler                     | Tesis kodu, Tesis adı, Eyalet ve Şehir                          |
| Varlıklar                  | Kimlik ve Ad                                                   |
| Kaynaklar                 | Kaynak Kodu, Kaynak adı, Kaynak türü ve Kaynak grubu |
| Ürünler                  | Ürün numarası, Ürün adı, Madde Kodu ve Madde grubu         |
