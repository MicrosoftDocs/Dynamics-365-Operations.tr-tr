---
title: Satınalma ve harcama analizi Power BI içeriği
description: Bu konu, Power BI Satınalma harcaması analizinde nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182865"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Satınalma ve harcama analizi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Power BI **Satınalma harcaması analizinde** nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

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
<img src="media/spend1.PNG" alt="Purchase by vendor">

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


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

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
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Satıcı konumu bazında satınalma rapor sayfası

**Grafikler**
- Şehre göre satınalma
- Satınalmada yıldan yıla büyüme yüzdesi
- Ülkeye göre satınalma

**Örnek**
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Zamana göre satınalma harcaması analizi rapor sayfası

**Grafikler** 
- Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)
- Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)

**Örnek**
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Satıcıya göre satınalma harcaması analizi rapor sayfası

**Grafikler** 
- İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)
- Yıllara göre artan harcamayla en iyi 10 satıcı
- Yıllara göre azalan harcamayla en iyi 10 satıcı

**Örnek** 
<img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Veri modeli ve varlıklar
Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).

Bu içerik paketindeki toplama ölçümler, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için, [Power BI ile Varlık deposu tümleştirmesine genel bakış bölümündeki toplanan ölçümleri Varlık Deposuna ekleme yordamına](power-bi-integration-entity-store.md) bakın. Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.

| Varlık        | Önemli toplam ölçümler | Veri kaynağı                                 | Alan              | Açıklama                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Fatura satırları | Satınalma                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Muhasebe para birimi cinsinden tutar. |

Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.

| Ölçü               | Hesaplama                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Geçerli yıldaki satınalma | Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])                                            |
| Geçen yılki satınalma    | Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\]) |
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
