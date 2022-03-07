---
title: Ağırlık pozitif olmalıdır
description: Ağırlık pozitif olmalıdır
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924315"
---
# <a name="weight-must-be-positive"></a>Ağırlık pozitif olmalıdır

Hata kodu: WeightMustBePositive

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> Ağırlık pozitif olmalıdır.

## <a name="cause"></a>Nedeni

**Brüt Ağırlık** alanı *0* (sıfır) veya negatif değer olarak ayarlanmıştır.

## <a name="resolution"></a>Çözünürlük

Bir ağırlık belirlemem için aşağıdaki adımlardan birini izleyin.

- **Brüt ağırlık** alanında bir değer belirleyin. Ardından açılan listede bir birim seçin.
- **Brüt ağırlık** değerini hesaplamak için **Sistem ağırlığını al**'ı seçin.
