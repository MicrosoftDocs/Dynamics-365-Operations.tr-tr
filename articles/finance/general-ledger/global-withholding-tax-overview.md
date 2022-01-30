---
title: Genel stopaj vergisi
description: Bu konu, genel stopaj vergisi işlevselliği ve nasıl ayarlanacağı hakkında bilgiler sağlar. Genel stopaj vergisi işlevselliği satıcı ve müşteri hareketleri için geliştirilmiştir, böylece stopaj vergisi kalem düzeyinde hesaplanır.
author: roschlom
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 7a3bb3c8766c7dd591f66a663d8be17769bb7d53
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986188"
---
# <a name="global-withholding-tax"></a>Genel stopaj vergisi

[!include [banner](../includes/banner.md)]

Bu konu, genel stopaj vergisi işlevselliği hakkında bilgiler sağlar ve nasıl ayarlanacağını açıklar. Bu yeni işlev, 10.0.17 sürümü ve sonrasında bulunur.

Genel stopaj vergisi işlevselliği satıcı ve müşteri hareketleri için geliştirilmiştir, böylece stopaj vergisi kalem düzeyinde hesaplanır. Satın alma hareketlerinden stopaj vergisi hesabındaki bakiye, stopaj vergisi ödeme işini stopaj vergisi kapatma hesabıyla karşılaştırılarak kapatılabilir.

> [!NOTE]
> Genel stopaj vergisi, satın alma siparişi, satıcı faturası ve satış siparişi sayfalarındaki **Giderleri koru** işlevini desteklemez.

## <a name="turn-on-global-withholding-tax"></a>Genel stopaj vergisini etkinleştirme

1. **Özellik Yönetimi** çalışma alanında, listeden **Genel stopaj vergisi**'ni seçin ve **Şimdi etkinleştir**'i seçin.
2. **Vergi \> Kurulum \> Parametreler \> Genel muhasebe parametreleri**'ne gidin ve **Stopaj vergisi** sekmesinde **Genel stopaj vergisini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
3. **Kaydet**'i seçin.
4. Web tarayıcınızda sayfayı yenileyin.

> [!NOTE]
> Yerelleştirilmiş stopaj vergisi çözümlerinin zaten sunulmakta olduğu ülkeler/bölgeler için genel stopaj vergisi işlevselliği etkinleştirilemez. Bu alanlar Hindistan, Brezilya, Tayland, Suudi Arabistan, İrlanda, Büyük Britanya ve ABD'yi içerir ancak bunlarla sınırlı değildir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
