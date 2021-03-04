---
title: Satın alma ve kaynak hizmetleri iş akışları ile ilgili sorunları giderme
description: Bu konu, satın alma ve kaynak hizmetleri iş akışları ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439724"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Satın alma ve kaynak hizmetleri iş akışları ile ilgili sorunları giderme

Bu konu, satın alma ve kaynak hizmetleri iş akışları ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Bir değişiklikten sonra bir satınalma siparişi iş akışına yeniden gönderilirken hata oluştu: "Değişiklik yönetimi etkinleştirildiğinde X satınalma siparişinde yapılan değişikliklere, yalnızca Taslak durumunda izin verilir"

Bu sorun yalnızca satınalma siparişi siz değişiklikleri talep etmeden önce *Onaylandı* durumdaysa oluşur. Satınalma siparişi *Onaylandı* durumunda iken değişiklik istediğinizde, iş akışı başarıyla işlenebilir.

### <a name="error-description"></a>Hata açıklaması

Bir satınalma siparişinin bir değişiklikten sonra yeniden gönderilmesi halinde, iş akışında aşağıdaki hata oluşur:

> Durduruldu (hata): X + + Özel durumu: PO0000569 numaralı satınalma siparişinde yapılan değişikliklere yalnızca değişiklik yönetiminin etkinleştirildiği Taslak durumunda izin verilir<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Sorun, [Microsoft Bilgi Bankası (KB) makalesi](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) ile düzeltilecektir.

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış.

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Değişiklik yönetiminin açık olduğu bir satınalma siparişinde teslimat kalanı iptal edilirse, satınalma siparişi Onaylı durumuna geçer.

### <a name="issue-description"></a>Sorun açıklaması

Değişiklik yönetimine bağlı bir satınalma siparişi için, istenen tek değişiklik bir veya daha fazla satırda kalan teslimatın iptali ise, onaylandığında satınalma siparişi doğrudan *Onaylandı* durumuna geçer ve hiçbir günlük oluşturulmaz.

### <a name="issue-resolution"></a>Sorunun çözümü

Bir teslim işleminin geri kalanının iptal edilmesi onay günlüğünün içeriğini etkilemez. Bu işlev, satır kısmen alındığında kullanılmalıdır ve satınalma siparişi satıcıyla onaylandıktan sonra işlem adımında geri kalan miktarı iptal edilmelidir.

Bu, satınalma siparişi teyidini yansıtılacağından, onayın gerekli olabilmesi için satınalma siparişi satırında miktar ayarlanmalıdır. Bunun yerine, satırda hiçbir şey alınmadığında, miktar kaldırılır. Bu durumda, yeniden onay gerekir.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>İptal edilen satınalma siparişleri Satınalma siparişi hazırlama çalışma alanındaki taslak listesinde görüntülenir.

### <a name="issue-description"></a>Sorun açıklaması

*Onaylanmış* durumda olan satınalma siparişlerini iptal ettikten sonra, iptal edilen satınalma siparişleri **Satınalma siparişi hazırlama** çalışma alanındaki taslak satınalma siparişleri listesinde görünmeye devam eder.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun yalnızca değişiklik yönetimine bağlı satınalma siparişlerinde oluşur. Bunun nedeni, iptal işleminin onaylanması gereken bir değişiklik olduğu kabul edilir. Onay, sistem tarafından otomatik olarak yapılabilir. Bu nedenle işlem, iptal edilen satınalma siparişinin onay iş akşına gönderilmesidir. Böylece *Onaylı* durumuna geçebilir. Bu noktada, satınalma siparişi artık **Satınalma siparişi hazırlama** çalışma alanındaki taslak satınalma siparişleri listesinde görünmez.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]