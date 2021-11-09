---
title: Finance Insights kurulumu ile ilgili sorunları giderme
description: Bu konuda, Finance Insights yeteneklerini kullandığınızda oluşabilecek sorunlar listelenmektedir. Ayrıca bu sorunların nasıl düzeltileceği açıklanmıştır.
author: panolte
ms.date: 08/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512902"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insights kurulumu ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Finance Insights yeteneklerini kullandığınızda oluşabilecek sorunlar listelenmektedir. Ayrıca bu sorunların nasıl düzeltileceği açıklanmıştır.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Belirti: Müşteri ödeme öngörüleri Veri Tümleştirme şablonu hedef sütununu neden eşleyemiyorum?

### <a name="resolution"></a>Çözüm

Daha eski bir sürüm için şablon kullanıyor olabilirsiniz. 10.0.17 sürümü yayımlanmadan önce, önizleme müşterileri **Ödeme tahmini sonucu (önizleme)** varlığını kullanarak **Müşteri ödeme içgörüleri sonuçları (CDS-Fin and Ops)** Veri Tümleştirme (DI) şablonunu yapılandırıyordu. 10.0.17 ve sonraki bir sürüme yükseltme yaptıktan sonra, eşleştirmeyi tamamlamak için **Müşteri ödeme içgörüleri sonuçları (Fin için CDS, Ops 10.0.17 ve sonrası)** DI şablonunu kullanmalısınız. Veri yönetimi varlık listesi yenilenip içinde **Ödeme tahmini sonucu** varlığı görünene kadar DI şablonu hedef sütununu eşleyemeyebilirsiniz. Varlık listesini yenilemek ve ödeme tahmini sonucunu göstermek için Microsoft Dynamics 365 Finance ve Dataverse (önceden Common Data Service \[CDS\] yönetici portalı olarak biliniyordu) adımlarını tamamlayacaksınız.

### <a name="in-finance"></a>Finance'ta

Yükselttikten sonra Finance'ta aşağıdaki adımları izleyin.

1. **Sistem Yönetimi \> Çalışma alanları \> Veri yönetimi** seçeneğine gidin.
2. **Veri yönetimi** çalışma alanında, **Çerçeve parametreleri** kutucuğunu seçin.
3. **Veri içe/dışa aktarma çerçevesi parametreleri** sayfasında, **Varlık ayarlarını seçin** ve ardından **Varlık listesini yenile** sekmesini seçin.
4. **Veri içe aktarma/dışa aktarma çerçevesi parametreleri** sayfasını kapatın.
5. **Veri yönetimi** çalışma alanında **Veri varlıkları** kutucuğunu seçin.
6. "Ödeme tahmini sonucu" için arama yapın. **Ödeme tahmini sonucu** varlığının önizleme sürümü olmadığını doğrulayın. Önizleme sürümünün adının sonunda "(önizleme)" ifadesi yer alır. Yalnızca varlığın önizleme sürümünü görüyorsanız Microsoft Destek birimiyle iletişime geçin.

### <a name="in-dataverse"></a>Dataverse'te

Veri tümleştirme projelerinizi güncelleştirmek için [Power Platform yönetim merkezinde](https://admin.powerplatform.microsoft.com/environments) aşağıdaki adımları izleyin.

1. Finance Insights önizleme sürümünü kullanıyorsanız **Müşteri ödeme içgörüleri sonuçları (CDS'den Fin ve Ops'a)** şablonuyla ilişkili DI projesini kaldırın.
2. [Veri tümleştirici projesi oluşturma](create-data-integrate-project.md) bölümündeki adımları izleyin. **Müşteri ödeme içgörüleri sonuçları (CDS'den Fin, Ops 10.0.17 ve sonraki sürümlere)** şablonunu kullanın.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Belirti: Nakit akışı tahmini çalışma alanındaki Nakit tahmini sekmesinde neden veri gösterilmiyor?

### <a name="resolution"></a>Çözüm

Nakit ve banka yönetimindeki nakit akışı tahmini işlevi ve Finance Insights'taki Nakit akışı tahminleri özelliği, **Nakit akışı tahmini** çalışma alanındaki verileri doğru şekilde gösterecek şekilde ayarlanmalı ve etkinleştirilmelidir.

İlk olarak, nakit akışı tahmini ve likidite hesaplarını kurun ve etkinleştirin. Daha fazla bilgi için bkz. [Nakit akışı tahminleri](../cash-bank-management/cash-flow-forecasting.md). Bu kurulum tamamlandıysa ancak beklediğiniz sonuçları görmüyorsanız daha fazla bilgi için [Nakit akışı tahmin kurulumu ile ilgili sorunları giderme](../cash-bank-management/cash-flow-forecasting-tsg.md) bölümüne bakın.

Ardından, Finance Insights'taki Nakit akışı tahminleri özelliğinin (**Nakit ve banka yönetimi \> Kurulum \> Finance Insights \> Nakit akışı tahminleri**) etkinleştirildiğini ve AI modelinin eğitiminin tamamlandığını onaylayın. Eğitim tamamlanmadıysa model eğitim sürecini başlatmak için **Şimdi tahminde bulun**'u seçin.