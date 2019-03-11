---
title: Nakde genel bakış Power BI içeriği
description: Bu konu, Nakde genel bakış Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dccb5c5c6c336607603dfc7a935c039e5ac4aa5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "318661"
---
# <a name="cash-overview-power-bi-content"></a>Nakde genel bakış Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **Nakide genel bakış** Microsoft Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Nakde genel bakış** Power BI içeriği, kuruluşları içindeki nakitten sorumlu olan kişiler için oluşturulmuştur. **Nakde genel bakış** Power BI içeriği, nakit akışınıza görünürlük sağlar. Ayrıca, daha iyi kararlar vermenize ve bu sayede nakit akışınızın sağlını iyileştirmenize yarayan tahminler de sağlar. Fazlalıklar ve eksiklikler hakkında daha iyi fikir sahibi olabilmeniz için nakdi tüzel varlığa, para birimine ve banka numarasına göre analiz edebilirsiniz.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim

**Nakde genel bakış** Power BI içeriğindeki raporlar **Nakde genel bakış** ve **Banka yönetimi** çalışma alanlarında görüntülenir.

Nakit akışı tahmin raporlarını veri ile görmek için önce Nakit ve banka yönetimi alanından **Nakit akışı tahminlerini hesapla** işlevini kullanarak tahmin hesaplama işlemini çalıştırmanız gerekir.  Bunun tahmine dahil olan her bir şirket için tamamlanması gerekir.  Daha sonra LedgerCovLiquidityMeasurement toplam ölçümünü **Varlık Deposu** sayfası üzerinde yenilemeniz gerekir.  

Nakit akışı tahmin demo verisini Demo veri modülündeki **Veri oluştur** sayfasını kullanarak Gösteri amacıyla ekleyebilirsiniz.  Bu komut dosyası, raporlar için gerekli olan bilgileri hızlıca doldurmak için nakit akışı tahmin tablolarına veri ekleyecektir.  Bu modül yalnızca Demo verisi paketi modelini ortamda dağıtmışsanız kullanılabilir. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan raporlar
Aşağı tablo, **Nakit genel bakışı** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor                                | İçindekiler |
|---------------------------------------|----------|
| Nakit özeti – tüm şirketler         | <ul><li>Sistem para biriminden girişler ve çıkışlar</li><li>Tahmin edilen para birimi bakiyeleri</li><li>Sistem para biriminden toplam banka bakiyesi</li><li>Tüzel kişiliğe göre bakiye</li><li>Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</li></ul> |
| Nakit özeti – geçerli şirket       | <ul><li>Muhasebe para biriminden girişler ve çıkışlar</li><li>Tahmin edilen para birimi bakiyeleri</li><li>Muhasebe para biriminden toplam banka bakiyesi</li><li>Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</li></ul> |
| Nakit akışı tahmini – tüm şirketler    | <ul><li>Sistem para biriminden girişler ve çıkışlar</li><li>Günlük tahmin özeti</li><li>Tahmin ayrıntıları</li></ul> |
| Nakit akışı tahmini – şirket para birimi | <ul><li>Muhasebe para biriminden girişler ve çıkışlar</li><li>Günlük tahmin özeti</li><li>Tahmin ayrıntıları</li></ul> |
| Para birimi tahmini                     | <ul><li>Tahmin edilen para birimi bakiyeleri</li><li>Günlük para birimi özeti</li><li>Tahmin ayrıntıları</li></ul> |
| Banka bakiyeleri                         | <ul><li>Sistem para biriminden toplam banka bakiyesi</li><li>Tüzel kişiliğe göre bakiye</li><li>Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</li><li>Banka hesabına göre bakiye</li><li>Döviz cinsinden bakiye</li></ul> |


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


