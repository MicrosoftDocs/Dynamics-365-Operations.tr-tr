---
title: Nakit akışı tahmin kurulumu ile ilgili sorunları giderme
description: Bu konuda nakit akışı tahminini yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir. Nakit akışı kurulumu, nakit akışı güncelleştirmeleri ve nakit akışı Power BI hakkında sık sorulan soruları (SSS) ele alır.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985299"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Nakit akışı tahmin kurulumu ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda nakit akışı tahminini yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir. Nakit akışı kurulumu, nakit akışı güncelleştirmeleri ve nakit akışı Power BI hakkında sık sorulan soruları (SSS) ele alır.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Neden yalnızca bir tüzel kişilik için nakit akışı gösteriliyor?

Nakit akışı tahmini tüzel kişilik başına yapılandırılır ve hesaplanır. Finance Insights'taki Power BI raporları ve nakit akışı tahminleri özelliği sonuçları gösterir.

Tahmin görmek istediğiniz her tüzel kişilik için nakit akışı tahmini ayarlanmalıdır. Tüm tüzel kişiliklerinizde nakit akışı tahmini yapılandırmasını inceleyin. Alternatif olarak, nakit akışı tahmini için tüm tüzel kişiliklerin yapılandırmasını inceleyin ve istediğiniz gibi ayarlandıklarından emin olun.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Power BI neden tüm nakit akışı verilerini göstermiyor?

Nakit akışı tahminlerinin Power BI görünümlerinde görünebilmesi için birkaç adımın tamamlanması gerekir. Aşağıdaki denetim listesini inceleyin ve her adımın tamamlandığından emin olun:

- Her tüzel kişilik için nakit akışını ayarlayın.
- Genel muhasebe parametrelerinde, sistem para birimini ve sistem döviz kuru türünü ayarlayın.
- Genel muhasebe muhasebe para birimini ve döviz kuru türünü ayarlayın.
- Hareket para birimi ile muhasebe para birimi arasında döviz kurları girin.
- Muhasebe para birimi ile sistem para birimi arasında döviz kurları girin.
- Muhasebe para birimi ile her banka para birimi arasında döviz kurları girin.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Nakit akışı Power BI neden önceki sürümlerde çalışıyordu ancak şimdi boş?

Varlık deposundaki "Nakit akışı ölçümü V2" ve "LedgerCovLiquidityMeasurement" ölçümlerinin yapılandırıldığını doğrulayın. Varlık deposundaki verilerle çalışma hakkında daha fazla bilgi için bkz. [Varlık deposuyla Power BI tümleştirmesi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Power BI içeriğini görüntülemek için gereken tüm adımların tamamlandığını doğrulayın. Daha fazla bilgi için bkz. [Nakde genel bakış Power BI içeriği](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Varlık deposu varlıkları yenilendi mi?

Verilerin güncel ve doğru olduğundan emin olmak için varlıklarınızı düzenli aralıklarla yenilemeniz gerekir. Belirli bir varlığı el ile yenilemek için **Sistem yönetimi \> Kurulum \> Varlık deposu**'na gidin, varlığı seçin ve sonra **Yenile**'yi seçin. Veriler otomatik olarak da güncelleştirilebilir. **Varlık deposu** sayfasında, **Otomatik yenileme etkin** seçeneğini **Evet** olarak ayarlayın.
