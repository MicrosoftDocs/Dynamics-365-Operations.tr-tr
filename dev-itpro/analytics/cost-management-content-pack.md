---
title: "Power BI maliyet yönetimi içeriği"
description: "Bu konu, Power BI Maliyet Yönetimi&quot;nde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 50889ffbbbc44d966081d60e5d631bd17476b6df
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="cost-management-power-bi-content"></a>Power BI maliyet yönetimi içeriği

[!include[banner](../includes/banner.md)]


Bu konu, Power BI Maliyet Yönetimi'nde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

# <a name="overview"></a>Özet

**Maliyet yönetimi** Microsoft Power BI içeriği stok muhasebecileri veya kuruluştaki stoktan sorumlu olan kişiler için tasarlanmıştır. **Yönetimi maliyeti** Power BI içeriği stok ve sürmekte olan iş (WIP) stokuna dair yönetimsel bilgi sağlar ve maliyetlerin bunların arasında zaman içerisinde nasıl bir akış gösterdiğini kategorilerle gösterir. Bu bilgiler, mali tabloya detaylı bir destekleyici olarak da kullanılabilir.

## <a name="key-measures"></a>Önemli ölçüler

+ Başlangıç bakiyesi
+ Kapanış bakiyesi
+ Net değişiklik
+ %'deki net değişiklik
+ Yaşlandırma

## <a name="key-performance-indicators"></a>Temel performans göstergeleri
+ Stok dönüşü
+ Stok doğruluğu

CostAggregatedCostStatementEntryEntity için birincil veri kaynağı CostStatementCache tablosudur. Bu tablo Veri kümesi önbelleğini çerçevesi tarafından yönetilir. Tablo varsayılan olarak her 24 saatte bir güncelleştirilir, ancak güncelleştirmeleri veri önbelleği yapılandırmasında el ile etkinleştirebilirsiniz. Daha sonra **Yönetimi maliyeti** veya **Maliyet analizi** çalışma alanlarında bir el ile güncelleştirme gerçekleştirebilirsiniz. CostStatementCache güncelleştirmesi çalıştırıldıktan sonra sitede güncelleştirilmiş verileri görmek için Power BI.com'da OData bağlantısını güncelleştirmeniz gerekir. Bu Power BI içeriğindeki fark (satın alma, üretim) önlemler, yalnızca Standart maliyet stok yönteminde değerlenmiş olan öğelerle ilgilidir. Üretim farkı gerçekleşmiş maliyet ve etkin maliyet arasındaki fark olarak hesaplanır. Üretim farkı, üretim siparişinin durumu **Bitti** olduğunda hesaplanır. Üretim farkı türleri ve her türün nasıl hesaplandığı hakkında daha fazla bilgi için bkz: [Tamamlanmış üretim emri için varyans çözümleme hakkında](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
**Yönetimi maliyeti** Power BI içeriği PowerBI.com adresinde bulunabilir. Microsoft Dynamics 365 for Operations verinizi yüklemek ve bağlamak hakkında daha fazla bilgi için bkz. [Power BI içeriğine PowerBI.com'dan erişin](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan ölçümler
İçerik bir dizi rapor sayfası içermektedir. Her sayfa grafikler, döşemeler ve tablolar ile görselleştirilen bir dizi ölçüm kümesinden oluşur. Aşağıdaki tablo **Yönetim maliyeti** Power BI içeriğindeki görselleştirmelere bir bakış sağlar.

| Rapor sayfası | Grafikler | Başlıklar |
|---|---|---|
|Stok genel (Varsayılan geçerli döneme göre) |Doğruluk |Stok ölçüleri:<br>Stok bitiş bakiyesi<br>Stok net değişimi<br>Stok net değişimi %'si<br>|
| |Stok dönüşü | |
| |Kaynak grubuna göre stok kapanış bakiyesi | |
| |Kategori adı düzey 1 ve Kategori adı düzeyi 2 stok net değişimi| |
| |Kaynak grubu ve kategori adı düzeyi 3 ile satınalma sapmaları | |
|Siteye göre stok (Varsayılan geçerli döneme göre) |Site adı ve Kaynak grubuna göre stok kapanış bakiyesi | |
| |Site adı ve Kaynak grubuna göre stok dönüşü | |
| |Şehre ve Kaynak grubuna göre stok kapanış bakiyesi | |
|Kaynak grubuna göre stok (Varsayılan geçerli döneme göre) |Stok ölçüleri | |
| |Tutara göre kaynağa göre stok doğruluğu | |
| |Tutara göre kaynağa göre stok dönüşü | |
|Yıldan yıla stok (varsayılan geçerli yıl - önceki yıla göre) |Stok ölçüleri | |
| |Stok KPI'ları:<br>Stok dönüşü<br>Stok doğruluğu | |
| |Yıl ve Kaynak grubuna göre stok kapanış bakiyesi | |
| |Yıl ve kategori adı düzeyi 3 ile satınalma sapmaları | |
|Stok yaşlandırma (Varsayılan olarak geçerli yıl) |Üç aylık dönem ve kaynak grubuna göre stok yaşlandırma | |
| |Üç aylık dönem ve Site adına göre stok yaşlandırma | |
|Süren iş genel (Varsayılan geçerli döneme göre) |Kategori adı düzey 1 ve Kategori adı düzeyi 2 Süren iş net değişimi |Süren iş süreci WIP ölçüleri:<br>Süren iş kapanış bakiyesi<br>Süren iş net değişim<br>Süren iş net değişim %'si<br> |
| |Kaynak grubu ve kategori adı düzeyi 3 ile üretim sapmaları | |
| |Kaynak grubuna göre süren iş net değişimi | |
|Siteye göre süren iş (Varsayılan geçerli döneme göre) |Süren iş süreci WIP ölçüleri | |
| |Site adı ve Kategori adı düzeyi 2 Süren iş net değişimi | |
| |Site adı ve kategori adı düzeyi 3 ile üretim sapmaları | |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 for Operations verisi, **Yönetim maliyeti** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, analytics için en iyi duruma getirilen bir Microsoft SQL veritabanı olan Varlık mağazasında hazırlanmış toplam ölçümler olarak temsil edilir. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md). Aşağıdaki önemli toplam ölçümler, içeriğin temeli olarak kullanılır.

| Varlık            | Kilit toplam ölçüm | Dynamics 365 for Operations için veri kaynağı | Alan             | Açıklama                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Rapor girişleri | Net değişiklik                | CostAggregatedCostStatementEntryEntity      | toplam(\[Tutar\])   | Muhasebe para birimi cinsinden tutar |
| Rapor girişleri | Net değişim miktarı       | CostAggregatedCostStatementEntryEntity      | toplam(\[Miktar\]) |                                   |

Aşağıdaki tablo önemli toplam ölçümlerin çok sayıda hesaplanmış ölçümünü içerik veri kümesini oluşturmak için nasıl kullanıldığını gösterir.

| Ölçü                                 | Ölçümün hesaplanması                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Başlangıç bakiyesi                       | \[Kapanış bakiyesi\]-\[Net değişiklik\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Başlangıç bakiyesi miktarı              | \[Bitiş bakiye miktarı\]-\[Net değişim miktarı\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Kapanış bakiyesi                          | HESAPLA(TOPLA (\[Tutar\]), FİLTRE(ALLEXCEPT('Mali takvimler', 'Mali takvimler'\[LedgerRecId\], 'varlık'\[kimlik\], 'varlık'\[adı\], 'Defterler'\[Para birimi\], 'Defterler'\[Açıklama\], 'Defterler'\[Adı\]), 'Mali takvimler'\[Tarih\] &lt;= MAX('Mali takvimler'\[Tarih\])))                                                                                                                                                                                           |
| Bitiş bakiye miktarı                 | HESAPLA(TOPLA (\[Miktar\]), FİLTRE(ALLEXCEPT('Mali takvimler', 'Mali takvimler'\[LedgerRecId\], 'varlık'\[kimlik\], 'varlık'\[adı\], 'Defterler'\[Para birimi\], 'Defterler'\[Açıklama\], 'Defterler'\[Adı\]), 'Mali takvimler'\[Tarih\] &lt;= MAX('Mali takvimler'\[Tarih\])))                                                                                                                                                                                         |
| Stok başlangıç bakiyesi             | HESAPLA(\[Açılış bakiyesi\], 'Ekstre girişleri'\[Ekstre türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                      |
| Stok bitiş bakiyesi                | HESAPLA(\[Kapanış bakiyesi\], 'Ekstre girişleri'\[Ekstre türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                         |
| Stok net değişimi                    | HESAPLA(\[Net değişim\], 'Ekstre girişleri'\[Ekstre türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                             |
| Stok net değişimi miktarı           | HESAPLA(\[Net değişim miktarı\], 'Ekstre girişleri'\[Ekstre türü\] = "Stok")                                                                                                                                                                                                                                                                                                                                                                                    |
| Stok net değişimi %'si                  | EĞER (\[Stok kapanış bakiyesi\] = 0, 0, \[Stok net değişimi\] / \[Stok kapanış bakiyesi\])                                                                                                                                                                                                                                                                                                                                                                           |
| Tutara göre stok devri                | Eğer(YA DA (\[stok ortalama bakiyesi\] &lt;= 0, \[Satılan stok veya tüketilen sorunlar\] &gt;= 0), 0, ABS (\[Satılan stok veya tüketilen sorunlar\])/\[Stok ortalama bakiye\])                                                                                                                                                                                                                                                                                                  |
| Stok ortalama bakiye               | (\[Stok kapanış bakiyesi\] + \[Stok başlangıç bakiyesi\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Satılan stok veya tüketilen sorunlar       | \[Satılan stok\] + \[tüketilen stok malzeme maliyeti\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Stok tüketilen malzeme maliyeti        | Hesapla (\[Stok net değişim\], 'Ekstre girişleri'\[Kategori adı - düzey 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Satılan stok                          | Hesapla (\[Stok net değişim\], 'Ekstre girişleri'\[Kategori adı - düzey 2\_\] = "Satılan")                                                                                                                                                                                                                                                                                                                                                                             |
| Tutara göre stok doğruluğu            | EĞER(\[stok kapanış bakiyesi\] &lt;= 0, EĞER(VEYA (\[stok sayımı tutarı\] &lt;&gt; 0, \[stok kapanış bakiyesi\] &lt; 0), 0, 1), MAKS (0, (\[stok kapanış bakiyesi\] -ABS (\[stok sayımı tutar\])) /\[stok kapanış bakiyesi\]))                                                                                                                                                                                                                              |
| Stok sayılan tutar                | Hesapla (\[Stok net değişim\], 'Ekstre girişleri'\[Kategori adı - düzey 3\_\] = "Sayılmakta")                                                                                                                                                                                                                                                                                                                                                                         |
| Stok eskimesi                         | Eğer (BOŞSA (maks ('Mali Takvimler'\[Tarih\])), blank(), MAKS (0, MİN (\[Stok yaşlandırma alınanlar miktarı\], \[Stok yaşlandırma bitiş bakiye miktarı\] - \[Gelecekteki stok yaşlandırma miktarı alınanları\]))) \* \[Stok ortalama birim maliyeti\]                                                                                                                                                                                                                                |
| Stok yaşlandırma alınanlar miktarı       | EĞER (\[minDate\] = \[minDateAllSelected\], HESAPLA (\[Stok net değişim miktarı\], 'Deyim girişleri'\[Miktar\] &gt; 0, FİLTRE (ALLEXCEPT ('Mali takvimler', 'Mali takvimler'\[LedgerRecId\], 'varlık'\[kimliği\], 'varlık'\[adı\], 'Defterler'\[Para birimi\], 'Defterler'\[Açıklama\], 'Defterler'\[Adı\]), 'Mali takvimler'\[Tarih\] &lt;MAKS = ('Mali takvimler'\[Tarih\]))), Hesapla (\[Stok net değişim miktarı\], 'Ekstre girişleri'\[Miktar\] &gt; 0)) |
| Stok yaşlandırma bitiş bakiye miktarı | \[Stok bitiş bakiye miktarı\] + HESAPLA(\[Stok net değişim miktarı\], FİLTRE(ALLEXCEPT('Mali takvimler', 'Mali takvimler'\[LedgerRecId\], 'varlıklar'\[ID\], 'varlıklar'\[Adı\], 'Defterler'\[Para birimi\], 'Defterler'\[Açıklama\], 'Defterler'\[Adı\]), 'Mali takvimler'\[Tarih\] &gt; maks('Mali takvimler'\[Tarih\]) ))                                                                                                                                 |
| Gelecekteki stok yaşlandırma alacakları  | CALCULATE(\[Stok net değişim\], 'Ekstre girişleri'\[Tutar\] &gt; 0, FILTER(ALLEXCEPT('Mali takvimler', 'Mali takvimler'\[LedgerRecId\], 'varlıklar'\[ID\], 'varlıklar'\[Adı\], 'Defterler'\[Para birimi\], 'Defterler'\[Açıklama\], 'Defterler'\[Adı\]), 'Mali takvimler'\[Tarih\] &gt; MAX('Mali takvimler'\[Tarih\])))                                                                                                                                             |
| Stok ortalama birim maliyeti                 | CALCULATE(\[Stok bitiş bakiyesi\] / \[Stok bitiş bakiye miktarı\],ALLEXCEPT('Mali takvimler', 'Mali takvimler'\[LedgerRecId\], 'varlıklar'\[ID\], 'varlıklar'\[Adı\], 'Defterler'\[Para birimi\], 'Defterler'\[Açıklama\], 'Defterler'\[Adı\]))                                                                                                                                                                                                                 |
| Satınalma farkları                      | HESAPLA (TOPLA (\[Tutar\]), 'Ekstre girişleri'\[Kategori adı - düzey 2\_\] = "Alınan", 'Ekstre girişleri\[Ekstre türü\] ="Fark")                                                                                                                                                                                                                                                                                                                              |
| Süren iş başlangıç bakiyesi                   | HESAPLA(\[Açılış bakiyesi\], 'Ekstre girişleri'\[Ekstre türü\] = "süren iş")                                                                                                                                                                                                                                                                                                                                                                                            |
| Süren iş kapanış bakiyesi                      | HESAPLA(\[Kapanış bakiyesi\], 'Ekstre girişleri'\[Ekstre türü\] = "süren iş")                                                                                                                                                                                                                                                                                                                                                                                               |
| Süren iş net değişim                          | HESAPLA(\[Net değişim\], 'Ekstre girişleri'\[Ekstre türü\] = "Süren iş")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Süren iş net değişim %'si                        | EĞER (\[Süren iş kapanış bakiyesi\] = 0, 0, \[Süren iş net değişim\] / \[Süren iş kapanış bakiyesi\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Üretim farkları                    | HESAPLA (TOPLA (\[Tutar\]), 'Ekstre girişleri'\[Kategori adı - düzey 2\_\] = "ManufacturedCost", 'Ekstre girişleri\[Ekstre türü\] ="Fark")                                                                                                                                                                                                                                                                                                                      |
| Kategori adı - seviye 1                 | geçiş(\[Kategori adı - düzey 1\_\], "Yok", "Yok", "NetSourcing", "Net kaynağı", "NetUsage", "Net kullanım", "NetConversionCost", "Net maliyet dönüştürme", "NetCostOfGoodsManufactured", "Üretilen malların net maliyeti", "BeginningBalance", "Başlangıç bakiyesi")                                                                                                                                                                                                         |
| Kategori adı - seviye 2                 | geçiş(\[adı - seviye 2\_\], "yok", "Yok", "Alınan", "Alınan", "Atılan", "Atılan", "Aktarılan", "Aktarılan", "Satılan", "Satılan", "ConsumedMaterialsCost", "Tüketilen malzeme maliyeti", "ConsumedManufacturingCost", "Tüketilen üretim maliyeti", "ConsumedOutsourcingCost", "Tüketilen dış kaynak maliyeti", "ConsumedIndirectCost", "Tüketilen dolaylı maliyet", "ManufacturedCost", "Üretilen maliyet", "Farklar", "Farklar")                            |
| Kategori adı - seviye 3                 | Geçiş (\[Kategori adı - düzey 3\_\], "Yok", "Yok", "Sayım", "None", "ProductionPriceVariance", "Üretim fiyatı", "QuantityVariance", "Miktar", "SubstitutionVariance", "Yedek", "ScrapVariance", "Hurda", "LotSizeVariance", "Lot Boyutu", "RevaluationVariance", "Değerleme", "PurchasePriceVariance", "Satınalma fiyatı", "CostChangeVariance" "" Yuvarlama farkı", "RoundingVariance", "Yuvarlama varyansı)                                                   |

Aşağıdaki anahtar boyutlar, daha büyük hassasiyet elde etmek ve daha derin analitik bilgiler edinmek için toplam ölçümleri bölmek amaçlı filtreler olarak kullanılır.

| Varlık           | Öznitelik örnekleri                       |
|------------------|----------------------------------------------|
| Varlıklar         | Kimliği, Adı                                     |
| Mali takvimler | Takvim, Ay, Dönem, Çeyrek, Yıl       |
| KPI hedefleri        | Stok doğruluk hedefi, Stok dönüş hedefi |
| Genel muhasebe defterleri          | Para birimi, Adı, Açıklama                  |
| Tesisler            | Kimlik, Ad, Ülke, Şehir                      |

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)





