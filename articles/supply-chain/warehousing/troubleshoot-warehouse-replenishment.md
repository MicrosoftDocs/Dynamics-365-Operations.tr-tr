---
title: Ambar stok yenileme sorunlarını giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993912"
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