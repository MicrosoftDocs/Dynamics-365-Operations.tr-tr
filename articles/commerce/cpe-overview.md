---
title: Dynamics 365 Commerce değerlendirme ortamına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı genel görünümünü vermektedir.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f225db13fba91ce78287adfda9c6d084dea20af33e62287f517e51cc5a296352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752524"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Dynamics 365 Commerce değerlendirme ortamına genel bakış

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı genel görünümünü vermektedir.

> [!NOTE]
> Commerce değerlendirme ortamları genel olarak kullanıma sunulmamıştır ve iş ortakları ile müşterilere istek üzerine sunulmaktadır. Daha fazla bilgi için Microsoft iş ortağı ilgili kişisine ulaşın.

Commerce değerlendirme ortamı, iş ortaklarının ve potansiyel müşterilerin Commerce ürününü denemesini sağlayan isteğe bağlı bir uçtan uca Dynamics 365 Commerce değerlendirme ortamıdır.

Değerlendirme ortamları, gerekli sağlama sonrası adımları azaltmak amacıyla kısmi olarak önceden yapılandırılır.

Özellikleri veya işlevleri etkilemeyen bazı küçük sınırlamalara karşın, Commerce değerlendirme ortamı eksiksiz bir ticaret deneyimi sağlar ve müşteriler ve uygulama ortakları tarafından ürünü değerlendirmek, geribildirim sağlamak ve uygunluk/boşluk analizi yapmak için kullanılabilir.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Commerce değerlendirme ortamının sınırlamaları

Commerce değerlendirme ortamı tam Commerce özellik ve işlevsellik kümesini sağlasa da, küçük bazı sınırlamalar vardır:

- Commerce değerlendirme ortamının hiç coğrafi sınırlaması olmamasına karşın, Retail Cloud Scale Unit (RCSU) ve e-Ticaret uygulamaları gibi ortam bileşenleri yalnızca Amerika Birleşik Devletleri'nde sağlanabilir.
- Commerce değerlendirme ortamının kullanımında, e-Ticaret sağlama tarihinden itibaren 30 günlük zaman sınırlaması vardır.
- Commerce değerlendirme ortamı, yalnızca bir ortamdaki tüm bileşenlerin bulutta barındırılan tek bir sanal makinede (VM) dağıtıldığı gösteri topolojisini kullanan bir ortamda başarıyla dağıtılabilir ve başlatılabilir. Bu topolojinin ana sınırlaması, ortamın destekleyebileceği eşzamanlı kullanıcı sayısıdır.

## <a name="get-started"></a>Başlayın

Commerce değerlendirme ortamını sağlamak için bkz. [Commerce değerlendirme ortamı sağlama](provisioning-guide.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce değerlendirme ortamı sağlama](provisioning-guide.md)

[Dynamics 365 Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
