---
title: Toplu iş üst maddeleri için eldeki stok dikkate alınmıyor
description: Bazı yerleştirme şablonları, toplu iş üst maddeleri için mevcut eldeki stoku dikkate almıyor. Toplu iş veya seri numarasının, talep emrinde belirtilmesi gerekir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477848"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Yerleştirme şablonları, toplu iş üst maddeleri için eldeki stoku dikkate almıyor

## <a name="symptoms"></a>Belirtiler

*Eldeki miktarı dikkate al* ölçütüne sahip yerleştirme şablonları, *toplu iş üstü* maddeler için geçerli eldeki stok envanterini dikkate almaz. Bunlar yalnızca, toplu iş numarası satış siparişi satırında belirtilmişse bunu dikkate alır.

Ancak, *toplu iş altı* maddeleri kullandığınızda, geçerli eldeki stok beklendiği gibi kabul edilir.

Daha fazla bilgi için bkz. [Ambar yerleştirme](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Çözüm

Yerleştirme şablon başlığı *sipariş edilen*, *rezerve edilen* veya *serbest bırakılan* talep stratejisi için tanımlanabilir. *Sipariş edilen* talep stratejisi için, rezervasyon veya ambara serbest bırakma işlemlerine uygulanan aynı rezervasyon hiyerarşisi gereksinimleri geçerlidir. Bu nedenle, *toplu iş üstü* ve *Seri üstü* ayırma hiyerarşileri bulunan maddeler için, toplu iş veya seri numarasının talep emrinde (satış veya transfer) belirtilmesi gerekir.

Alternatif olarak, Ambar yerleştirme talebi oluşturulmadan önce toplu iş veya seri numarasını seçmek için *Rezerve edilen* talep stratejisi kullanılabilir.
