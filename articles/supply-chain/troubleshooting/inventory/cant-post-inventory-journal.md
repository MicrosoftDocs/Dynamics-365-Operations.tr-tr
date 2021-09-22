---
title: Stok günlüğü iş akışı hiçbir zaman tamamlanmıyor ve günlük işlenemiyor
description: Bir günlük onay iş akışını gönderdikten sonra, iş akışı işlemesi yanıt vermemeye başlar ve günlüklerinizi düzenleyemez veya işleyemezsiniz.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477810"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Stok günlüğü iş akışı hiçbir zaman tamamlanmıyor ve günlük işlenemiyor

## <a name="symptoms"></a>Belirtiler

Bir günlük onay iş akışını gönderdikten sonra, iş akışı işlemesi yanıt vermemeye başlar ve günlüklerinizi düzenleyemez veya işleyemezsiniz.

## <a name="resolution"></a>Çözüm

İş akışı işlemenin tamamlanmamasının birden fazla nedeni olabilir. Aşağıdaki sorunların olup olmadığını kontrol edin:

- **Stok yönetimi &gt; Kurulum &gt; Stok yönetimi iş akışları**'na gidin ve etkilenen iş akışının yapılandırmasını inceleyin. Daha fazla bilgi için bkz. [Stok günlüğü onay iş akışları](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- İş akışı bir özel durum veya hata ile karşılaşıyor olabilir. Etkilenen iş akışının iş öğesi geçmişini gözden geçirerek iş akışını sonlandıran bir uygulama hatası içerip içermediğini inceleyin.
- Stok günlüğü yalnızca onaylanırsa güncelleştirilebilir veya düzenlenebilir. Geri çağırma etkinse, günlüğü geri çağırmayı deneyebilirsiniz. İş akışı toplu işinin yürütülmesi birden çok nedenle askıya alınabilir. Bu nedenlerden bazıları iş akışı çerçevesi sorunundan kaynaklanıyor olabilir.
