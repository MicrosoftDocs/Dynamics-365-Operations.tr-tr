---
title: Varsayılan vergi grubu ve nakit iskontosu fatura hesabından doldurulamıyor
description: Varsayılan bir vergi grubu ve varsayılan nakit iskontosu fatura hesabından doldurulamıyor
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477841"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Varsayılan vergi grubu ve nakit iskontosu fatura hesabından doldurulamıyor

## <a name="symptoms"></a>Belirtiler

Müşteri hesabından farklı bir fatura hesabı kullanıyorsanız, bir satınalma siparişi oluşturulduğunda varsayılan vergi grubu ve varsayılan nakit iskontosu fatura hesabından doldurulmaz.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. Vergi grubu, nakit iskontoları ve diğer fiyat bilgilerinin varsayılan değerleri fatura hesabına değil müşteri hesabına dayanır.
