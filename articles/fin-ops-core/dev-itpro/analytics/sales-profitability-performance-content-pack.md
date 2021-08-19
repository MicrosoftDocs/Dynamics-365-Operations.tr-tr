---
title: Satış ve karlılık performansı Power BI içeriği
description: Bu konu, Satış ve karlılık performansı Power BI içeriğinde nelerin bulunduğunu açıklar.
author: ShylaThompson
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9ec9ef5f4abf898100c670b1ca1cc845d6ebeeea36f21cdda3a9b7d3f1027d4e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725222"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Satış ve karlılık performansı Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **Satış ve kârlılık performansı** Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Satış ve karlılık performansı** Power BI içeriği, satış yöneticilerinin gelir, brüt kar ve kar marjları temel satış ölçümlerini izleyebilmesi için oluşturulmuştur. Satış hareketi verilerini kullanır ve hem şirket çapında satış rakamlarının toplam görünümünü hem de müşteriler ve ürünler için satış performansının dağılımını verir.

Rapor zaman içinde gelirdeki değişiklikleri ve kar artışını vurgular. Bu nedenle, raporlar yöneticileri ayrı müşteriler ve ürünlerle ilgili olarak pozitif ve negatif eğilimleri hakkında uyarmak için kullanılabilir. Ayrıca, grafik farklı ürün kategorilerinin gelirini ve karlılığını ve müşteri gruplarını birbiriyle karşılaştırır. Bu nedenle, kategori ve bölge yöneticileri geride kalanları ve liderleri tanımlayabilir. Son olarak, kapsamlı bir rapor tek tek müşteri gelirinin kar marjıyla karşılaştırmasını sunar. Bu nedenle hesap yöneticileri her müşteri profiline yönelik satış ve pazarlama çalışmalarını ayarlamak için kullanabilecekleri verilere dayanan bir temele sahip olur.

**Satış ve karlılık performansı** içeriği satış yöneticilerinin satış performansını aşağıdaki şekillerde analiz etmesini sağlar:

- Gelir, yılbaşından bugüne (müşteri grubu ve bireysel müşteriler, satış kategorileri ve bireysel ürünler ve coğrafyalara göre)
- Gelir değişimi, yıldan yıla (müşteri bölgelerine ve satışları kategorilerine göre)

Karlılık analiz aşağıdaki şekillerde analiz edilebilir:

- Brüt kar ve kar marjı (müşteri gruplarına ve ürün satış kategorilerine göre)
- Brüt kar değişikliği, yıldan yıla
- Müşteri karlılığı (gelir - brüt kar marjı karşılaştırması)

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**Satış ve karlılık performansı** Power BI içeriği, **Satış ve karlılık performansı** sayfasında gösterilir (**Satış ve pazarlama** \> **Sorgular ve raporlar** \> **Satış performansı analizi** \> **Satış ve karlılık performansı**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler
**Satış ve karlılık performansı** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. Aşağıdaki tabloda içerikteki görselleştirmelere genel bakış sunulmaktadır.

| Rapor sayfası            | Grafikler                                     | Kutucuklar                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Müşteriye göre gelir    | Gelire göre ilk 10 müşteri                | Toplam gelir                                           |
|                        | Müşteri grubuna göre toplam gelir            | Yıldan yıla gelir büyümesi                                      |
|                        | Müşteri grubuna göre ortalama müşteri geliri | Brüt kar                                            |
|                        | Müşteri grubuna göre gelir ve brüt kar   |                                                         |
| Ürüne göre gelir     | Satış kategorisine göre gelir ve brüt kar   | Toplam \# ürün sayısı                                    |
|                        | Gelire göre ilk 10 ürün                 | Etkin ürünlerin toplam sayısı ve toplamdaki yüzdesi |
|                        | Satış kategorisine göre toplam gelir            | Gelirin %80'ini oluşturan ürünlerin sayısı           |
| Gelir, döneme göre\*    | Gelir, aya göre                           | Gelir büyümesi, yıldan yıla                                      |
|                        | Son bütçe farkı, yıldan yıla             | Gelir büyümesi yüzdesi, yıldan yıla                                    |
|                        | Satış toplamı farkı, müşteri bölgesine göre    |                                                         |
| Gelir, yerleşime göre    | Satış geliri, şehre göre                      |                                                         |
|                        | Gelir büyümesi yüzdesi, yıldan yıla                       |                                                         |
|                        | Satış geliri, bölgeye göre                    |                                                         |
| Müşteri karlılığı | Brüt marj - gelir karşılaştırması, müşteriye göre   | Brüt kar, brüt marj, yıldan yıla gelir büyümesi          |
| Karlılık analizi | Gelir ve brüt kar, aya göre          |                                                         |
|                        | İlk 15 müşteri, brüt kara göre           |                                                         |
|                        | Brüt kar, aya göre, yıldan yıla                 |                                                         |

\* Bu yılki ve geçen yılki gelir ve büyüme, satış kategorisine göre.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Aşağıdaki veriler **Satış ve karlılık performansı** Power BI içeriğindeki raporu doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesi](power-bi-integration-entity-store.md).

Bu içerik paketindeki toplama ölçümler, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satış Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için, şu blog yazısındaki toplama ölçümlerini Varlık Deposuna ekleme yordamına bakın: [Dynamics'te Power BI ile Varlık deposu tümleştirmesi](/archive/blogs/dynamicsaxbi/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update).

Fatura satırları varlığının aşağıda verilen önemli toplama ölçümleri, içeriğin temeli olarak kullanılır.

| Varlık        | Önemli toplam ölçümler                   | Dynamics 365 için Veri kaynağı | Alan                                        | Açıklama                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Fatura satırları | Gelir                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Muhasebe para birimi cinsinden tutar.            |
|               | Satılan malların maliyeti                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | Maliyet tutarı toplamı ve ayarlama.    |
|               | Komisyon satırı tutarı: muhasebe para birimi | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Muhasebe para birimi cinsinden komisyon tutarı. |

Aşağıdaki tabloda, içeriğin veri kümesinde çeşitli hesaplanan ölçümler oluşturmak için kullanılan Fatura satırları varlığının önemli toplama ölçümleri gösterilmektedir.

| Ölçü           | Hesaplama                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Brüt kar      | SUM(Gelir: SMM: Komisyon: Satış vergisi (müşteri faturası satır tutarı dahil))          |
| Brüt kar      | SUM(Brüt kar / (Gelir: Satış vergisi (müşteri faturası satır tutarı dahil)))             |
| Geçen yılın geliri | Geçen yılın geliri = CALCULATE(SUM('Fatura satırları'\[Gelir\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\]) |

Satış Küpündeki aşağıda belirtilen temel boyutlar daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.

| Varlık           | Öznitelik örnekleri                               |
|------------------|------------------------------------------------------|
| Müşteriler        | Müşteri grupları, Müşteri bölgeleri, Adres, Sektör |
| Ürünler         | Ürün numarası, Ürün adı, Madde grupları adı       |
| Satış kategorileri | Satış kategorisi adları                                 |
| Tüzel kişilikler   | Tüzel kişilik adları                                   |
| Tarihler            | Tarihler                                                |

Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir. Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz. Şirket filtresini de değiştirebilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]