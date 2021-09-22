---
title: Tamamlandığı bildirildi durumu Bitti olarak değiştirilirken hata oluştu
description: Tamamlandığı bildirildi üretim emri durumu Bitti olarak değiştirilirken bir hata alabilirsiniz. Bu sayfada, sorunun nasıl hafifletileceği açıklanmaktadır.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477854"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Tamamlandığı bildirildi üretim emri durumu Bitti olarak değiştirilirken oluşan hata

## <a name="symptoms"></a>Belirtiler

Tamamlandığı bildirildi üretim emri durumu Bitti olarak değiştirildiğinde aşağıdaki hata iletilerinden birini alırsınız:

> Çakışmayı güncelleştirin. Standart maliyet, güncelleştirmeden sonraki mali stok değeriyle eşleşmez.

> InventCostMovement.checkVariance işlevinde kritik bir hata oluşur.

## <a name="cause"></a>Nedeni

Bu sorun, temel veriler başka bir işlem tarafından değiştirildiğinde oluşur. İşlem, verileri en fazla beş kez güncelleştirmeyi deneyecektir. Çakışma beş denemeden sonra hala devam ediyorsa yukarıda listelenen iletilerden birini alırsınız.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. Sorunu gidermek için toplu işi sürdürün. Çalıştırmayı sonlandırmalıdır.

Toplu iş, siz devam ettikten sonra sürekli olarak başarısız olursa, kayıt defterinin varsayılan para biriminin yuvarlama hassasiyetinin InventSum tablosundaki değerlere uygulanan yuvarlama ile uyumlu olduğunu doğrulayın. Yuvarlama hassasiyeti uyumlu olmayan bir değer olarak değiştirildiyse büyük olasılıkla uyumlu bir değer olarak tekrar değiştirmeniz gerekir. **ModifiedDateTime** değerini arayın. Bu durumda, değer genellikle yuvarlama hassasiyetinin son zamanlarda değiştirildiğini gösterir.
