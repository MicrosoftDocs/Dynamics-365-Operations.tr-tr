---
title: "Nakde genel bakış Power BI içeriği"
description: "Bu konu, Nakde genel bakış Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: saraschi2
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e969c2033463d565ce782c7dc8cfc4b458349289
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017

---

# <a name="cash-overview-power-bi-content"></a>Nakde genel bakış Power BI içeriği

[!include[banner](../includes/banner.md)]

Bu konu, **Nakde genel bakış** Microsoft Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Özet

**Nakde genel bakış** Power BI içeriği, kuruluşları içindeki nakitten sorumlu olan kişiler için oluşturulmuştur. **Nakde genel bakış** Power BI içeriği, nakit akışınıza görünürlük sağlar. Ayrıca, daha iyi kararlar vermenize ve bu sayede nakit akışınızın sağlını iyileştirmenize yarayan tahminler de sağlar. Fazlalıklar ve eksiklikler hakkında daha iyi fikir sahibi olabilmeniz için nakdi tüzel varlığa, para birimine ve banka numarasına göre analiz edebilirsiniz.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek

Dynamics 365 for Finance and Operations, Enterprise edition 2017 Temmuz güncelleştirmesini kullanıyorsanız, **Naki genel bakışı** Power BI içeriğinden raporlar, **Nakit genel bakışı** ve **Banka yönetimi** çalışma alanlarında gösterilir.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan raporlar
Aşağı tablo, **Nakit genel bakışı** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor                                | İçindekiler |
|---------------------------------------|----------|
| Nakit özeti – tüm şirketler         | <ul><li>Sistem para biriminden girişler ve çıkışlar</li><li>Tahmin edilen para birimi bakiyeleri</li><li>Sistem para biriminden toplam banka bakiyesi</li><li>Tüzel kişiliğe göre bakiye</li><li>Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</li></ul> |
| Nakit özeti – geçerli şirket       | <ul><li>Muhasebe para biriminden girişler ve çıkışlar</li><li>Tahmin edilen para birimi bakiyeleri</li><li>Muhasebe para biriminden toplam banka bakiyesi</li><li>Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</li></ul> |
| Nakit akışı tahmini – tüm şirketler    | <ul><li>Sistem para biriminden girişler ve çıkışlar</li><li>Günlük tahmin özeti</li><li>Tahmin ayrıntıları</li></ul> |
| Nakit akışı tahmini – şirket para birimi | <ul><li>Muhasebe para biriminden girişler ve çıkışlar</li><li>Günlük tahmin özeti</li><li>Tahmin ayrıntıları</li></ul> |
| Para birimi tahmini                     | <ul><li>Tahmin edilen para birimi bakiyeleri</li><li>Günlük para birimi özeti</li><li>Tahmin ayrıntıları</li></ul> |
| Banka bakiyeleri                         | <ul><li>Sistem para biriminden toplam banka bakiyesi</li><li>Tüzel kişiliğe göre bakiye</li><li>Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</li><li>Banka hesabına göre bakiye</li><li>Döviz cinsinden bakiye</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI içeriğini genişletmek
Dynamics 365'e oturum açmayanlar için, Lifecycle Services (LCS) içindeki içerik paketlerini kullanarak harika analizler sağlayabilirsiniz. Bu içerik paketleri, başka raporları veya görselleri içermek üzere değiştirilebilir ve daha sonra Power BI.com kiracınızda analiz edilmek üzere yayımlanabilir. 

**Nakit genel bakışı** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Aşağıdaki tablo, **Nakit genel bakışı** Power BI içeriğinin temel aldığı varlıkları gösterir.

| Varlık                                                                          | İçindekiler |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Şirket                                          | Raporların filtreleneceği şirketler |
| LedgerCovLiquidityMeasurement\_Tarih                                             | Raporların filtreleneceği tarihler |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Gerçek banka bakiyesi ve son tahmin edilen banka bakiyesi karşılaştırması |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Tahmin edilen hareket ayırtıları |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Her bir şirketin muhasebe para birimi kullanılarak özetlenen nakit girişleri, çıkışları ve bakiyeler |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Tüm şirketlerin sistem para birimi kullanılarak özetlenen nakit girişleri, çıkışları ve bakiyeler |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Hareket para birimini kullanan para birimlerinin net işlem tutarı ve bakiyesinin özeti |

Bu varlıklar, veri modelinde hesaplanmış ölçümler oluşturmak için kullanılıyordu. Bu hesaplanmış ölçümler daha sonra **Nakit genel bakışı** Power BI içeriği içinde kullanılan grafikleri ve raporları hesaplamak için kullanılır. Raporlarınıza ve panonuza ek hesaplamalar dahil etmek için Power BI dosyasından LCS'den indirebilir ve değiştirebilirsiniz. Bu dosya, içeriği oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yaptıktan sonra, eklediğiniz içerikleri kapsayan kuruluş içerik paketi ve panoları oluşturabilirsiniz.

