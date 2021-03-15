---
title: RCS/genel depoda RCS gelişmiş filtre uygulama
description: Bu konu, ek filtreler içermek üzere geliştirilmiş olan RCS Genel deposu için gelişmiş filtreleme özelliklerini açıklamaktadır.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005854"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS/Genel depoda yapılandırmaları bulmak için RCS gelişmiş filtreleme seçenekleri

[!include [banner](../includes/banner.md)]

Bu konu, aşağıdaki ölçütlere sahip filtreleme olanağını içermek üzere geliştirilmiş olan Regulatory Configuration Services (RCS) Genel deposu için gelişmiş filtreleme özelliklerini açıklamaktadır: 
- **Ülke/bölge** - ISO ülke kodlarını temel alarak  
- **Etiket** türleri:
  - İşlevsel alan
  - Özellik alanı
  - Sektör 
  - İş belgesi 

Belirli veya ilgili yapılandırmaları daha kolay bulmak için, ayrı olarak veya grup halinde filtreler uygulayabilirsiniz. Örneğin, satıcı faturalarıyla ilişkili yapılandırılabilir iş belgelerinin tek bir türünü bulmak için, bu belge türünü aramak üzere **İş belgesi türü** filtresi uygulayabilirsiniz. 

[![Genel depo için filtre bölümü](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Belge türünü seçip (örneğin 'satıcı faturası') **Filtre uygula**'ya tıklayarak aramayı daha da belirginleştirebilirsiniz. Aşağıdaki örnek, **İş belgesi türü**'nde filtre uygulandığındaki sonuçları belge türü eklenmiş şekilde gösterir. 

[![İş belgesi türü için uygulanan filtre ve içe aktarma](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtre uygulanan sonuçlar bir kullanıcı RCS deposuna veya Dynamics 365 Finance ortamına tek başına veya küme olarak aktarılabilir. Bunu yapmak için, yapılandırmalar grubunu seçin ve **İçe aktar**'a tıklayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]