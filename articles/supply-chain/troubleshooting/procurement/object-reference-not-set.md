---
title: Satınalma siparişi onayı sırasında "Nesne başvurusu ayarlanmadı" hatası oluşuyor
description: Satınalma siparişi onayı sırasında "Nesne başvurusu ayarlanmadı" hatası oluşuyor
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
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477869"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>Satınalma siparişi onayı sırasında "Nesne başvurusu ayarlanmadı" hatası oluşuyor

## <a name="symptoms"></a>Belirtiler

Satınalma siparişini onaylarken aşağıdaki özel durumu alırsınız:

> Nesne başvurusu ayarlanmadı

## <a name="cause"></a>Nedeni

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

## <a name="resolution"></a>Çözüm

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
