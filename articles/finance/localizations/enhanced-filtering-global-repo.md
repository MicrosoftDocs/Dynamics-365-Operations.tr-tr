---
title: RCS/genel depoda RCS gelişmiş filtre uygulama
description: Bu makalede, ilave filtreler eklenerek geliştirilmiş olan RCS Genel deposu için gelişmiş filtreleme özellikleri açıklanmaktadır.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a343b9f1af68a727cb2a8d1e390f85e10aab2d39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901226"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS/Genel depoda yapılandırmaları bulmak için RCS gelişmiş filtreleme seçenekleri

[!include [banner](../includes/banner.md)]

Bu makalede, aşağıdaki ölçütlere sahip filtreleme olanağı eklenerek geliştirilmiş olan Regulatory Configuration Services (RCS) Genel deposu için gelişmiş filtreleme özellikleri açıklanmaktadır: 
- **Ülke/bölge** - ISO ülke kodlarını temel alarak  
- **Etiket** türleri:
  - İşlevsel alan
  - Özellik alanı
  - Sektör 
  - İş belgesi 

Belirli veya ilgili yapılandırmaları daha kolay bulmak için, ayrı olarak veya grup halinde filtreler uygulayabilirsiniz. Örneğin, satıcı faturalarıyla ilişkili yapılandırılabilir iş belgelerinin tek bir türünü bulmak için, bu belge türünü aramak üzere **İş belgesi türü** filtresi uygulayabilirsiniz. 

[![Genel depo için filtre bölümü.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Belge türünü seçip (örneğin 'satıcı faturası') **Filtre uygula**'ya tıklayarak aramayı daha da belirginleştirebilirsiniz. Aşağıdaki örnek, **İş belgesi türü**'nde filtre uygulandığındaki sonuçları belge türü eklenmiş şekilde gösterir. 

[![İş belgesi türü için uygulanan filtre ve içe aktarma.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtre uygulanan sonuçlar bir kullanıcı RCS deposuna veya Dynamics 365 Finance ortamına tek başına veya küme olarak aktarılabilir. Bunu yapmak için, yapılandırmalar grubunu seçin ve **İçe aktar**'a tıklayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]