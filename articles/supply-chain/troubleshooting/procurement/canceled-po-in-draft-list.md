---
title: İptal edilen satınalma siparişleri çalışma alanındaki taslak listesinde görüntüleniyor
description: İptal edilen satınalma siparişleri Satınalma siparişi hazırlama çalışma alanındaki taslak listesinde görüntüleniyor
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
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477870"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>İptal edilen satınalma siparişleri çalışma alanındaki taslak listesinde görüntüleniyor

## <a name="symptoms"></a>Belirtiler

*Onaylanmış* durumda olan satınalma siparişlerini iptal ettikten sonra, iptal edilen satınalma siparişleri **Satınalma siparişi hazırlama** çalışma alanındaki taslak satınalma siparişleri listesinde görünmeye devam eder.

## <a name="resolution"></a>Çözüm

Bu sorun yalnızca değişiklik yönetimine bağlı satınalma siparişlerinde oluşur. Bunun nedeni, iptal işleminin onaylanması gereken bir değişiklik olduğu kabul edilir. Onay, sistem tarafından otomatik olarak yapılabilir. Bu nedenle işlem, iptal edilen satınalma siparişinin onay iş akşına gönderilmesidir. Böylece *Onaylı* durumuna geçebilir. Bu noktada, satınalma siparişi artık **Satınalma siparişi hazırlama** çalışma alanındaki taslak satınalma siparişleri listesinde görünmez.
