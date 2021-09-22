---
title: Bu konum için plaka belirtilmelidir
description: Bu hatayı WMS özellikli bir ambar için transfer emri oluşturduktan sonra alırsanız transit ambarı için Varsayılan giriş konumu boştur.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477815"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Transfer emri için sevkiyat onaylanırken plaka belirtimi hatası

## <a name="symptoms"></a>Belirtiler

Gelişmiş ambar yönetimi (WMS) için etkinleştirilen bir ambarı kullanarak bir transfer emri oluşturup ardından iş tamamlandıktan sonra sevkiyatı onaylamayı denerseniz aşağıdaki hata iletisini alabilirsiniz:

> Bu yerleşim için plaka belirtilmelidir.

## <a name="cause"></a>Nedeni

Bunun nedeni, **Varsayılan giriş konumu** alanının "çıkış" ambarına ait bir transit ambar için boş olmasıdır.

## <a name="resolution"></a>Çözüm

Bu sorunu gidermek için transit ambarında varsayılan bir giriş konumu belirtin. Bu konumun plaka denetimli olduğundan emin olun.
