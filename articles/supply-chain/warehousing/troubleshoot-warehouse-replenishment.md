---
title: Ambar stok yenileme sorunlarını giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828094"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Ambar stok yenileme sorunlarını giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>"%1 kimlikli iş, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir hata iletisi alıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenmiştir.

### <a name="issue-resolution"></a>Sorunun çözümü

Dalga talep stok yenilemesini kullandığınızda, kaynak sipariş talebini yerine getirmek için bir malzeme çekme konumunda stoğun yenilenmesi gerekiyorsa sistem hem stok yenileme işini, hem de malzeme çekme işini oluşturur. Ancak, stok yenileme işi tamamlanana kadar malzeme çekme işini engeller. Bu davranış kasıtlı yapılır çünkü stok yenileme işi tamamlanana kadar malzeme çekme konumunda stok yeterli olmaz. Stok yenileme işini tamamlayın ve sonra malzeme çekme işini işleyin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]