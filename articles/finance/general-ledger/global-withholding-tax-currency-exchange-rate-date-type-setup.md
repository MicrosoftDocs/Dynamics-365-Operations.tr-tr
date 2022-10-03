---
title: Global stopaj vergisi para birimi döviz kuru türü ve tarih türü kurulumunu etkinleştirme
description: Bu makalede, stopaj vergisi para birimi döviz kuru türü ve tarih türü genel kurulumunun nasıl etkinleştirileceği açıklanmaktadır.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573237"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Global stopaj vergisi para birimi döviz kuru türü ve tarih türü kurulumunu etkinleştirme

[!include[banner](../includes/banner.md)]

Bu makalede, stopaj vergisi para birimi döviz kuru türü ve tarih türü genel kurulumunun nasıl etkinleştirileceği açıklanmaktadır. Stopaj vergisi para birimi için artık özel bir döviz kuru türü ve döviz kuru hesaplaması tarih türü seçebilirsiniz. Bu seçimler, stopaj vergisi para biriminde, ödeme hareketlerinde stopaj vergisi tutarının hesaplanmasında kullanılan yabancı para birimi döviz kurunu belirler.

Bu işlevsellik, Microsoft Dynamics 365 Finance 10.0.29 ve daha ileri sürümlerinde kullanılabilir.

1. **Vergi** \> **Kurulum** \> **Parametreler** \> **Genel muhasebe parametreleri**'ne gidin.
2. **Stopaj vergisi** sekmesinde, **Peşin stopaj vergisi para birimini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
3. **Döviz kuru türü** alanında, stopaj vergisi para birimi için bir döviz kuru türü seçin.
4. **Hesaplama tarihi türü** alanında, stopaj vergisi para birimi döviz kurunu belirleyen bir hesaplama tarihi türü seçin:

    - **Ödeme tarihi** – Ödeme günlüğünün deftere nakil tarihini esas alan döviz kurunu belirleyin.
    - **Fatura tarihi** – Fatura günlüğünün fatura tarihini esas alan döviz kurunu belirleyin. Fişin fatura tarihi boşsa, fatura deftere nakil tarihi kullanılır. 
    - **Belge tarihi** – Ödeme günlüğünün belge tarihini esas alan döviz kurunu belirleyin. Fişin belge tarihi boşsa, ödeme tarihi kullanılır.

5. **Kaydet**'i seçin.

Hareket para birimi, stopaj vergisi kodunda tanımlanan stopaj vergisi para biriminden farklıysa, stopaj vergisi para birimindeki tutar önceki ayarlara göre hareket para biriminden hesaplanır ve deftere nakledilen stopaj vergisi hareketlerinde kaydedilir.
