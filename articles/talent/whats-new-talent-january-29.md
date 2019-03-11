---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (31 Ocak 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2019
ms.locfileid: "374746"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (31 Ocak 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır

**Derleme 8.1.2128**

## <a name="core-hr-changes"></a>Core HR Değişiklikleri

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Alına izin kişi kartı, izin planı tarihlerini dikkate almaz.
Takvim yılında yürütülmeyen izin planlarına sahip olanlar için **Alınan** kartı artık plan tanımlı izin yılında alınan izinleri görüntüler. Örneğin, bir kuruluşun izin yılı 1 Haziran ile 30 Mayıs arasındaysa ve bir çalışan Aralıkta 3 gün izin aldıysa, 15 Ocaktaki **Alındı** kartı 3 gün görüntüleyecektir. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Tahakkuk tutarları katman tarihi esasıyla eşleşmiyor
Müşterilerin, çalışanların hizmet aylarının etkin olduğunu belirlemeleri için İzin ve devamsızlık (**İnsan kaynakları** parametreleri) eklemek için yeni seçenekler eklenmiştir. Bazı kuruluşlar için tarih ay sonundadır, ancak diğerleri için diğer ayın başında olabilir. Örneğin, bir kuruluş 31 Aralıkta izin verebilirken bir başkası 1 Ocakta verebilir. Bu seçenek, ödüllendirmenin ne zaman gerçekleşeceğini seçmenize izin verir. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Çalışan işe alma işlemleri "İş akışı tamamlandı" durumunda takıldı
Az sayıda iş akışının "İş akışı tamamlandı" durumu ile sonlandırılmış olduğu bir hatayı düzeltmek için değişiklikler yapıldı. Yeni iş akışları şimdi bir iş akışı tamamlandığında "Tamamlandı" durumuna geçecektir. Bir iş akışı tamamlandı durumu içindeki tüm iş akışları, gerektiği taktirde güncelleştirme veya kaldırılması için bir hata durumuna geçirilecektir. 
