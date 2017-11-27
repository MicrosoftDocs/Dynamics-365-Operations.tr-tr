---
title: "Kredi ve tahsilatlar yönetimi Power BI içeriği"
description: "Bu konu, Power BI Kredi ve Tahsilatlar Yönetimi'nde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f08df6cb8549e87e123b10c5a771ae1c60ff39c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Kredi ve tahsilatlar yönetimi Power BI içeriği

Bu konu, Microsoft Power BI **Kredi ve Tahsilatlar Yönetimi**'nde nelerin bulunduğunu açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Kredi ve tahsilatlar yönetimi** Power BI içeriği, kredi ve tahsilatlar yöneticileri ve tahsilat elemanları için oluşturulmuştur. Bekleyen satış gün sayısı, vadesi geçmiş bakiye, kredi riski ve kredi limitini aşan müşteriler gibi önemli kredi ve tahsilatlar ölçümleri sağlar. Hareket verileri kullanır ve kredi ve tahsilatların tüm şirket içindeki toplam görünümünü sağlar. Şirket, müşteri grubu ve müşteri başına çözümleme de sağlar.

Bu Power BI içeriği 10 rapor sayfasından oluşur:

- İki genel bakış sayfası (kredi genel bakışı için bir sayfa ve tahsilatlar genel bakışı için bir sayfa)
- Çeşitli boyutların dilimlenmiş kredi ve tahsilatlar ölçümlerinin ayrıntılarını sağlayan sekiz sayfa

Gösterilen tüm tutarlar sistem para birimi cinsindendir. Sistem para birimini **Sistemler parametreleri** sayfasından ayarlayabilirsiniz.

Şirket için kredi ve tahsilatlar verisi varsayılan olarak gösterilir. Tüm şirketler arasında veriyi görmek için **CustCollectionsBICrossCompany** görevini role ekleyin.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) kullanıyorsanız, **Kredi ve tahsilatlar yönetimi** Power BI içeriği **Müşteri kredi ve tahsilatları** çalışma alanında görüntülenir.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan raporlar

The **CustCollectionsBICrossCompany** Power BI içeriği, bir dizi ölçümden oluşan bir rapor içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. Aşağıdaki tablo **CustCollectionsBICrossCompany** Power BI içeriğindeki görselleştirmelere bir bakış sağlar.

| Rapor sayfası                 | Gözde canlandırma |
|-----------------------------|---------------|
| Tahsilatlar genel bakışı        | <ul><li>Vadesi geçmiş müşteriler</li><li>Müşteri fazla kredi limiti</li><li>DSO 30 gün</li><li>Açık servis talepleri</li><li>Vakanın kapatılacağı ortalama gün sayısı</li><li>Açık faaliyetler</li><li>Etkinliklerin kapatılacağı ortalama gün sayısı</li><li>Vade farkı dekontlarını aç</li><li>Tahsilatlar mektuplarını aç</li><li>Müşteri bekletme</li><li>Satış bekletme</li><li>Yaşlandırılmış bakiyeler</li><li>Tahsilatların durum tutarları</li><li>Tahsilatların kod tutarları</li><li>Sebebine göre silme nedeni</li><li>Bölgeye göre borç bakiyesi</li><li>Beklenen ödemeler</li></ul> |
| Kredi genel bakışı             | <ul><li>Vadesi geçmiş müşteriler</li><li>Kredi limiti ve kalan bakiye karşılaştırması</li><li>Kredi limitini aşan müşteriler kılavuzu</li><li>Şirket başına müşterilerin fazla kredi limiti</li><li>Kullanılan kredi ve toplam kredi limiti karşılaştırması</li><li>Kredi limiti ve Bölgeye göre kullanılan kredi karşılaştırması</li><li>Kredi notuna göre müşteriler</li></ul> |
| Kredi limiti                | <ul><li>Kredi limiti</li><li>Kredi limiti ayrıntıları</li><li>Müşteri başına kredi limiti</li><li>Müşteri grubu başına kredi limiti</li><li>Şirket başına kredi notuna göre kredi limiti</li><li>Kredi limiti ve bölgeye göre kullanılan kredi karşılaştırması</li></ul> |
| Müşteri fazla kredi limiti | <ul><li>Müşteri fazla kredi limiti</li><li>Müşteri fazla kredi limiti ayrıntısı</li><li>Şirket başına müşterilerin fazla kredi limiti</li><li>Müşteri grubu başına müşteri fazla kredi limiti</li><li>Bölgeye göre müşteri fazla kredi limiti</li></ul> |
| Vadesi geçmiş müşteriler          | <ul><li>Vadesi geçmiş müşteriler</li><li>Vadesini geçirmiş müşterilerin ayrıntıları</li><li>Şirket başına vadesi geçmiş müşteri</li><li>Müşteri grubu başına vadesi geçmiş müşteri</li><li>Bölgeye göre vadesi geçmiş müşteri</li></ul> |
| Yaşlandırılmış bakiyeler               | <ul><li>Yaşlandırılmış bakiyeler</li><li>Yaşlandırılmış bakiyelerin ayrıntıları</li><li>Şirket başına yaşlandırılmış bakiyeler</li><li>Müşteri grubu başına yaşlandırılmış bakiyeler</li></ul> |
| Beklenen ödemeler           | <ul><li>Beklenen ödemeler</li><li>Beklenen ödemelerin ayrıntıları</li><li>Şirkete göre beklenen ödemeler</li><li>Müşteri grubu başına beklenen ödemeler</li><li>Bölgeye göre beklenen ödemeler</li></ul> |
| Silmeler                  | <ul><li>Bölgeye göre silmeler</li><li>Silmelerin ayrıntıları</li><li>Ana hesaba göre silmeler</li><li>Şirkete göre silmeler</li><li>Müşteri grubuna göre silmeler</li><li>Bölgeye göre silmeler</li></ul> |
| Tahsilat durumu          | <ul><li>İhtilaflı</li><li>Ödeme taahhüdü yerine getirilmedi</li><li>Ödeme taahhüdü</li><li>Tahsilatların durum ayrıntıları</li><li>Tahsilatların durum tutarları</li><li>Açık servis talepleri</li><li>Açık faaliyetler</li></ul> |
| Tahsilatlar mektupları         | <ul><li>Tahsilat kodu tutarları</li><li>Tahsilatlar kodu tutar ayrıntıları</li><li>Şirkete göre tahsilat mektubu tutarı</li><li>Müşteri grubuna göre tahsilat mektubu tutarı</li><li>Bölgeye göre tahsilat mektup tutarı</li></ul> |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Altta yatan veriyi Dışa aktar işlevini de görselleştirmede özetlenen altta yatan veriyi dışa aktarmak için kullanabilirsiniz.

## <a name="extending-the-power-bi-content"></a>Power BI içeriğini genişletmek
Microsoft Dynamics Lifecycle Services (LCS) içinde kullanılabilir durumda olan içerik paketlerini kullanarak, Finance and Operations'a oturum açmayan kişilere harika analizler sunabilirsiniz. Bu içerik paketlerini diğer raporları veya görsel öğeleri içerecek şekilde değiştirebilir ve içerik paketlerini analiz için Power BI.com kiracınıza yayınlayabilirsiniz.

**Kredi ve tahsilatlar yönetimi** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.

Kullandığınız Finance ve Operations uygulanan **Kredi ve tahsilatlar yönetimi** Power BI içeriğini indirdiğinizden emin olun.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Aşağıdaki veriler **Kredi ve tahsilatlar yönetimi** Power BI içeriğindeki raporu doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| Varlık                                      | Önemli toplam ölçümler           | Veri kaynağı                                 | Alan                                                      | Açıklama |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Kapalı etkinliklerin sayısı ve bu etkinlikleri kapamak için ortalama süre. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Açık aktivitelerin sayısı. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | SUM(SystemCurrencyBalance)                                 | Yaşlandırılmış bakiyelerin toplamı. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Vadesi geçmiş tutarlar. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Kapalı vakaların sayısı ve bu vakaları kapamak için ortalama süre. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Açık vakaların sayısı. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Açık tahsilat mektuplarının sayısı. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Nakledilen tahsilat mektuplarının bakiyesi. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Tahsilat durumundaki hareketlerin bakiyesi. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Kredi riski ve müşterilerin kredi limitlerinin üzerinde oldukları tutarların toplamı. |
| CustCollectionsBICustOnHold                 | Bloke edilmiş                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Beklemede olan müşterilerin sayısı. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | 30 gün için bekleyen satış gün sayısı. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Sonraki yılda beklenen ödemelerin toplamı. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Oluşturulmuş olan vade farkı dekontlarının sayısı. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Bekleme olan toplam satış siparişlerinin sayısı. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Silinmiş olan hareketlerin toplamı. |

