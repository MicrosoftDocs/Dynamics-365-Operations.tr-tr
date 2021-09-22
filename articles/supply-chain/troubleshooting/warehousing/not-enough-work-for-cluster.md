---
title: Profil yapılandırıldıktan sonra küme için yeterli iş bulunamadı
description: Küme profili yapılandırıyorsanız yeterli iş bulunamadığını belirten bir hata iletisi alabilirsiniz. Profili düzenleyin ve Pozisyonları etkinleştir seçeneğini Hayır olarak ayarlayın.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477814"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Sistem tarafından yönlendirilen küme malzeme çekme kullanılırken küme için yeterli iş bulunamadı

## <a name="symptoms"></a>Belirtiler

*Sistem tarafından yönlendirilen küme malzemesi çekme* işlemini kullanırken örneğin, 10 pozisyonun çekildiği bir küme profili yapılandırırsanız işlem, 10 pozisyona kadar malzeme çekme için yeterli iş olduğunda planlanan şekilde çalışır. Ancak malzemenin çekileceği yalnızca sekiz pozisyon varsa aşağıdaki hata iletisini alırsınız:

> Küme için yeterli iş bulunamadı.

## <a name="resolution"></a>Çözüm

Bu sorunu gidermek için küme profilini düzenleyin ve **Pozisyonları etkinleştir** seçeneğini *Hayır* olarak ayarlayın.
