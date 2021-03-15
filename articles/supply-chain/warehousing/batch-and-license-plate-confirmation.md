---
title: Toplu iş ve lisans plaka onayı
description: Bu konu bir mobil cihazdan toplu iş ve plaka onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97790b91d4de536b89b580c26ef1e37145f7d7c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977450"
---
# <a name="batch-and-license-plate-confirmation"></a>Toplu iş ve lisans plaka onayı

[!include [banner](../includes/banner.md)]

Toplu iş onayı, doğru toplu işin mobil cihazdan alındığını onaylamanıza olanak sağlar. Toplu iş üstü'nün arama hiyerarşisindeki toplu iş aralıklarının daha yüksek olduğunu belirttiği yalnızca toplu iş üstü maddelerin ilk çekilmesinde, çekilen toplu işin, iş satırındaki toplu iş olduğunu doğrulamanız gerekir.

Plaka onayı, doğru plakanın mobil cihazdan alındığını onaylamanıza olanak sağlar. Bir aşama konumundan iş çekerken, çekilen plakanın, iş ile ilişkilendirilmiş plaka ile eşleştiğini doğrulamanız gerekir. İş, bir plakanın taratılması ile başlatıldıysa, onay adımı atlanacaktır.

## <a name="where-it-applies"></a>Uygulandığı yerler

Onay yalnızca aşağıdaki senaryolarda geçerlidir:

- Toplu onay, yalnızca toplu iş üst maddeleri için işin ilk çekmelerine uygulanır.
- Plaka onayı, aşama konumlarından çekmelere uygulanır.

> [!IMPORTANT]
> Plaka onayı için stok yenileme desteklenmez. Stok yenileme işi yürütülürken, hiçbir plaka onay adımı oluşturulmaz.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Toplu iş ve plaka onayını ayarlama

Toplu iş ve plaka onayı yapılandırmasını mobil cihaz menü öğelerinden yapılandırabilirsiniz.

1. İşler mobil cihaz menü öğesinden, iş onay kurulumunu açın.  
1. Toplu iş veya plaka onayı için seçeneği işaretleyin. Her iki seçenek de otomatik onayın etkinleştirilmiş olmadığı iş türü çekmeleri için kullanılabilir.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]