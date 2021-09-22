---
title: İş türü olarak Stok durumu değişikliği seçilemiyor
description: İş türü yalnızca sistem süreçleri tarafından kullanıldığından Stok durumu değişikliği için bir iş şablonu satırı oluşturamazsınız. Farklı bir iş türü seçin.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477882"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>İş türü sütununda Stok durumu değişikliği seçilemiyor

## <a name="symptoms"></a>Belirtiler

Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken aşağıdaki hata iletisini alabilirsiniz:

> İş türü geçerli olmadığından Stok durumu değişikliği için bir iş şablonu satırı oluşturamazsınız. Farklı bir iş türü seçin.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. *Stok durumu değişikliği* iş türü, yalnızca sistem süreçleri tarafından kullanılır. Bu değer yapılandırılamaz. İş türleri listesi bir numaralandırma olarak düzeltildiğinden, ekstra girişler, **İş türü** açılan menüsünden filtre dışı bırakılamaz.
