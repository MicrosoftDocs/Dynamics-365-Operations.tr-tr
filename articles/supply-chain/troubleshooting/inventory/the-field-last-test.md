---
title: Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor
description: Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026994"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor

KB numarası: 4612803

## <a name="symptoms"></a>Belirtiler

Birden fazla kalite emri oluşturulduğunda, **Son test tarihi** alanı güncelleştirilmiyor.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Son test tarihi, kalite emirleriyle ilgili değildir. Tamamlanan malların ilk olarak satın alındığı veya üretildiği tarihi depolar. Bu tarih, önerilen raf ömrü tarihini hesaplamak için kullanılır.
