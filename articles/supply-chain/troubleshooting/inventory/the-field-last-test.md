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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742040"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor

KB numarası: 4612803

## <a name="symptoms"></a>Belirtiler

Birden fazla kalite emri oluşturulduğunda, **Son test tarihi** alanı güncelleştirilmiyor.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Son test tarihi, kalite emirleriyle ilgili değildir. Tamamlanan malların ilk olarak satın alındığı veya üretildiği tarihi depolar. Bu tarih, önerilen raf ömrü tarihini hesaplamak için kullanılır.
