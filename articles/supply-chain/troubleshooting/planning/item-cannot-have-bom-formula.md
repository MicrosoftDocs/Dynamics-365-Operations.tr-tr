---
title: Maddenin ürün reçetesi veya formülü olamaz
description: Bir siparişi kesinleştirmeye çalıştığınızda, madde doğrulaması sırasında bir hata iletisi alırsınız. Maddenin ürün reçetesi (BOM) veya formülü olamayacağını belirtir.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730118"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Maddenin ürün reçetesi veya formülü olamaz

Hata kodu: PRO2614

## <a name="symptoms"></a>Belirtiler

Bir siparişi kesinleştirmeye çalıştığınızda, madde doğrulaması sırasında aşağıdaki hata iletisi alırsınız:

> Madde bir ürün reçetesi veya formüle sahip olamaz

## <a name="resolution"></a>Çözüm

Ürün reçetesi (BOM) veya formülü olan maddeler *Planlama maddesi*, *BOM* veya *formül* türünde olmalıdır. Maddenin türünü değiştirmek için, aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. İlgili ürünü açın.
1. **Mühendis** hızlı sekmesinde **Üretim türü** alanını *Planlama maddesi*, *BOM* veya *formül* olarak ayarlayın.
