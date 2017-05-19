---
title: "Satınalma harcaması analizi Power BI içeriği"
description: "Bu konu, Microsoft Power BI Satınalma harcaması analizi içerik paketinde nelerin bulunduğunu açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d392b88942f4b7d7365b000df1cd69809060b910
ms.openlocfilehash: e39b1677038037cd91cfad8d104d0130bc20fb9b
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Satınalma harcaması analizi Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Power BI Satınalma harcaması analizi içerik paketinde nelerin bulunduğunu açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="overview"></a>Özet
--------

Microsoft Power BI için satınalma harcaması analiz paketi, satınalma yöneticileri ve bütçelerden sorumlu yöneticiler için oluşturulmuştur. Satınalma harcamasını izlemelerine yardımcı olmak amacıyla tasarlanmıştır. Microsoft Dynamics 365 for Operations'tan alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir. Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır. Bu nedenle, yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir. Grafikler, farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir. Kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanmayı yararlı bulabilirler. İçerik paketi satınalma yöneticilerinin ve bütçelerden sorumlu yöneticilerin satınalma harcamasını aşağıdaki şekillerde analiz etmesine olanak tanır:

-   Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)
-   Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)

## <a name="accessing-the-content-pack"></a>İçerik paketine erişmek
Satınalma harcaması analizi içerik paketi, Microsoft Dynamics Lifecycle Services'da (LCS) bir uygulama varlığı olarak yayınlanır ve Microsoft Dynamics 365 for Operations'tan erişilebilir. Power BI raporlarına erişme ve raporları açma hakkında daha fazla bilgi için bkz. [Microsoft ve iş ortaklarınızdan LCS'de Power BI içeriği](power-bi-content-microsoft-partners.md).
Not: KB 4011327 bu Power BI içeriği için önkoşuldur. Lifecycle Services'a oturum açtıktan sonra KB'ye buradan erişebilirsiniz: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="metrics-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan ölçümler
Satın alma harcaması analizi içerik paketi bir dizi ölçümden oluşan bir rapor içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. Aşağıdaki tabloda içerik paketindeki görselleştirmelere genel bakış sunulmaktadır.

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
Dynamics 365 for Operations verileri Satınalma harcaması analizi içerik paketindeki rapor için kullanılır. Bu veri, analytics için en iyi duruma getirilen bir Microsoft SQL veritabanı olan Varlık mağazasında hazırlanmış toplam ölçümler olarak temsil edilir. Varlık deposu hakkında daha fazla bilgi için [Dynamics'te Power BI ile Varlık Deposu tümleştirmesi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog gönderisine bakın. Bu içerik paketindeki toplamın ölçümleri, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için, şu blog yazısındaki toplama ölçümlerini Varlık Deposuna ekleme yordamına bakın: [Dynamics'te Power BI ile Varlık deposu tümleştirmesi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Aşağıda verilen önemli toplama ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içerik paketinin temeli olarak kullanılır.

| Varlık        | Önemli toplam ölçümler | Dynamics 365 for Operations için veri kaynağı | Alan              | Açıklama                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Fatura satırları | Satınalma                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Muhasebe para birimi cinsinden tutar |

Aşağıdaki tablo içerik paketinde Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.

| Ölçü               | Hesaplama                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Geçerli yıldaki satınalma | Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])                                            |
| Geçen yılki satınalma    | Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\]) |
| Yıllara göre satınalmadaki büyüme   | Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\] – \[Geçen yıldaki satınalma\]                            |

İçerik paketinde bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.

| Varlık                 | Öznitelik örnekleri                                |
|------------------------|-------------------------------------------------------|
| Satıcılar                | Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı |
| Ürünler               | Ürün numarası, Ürün adı, Madde grupları adı        |
| Tedarik kategorileri | Tedarik kategorisi, Tedarik kategorisi adları      |
| Tüzel kişilikler         | Tüzel kişiliğin adı                                     |
| Tarihler                  | Tarihler, Yıl denkleştirme                                    |

Varsayılan olarak, içerik paketi geçerli takvim yılına ilişkin verileri gösterir. Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz. Şirket filtresini de değiştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)





