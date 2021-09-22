---
title: Bir siparişi sonlandırmaya çalışırken oluşan toplam mal miktarı hatası
description: Üretim emrini ve raporu tamamlandı olarak sonlandırmaya çalışırken toplam mal miktarı hatası alabilirsiniz. Bu sayfada, sorunun nedeni ve nasıl düzeltileceği açıklanmaktadır.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477838"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Bir üretim emrini sonlandırmaya çalışırken oluşan toplam mal miktarı hatası

## <a name="symptoms"></a>Belirtiler

Bir raporu üretim emrinde tamamlanmış günlük olarak deftere nakletmeye çalıştığınızda, aşağıdaki hata iletisini alırsınız:

> Üretimde mamul olarak rapor edilen toplam sağlam miktar %1 olacak. Son işlem için geri bildirim toplamı 0,00'dır.

## <a name="cause"></a>Nedeni

Bu sorun, son işlemlerde deftere nakledilen miktarlar yanlışsa oluşur. Örneğin, üretim başlatıldıysa ancak başlatılması gereken miktar tahsis edilmediyse rota kartı günlüğü herhangi bir satır olmadan deftere nakledilir. Durumu onaylamak için üretim emrini açın ve ardından Eylem Bölmesi'nde, **Görünüm** sekmesinde **Rota kartı**'nı seçin.

## <a name="resolution"></a>Çözüm

Bu sorunu, günlüklerin deftere doğru şekilde nakledilmediği işlemler için ek günlükler göndererek düzeltebilirsiniz. Üretim emrini yeniden başlatın ve ek günlükleri deftere nakletmeyi seçin. Bu eylem üretim emrini başlatmaz ancak günlükleri deftere nakleder. Rota kartı deftere nakledilen miktarları göstermelidir ve üretim emirlerini başarıyla sonlandırabilirsiniz.
