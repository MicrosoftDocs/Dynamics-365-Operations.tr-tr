---
title: Master planlama, kullanılabilir kapasitenin fazlasını planlıyor
description: Master planlama, kapasite sınırlamalarını dikkate almıyor ve kullanılabilir kapasitenin fazlasını planlıyor
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477862"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Master planlama, kullanılabilir kapasitenin fazlasını planlıyor

## <a name="symptoms"></a>Belirtiler

Master planlama, kapasite sınırlamalarını dikkate almıyor ve kullanılabilir kapasitenin fazlasını planlıyor.

Sınırlı kapasite bulunan ve rotanın hem bir kaynak grubu hem de bağımsız kaynaklar için çeşitli gereksinimler belirttiği durumlarda işlem programlamayı kullandığınızda, algoritmanın kapasite çakışmalarını doğrulama biçimi nedeniyle küçük bir aşırı planlama olasılığı vardır. Bu fazla planlama, master planlamayı çalıştırmak için yardımcıları kullandığınızda ortaya çıkabilir. Görece daha kısa bir çalışma zamanı olan birçok iş olduğunda ortaya çıkması olasıdır.

## <a name="resolution"></a>Çözüm

İşlem programlama için hiçbir fazla planlama oluşmuyorsa **Master planlama parametreleri** sayfasında **İşlem Programlaması için Sınırlı Doğru Kapasite**'yi açarak master planlamanın programlama bölümünü tekli iş parçacıklı hale getirebilirsiniz. Bu seçenek varsayılan olarak kullanılamaz. Kişiselleştirme özelliklerini kullanarak bunu sayfaya el ile eklemeniz gerekir. Bu seçeneği kullandığınızda, paralel işlem olmaması nedeniyle planlama daha yavaş çalışır.
