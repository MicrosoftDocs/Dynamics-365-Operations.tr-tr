---
title: Store Commerce uzantısı sorunlarını giderme
description: Bu makalede, Microsoft Dynamics 365 Commerce Store Commerce uygulamasındaki uzantı sorunlarının nasıl giderileceği açıklanmaktadır.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269794"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Store Commerce uzantısı sorunlarını giderme

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce Store Commerce uygulamasındaki uzantı sorunlarının nasıl giderileceği açıklanmaktadır.

## <a name="extensions-packages-arent-loaded"></a>Uzantı paketleri yüklü değil

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Uzantı paketleri, POS \>Ayarlar sayfasında görünmüyor

Commerce Runtime (CRT) tetikleyicileri, uzantı paketini içerecek şekilde güncelleştirilmemiş veya dağıtılmamış olabilir. Daha fazla bilgi için bkz. [Commerce Runtime (CRT) genişletilebilirliği ve tetikleyicileri](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Uzantı paketleri POS \>Ayarlar sayfasında görünüyor ancak bildirim yüklenmiyor

Uzantılar paketlerinin  **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions** klasöründe bulunduğunu doğrulayın. Paketler varsa bildirimin yer aldığı bir **POS** klasörü bulunmalıdır.

**POS** klasörü yoksa Store Commerce projesinin satış noktası (POS) uzantı projesine doğru şekilde başvuruda bulunduğunu doğrulayın. Proje referans yolunu doğrulayın ve var olduğundan emin olun. 

Aşağıdaki örnek çizimde, yükleyici projesi referans verilen uzantı projesiyle ilgili sorun yaşıyor.

![Store Commerce yükleyici proje referansı geçerli değil.](media/ReferenceNotValid.png)

Uzantı projesinin başvurusu doğru şekilde eklendiyse aşağıdaki örnek çizimde gösterildiği gibi, yükleyici projesinde hiçbir uyarı veya bağımlılık sorunu olmaz.

![Store Commerce yükleyici proje referansı geçerli.](media/ReferenceValid.png)
