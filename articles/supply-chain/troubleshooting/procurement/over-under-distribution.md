---
title: Muhasebe dağıtımları fazla ya da eksik dağıtılmış
description: Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış.
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
ms.openlocfilehash: 7ff0172469df50da9e4272b3fa3f75001a4eb7eb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477846"
---
# <a name="accounting-distributions-are-either-over--or-under-distributed"></a>Muhasebe dağıtımları fazla ya da eksik dağıtılmış


## <a name="symptoms"></a>Belirtiler

Aşağıdaki hatayı alırsınız:

> Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış ya da eksik dağıtılmış

## <a name="cause"></a>Nedeni

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

## <a name="resolution"></a>Çözüm

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
