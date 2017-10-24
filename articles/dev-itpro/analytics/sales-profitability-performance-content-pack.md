---
title: "Satış ve karlılık performansı Power BI içeriği"
description: "Bu konu, Satış ve karlılık performansı Power BI içeriğinde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97c8f3d57ba1accb8d940c7edd3ddcac2146968b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Satış ve karlılık performansı Power BI içeriği

[!include[banner](../includes/banner.md)]

Bu konu, **Satış ve karlılık performansı** Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Satış ve karlılık performansı** Power BI içeriği, satış yöneticilerinin gelir, brüt kar ve kar marjları temel satış ölçümlerini izleyebilmesi için oluşturulmuştur. Satış hareketi verilerini kullanır ve hem şirket çapında satış rakamlarının toplam görünümünü hem de müşteriler ve ürünler için satış performansının dağılımını verir.

Rapor zaman içinde gelirdeki değişiklikleri ve kar artışını vurgular. Bu nedenle, raporlar yöneticileri ayrı müşteriler ve ürünlerle ilgili olarak pozitif ve negatif eğilimleri hakkında uyarmak için kullanılabilir. Ayrıca, grafik farklı ürün kategorilerinin gelirini ve karlılığını ve müşteri gruplarını birbiriyle karşılaştırır. Bu nedenle, kategori ve bölge yöneticileri geride kalanları ve liderleri tanımlayabilir. Son olarak, kapsamlı bir rapor tek tek müşteri gelirinin kar marjıyla karşılaştırmasını sunar. Böylece, hesap yöneticileri her müşteri profiline yönelik satış ve pazarlama çalışmalarını ayarlamak için kullanabilecekleri verilere dayanan bir temele sahip olur. 

**Satış ve karlılık performansı** içeriği satış yöneticilerinin satış performansını aşağıdaki şekillerde analiz etmesini sağlar:

-   Gelir, yılbaşından bugüne (müşteri grubu ve bireysel müşteriler, satış kategorileri ve bireysel ürünler ve coğrafyalara göre)
-   Gelir değişimi, yıldan yıla (müşteri bölgelerine ve satışları kategorilerine göre)

Karlılık analiz aşağıdaki şekillerde analiz edilebilir:

-   Brüt kar ve kar marjı (müşteri gruplarına ve ürün satış kategorilerine göre)
-   Brüt kar değişikliği, yıldan yıla
-   Müşteri karlılığı (gelir - brüt kar marjı karşılaştırması)

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) kullanıyorsanız, **Satış ve karlılık performansı** Power BI içeriği **Satış ve karlılık performansı** sayfasında (**Satış ve pazarlama** > **Sorgular ve raporlar** > **Satış performansı analizi** > **Satış ve karlılık performansı**) gösterilir. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan ölçümler
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

## <a name="extending-the-power-bi-content"></a>Power BI içeriğini genişletmek
Microsoft Dynamics Lifecycle Services (LCS) içinde kullanılabilir durumda olan içerik paketlerini kullanarak, Microsoft Dynamics 365'e oturum açmayan kişilere harika analizler sunabilirsiniz. Bu içerik paketlerini diğer raporları veya görsel öğeleri içerecek şekilde değiştirebilir ve içerik paketlerini analiz için Power BI.com kiracınıza yayınlayabilirsiniz.

**Satış ve karlılık performansı** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](power-bi-content-microsoft-partners.md). Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.

Kullanmakta olduğunuz Dynamics 365 sürümü için geçerli **Satış ve karlılık performansı** içeriğini indirdiğinizden emin olun.

> [!NOTE]
> Microsoft Dynamics 365 for Operations, 1611 sürümünü kullanıyorsanız, bu Power BI içeriği için KB 4011327 bir önkoşuldur: LCS'de oturum açtıktan sonra KB'ye buradan erişebilirsiniz: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Aşağıdaki veriler **Satış ve karlılık performansı** Power BI içeriğindeki raporu doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md). 

Bu içerikteki toplam ölçümleri, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satış Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için, şu blog yazısındaki toplama ölçümlerini Varlık Deposuna ekleme yordamına bakın: [Dynamics'te Power BI ile Varlık deposu tümleştirmesi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

Fatura satırları varlığının aşağıda verilen önemli toplama ölçümleri, içeriğin temeli olarak kullanılır.

| Varlık        | Önemli toplam ölçümler                   | Dynamics 365 için Veri kaynağı                    | Alan                                        | Açıklama                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Fatura satırları | Gelir                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Muhasebe para birimi cinsinden tutar.            |
|               | Satılan malların maliyeti                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Maliyet tutarı toplamı ve ayarlama.    |
|               | Komisyon satırı tutarı – muhasebe para birimi | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Muhasebe para birimi cinsinden komisyon tutarı. |

Aşağıdaki tabloda, içerikte veri kümesini oluşturmak için kullanılan Fatura satırları varlığı önemli toplama ölçümleri gösterilmektedir.

| Ölçü           | Hesaplama                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Brüt kar      | SUM(Gelir – SMM – Komisyon – Satış vergisi (müşteri faturası satır tutarı dahil))          |
| Brüt kar      | SUM(Brüt kar / (Gelir – Satış vergisi (müşteri faturası satır tutarı dahil)))             |
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

