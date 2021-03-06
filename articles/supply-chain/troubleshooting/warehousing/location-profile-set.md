---
title: Konum profili negatif stoka izin vermiyor ancak eksi eldeki stoka izin veriliyor
description: Konum profili için Negatif stoka izin ver seçeneği Hayır olarak ayarlanmış, ancak sistem yine de negatif eldeki stoka izin veriyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026981"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Konum profili negatif stoka izin vermiyor ancak eksi eldeki stoka izin veriliyor

KB numarası: 4613622

## <a name="symptoms"></a>Belirtiler

Konum profili için **Negatif stoka izin ver** seçeneği *Hayır* olarak ayarlanmış, ancak sistem yine de negatif eldeki stoka izin veriyor.

## <a name="example-scenario"></a>Örnek senaryo

Resmi düzenlemeye tabi hareketler için sistem, defter zararlarına negatif stok kaydedebilmelidir. Bir maddenin negatif stok gösterebilmesini ancak bunu sadece tanklar gibi atanan konumlarda yapmasını istersiniz. Ancak, madde modeli grubu negatif stoka izin veriyor ise konumun negatif stoka izin verecek şekilde ayarlanıp ayarlanmadığı fark etmez. Madde, negatif stoka izin verilmeyecek şekilde ayarlanmışsa, konum profilinin nasıl ayarlandığı önemli değildir.

## <a name="resolution"></a>Çözünürlük

Konum profilinden **Negatif stoka izin ver** ayarı, yalnızca malzeme çekme gibi ambar işlemlerine uygulanır. Ancak, negatif stoka izin verilecek şekilde ayarlanan madde modeli grupları, Stok yönetimi ve Ambar yönetimi modüllerinden tüm işlemleri etkiler ve konum profili ayarı geçersiz kılmaz.

Bir ambarın negatif stok taşıma izni olup olmadığını kontrol edebilirsiniz. Madde modeli gruplarınızı negatif fiziksel stoka izin vermeyecek şekilde ayarlayın ve yalnızca ilgili ambarı negatif stoka izin verecek şekilde ayarlayın.
