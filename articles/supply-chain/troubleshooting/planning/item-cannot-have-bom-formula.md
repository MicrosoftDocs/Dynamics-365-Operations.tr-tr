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
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294200"
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
