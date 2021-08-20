---
title: Üretim katı yürütme arabirimini tasarlama
description: Bu konuda her yapılandırma için kullanıcı arabirimi içeriğinin nasıl tasarlanacağı açıklanmaktadır.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 6332b4b15b277faca506da4ea67fcc3ddb9799153a6fe73a711050ab93bdf565
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782479"
---
# <a name="design-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini tasarlama

[!include [banner](../includes/banner.md)]

Üretim katı yürütme arabirimi tarafından kullanılan her yapılandırma için kullanıcı arabirimi içeriği tasarlayabilirsiniz. Örneğin, bir çalışma hücresindeki çalışanların üretim katındaki iş talimatlarını başka bir çalışma hücresinde açabilmesi gerekebilir. Bu durumda, biri belge eklerini açmak için kullanılan bir düğmeye ve diğeri bu düğmeye sahip olmayan iki yapılandırma oluşturulmalıdır.

## <a name="design-a-tab"></a>Sekme tasarlama

**Üretim katı yürütmesini yapılandırma** sayfasında, Eylem bölmesinde **Sekme tasarla**'yı seçerek sekme oluşturabilir ve yapılandırabilirsiniz.

Aşağıdaki çizimde gösterildiği gibi her sekme dört bölüme ayrılmıştır.

![Sekme düzeni.](media/pfe-tab-layout.png "Sekme düzeni")

Çizimde aşağıdaki öğeler gösterilir:

1. Birincil araç çubuğu
1. İkincil araç çubuğu
1. Ana görünüm
1. Ayrıntılı görünüm

Yeni bir sekme oluşturmak ve yapılandırmak için bu adımları izleyin:

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.

1. **Sekme tasarla** sayfasını açmak için, eylem bölmesinde **Sekme tasarla**'yı seçin.

    ![Sekme tasarla sayfası.](media/pfe-design-tabs.png "Sekme tasarla sayfası")

1. Eylem Bölmesi'nde **Yeni**'yi seçin.

1. Sayfanın üst bilgisinde aşağıdaki ayarları yapın:

    - **Sekme adı**: Sekme için bir ad belirtin.
    - **Ana görünüm**: Önceden tanımlanmış iş listeleri (*Etkin işler*, *Tüm işler* veya *Makinem*) arasında seçim yapın.
    - **Ayrıntılar görünümü**: Boş bir değer veya **İş ayrıntıları** arasında seçim yapın. Boş değeri seçerseniz, sekmede ayrıntılı görünüm olmaz. **İş detayları**'nı seçerseniz, ayrıntılı görünümde ana görünümdeki iş listesinde seçilen işin ayrıntılı açıklaması yer alır.

1. **Birincil araç çubuğu** bölümünde, birincil araç çubuğunda hangi düğmelerin kullanılabilir olmasını istediğinizi seçin. **Kullanılabilir eylemler** sütunu, eklenebilecek tüm düğmelerin listesini gösterir. **Seçilen eylemler** sütunları, geçerli yapılandırmaya dahil edilen tüm düğmelerin listesini gösterir. Sütunlar arasında seçili öğeleri gerektiği gibi taşımak için sütunlar arasındaki düğmeleri kullanın. Düğmelerin kullanıcı arabiriminde sunulduğu sırayı denetlemek için **Seçili eylemler** sütununun yanındaki yukarı ve aşağı düğmelerini kullanın.

1. **İkincil** **araç çubuğu** bölümünde, ikincil araç çubuğunda hangi düğmelerin kullanılabilir olmasını istediğinizi seçin. **Kullanılabilir eylemler** sütunu, eklenebilecek tüm düğmelerin listesini gösterir. **Seçilen eylemler** sütunları, geçerli yapılandırmaya dahil edilen tüm düğmelerin listesini gösterir. Sütunlar arasında seçili öğeleri gerektiği gibi taşımak için sütunlar arasındaki düğmeleri kullanın. Düğmelerin kullanıcı arabiriminde sunulduğu sırayı denetlemek için **Seçili eylemler** sütununun yanındaki yukarı ve aşağı düğmelerini kullanın.

## <a name="associate-a-tab-with-a-configuration"></a>Sekmeyi yapılandırma ile ilişkilendirme

Gereksinim duyduğunuz tüm sekmeleri tasarladıktan sonra, bunları bir yapılandırma ile ilişkilendirebilirsiniz.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.

    ![Üretim katı yürütmeyi yapılandırma.](media/pfe-config-prod-floor-execution.png "Üretim katı yürütmeyi yapılandır")

1. **Sekme seçimi** hızlı sekmesinde **Ekle**'yi seçin.

1. Kılavuza yeni bir satır eklenir. Bu yeni satır için yapılandırmaya eklemek istediğiniz sekmenin adını seçin.

1. Gerektikçe ek sekmeler eklemeye devam edin.

1. Sekmeleri gerektiği gibi düzenlemek için araç çubuğundaki **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanın. Sekmeler, yukarıdaki ekran görüntüsünde gösterilen sırada soldan sağa doğru görüntülenecektir (üstteki sekme solda gösterilir).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]