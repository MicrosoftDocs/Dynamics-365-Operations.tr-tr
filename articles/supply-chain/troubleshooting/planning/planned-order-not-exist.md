---
title: Sistem, birden fazla siparişteki işlemler sırasında planlı sipariş bulamıyor
description: Birden fazla planlı sipariş üzerinde işlemler gerçekleştirdiğinizde ve en az iki sipariş aynı madde koduna ait olduğunda "Planlı sipariş yok" hatası oluşur.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920821"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Sistem, birden fazla siparişteki işlemler sırasında planlı sipariş bulamıyor

Hata kodu: SYS24774

## <a name="symptoms"></a>Belirtiler

Aynı anda birden fazla planlı sipariş üzerinde işlem gerçekleştirmeye çalıştığınızda ve siparişlerden en az ikisi aynı madde koduna ait olduğunda aşağıdaki hata iletisini alırsınız. Örneğin, siparişler kesinleştirildiğinde veya sipariş türleri değiştirildiğinde bu hata oluşabilir.

> %1 planlı siparişi yok

## <a name="cause"></a>Nedeni

Sistem, bir siparişi kesinleştirdiğinde veya türünü değiştirdiğinde, planlanan tedarikin talep ve mevcut tedarike uygun olduğundan emin olmak için maddeye ait planlı mevcut siparişleri yeniden değerlendirmelidir. Bu işlemin bir parçası olarak sistem, madde için planlanan siparişleri yeniden oluşturur. Bu nedenle, sistemin işlemek için beklediği ikinci planlı sipariş artık mevcut olmaz.

## <a name="workaround"></a>Geçici çözüm

Siparişleri işlemeden önce onaylayın. Bu şekilde, sistem maddenin ilk siparişini işlediğinde siparişler silinmeyecektir.
