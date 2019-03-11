---
title: Toplu iş ve lisans plaka onayı
description: Bu konu bir mobil cihazdan toplu iş ve plaka onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "344237"
---
# <a name="batch-and-license-plate-confirmation"></a>Toplu iş ve lisans plaka onayı

[!include [banner](../includes/banner.md)]

Toplu iş onayı, doğru toplu işin mobil cihazdan alındığını onaylamanıza olanak sağlar. Toplu iş üstü'nün arama hiyerarşisindeki toplu iş aralıklarının daha yüksek olduğunu belirttiği yalnızca toplu iş üstü maddelerin ilk çekilmesinde, çekilen toplu işin, iş satırındaki toplu iş olduğunu doğrulamanız gerekir. 

Plaka onayı, doğru plakanın mobil cihazdan alındığını onaylamanıza olanak sağlar. Bir aşama konumundan iş çekerken, çekilen plakanın, iş ile ilişkilendirilmiş plaka ile eşleştiğini doğrulamanız gerekir. İş, bir plakanın taratılması ile başlatıldıysa, onay adımı atlanacaktır.

## <a name="where-it-applies"></a>Uygulandığı yerler
Onay yalnızca aşağıdaki senaryolarda geçerlidir:

- Toplu onay, yalnızca toplu iş üst maddeleri için işin ilk çekmelerine uygulanır.
- Plaka onayı, aşama konumlarından çekmelere uygulanır.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Toplu iş ve plaka onayını ayarlama
Toplu iş ve plaka onayı yapılandırmasını mobil cihaz menü öğelerinden yapılandırabilirsiniz.  
1.  İşler mobil cihaz menü öğesinden, iş onay kurulumunu açın.  
2.  Toplu iş veya plaka onayı için seçeneği işaretleyin. Her iki seçenek de otomatik onayın etkinleştirilmiş olmadığı iş türü çekmeleri için kullanılabilir.  
