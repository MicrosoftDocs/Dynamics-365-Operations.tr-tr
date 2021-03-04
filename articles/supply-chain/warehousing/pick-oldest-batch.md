---
title: Mobil cihazda en eski toplu işi seçme
description: Bu konu bir mobil cihazdan en eski toplu işi seçme seçeneklerinin nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f235c34d6369c6f0584a7bac1c1be75f3d84c9c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439178"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Mobil cihazda en eski toplu işi seçme

[!include [banner](../includes/banner.md)]

**En eski toplu işi seç** konfigürasyonuna mobil cihaz menüsünden erişebilirsiniz ve bu konfigürasyon ambar çalışanlarını bulundukları yerleşimde en eski toplu işi seçme konusunda zorlamanızı veya uyarmanızı sağlar.  

## <a name="where-it-applies"></a>Uygulandığı yerler
En eski işi seçme mobil cihaz menü öğelerinde yapılandırılır ve aşağıdaki toplu iş maddeleri için seçimi etkiler.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>En eski toplu işi seçme için konfigürasyonu ayarlama 
Varolan işi kullanmak üzere ayarlanan maddeler için **En eski toplu işi seç** mobil cihaz menüsünden **Hiçbiri**, **Uyar** veya **Zorla** olarak ayarlanabilir.

**Hiçbiri**: Çalışanlar herhangi bir ileti almaz ve bulundukları yerleşimde herhangi bir toplu işi seçmelerine izin verilir.

**Uyar** ve **Zorla**: Çalışan bir toplu iş seçerken toplu iş denetiminin üstünde en eski bitiş tarihine sahip olan toplu işlerin listesi görüntülenir. Konum plaka denetimli ise, en eski toplu işe sahip plakaların listesi plaka denetiminin üst kısmında gösterilir. 
-   **Uyar**: Çalışan gösterilen listede olmayan bir plaka veya toplu iş seçerse, denetim boş bırakılacak ve seçilmek üzere daha eski bir toplu iş bulunduğunu belirten bir uyarı görüntülenecektir. Çalışmaya devam etmek için, çalışan aynı toplu işi veya plakayı yeniden seçebilir.  
-   **Zorla**: Çalışanlar seçmek için daha eski bir toplu iş olduğunu gösteren iletiyi almaya devam eder.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]