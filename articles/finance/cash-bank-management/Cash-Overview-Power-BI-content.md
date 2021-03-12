---
title: Nakde genel bakış Power BI içeriği
description: Bu konu, Nakde genel bakış Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.
author: saraschi2
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0f10022ae4906972d08e08e3e5476630213468d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985473"
---
# <a name="cash-overview-power-bi-content"></a>Nakde genel bakış Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **Nakide genel bakış** Microsoft Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Nakde genel bakış** Power BI içeriği, kuruluşları içindeki nakitten sorumlu olan kişiler için oluşturulmuştur. **Nakde genel bakış** Power BI içeriği, nakit akışınıza görünürlük sağlar. Ayrıca, daha iyi kararlar vermenize ve bu sayede nakit akışınızın sağlını iyileştirmenize yarayan tahminler de sağlar. Fazlalıklar ve eksiklikler hakkında daha iyi fikir sahibi olabilmeniz için nakdi tüzel varlığa, para birimine ve banka numarasına göre analiz edebilirsiniz.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI içeriğini görüntülemek için kurulum gerekiyor

**Nakde genel bakışı** ve **Banka yönetimi** Power BI görsellerinde görüntülenmesi için aşağıdaki kurulumun tamamlanması gerekir.

1. **Sistem para birimi** ve **Sistem döviz kuru**'nu ayarlamak için **Sistem yönetimi > Kurulum > Sistem Paramatreleri**'ne gidin.
2. Etkin döneme atanan mali takvim tarihlerini doğrulamak için **Genel muhasebe > Takvimler > Mali takvimler**'e gidin.
3. **Muhasebe Para Birimi** ve **Döviz Kuru Türü**'nü ayarlamak için **Genel Muhasebe > Ayarlar > Muhasebe**'ye gidin
4. Hareket para birimleri ile muhasebe para birimi, muhasebe para birimi ve sistem para birimi ve muhasebe para birimi ile banka para birimleri arasındaki döviz kurlarını tanımlayın. Bunu yapmak için **Genel Muhasebe > Para Birimleri > Para birimi döviz kurları**'na gidin.
5. Nakit Akışı tahminini yapılandırın ve çalıştırın. Nakit akışı tahmini ayarlamak hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting). 
6. **LedgerCovLiquidityMeasurement** toplam ölçümünü Varlık Deposu sayfası üzerinde yenilemek için **Sistem yönetimi > Ayarlar > Varlık Deposu**'na gidin

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim

**Nakde genel bakış** Power BI içeriğindeki raporlar **Nakde genel bakış** ve **Banka yönetimi** çalışma alanlarında görüntülenir.

Nakit akışı tahmin raporlarını veri ile görmek için önce Nakit ve banka yönetimi alanından **Nakit akışı tahminlerini hesapla** işlevini kullanarak tahmin hesaplama işlemini çalıştırmanız gerekir. Bunun tahmine dahil olan her bir şirket için tamamlanması gerekir.  Daha sonra LedgerCovLiquidityMeasurement toplam ölçümünü **Varlık Deposu** sayfası üzerinde yenilemeniz gerekir.  

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
