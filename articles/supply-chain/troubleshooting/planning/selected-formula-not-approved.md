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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712922"
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
