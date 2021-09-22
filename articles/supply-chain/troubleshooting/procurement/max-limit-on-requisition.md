---
title: Satınalma sözleşmesi maksimum sınırı, satınalma talebinde etkili değil
description: Satınalma sözleşmesi maksimum sınırı, satınalma talebinde etkili değil
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477826"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Satınalma sözleşmesi maksimum sınırı, satınalma talebinde etkili değil

## <a name="symptoms"></a>Belirtiler

Bir satınalma talebi bir satınalma sözleşmesine bağlandığında, satınalma sözleşmesinden maksimum limit satınalma talebi üzerinde etkili olmaz. Varsayılan fiyat bilgileri doğru girilmiştir, ancak satınalma sözleşmesinden maksimum sınırdan fazlası satınalma talebinde sipariş edilebilir.

## <a name="resolution"></a>Çözüm

Bu davranış beklenmektedir. Talepler her zaman onaylanmadığından, satınalma sözleşmesinde bir miktar veya tutar rezerve edilmemelidir. Bu nedenle, satınalma sözleşmesinden maksimum sınırı karşılamazsınız.
