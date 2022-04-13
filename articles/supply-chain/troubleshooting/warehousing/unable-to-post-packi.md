---
title: Durdurulmuş bir satış sipariş satırı için sevk irsaliyesi gönderilemiyor
description: Durdurulmuş bir satış sipariş satırı için sevk irsaliyesi gönderemiyorsunuz
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462862"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Durdurulmuş bir satış sipariş satırı için sevk irsaliyesi gönderilemiyor

Hata kodu: SYS13203

## <a name="symptoms"></a>Belirtiler

Yük için sevk irsaliyesi göndermeye çalıştığınızda sistem aşağıdaki hata iletisini görüntüler:

> Giden sevkiyatı onayladıktan sonra bir satış sipariş satırı durdurulduğunda sevk irsaliyesi gönderilemiyor, herhangi bir miktar seçilemiyor.

## <a name="cause"></a>Nedeni

İlgili satış sipariş satırlarından biri veya daha fazlası durdurulabilir, bu da sistemin bu satış siparişinin daha fazla işlenmesini engelleyeceği anlamına gelir. Diğer işlemlerin yanı sıra bu, sistemin sipariş için bir sevk irsaliyesi göndermeyeceği anlamına gelir.

Örneğin, müşteri geri arayıp siparişini iptal ettiği için bir kullanıcı bir veya daha fazla sipariş satırını durdurmaya karar vermiş olabilir. Ancak, giden sevkiyat zaten onaylanmışsa satış siparişini içeren sevkiyat ambardan zaten fiziksel olarak ayrılmış olabilir, bu da satış sipariş satırlarının durdurulmasının herhangi bir etkisi olmayacağı anlamına gelir. Sevkiyatı fiziksel olarak durdurmak artık mümkün olmadığından sevk irsaliyesini gönderebilmek için satırları da durduramazsınız. Daha sonra iptal edilen siparişi iade olarak işlemeniz gerekir.

## <a name="resolution"></a>Çözüm

Sevk irsaliyesini kaydedebilmek için aşağıdaki adımları uygulayarak ilgili satış sipariş satırlarından hiçbirinin durdurulmadığından emin olun.

1. **Tüm satış siparişleri \> Satış ve pazarlama \> Tüm satış siparişleri**'ne gidin.
1. Sorun yaşadığınız satış siparişini bulun ve açın.
1. **Satış siparişi satırları** hızlı sekmesinde, satış siparişi satırını seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Genel** sekmesini açın ve **Durduruldu** alanının *Hayır* olarak ayarlandığından emin olun.
1. Durdurulan ilgili satış satırları kalmayana kadar devam edin.
1. Yükleme veya satış siparişi için sevk irsaliyesini yeniden göndermeyi deneyin.
