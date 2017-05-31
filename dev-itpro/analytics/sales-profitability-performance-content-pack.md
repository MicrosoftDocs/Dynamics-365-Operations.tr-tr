---
title: "Satış ve karlılık performansı Power BI içeriği"
description: "Bu konuda, Dynamics 365 for Operations - Microsoft Power BI için satış ve karlılık performansı içerik paketinin içeriği açıklanmaktadır. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 357f7071d801b13518c83170f8d0e7946dd9dede
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Satış ve karlılık performansı Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konuda, Dynamics 365 for Operations - Microsoft Power BI için satış ve karlılık performansı içerik paketinin içeriği açıklanmaktadır. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="overview"></a>Özet
--------

Bu içerik paketi, satış yöneticilerinin gelir, brüt kar ve kar marjları anahtar satış ölçümlerini izlemesi için oluşturulmuştur. Dynamics 365 for Operations'tan alınan satış işlem verilerini kullanır ve hem şirket çapında satış rakamlarının toplam görünümünü hem de müşteriler ve ürünler için satış performansının dağılımını verir. Zaman içindeki gelir ve kar büyümesindeki değişiklikleri vurgulayarak, raporlar yöneticileri bireysel müşteriler ve ürünler için olumlu ve olumsuz eğilimler konusunda uyarmak için kullanılabilir. Kategori ve bölge müdürleri, geride kalanları ve liderleri birbirinden ayırmak için farklı ürün kategorilerinin ve müşteri gruplarının gelir ve karlılıklarını karşılaştıran çizelgeleri yararlı bulacaktır. Bireysel müşteri gelirini kar marjıyla karşılaştıran kapsamlı bir rapor, hesap yöneticilerine satış ve pazarlama çabalarını her bir müşterinin ilgili profiline uyumlu hale getirmek için verilere dayalı bir zemin sunar. Satış ve karlılık performansı içerik paketi Satış yöneticilerinin satış performansını şu ölçütlerle çözümlemesini sağlar:

-   Gelir, yılbaşından bugüne (müşteri grubu ve bireysel müşteriler, satış kategorileri ve bireysel ürünler ve coğrafyalara göre)
-   Gelir değişimi, yıldan yıla (müşteri bölgelerine ve satışları kategorilerine göre)

Karlılık şu ölçütlere göre çözümlenebilir:

-   Brüt kar ve kar marjı (müşteri gruplarına ve ürün satış kategorilerine göre)
-   Brüt kar değişikliği, yıldan yıla
-   Müşteri karlılığı (gelir - brüt kar marjı karşılaştırması)

## <a name="accessing-the-content-pack"></a>İçerik paketine erişmek
Satış ve karlılık performansı Power BI içerik paketi, Lifecycle Services'da (LCS) bir uygulama varlığı olarak yayınlanır ve Dynamics 365 for Operations'tan erişilebilir. Power BI raporlarına erişme ve raporları başlatma hakkında daha fazla bilgi için bkz. [Microsoft ve iş ortaklarınızdan LCS'de Power BI içeriği](power-bi-content-microsoft-partners.md).
**Not:** KB 4011327 bu Power BI içeriği için önkoşuldur. Lifecycle Services'a oturum açtıktan sonra KB'ye buradan erişebilirsiniz: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>İçerik paketindeki ölçümler
İçerik paketi ölçümleri grafikler, kutucuklar ve tablolar halinde görselleştirilmiş bir dizi ölçümden oluşan bir rapor içerir. Aşağıdaki tabloda içerik paketindeki görselleştirmelere bir genel bakış sunulmaktadır.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapor sayfası**        | **Grafikler**                                 | **Kutucuklar**                                               |
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
Dynamics 365 for Operations verileri, Satış ve karlılık performansı içerik paketindeki raporu doldurmak için kullanılır. Bu, analiz için optimize edilmiş bir Microsoft SQL veritabanı olan Varlık Deposunda hazırlanmış toplama ölçümler olarak temsil edilir. Hakkında daha fazla bilgi için blog yazısına bakın: [Dynamics'te Power BI ile Varlık Deposu tümleştirmesi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Bu içerik paketindeki toplama ölçümler, Dynamics AX 2012 ve AX 2012 R3'teki Satış Küpü'nde bulunan toplama ölçümlerin alt kümesidir. Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir. Daha fazla bilgi için, şu blog yazısındaki toplama ölçümlerini Varlık Deposuna ekleme prosedürüne bakın: [Dynamics'te Power BI ile Varlık deposu tümleştirmesi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Fatura satırları varlığının aşağıda verilen önemli toplama ölçümleri, içerik paketinin temeli olarak kullanılır.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Varlık**    | **Önemli toplama ölçümler**               | **Dynamics 365 for Operations için veri kaynağı** | **Alan**                                    | **Açıklama**                          |
| Fatura satırları | Gelir                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Muhasebe para birimi cinsinden tutar            |
|               | Satılan malların maliyeti                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Maliyet tutarı + düzeltme                 |
|               | Komisyon satırı tutarı – muhasebe para birimi | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisyon satırı tutarı, muhasebe para birimi cinsinden |

Aşağıdaki tabloda, içerik paketinde veri kümesini oluşturmak için kullanılan fatura satırları varlığı önemli toplama ölçümleri gösterilmektedir.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Ölçüm**       | **Hesaplama şekli**                                                                                |
| Brüt kar      | SUM(Gelir – SMM – Komisyon – Satış vergisi (müşteri faturası satır tutarı dahil))          |
| Brüt kar      | SUM(Brüt kar / (Gelir – Satış vergisi (müşteri faturası satır tutarı dahil)))             |
| Geçen yılın geliri | Geçen yılın geliri = CALCULATE(SUM('Fatura satırları'\[Gelir\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\]) |

Aşağıdaki **Satış küpü** anahtar boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde etmek üzere toplama ölçümleri bölmek için filtre olarak kullanılır.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Varlık**       | **Öznitelik örnekleri**                           |
| Müşteriler        | Müşteri grupları, Müşteri bölgeleri, Adres, Sektör |
| Ürünler         | Ürün numarası, Ürün adı, Madde grupları adı       |
| Satış kategorileri | Satış kategorisi adları                                 |
| Tüzel kişilikler   | Tüzel kişilik adları                                   |
| Tarihler            | Tarihler                                                |

Varsayılan olarak, içerik paketi, geçerli takvim yılının verilerini görüntüler ancak rapor filtreleri bölümü açıp tarih filtresini değiştirebilirsiniz. Şirket filtresini de değiştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)





