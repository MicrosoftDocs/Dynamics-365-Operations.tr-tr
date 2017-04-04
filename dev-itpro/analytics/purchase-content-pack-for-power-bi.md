---
title: "Satınalma Analiz güç BI içeriği harcadığınız"
description: "Bu konuda ne dahil olduğunu açıklar Satınalma Analiz İçerik Paketi için Microsoft Power BI harcamak. İçerik paketinde bulunan raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Satınalma Analiz güç BI içeriği harcadığınız

Bu konuda ne dahil olduğunu açıklar Satınalma Analiz İçerik Paketi için Microsoft Power BI harcamak. İçerik paketinde bulunan raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

<a name="overview"></a>Özet
--------

Satınalma Analiz paketi Microsoft Power BI yöneticileri ve bütçeler için sorumlu yöneticileri satın aldığınız için oluşturulmuş içerik ayırın. Satınalma harcama üzerinde bir göz tutmak yardımcı olmak için tasarladı. Microsoft Dynamics 365 işlem verilerinden satınalma işlemleri için kullanır ve iki şirket genelinde satınalma rakamları toplam görünümünü ve bir harcama satıcı ve ürünlere göre satınalma dökümü sağlar. Rapor zamanla harcama satınalma değişikliklere yer verilmiştir. Bu nedenle, bunlar pozitif ve negatif harcama eğilimleri hakkında uyarı yöneticileri için tek tek satıcılara ve ürünleri için kullanılabilir. Grafikleri kategoriler farklı satın alma ve Satıcı grupları için harcama satınalma gösterir. Kategori ve bölgesel yöneticileri fazla harcama davranış değişiklikleri tanımlamanıza yardımcı olması için bu grafikler kullanmak yararlı olabilir. İçerik paketi aşağıdaki şekillerde harcama satınalma satınalma yöneticileri ve bütçeler için sorumlu yöneticileri yapalım çözümleyin:

-   Yıl satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategori ve bireysel ürün ve satıcı konum)
-   Yıl üzerinden yıl satınalma Değiştir (satıcı grubu ve tedarik kategoriye göre)

## <a name="accessing-the-content-pack"></a>İçerik Paketi erişme
Satınalma Analiz paketi Microsoft Dynamics ömrü Hizmetleri (LCS) bir uygulama varlığı olarak yayınlanır ve Microsoft Dynamics 365 işlemleri için erişilebilir içerik ayırın. Erişim ve açık güç BI raporları hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan ölçümleri
Satınalma harcamak analiz ölçümler kümesinden oluşan bir rapor içerik paketi içerir. Bu ölçümler, grafikler, döşeme ve tablolar görünür. Aşağıdaki tabloda, görsel içerik paketinde genel bir bakış sağlar.

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
<th>Döşeme</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Satıcı tarafından satın</td>
<td><ul>
<li>En iyi 10 satıcıları tarafından satınalma (yığılmış çubuk grafik)</li>
<li>Toplam satınalma satıcıya göre grup / ülke / name (pasta grafik)</li>
<li>Satınalma satıcıya göre grup / ülke / name (sütun grafiği)</li>
<li>Ortalama satınalma satıcıya göre grup / ülke / name (sütun grafiği)</li>
</ul></td>
<td><ul>
<li>Satınalma toplamı</li>
<li>Yıllara göre satınalma büyüme</li>
<li>Toplam # satıcılar</li>
<li>Etkin satıcılara toplam sayısı</li>
</ul></td>
</tr>
<tr class="even">
<td>Ürüne göre satın alma</td>
<td><ul>
<li>Satınalma tedarik kategoriye göre / ürün adı (sütun grafiği)</li>
<li>Toplam Satınalma tedarik kategoriye göre / ürün adı (pasta grafik)</li>
<li>Satınalma (yığılmış çubuk grafik) göre ilk 10 ürünler</li>
</ul></td>
<td><ul>
<li>Toplam ürün sayısı</li>
<li>Toplam etkin ürünler ürünler toplam sayısı yüzdesi</li>
<li>Ürünlerin % 80 satınalma için hesap numarası</li>
</ul></td>
</tr>
<tr class="odd">
<td>Dönem * tarafından satın</td>
<td><ul>
<li>Aya göre satınalma / gün (sütun grafiği)</li>
<li>Toplam Satınalma yıllara göre varyans (waterfall grafik)</li>
<li>Toplam Satınalma yıllara göre büyüme (sütun grafiği)</li>
<li>Satın alma deyimi (matrix)</li>
</ul></td>
<td><ul>
<li>Yıllara göre satınalma büyüme</li>
<li>Yıllara göre satınalma büyüme %</li>
</ul></td>
</tr>
<tr class="even">
<td>Satıcı konumuna göre satın alma</td>
<td><ul>
<li>Şehir tarafından satın</li>
<li>Satınalma yıllara göre büyüme %</li>
<li>Ülkeye göre satın alma</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Satınalma Analiz tarafından zaman harcayın</td>
<td><ul>
<li>Aya göre bu yıl satınalma / gün (çizgi grafiği)</li>
<li>Satınalma geçerli ve geçen yıl (satır ve sütun grafiği)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Satınalma Analiz satıcı tarafından harcamak</td>
<td><ul>
<li>Satınalma (Huni) ilk 10 satıcı satınalma %</li>
<li>Top 10 satıcılarla artan harcama yıllara göre</li>
<li>Top 10 satıcı ile azalan harcama yıllara göre</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Bu yıl ve geçen yıl satınalma ve tedarik kategoriye göre büyüme

## <a name="data-model-and-entities"></a>Veri modeli ve varlıklar
İçerik Paketi analiz raporu satınalma için kullanılan veri işlemleri için Dynamics 365 ayırın. Bu veriler hazırlanır toplama ölçümleri temsil varlık deposunda olduğu analytics için en iyi duruma getirilmiş bir Microsoft SQL veritabanı. Varlık deposu hakkında daha fazla bilgi için bkz: [Dynamics varlık deposu ile tümleştirme güç BI](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog postası. Bu içerik paketi toplam ölçüleri Microsoft Dynamics AX 2012 ve Microsoft Dynamics 365 işlemleri 2012 R3 için satınalma küpteki kullanılabilir toplama ölçümlerin alt kümesidir. Toplama küp ölçüleri varlık deposundaki hazırlamak için konuşlandırılabilir yapmanız gerekir. Toplam ölçüleri varlık deposunda hazırlama işlemini daha fazla bilgi için bkz: [Dynamics varlık deposu ile tümleştirme güç BI](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog postası. Aşağıdaki anahtar toplam ölçüleri doğrudan fatura satırları varlıktan kullanılabilir ve İçerik Paketi için temel olarak kullanılır.

| Varlık        | Anahtar toplam ölçüleri | Dynamics 365 işlemleri için veri kaynağı | Alan              | Açıklama                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Fatura satırları | Satınalma                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Muhasebe para birimi cinsinden tutar |

Aşağıdaki tablo içerik paketinde fatura satırları varlıktan hesaplanan anahtar ölçüleri gösterir.

| Ölçü               | Hesaplama                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Satınalma cari yıl | Satınalma bu yıl = TOPLA ('Fatura satırlarını'\[satınalma\])                                            |
| Geçen yıl satın    | Satınalma hesapla geçen yıl = (toplam ('Fatura satırlarını'\[satınalma\]), SAMEPERIODLASTYEAR (tarihleri\[tarih\])) |
| Yıllara göre satınalma büyüme   | Yıllara göre büyüme satın = \[bu yıl satın\] – \[geçen yıl satın\]                            |

Daha fazla tanecik ve analitik daha derin incelemeler elde edebilirsiniz böylece içerik paketinde aşağıdaki anahtar boyutları toplam ölçüleri, dilim için filtre olarak kullanılır.

| Varlık                 | Öznitelik örnekleri                                |
|------------------------|-------------------------------------------------------|
| Satıcılar                | Satıcı grupları, satıcı ülke veya bölgelerde, satıcı adı |
| Ürünler               | Ürün numarası, ürün adı, madde grupları adı        |
| Tedarik kategorileri | Tedarik kategori, kategori adlarını tedarik      |
| Tüzel kişilikler         | Tüzel kişiliğin adı                                     |
| Tarihler                  | Tarih, yıl farkı                                    |

Varsayılan olarak, İçerik Paketi için geçerli takvim yılı verileri gösterir. Ancak Tarih Filtresi alanında filtreler bölümünde raporu değiştirebilirsiniz. Şirket Filtresi de değiştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)



