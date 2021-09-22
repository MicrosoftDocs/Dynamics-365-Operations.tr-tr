---
title: Satınalma siparişi bir değişiklikten sonra iş akışına yeniden gönderilirken hata oluşuyor
description: Satınalma siparişi bir değişiklikten sonra iş akışına yeniden gönderilirken hata oluşuyor
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477895"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Satınalma siparişi bir değişiklikten sonra iş akışına yeniden gönderilirken hata oluşuyor


## <a name="symptoms"></a>Belirtiler

Bir satınalma siparişinin bir değişiklikten sonra yeniden gönderilmesi halinde, iş akışında aşağıdaki hata oluşur:

> Durduruldu (hata): X + + Özel durumu: PO0000569 numaralı satınalma siparişinde yapılan değişikliklere yalnızca değişiklik yönetiminin etkinleştirildiği Taslak durumunda izin verilir<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Bu sorun yalnızca satınalma siparişi siz değişiklikleri talep etmeden önce *Onaylandı* durumdaysa oluşur. Satınalma siparişi *Onaylandı* durumunda iken değişiklik istediğinizde, iş akışı başarıyla işlenebilir.

## <a name="resolution"></a>Çözüm

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Sorun, [Microsoft Bilgi Bankası (KB) makalesi](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) ile düzeltilecektir.
