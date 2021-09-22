---
title: Yük ağırlığı yalnızca pozitif sayılar içerebilir
description: Konumlar arasında işi işlerken yük ağırlığı ve güncelleştirmenizin iptal edilmesi ile ilgili bir hata alabilirsiniz. Sorunu düzeltmek için şu adımları izleyin.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477836"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Konumlar arasında iş işlenirken yük ağırlığı hatası ve güncelleştirme iptal edildi

## <a name="symptoms"></a>Belirtiler

Paketleme konumlarından hazırlama konumlarına veya hazırlama konumlarından yerleştirme konumlarına iş işlerken açık iş varsa aşağıdaki hatayı alabilirsiniz:

> "Yük ağırlığı"(=-%1) alanı yalnızca pozitif sayılar içerebilir. Güncelleştirme iptal edildi.

## <a name="resolution"></a>Çözüm

Bu sorunu gidermek için **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin ve **Ambar yükü ağırlık tutarlılık denetimi** için işlemi çalıştırın.
