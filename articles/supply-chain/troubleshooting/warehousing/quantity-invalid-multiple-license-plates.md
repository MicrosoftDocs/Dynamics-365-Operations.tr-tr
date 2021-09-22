---
title: Miktar birden fazla LP ile malzeme çekme işi için geçerli değil
description: Tek bir konumda birden fazla plakayla malzeme çekme işi varken miktar ea birimi için geçerli değildir. Aşağıdaki alanların doğru olduğundan emin olun.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477807"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Miktar tek bir konumda birden fazla LP ile malzeme çekme işi varken geçerli değil

## <a name="symptoms"></a>Belirtiler

Tek bir konuma birden fazla plakayla malzeme çekme işi varken miktar *ea* birimi için geçerli değildir ve aşağıdaki hata iletisini alırsınız:

> Miktar 1% birimi için geçerli değil.

## <a name="resolution"></a>Çözüm

Serbest bırakılan ürün veya ürün varyantındaki **Birim dizisi grup kodu** ve **Birim dönüştürmeleri** alanlarının doğru ayarlandığını doğrulayın.

Hata iletisinin beklenen miktarı göstermek için 10.0.15 sürümünde geliştirilmiş olduğunu unutmayın (bkz. [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Yeni hata iletisi:

> Miktar geçersiz. Beklenen %1 %2.
