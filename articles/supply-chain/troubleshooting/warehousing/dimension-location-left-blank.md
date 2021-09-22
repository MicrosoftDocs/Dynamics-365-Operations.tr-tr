---
title: Seri numarası ayarlanmışsa boyut konumu boş olamaz
description: Seri haldeki maddeler için transfer emri oluşturduktan sonra bir sevkiyatı onaylarken bu hatayı alıyorsanız Varsayılan giriş konumu alanı boştur.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477884"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Seri haldeki maddeler için transfer emri oluşturduktan sonra sevkiyat onaylanırken oluşan hata

## <a name="symptoms"></a>Belirtiler

Gelişmiş ambar yönetimi (WMS) için etkinleştirilmiş bir ambar kullanarak seri haldeki maddeler için transfer emri oluşturursanız ve iş tamamlandıktan sonra sevkiyatı onaylamaya çalışırsanız aşağıdaki hata iletisini alırsınız:

> Boyut seri numarası ayarlanmışsa boyut konumu boş bırakılamaz.

## <a name="cause"></a>Nedeni

Bunun nedeni, **Varsayılan giriş konumu** alanının "çıkış" ambarına ait bir transit ambar için boş olmasıdır.

## <a name="resolution"></a>Çözüm

Bu sorunu gidermek için transit ambarında varsayılan bir giriş konumu belirtin. Bu konumun plaka denetimli olduğundan emin olun.
