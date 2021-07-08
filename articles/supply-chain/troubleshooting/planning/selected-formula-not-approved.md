---
title: Seçili formül numarası toplu iş emri için onaylanmadı
description: Planlı bir siparişi kesinleştirmeye çalışırken, seçili formül numarasının bir toplu iş emri için onaylanmadığını bildiren bir hata iletisi alırsınız.
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
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294196"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Seçili formül numarası toplu iş emri için onaylanmadı

Hata kodu: PRO2614

## <a name="symptoms"></a>Belirtiler

Planlı siparişi kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:

> Seçili formül numarası, bir toplu iş emri için onaylanmamış.

## <a name="cause"></a>Nedeni

Sistem, etkin madde için onaylanmış bir formülün kullanılabilir olduğundan emin olmak üzere kesinleştirme işlemini doğrular. Formülü onaylamanız gerekir.

## <a name="resolution"></a>Çözüm

Formülü onaylamak için aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürün reçeteleri ve formüller \> Formüller** seçeneğine gidin.
1. İlgili formülü seçin.
1. Eylem Bölmesinde, **Formül** sekmesinde **Koru** gurubunda **Formülü onayla**'yı seçin.
1. **Ürün reçetesini veya formülü onayla** iletişim kutusunda, bir onaylayan seçin ve sonra **Tamam**'ı seçin.
