---
title: İçerik teslimi ağı uygulama seçenekleri
description: Bu makale, Microsoft Dynamics 365 Commerce ortamlarıyla kullanılabilecek içerik teslim ağı (CDN) uygulaması için farklı seçenekleri inceler. Bu seçenekler arasında, yerel, Commerce tarafından sağlanan Azure Front Door örnekleri ve müşterilere ait Azure Front Door örnekleri bulunur.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: de2ecab86809af3ace64ba06956f00137d254ab7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275160"
---
# <a name="content-delivery-network-implementation-options"></a>İçerik teslimi ağı uygulama seçenekleri

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce ortamlarıyla kullanılabilecek içerik teslim ağı (CDN) uygulaması için farklı seçenekleri inceler. Bu seçenekler arasında, yerel, Commerce tarafından sağlanan Azure Front Door örnekleri ve müşterilere ait Azure Front Door örnekleri bulunur.

Commerce müşterilerinin, Commerce ortamlarıyla hangi CDN hizmetini kullanacaklarını düşündüklerinde çeşitli seçenekleri vardır. Commerce temel barındırma ve özel etki alanı gereksinimlerini kapsayan temel Azure Front Door desteği ile sunulmuştur. Web uygulaması güvenlik duvarı (WAF) gibi daha fazla denetim ve daha fazla belirli güvenlik becerileri isteyen şirketler için en iyi seçenek, Azure Front Door'un müşteriye ait bir örneğini veya harici bir CDN hizmeti kullanmak olabilir.

Commerce ortamlarıyla aşağıdaki üç CDN uygulama seçeneği kullanılabilir:

- Commerce tarafından sağlanan Azure Front Door örneği
- Müşteriye ait Azure Front Door örneği (Artırılmış denetim ve ek güvenlik özellikleri için)
- Harici bir CDN hizmeti

Üç CDN uygulama seçeneği de özel etki alanlarından yalnızca dinamik HTML içeriği sunar. Commerce, tüm JavaScript, Geçişli stil sayfaları (CSS), görüntü, video ve diğer statik içeriği Microsoft tarafından yönetilen CDN'ler aracılığıyla otomatik olarak işler. Seçtiğiniz seçenek, işlevsel özellikleri, kontrol özelliklerini ve kullanılabilen ek güvenlik özelliklerini belirler.

Aşağıdaki örnekte Commerce mimarisine genel bakış verilmektedir.

![Commerce mimarisine genel bakış.](media/Commerce_CDN-Option_ComparisonModels.png)

Commerce siteniz için bir Azure Front Door örneği ayarlama hakkında daha fazla bilgi için bkz. [CDN Desteği ekleme](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Commerce tarafından sağlanan Azure Front Door örneğini kullanma

Aşağıdaki tabloda içerik bitiş noktalarını yönetmek üzere, Commerce tarafından sağlanan Azure Front Door örneğini kullanmanın avantajları ve dezavantajları listelenmektedir.

| Avantajlar | Dezavantajlar |
|------|------|
| <ul><li>Örnek, Commerce maliyetine dahildir.</li><li>Örnek Commerce ekibi tarafından yönetildiğinden, daha az bakım gerektirir ve paylaşılan kurulum adımları vardır.</li><li>Azure'da barındırılan altyapı ölçeklenebilir, güvenli ve güvenilirdir.</li><li>Güvenli Yuva Katmanı (SSL) sertifikası bir kerelik kurulum gerektirir ve otomatik olarak yenilenir.</li><li>Örnek, Commerce ekibi tarafından hatalar ve bozukluklar için izlenir.</li></ul> | <ul><li>WAF desteklenmez.</li><li>Belirli özelleştirmeler veya ayar ayarlamaları yoktur.</li><li>Örnek, güncelleştirmeler veya değişiklikler için Commerce ekibine bağlıdır.</li><li>Apex etki alanları için ayrı bir Azure Front Door örneği gereklidir ve Apex etki alanlarını Azure DNS ile bütünleştirmek için ek işler gereklidir.</li><li>Müşteriye saniyedeki yanıtlar (RPS) veya hata oranı hakkında hiçbir telemetri sağlanmaz.</li></ul> |

Aşağıdaki resimde, Commerce tarafından sağlanan Azure Front Door örneğinin mimarisi gösterilmektedir.

![Commerce tarafından sağlanan Azure Front Door örneği.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Müşteriye ait bir Azure Front Door örneği kullanma

Aşağıdaki tabloda içerik bitiş noktalarını yönetmek üzere, müşteriye ait Azure Front Door örneğini kullanmanın avantajları ve dezavantajları listelenmektedir.

| Avantajlar | Dezavantajlar |
|------|------|
| <ul><li>Kurulum güvenli ve yönetilmesi kolaydır.</li><li>Azure'da barındırılan altyapı ölçeklenebilir, güvenli ve güvenilirdir.</li><li>Örnek, WAF tümleştirmesine ve özellikle sitenize göre ayarlanmış daha hassas güvenlik sağlayan detaylı kural denetimlerine olanak sağlar.</li><li>Örnek, SSL sertifikalarının (hem müşteriye ait hem de Azure Front Door'un yönettiği) ve etki alanı bağlamanın daha iyi denetimine olanak sağlar.</li><li>Örnek doğrudan Azure DNS ile eşlendiyse, bir Apex etki alanı çözümü sunar.</li><li>Telemetri ve uyarı sağlanır.</li><li>SSL sertifikası bir kerelik kurulum gerektirir ve otomatik olarak yenilenir.</li></ul> | <ul><li>Örnek kendi kendine yönetilir.</li><li>Öğrenme ve alışma süresi gereklidir.</li></ul> |

Aşağıdaki resimde, müşteriye ait bir Azure Front Door örneği içeren bir Commerce altyapısı gösterilmektedir.

![Müşteriye ait bir Azure Front Door örneği içeren bir Commerce altyapısı.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Harici bir CDN hizmeti kullanma

Aşağıdaki tabloda içerik son noktalarını yönetmek için harici bir CDN hizmeti kullanmanın avantajları ve dezavantajları listelenmektedir.

| Avantajlar | Dezavantajlar |
|------|------|
| <ul><li>Bu seçenek, varolan etki alanı zaten harici bir CDN'de barındırılıyorsa yararlıdır.</li><li>WAF: Harici sağlayıcıya bağlıdır.</li></ul> | <ul><li>Ayrı bir sözleşme ve ek maliyetlendirme gereklidir.</li><li>SSL ek maliyet gerektirebilir.</li><li>Hizmet Azure bulut yapısından ayrı olduğundan, ek altyapı yönetilmelidir.</li><li>Bu hizmet uç noktada ve güvenlik kurulumunda daha uzun süre yatırım gerektirebilir.</li><li>Hizmet kendi kendine yönetilir.</li><li>Hizmet kendi kendine izlenir.</li></ul> |

Aşağıdaki resimde, harici bir CDN hizmeti içeren bir Commerce altyapısı gösterilmektedir.

![Harici CDN hizmeti içeren Commerce altyapısı.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)
