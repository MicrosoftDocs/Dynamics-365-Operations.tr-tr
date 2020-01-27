---
title: Ticaret önizleme ortamına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı genel görünümünü vermektedir.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906082"
---
# <a name="commerce-preview-environment-overview"></a>Ticaret önizleme ortamına genel bakış

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı genel görünümünü vermektedir.

## <a name="overview"></a>Genel Bakış

Commerce önizleme ortamı, müşterilerin genel kullanıma açık sürümünden önce Commerce ürününü denemesini sağlayan isteğe bağlı bir uçtan uca Dynamics 365 Commerce önizleme ortamıdır.

Özellikleri veya işlevleri etkilemeyen bazı küçük sınırlamalardan dolayı, Commerce önizleme ortamı eksiksiz bir ticaret deneyimi sağlar ve müşteriler ve uygulama ortakları tarafından ürünü değerlendirmek, geribildirim sağlamak ve sığdırma/boşluk analizi yapmak için kullanılabilir.

## <a name="limitations-of-the-commerce-preview-environment"></a>Commerce önizleme ortamının sınırlamaları

Commerce önizleme ortamı tam ticari özellik ve işlevsellik kümesini sağlasa da, küçük bazı sınırlamalar vardır:

- Commerce önizleme ortamının kendisinin hiç coğrafi sınırlamaları olmamasına rağmen, Retail Cloud Scale Unit (RCSU) ve e-ticaret uygulamaları gibi ortam bileşenleri yalnızca Amerika Birleşik Devletleri sağlanabilir.
- Commerce önizleme ortamının kullanımında, e-ticaret sağlama tarihinden itibaren 30 günlük zaman sınırlaması vardır.
- Commerce önizleme ortamı, yalnızca bir ortamdaki tüm bileşenlerin tek bir sanal makinede (VM) dağıtıldığı gösteri topolojisini kullanan bir ortamda başarıyla dağıtılabilir ve başlatılabilir. Bu OneBox VM topolojisinin ana sınırlaması, önizleme ortamının destekleyebileceği eşzamanlı kullanıcı sayısıdır.
- Ticari önizleme ortamı yalnızca, ticaret ürününün genel kullanılabilirliği (GA) kadar değerlendirilebilir. Yeni tanıtım ortamları GA'dan sonra kullanılabilecektir.

## <a name="get-started"></a>Başlayın

Commerce önizleme ortamını sağlamak için bkz. [Commerce önizleme ortamı sağlama](provisioning-guide.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Ticaret önizleme ortamı sağlama](provisioning-guide.md)

[Ticaret önizleme ortamı yapılandırma](cpe-post-provisioning.md)

[Bir Commerce Preview ortamı için isteğe bağlı özellikleri konfigüre edin](cpe-optional-features.md)

[Ticaret önizleme ortamı SSS](cpe-faq.md)
