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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776788"
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
