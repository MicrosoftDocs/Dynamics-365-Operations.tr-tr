---
title: "Satınalma harcaması analizi Power BI içeriği"
description: "Bu konu, Power BI Satınalma harcaması analizinde nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 07b6f433a8355d7f9ed6dce8e26f78d38a86a713
ms.contentlocale: tr-tr
ms.lasthandoff: 12/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Satınalma harcaması analizi Power BI içeriği

[!INCLUDE [banner](../includes/banner.md)]

Bu konu, Power BI **Satınalma harcaması** analizinde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Satınalma harcaması analizi** Power BI içeriği satınalma yöneticilerine ve bütçelerden sorumlu yöneticilere satınalma harcamalarını izleme konusunda yardımcı olmak üzere tasarlanmıştır. Yöneticiler satınalma harcamasını aşağıdaki şekillerde analiz edebilirler:

-   Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)
-   Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)

İçerik, alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir. Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır. Bu nedenle, raporlar yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir. Ek olarak grafikler farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir. Bu nedenle, kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanabilirler.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
**Satınalma harcaması analizi** Power BI içeriği **Satın alma ve harcama analizi** sayfasında gösterilir (**Tedarik ve kaynak atama** > **Sorgulamalar ve raporlar** > **Satın alma performansı analizi** > **Satın alma ve harcama analizi**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan ölçümler
**Satın alma harcaması analizi** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. Aşağıdaki tabloda, görsellere yönelik genel bakış sunulur.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Rapor sayfası</th>
<th>Grafikler</th>
<th>Kutucuklar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Satıcıya göre satınalma</td>
<td><ul>
<li>Satınalmaya göre en iyi 10 satıcı (yığılmış çubuk grafik)</li>
<li>Satıcı grubuna / ülkeye / ada göre toplam satınalma (pasta grafik)</li>
<li>Satıcı grubuna / ülkeye / ada göre satınalma (sütun grafik)</li>
<li>Satıcı grubuna / ülkeye / ada göre ortalama satınalma (sütun grafik)</li>
</ul></td>
<td><ul>
<li>Satınalma toplamı</li>
<li>Yıllara göre satınalmadaki büyüme</li>
<li>Toplam satıcı sayısı</li>
<li>Toplam etkin satıcı sayısı</li>
</ul></td>
</tr>
<tr class="even">
<td>Ürüne göre satın alma</td>
<td><ul>
<li>Tedarik kategorisine / ürün adına göre satınalma (sütun grafiği)</li>
<li>Tedarik kategorisine / ürün adına göre toplam satınalma (pasta grafik)</li>
<li>Satınalmaya göre en iyi 10 ürün (yığılmış çubuk grafik)</li>
</ul></td>
<td><ul>
<li>Toplam ürün sayısı</li>
<li>Etkin ürünlerin toplam sayısının toplam etkin ürünlere yüzdesi</li>
<li>Satınalmanın %80'ini oluşturan ürünlerin sayısı</li>
</ul></td>
</tr>
<tr class="odd">
<td>Döneme göre satınalma*</td>
<td><ul>
<li>Aya / güne göre satınalma (sütun grafiği)</li>
<li>Toplam satınalmanın yıllara görefarkı (şelale grafik)</li>
<li>Toplam satınalmada yıllara göre büyüme (sütun grafik)</li>
<li>Tedarik ekstresi (matriks)</li>
</ul></td>
<td><ul>
<li>Yıllara göre satınalmadaki büyüme</li>
<li>Yıllara göre satınalmadaki büyüme yüzdesi</li>
</ul></td>
</tr>
<tr class="even">
<td>Satıcı konumuna göre satınalma</td>
<td><ul>
<li>Şehre göre satınalma</li>
<li>Satınalmada yıldan yıla büyüme yüzdesi</li>
<li>Ülkeye göre satınalma</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Zaman göre satınalma harcaması analizi</td>
<td><ul>
<li>Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)</li>
<li>Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Satıcıya göre satınalma harcaması analizi</td>
<td><ul>
<li>İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)</li>
<li>Yıllara göre artan harcamayla en iyi 10 satıcı</li>
<li>Yıllara göre azalan harcamayla en iyi 10 satıcı</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Bu yılki ve geçen yılki satınalma ve tedarik kategorisine göre büyüme.

## <a name="data-model-and-entities"></a>Veri modeli ve varlıklar
Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).

Bu içerikteki toplam ölçümleri, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için, [Power BI ile Varlık deposu tümleştirmesine genel bakış](power-bi-integration-entity-store.md) bölümündeki toplanan ölçümleri Varlık Deposuna ekleme yordamına bakın. Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.

| Varlık        | Önemli toplam ölçümler | Veri kaynağı                                 | Alan              | Açıklama                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Fatura satırları | Satınalma                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Muhasebe para birimi cinsinden tutar. |

Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.

| Ölçü               | Hesaplama                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Geçerli yıldaki satınalma | Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])                                            |
| Geçen yılki satınalma    | Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\]) |
| Yıllara göre satınalmadaki büyüme   | Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\] – \[Geçen yıldaki satınalma\]                            |

İçerikte bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.

| Varlık                 | Öznitelik örnekleri                                |
|------------------------|-------------------------------------------------------|
| Satıcılar                | Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı |
| Ürünler               | Ürün numarası, Ürün adı, Madde grupları adı        |
| Tedarik kategorileri | Tedarik kategorisi, Tedarik kategorisi adları      |
| Tüzel kişilikler         | Tüzel kişiliğin adı                                     |
| Tarihler                  | Tarihler, Yıl denkleştirme                                    |

Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir. Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz. Şirket filtresini de değiştirebilirsiniz.

