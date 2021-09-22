---
title: Satırlardan biri zaten bir yükte yer alıyor
description: Bu sayfada neden "Satırlardan biri zaten yükte yer alıyor. Ambara serbest bırakılamıyor" hatasını alabileceğiniz ve sorunun nasıl çözüleceği açıklanmaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477898"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Satırlardan biri zaten bir yükte yer alıyor

## <a name="symptoms"></a>Belirtiler

Yük oluşturma ve sevkiyatlarla çalışırken aşağıdaki hata iletisini alabilirsiniz:

> Satırlardan biri zaten bir yükte yer alıyor. Ambara serbest bırakılamıyor.

Yükleri el ile oluşturursanız veya süreci satış siparişi satırı girişi gerçekleşmeden önce yükler oluşturulacak şekilde ayarlarsanız sonraki serbest bırakmanın el ile yapılacağı ve yükün rotası ve değerlendirmesinin kullanılacağı varsayılır.

Başka bir olası senaryoda, ambara otomatik olarak serbest bırakma işlemi yapmaya çalışırsınız ancak dalga süreci işi oluşturamaz. Bu nedenle, açık bir sevkiyat veya yük yine de oluşturulur. Bu açık sevkiyat veya yük, açık sevkiyatı ya da yükü silinceye veya dalgayı el ile yeniden işleyinceye kadar, siparişin otomatik olarak serbest bırakılmasını deneyen sonraki girişimleri engeller.

## <a name="resolution"></a>Çözüm

Yalnızca ambara serbest bırakmadan önce yük yoksa satış siparişi sayfasından serbest bırakabilirsiniz veya otomatik serbest bırakma oluşturabilirsiniz. Dalga işlendikten sonra yük otomatik olarak oluşturulacaktır.
