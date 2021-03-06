---
title: Planlı üretim emrinin kesinleştirebilmesi için önce planlanması gerekir
description: Planlı bir siparişi kesinleştirmeye çalıştığınızda, siparişin kesinleştirilebilmesi için önce zamanlanması gerektiğini bildiren bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294204"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Planlı üretim emrinin kesinleştirebilmesi için önce planlanması gerekir

Hata kodu: SYS309802

## <a name="symptoms"></a>Belirtiler

Planlı siparişi kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:

> Planlanlı üretim emrinin kesinleştirilmeden önce zaman çizelgesinin yapılması gerekir.

## <a name="cause"></a>Nedeni

Zamanlanan başlangıç ve bitiş tarihleri boş olamaz.

## <a name="resolution"></a>Çözüm

Planlı siparişin başlangıç ve bitiş tarihlerini belirtmek için şu adımları izleyin.

1. **Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin.
1. İlgili planlı siparişi açın.
1. **Genel** Hızlı Sekmesinde, **Zamanlanmış** bölümünde, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında tarihleri belirtin.
