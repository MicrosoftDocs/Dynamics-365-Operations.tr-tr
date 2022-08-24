---
title: Satınalma ve harcama analizi Power BI içeriği
description: Bu makale, Satınalma harcaması analizi Power BI içeriğinde nelerin bulunduğunu açıklar.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.form: PurchaseSpendAnalysisPowerBI
ms.openlocfilehash: 757b782131617104422e15f3ceec747b92d96666
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276675"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Satınalma ve harcama analizi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makale, **Satınalma harcaması analizi** Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Satınalma harcaması analizi** Power BI içeriği satınalma yöneticilerine ve bütçelerden sorumlu yöneticilere satınalma harcamalarını izleme konusunda yardımcı olmak üzere tasarlanmıştır. Yöneticiler satınalma harcamasını aşağıdaki şekillerde analiz edebilirler:

- Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)
- Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)

İçerik, alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir. Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır. Bu nedenle, raporlar yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir. Ek olarak grafikler farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir. Bu nedenle, kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanabilirler.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**Satınalma ve harcama analizi** Power BI içeriği **Satın alma ve harcama analizi** sayfasında gösterilir (**Tedarik ve kaynak atama** \> **Sorgular ve raporlar** \> **Satın alma performansı analizi** \> **Satın alma ve harcama analizi**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler
**Satın alma harcaması analizi** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. 

Aşağıdaki bölümde, görsellere yönelik genel bakış sunulur.

### <a name="purchase-by-vendor-report-page"></a>Satıcı bazında satınalma rapor sayfası
**Grafikler**
- Satınalmaya göre en iyi 10 satıcı (yığılmış çubuk grafik)
- Satıcı grubuna / ülkeye / ada göre toplam satınalma (pasta grafik)
- Satıcı grubuna / ülkeye / ada göre satınalma (sütun grafik)
- Satıcı grubuna / ülkeye / ada göre ortalama satınalma (sütun grafik)

**Kutucuklar**
- Satınalma toplamı
- Yıllara göre satınalmadaki büyüme
- Toplam satıcı sayısı
- Toplam etkin satıcı sayısı

**Örnek**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Ürün bazında satınalma rapor sayfası

**Grafikler**
- Tedarik kategorisine / ürün adına göre satınalma (sütun grafiği)
- Tedarik kategorisine / ürün adına göre toplam satınalma (pasta grafik)
- Satınalmaya göre en iyi 10 ürün (yığılmış çubuk grafik)

**Kutucuklar**
- Toplam ürün sayısı</li>
- Etkin ürünlerin toplam sayısının toplam etkin ürünlere yüzdesi
- Satınalmanın %80'ini oluşturan ürünlerin sayısı

**Örnek**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Dönem bazında satınalma rapor sayfası
Bu sayfa bu yılki ve geçen yılki satınalmayı ve tedarik kategorisine göre büyümeyi gösterir.

**Grafikler** 
- Aya / güne göre satınalma (sütun grafiği)
- Toplam satınalmanın yıllara görefarkı (şelale grafik)
- Toplam satınalmada yıllara göre büyüme (sütun grafik)
- Tedarik ekstresi (matriks)

**Kutucuklar**
- Yıllara göre satınalmadaki büyüme
- Yıllara göre satınalmadaki büyüme yüzdesi

**Örnek**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Satıcı konumu bazında satınalma rapor sayfası

**Grafikler**
- Şehre göre satınalma
- Satınalmada yıldan yıla büyüme yüzdesi
- Ülkeye göre satınalma

**Örnek**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Zamana göre satınalma harcaması analizi rapor sayfası

**Grafikler** 
- Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)
- Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)

**Örnek**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Satıcıya göre satınalma harcaması analizi rapor sayfası

**Grafikler** 
- İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)
- Yıllara göre artan harcamayla en iyi 10 satıcı
- Yıllara göre azalan harcamayla en iyi 10 satıcı

**Örnek** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Veri modeli ve varlıklar
Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır. Daha fazla bilgi için bkz. [Varlık mağazası ile Power BI tümleştirmesi](power-bi-integration-entity-store.md).

Bu içerik paketindeki toplama ölçümler, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için [Power BI ile Varlık deposu tümleştirmesi](power-bi-integration-entity-store.md) bölümündeki toplanan ölçümleri Varlık Deposuna ekleme prosedürüne bakın. Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.

| Varlık        | Önemli toplam ölçümler | Veri kaynağı                                 | Alan              | Açıklama                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Fatura satırları | Satınalma                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Muhasebe para birimi cinsinden tutar. |

Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.

| Ölçü               | Hesaplama                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Geçerli yıldaki satınalma | Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])                                            |
| Geçen yılki satınalma    | Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\])) |
| Yıllara göre satınalmadaki büyüme   | Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\]: \[Geçen yıldaki satınalma\]                            |

İçerikte bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.

| Varlık                 | Öznitelik örnekleri                                |
|------------------------|-------------------------------------------------------|
| Satıcılar                | Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı |
| Ürünler               | Ürün numarası, Ürün adı, Madde grupları adı        |
| Tedarik kategorileri | Tedarik kategorisi, Tedarik kategorisi adları      |
| Tüzel kişilikler         | Tüzel kişiliğin adı                                     |
| Tarihler                  | Tarihler, Yıl denkleştirme                                    |

Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir. Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz. Şirket filtresini de değiştirebilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
