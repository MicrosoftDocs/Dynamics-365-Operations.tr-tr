---
title: "Maliyet Yönetimi güç BI içeriği"
description: "Bu konu, güç BI içeriği maliyet Yönetimi&quot;nde nelerin dahil edileceğini açıklar. Güç BI raporlara erişimi açıklar ve içerik oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Maliyet Yönetimi güç BI içeriği

Bu konu, güç BI içeriği maliyet Yönetimi'nde nelerin dahil edileceğini açıklar. Güç BI raporlara erişimi açıklar ve içerik oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

# <a name="overview"></a>Özet

**Yönetimi maliyet** Microsoft Power BI içerik stok muhasebeci veya kuruluş stok için sorumlu olan kişiler için tasarlanmıştır. **Yönetimi maliyet** güç BI içerik yönetim stok ve stok iş-arada devam eden (iş WIP) ve nasıl maliyet aralarında kategoriye göre zamanla akan bir anlayış sağlar. Bilgiler, mali tablo için ayrıntılı bir ek olarak da kullanılabilir.

## <a name="key-measures"></a>Anahtar ölçümleri

+ Başlangıç bakiyesi
+ Kapanış bakiyesi
+ Net değişiklik
+ Net Değişim %
+ Yaşlandırma

## <a name="key-performance-indicators"></a>Temel performans göstergeleri
+ Stok dönüşü
+ Stok doğruluğu

CostStatementCache tablo CostAggregatedCostStatementEntryEntity için birincil veri kaynağıdır. Bu tablo veri kümesi önbelleğini çerçevesi tarafından yönetilir. Varsayılan olarak, tablo, her 24 saatte bir güncelleştirilir, ancak veri önbelleği yapılandırmasında el ile güncelleştirmeleri etkinleştirebilir. El ile güncelleştirme sonra yapmak için **Yönetimi maliyet** veya **maliyet analizi** çalışma alanı. CostStatementCache güncelleştirme çalıştırdıktan sonra sitede güncelleştirilmiş verileri görmek için BI.com güç OData bağlantıda güncelleştirmeniz gerekir. Standart maliyet stok yöntemiyle valuated maddelerin varyans (satınalma, üretim) ölçümleri bu güç BI içerik ilgilidir. Üretim farkı gerçekleşmiş maliyet etkin maliyet arasındaki fark olarak hesaplanır. Üretim emrinin durumu varsa üretim farkı hesaplanır **Bitti**. Üretim farkı türleri ve her tür nasıl hesaplandığını hakkında daha fazla bilgi için bkz: [tamamlanmış üretim emri için varyans çözümleme hakkında](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Güç BI içeriğine erişerek
**Yönetimi maliyet** PowerBI.com güç BI içerik kullanılabilir. Bağlanmak ve veri işlemleri için Microsoft Dynamics 365 yükleme hakkında daha fazla bilgi için bkz: [PowerBI.com içeriği erişim güç BI](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Güç BI içeriğinde bulunan ölçümleri
İçerik rapor sayfaları kümesi içerir. Her sayfa, grafikler, döşeme ve tablo görünür ölçümler kümesinden oluşur. Aşağıdaki tabloda görsel bir bakış sağlar **Yönetimi maliyet** güç BI içeriği.

| Rapor sayfası | Grafikler | Başlıklar |
|---|---|---|
|Stok genel (varsayılan geçerli döneme göre) |Doğruluk |Stok ölçüleri:<br>Stok kapanış bakiyesi<br>Stok net değişim<br>Stok net değişim %<br>|
| |Stok dönüşü | |
| |Stok kapanış bakiyesi kaynak grubuna göre | |
| |Kategori adı düzey 1 ve kategori adı Düzey 2 stok net değişim| |
| |Satınalma sapmalarını kaynak grubu ve kategori adı düzeyi 3 | |
|Site (varsayılan olarak geçerli dönem) tarafından stok |Stok kapanış bakiyesi Site adı ve kaynak grubu | |
| |Site adı ve kaynak grubu ile Stok kapatma | |
| |Stok kapanış bakiyesi Şehir ve kaynak grubuna göre | |
|Kaynak grubu (varsayılan olarak geçerli dönem) tarafından stok |Stok ölçüleri | |
| |Envanter doğruluğu miktarda kaynak grubu tarafından | |
| |Stok kapatma tutarı ile kaynak grubu tarafından | |
|Stok yıllara göre (varsayılan geçerli yıl vs önceki yıl) |Stok ölçüleri | |
| |Stok KPI'ları:<br>Stok dönüşü<br>Stok doğruluğu | |
| |Stok kapanış bakiyesi yıl ve kaynak grubuna göre | |
| |Satınalma sapmalarını tarafından yıl ve kategori adı düzeyi 3 | |
|Stok yaşlandırma (varsayılan olarak geçerli yıl) |Üç aylık dönem ve kaynak grubuna göre stok yaşlandırma | |
| |Üç aylık dönem ve Site adına göre stok yaşlandırma | |
|Süren iş genel (varsayılan geçerli döneme göre) |Net Süren iş kategori adı düzey 1 ve kategori adı Düzey 2 değiştirin |Süren iş Süren ölçüleri:<br>Süren iş kapanış bakiyesi<br>Süren iş net değişim<br>Süren iş net değişim %<br> |
| |Üretim farklarının kaynak grubu ve kategori adı düzeyi 3 | |
| |Kaynak grubu tarafından Süren net değişim | |
|Süren iş sitesi (varsayılan geçerli döneme göre) |Süren iş Süren ölçümleri | |
| |Net Süren iş Site adı ve kategori adı Düzey 2 değiştirin | |
| |Üretim farklarının Site adı ve kategori adı düzeyi 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 işlemleri veriler için rapor sayfaları doldurmak için kullanılan **Yönetimi maliyet** güç BI içeriği. Bu veriler hazırlanır toplama ölçümleri temsil varlık deposunda olduğu analytics için en iyi duruma getirilmiş bir Microsoft SQL veritabanı. Daha fazla bilgi için bkz: [varlık deposu ile tümleştirme güç genel bakış BI](power-bi-integration-entity-store.md). Aşağıdaki anahtar toplama ölçümleri temel olarak kullanılır.

| Varlık            | Anahtar toplama ölçüm | Dynamics 365 işlemleri için veri kaynağı | Alan             | Açıklama                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Ekstresi girişlerindeki | Net değişiklik                | CostAggregatedCostStatementEntryEntity      | SUM (\[tutar\])   | Hesap para birimi cinsinden tutar |
| Ekstresi girişlerindeki | Net değişim miktarı       | CostAggregatedCostStatementEntryEntity      | SUM (\[miktar\]) |                                   |

Aşağıdaki tabloda anahtar toplam ölçüleri birkaç hesaplanmış ölçüler içinde içeriğin dataset oluşturmak için nasıl kullanıldığını gösterir.

| Ölçü                                 | Ölçü birimi nasıl hesaplanır                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Başlangıç bakiyesi                       | \[Kapanış bakiyesi\]-\[Net değişiklik\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Başlangıç bakiyesi miktarı              | \[Bitiş bakiye miktarı\]-\[Net değişim miktarı\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Kapanış bakiyesi                          | Hesapla (TOPLA (\[tutar\]), FİLTRE (ALLEXCEPT ('Mali Takvimler', 'Mali Takvimler'\[LedgerRecId\], 'varlık'\[kimlik\], 'varlık'\[adı\], 'Defterleri'\[para\], 'Defterleri'\[açıklama\], 'Defterleri'\[adı\]), 'Mali Takvimler'\[tarih\]&lt;MAX = ('Mali Takvimler'\[tarih\])))                                                                                                                                                                                           |
| Bitiş bakiye miktarı                 | Hesapla (TOPLA (\[miktar\]), FİLTRE (ALLEXCEPT ('Mali Takvimler', 'Mali Takvimler'\[LedgerRecId\], 'varlık'\[kimlik\], 'varlık'\[adı\], 'Defterleri'\[para\], 'Defterleri'\[açıklama\], 'Defterleri'\[adı\]), 'Mali Takvimler'\[tarih\]&lt;MAX = ('Mali Takvimler'\[tarih\])))                                                                                                                                                                                         |
| Stok Açılış bakiyesi             | Hesapla (\[Açılış bakiyesi\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                      |
| Stok kapanış bakiyesi                | Hesapla (\[kapanış bakiyesi\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                         |
| Stok net değişim                    | Hesapla (\[Net değişiklik\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                             |
| Stok net değişim miktarı           | Hesapla (\[Net değişim miktarı\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                    |
| Stok net değişim %                  | IF (\[stok kapanış bakiyesi\] = 0, 0, \[stok net değişim\] / \[stok kapanış bakiyesi\])                                                                                                                                                                                                                                                                                                                                                                           |
| Stok kapatma tutarı                | Varsa (OR (\[stok ortalama Bakiye\]&lt;= 0, \[stok satılan veya sorunlar tüketilen\]&gt;= 0), 0, ABS (\[stok satılan veya sorunlar tüketilen\]) /\[stok ortalama Bakiye\])                                                                                                                                                                                                                                                                                                  |
| Ortalama Stok bakiyesi               | (\[Stok kapanış bakiyesi\] + \[stok Başlangıç bakiyesi\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Stok satılan veya sorunlar tüketilen       | \[Satılan Stok\] + \[stok tüketilen malzeme maliyeti\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Stok tüketilen malzeme maliyeti        | Hesapla (\[stok net değişim\], 'Ekstresi girişlerindeki'\[kategori adını - Düzey 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Satılan Stok                          | Hesapla (\[stok net değişim\], 'Ekstresi girişlerindeki'\[kategori adını - Düzey 2\_\] = "Satıldı")                                                                                                                                                                                                                                                                                                                                                                             |
| Miktar stok doğruluk            | IF (\[stok kapanış bakiyesi\]&lt;= 0 ise (veya (\[stok sayımı tutar\]&lt;&gt; 0, \[stok kapanış bakiyesi\]&lt; 0), 0, 1), MAX (0, (\[stok kapanış bakiyesi\] -ABS (\[stok sayımı tutar\])) /\[stok kapanış bakiyesi\]))                                                                                                                                                                                                                              |
| Stok sayılan tutar                | Hesapla (\[stok net değişim\], 'Ekstresi girişlerindeki'\[kategori adını - Düzey 3\_\] = "Sayım")                                                                                                                                                                                                                                                                                                                                                                         |
| Stok eskimesi                         | Varsa (EBOŞSA (max ('Mali Takvimler'\[tarih\])), blank(), MAX (0, MIN (\[stok yaşlandırma giriş miktarı\], \[stok yaşlandırma Bitiş bakiye miktarı\] - \[miktar gelecekte tesellüm stok yaşlandırma\]))) \*\[stok ortalama birim maliyeti\]                                                                                                                                                                                                                                |
| Stok giriş miktarı eskime       | IF (\[minDate\] = \[minDateAllSelected\], Hesapla (\[stok miktarı net değişim\], 'Deyimi Girişleri'\[miktar\]&gt; 0, FİLTRE (ALLEXCEPT ('Mali Takvimler', 'Mali Takvimler'\[LedgerRecId\], 'varlık'\[kimliği\], 'varlık'\[adı\], 'Defterleri'\[para\], 'Defterleri'\[açıklama\], 'Defterleri'\[adı\]), 'Mali Takvimler'\[tarih\]&lt;MAX = ('Mali Takvimler'\[tarih\]))), Hesapla (\[stok miktarı net değişim\], 'Ekstresi girişlerindeki'\[miktar\]&gt; 0)) |
| Bitiş bakiye miktarı stok yaşlandırma | \[Bitiş bakiye miktarı stok\] + Hesapla (\[net değişim miktarı stok\], FİLTRE (ALLEXCEPT ('Mali Takvimler', 'Mali Takvimler'\[LedgerRecId\], 'varlık'\[kimlik\], 'varlık'\[adı\], 'Defterleri'\[para\], 'Defterleri'\[açıklama\], 'Defterleri'\[adı\]), 'Mali Takvimler'\[tarih\]&gt; max ('Mali Takvimler'\[tarih\])))                                                                                                                                 |
| Stok yaşlandırma gelecekte girişleri  | Hesapla (\[stok net değişim\], 'Deyimi Girişleri'\[tutar\]&gt; 0, FİLTRE (ALLEXCEPT ('Mali Takvimler', 'Mali Takvimler'\[LedgerRecId\], 'varlık'\[ID\], 'varlık'\[adı\], 'Defterleri'\[para\], 'Defterleri'\[açıklama\], 'Defterleri'\[adı\]), 'Mali Takvimler'\[tarih\]&gt; MAX ('Mali Takvimler'\[tarih\])))                                                                                                                                             |
| Stok ortalama birim maliyeti                 | Hesapla (\[stok kapanış bakiyesi\] / \[Bitiş bakiye miktarı stok\], ALLEXCEPT ('Mali Takvimler', 'Mali Takvimler'\[LedgerRecId\], 'varlık'\[ID\], 'varlık'\[adı\], 'Defterleri'\[para\], 'Defterleri'\[açıklama\], 'Defterleri'\[adı\]))                                                                                                                                                                                                                 |
| Satınalma sapmaları                      | Hesapla (TOPLA (\[tutar\]), 'Ekstresi girişlerindeki'\[kategori adı - Düzey 2\_\] "Ekstresi girişlerindeki'" Procured"=\[deyim türü\] ="Fark")                                                                                                                                                                                                                                                                                                                              |
| Süren iş başlangıç bakiyesi                   | Hesapla (\[Açılış bakiyesi\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Süren")                                                                                                                                                                                                                                                                                                                                                                                            |
| Süren iş kapanış bakiyesi                      | Hesapla (\[kapanış bakiyesi\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Süren")                                                                                                                                                                                                                                                                                                                                                                                               |
| Süren iş net değişim                          | Hesapla (\[Net değişiklik\], 'Ekstresi girişlerindeki'\[deyim türü\] = "Süren")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Süren iş net değişim %                        | IF (\[Süren kapanış bakiyesi\] = 0, 0, \[Süren net değişim\] / \[Süren kapanış bakiyesi\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Üretim farklarının                    | Hesapla (TOPLA (\[tutar\]), 'Ekstresi girişlerindeki'\[kategori adı - Düzey 2\_\] "Ekstresi girişlerindeki'" ManufacturedCost"=\[deyim türü\] ="Fark")                                                                                                                                                                                                                                                                                                                      |
| Kategori adı - düzey 1                 | Geçiş (\[kategori adı - düzey 1\_\], "None", "None", "NetSourcing", "kaynak Hizmeti'nden Net", "NetUsage", "Net kullanımı", "NetConversionCost", "maliyet dönüştürme Net", "NetCostOfGoodsManufactured", "Net üretilen Malların Maliyeti", "BeginningBalance", "Başlangıç bakiyesi")                                                                                                                                                                                                         |
| Kategori adı - Düzey 2                 | Geçiş (\[kategori adını - Düzey 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Transfer", "Transfer", "Satıldı", "Satıldı", "ConsumedMaterialsCost", "tüketilen malzeme maliyeti", "ConsumedManufacturingCost", "Üretim maliyet tüketilen", "ConsumedOutsourcingCost", "dış kaynak maliyeti tüketilen", "ConsumedIndirectCost", "dolaylı kullanılan maliyet", "ManufacturedCost", "Maliyet üreten", "Varyans", "Varyans")                            |
| Kategori adı - düzeyi 3                 | Geçiş (\[kategori adı - Düzey 3\_\], "None", "None", "Sayım", "None", "ProductionPriceVariance", "Üretim fiyatı", "QuantityVariance", "Miktar", "SubstitutionVariance", "Yedek", "ScrapVariance", "Hurda", "LotSizeVariance", "Lot Boyutu", "RevaluationVariance", "Değerleme", "PurchasePriceVariance", "Satınalma fiyatı", "CostChangeVariance" "" yuvarlama farkı"maliyeti değiştir", "RoundingVariance")                                                   |

Aşağıdaki anahtar boyutları daha parçalı yapı elde etmek ve daha derin analitik incelemeler sağlamak için toplam ölçüleri dilim için filtre olarak kullanılır.

| Varlık           | Öznitelik örnekleri                       |
|------------------|----------------------------------------------|
| Varlıklar         | Kimliği, adı                                     |
| Mali takvimler | Takvim Ay, dönem, üç ay, yıl       |
| KPI hedefleri        | Doğruluk hedef stok, stok açmak hedefi |
| Genel muhasebe defterleri          | Para birimi, ad, açıklama                  |
| Tesisler            | ID, ad, ülke, şehir                      |

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)



