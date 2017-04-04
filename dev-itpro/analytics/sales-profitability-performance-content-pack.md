---
title: "Satış ve Karlılık performansı güç BI içeriği"
description: "Dynamics 365 işlemleri - satış ve Karlılık performansı içerik paketi Microsoft Power BI de dahil bu konuda açıklanmıştır. Bu içerik paketinde raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Satış ve Karlılık performansı güç BI içeriği

Dynamics 365 işlemleri - satış ve Karlılık performansı içerik paketi Microsoft Power BI de dahil bu konuda açıklanmıştır. Bu içerik paketinde raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

<a name="overview"></a>Özet
--------

Bu içerik paketi satış yöneticilerinin gelir, brüt kar ve kar marjlarını anahtar satış ölçümlerini izlemek oluşturuldu. Dynamics 365 satış işlem verilerinden işlemler için kullanır ve müşteriler ve ürünler için hem toplam şirket çapındaki satış rakamlarının görünümünü ve dökümünü satış performansı sağlar. Zaman içinde gelir ve kazanç büyüme değişiklikleri vurgulayarak raporları pozitif ve negatif eğilimleri hakkında uyarı yöneticileri için tek tek müşteriler ve ürünleri için kullanılabilir. Kategori ve bölgesel yöneticileri geliri ve Karlılığı farklı ürün kategorileri ve müşteri gruplarına birbirlerine sona kalanlar ve liderleri tek karşılaştıran grafikler yararlı bulacaksınız. Bireysel Müşteri geliri Kar marjı teklifleri hesap yöneticileri ve satış ve pazarlama çabalarını attune her müşterinin ilgili profil için bir veri yedeği temel çizim kapsamlı bir rapor. Satış ve Karlılık performansı içerik paketi tarafından satış performansını çözümlemek satış yöneticileri sağlar:

-   Gelir, yıl-(müşteri grubu tek tek müşteriler, satış kategorilerini ve tek tek ürünler ve geographies tarafından) tarih
-   Yıl-over-(müşteri bölgeler ve satışları kategorilere göre) yıllık geliri değiştirme

Karlılık tarafından çözümlenebilir:

-   Brüt Kar ve kar marjıyla (müşteri grupları ve satış ürün kategorileri)
-   Brüt Kar değiştirme, yıl üzerinden yıl
-   Müşteri Karlılığı (tarafından brüt kar marjı karşılık gelir)

## <a name="accessing-the-content-pack"></a>İçerik Paketi erişme
Satış ve Karlılık performansı BI Power pack bir uygulama malın ömrü Hizmetleri (LCS) olarak yayınlanır ve Dynamics 365 işlemleri için erişilebilir içerik. Erişim ve güç BI raporları başlatma hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>İçerik paketinde ölçümleri
İçerik Paketi ölçümleri grafikler, döşeme ve tablo görünür kümesi oluşturan bir raporu içerir. Aşağıdaki tabloda içerik Pack visualisations genel bakış sağlar.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapor sayfası**        | **Charts**                                 | **Döşeme**                                               |
| Müşteriye göre gelir    | Gelire göre ilk 10 müşteriler                | Toplam gelir                                           |
|                        | Toplam Gelire göre müşteri grubu            | Yıllara göre gelir büyüme                                      |
|                        | Müşteri grubuna göre ortalama Müşteri geliri | Brüt kar                                            |
|                        | Gelir ve müşteri grubuna göre brüt kar   |                                                         |
| Ürüne göre gelir     | Gelir ve satış kategoriye göre brüt kar   | Toplam \#ürünleri                                    |
|                        | Gelire göre ilk 10 ürün                 | Etkin Ürünler ve toplamın yüzdesi toplam sayısı |
|                        | Toplam Gelire göre satış kategorisi            | Ürünlerin % 80 gelir için hesap numarası           |
| Döneme göre gelir\*    | Aya göre gelir                           | Yıllara göre gelir büyüme                                      |
|                        | Sonunda gelir farkı, yıllara göre             | Yıllara göre gelir büyüme %                                    |
|                        | Müşteri bölgeye göre satış toplam sapma    |                                                         |
| Konuma göre gelir    | Şehre göre satış geliri                      |                                                         |
|                        | Yıllara göre gelir büyüme %                       |                                                         |
|                        | Bölgeye göre satış geliri                    |                                                         |
| Müşteri Karlılığı | Brüt Kar / müşteriye göre gelir   | Brüt kar, brüt kar marjı, yıllara göre gelir büyüme          |
| Karlılık analizi | Gelir ve aylık brüt kar          |                                                         |
|                        | Brüt Kar marjı bazında ilk 15 müşteriler           |                                                         |
|                        | Aylara, yıllara göre brüt kar                 |                                                         |

\*Gelir bu ve son yıl ve satış kategoriye göre büyüme.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
İşlemler veri 365 Dynamics satış ve Karlılık performansı içerik paketi raporu doldurmak için kullanılır. Bu hazırlanır toplam ölçüleri ile temsil edilir varlık deposunda olduğu analytics için en iyi duruma getirilmiş Microsoft SQL veritabanı. Hakkında daha fazla bilgi blog içinde [Dynamics varlık deposu ile tümleştirme güç BI](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Bu içerik paketi toplam ölçüleri Dynamics AX 2012 ve AX 2012 R3 satış küpteki kullanılabilir toplama ölçümlerin alt kümesidir. Toplama küp ölçüleri varlık deposundaki hazırlamak için konuşlandırılabilir yapmanız gerekir. Blog varlık deposunda toplama ölçülerin aşama hakkında daha fazla bilgi için ilgili yordama bakın [Dynamics varlık deposu ile tümleştirme güç BI](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Aşağıdaki anahtar toplama ölçümleri fatura satırları varlık İçerik Paketi için temel olarak kullanılır.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Anahtar toplam ölçüleri**               | **Dynamics 365 işlemleri için veri kaynağı** | **Field**                                    | **Description**                          |
| Fatura satırları | Gelir                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Muhasebe para birimi cinsinden tutar            |
|               | Satılan malların maliyeti                           | InventTrans                                     | TOPLAMI (CostAmountPosted + CostAmountAdjustment) | Maliyet tutarı + düzeltme                 |
|               | Komisyon satır tutarı – hesap para birimi | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Hesap para birimi cinsinden komisyon tutarı |

Aşağıdaki tablo içerik paketinin veri kümesinde birden çok hesaplanmış ölçüler oluşturmak için kullanılan anahtar toplama ölçümleri fatura satırları varlık gösterir.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Olarak hesaplanan**                                                                                |
| Brüt kar      | SUM (gelir – SMM – komisyon – satış vergisi (müşteri fatura satır tutarına dahil))          |
| Brüt kar      | SUM (Brüt Kar / (gelir - Satış vergisi (müşteri fatura satır tutarına dahil)))             |
| Geçen yıl gelir | Geliri hesapla geçen yıl = (toplam ('Fatura satırlarını'\[gelir\]), SAMEPERIODLASTYEAR (tarihleri\[tarih\]) |

Aşağıdaki anahtar boyutları **satış küpü** daha parçalı yapı ve analitik daha derin incelemeler elde etmek için toplam ölçüleri dilim için filtre olarak kullanılır.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Öznitelik örnekleri**                           |
| Müşteriler        | Müşteri gruplarını, müşteri bölgeleri, adres, endüstri |
| Ürünler         | Ürün numarası, ürün adı, madde grupları adı       |
| Satış kategorileri | Satış kategori adları                                 |
| Tüzel kişilikler   | Yasal varlık adları                                   |
| Tarihler            | Tarihler                                                |

Varsayılan olarak, İçerik Paketi için geçerli takvim yılı verilerini görüntüler, ancak rapor filtreleri bölümü açın ve tarih filtresi değiştirme. Şirket Filtresi de değiştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)



