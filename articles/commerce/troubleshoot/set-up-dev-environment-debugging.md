---
title: Katman 1 Retail Server sanal makinede hata ayıklama için e-ticaret geliştirme ortamı ayarlama
description: Bu konuda Katman 1 Retail Server sanal makinede (VM) hata ayıklama için e-ticaret geliştirme ortamının nasıl ayarlandığı açıklanmaktadır.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801495"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Katman 1 Retail Server sanal makinede hata ayıklama için e-ticaret geliştirme ortamı ayarlama

[!include [banner](../../includes/banner.md)]

Bu konuda Katman 1 Retail Server sanal makinede (VM) hata ayıklama için e-ticaret geliştirme ortamının nasıl ayarlandığı açıklanmaktadır.

## <a name="description"></a>Tanım

Microsoft Dynamics 365 Commerce Katman 1 ortamları normal olarak Commerce Runtime (CRT) ve satış noktası (POS) uzantısı için dağıtılır. Bunlar bağımsız ortamlardır. Mimarinin hizmet olarak yazılım (SaaS) yapısı nedeniyle, bunlar e-ticaret bileşenleri içermez.

Bazı senaryolarda, bir katman 1 ortamındaki uzantılara yapılan çağrıları test etmek isteyebilirsiniz, böylece e-ticaret bileşenlerinden gelen uzantılar için hata ayıklayabilirsiniz. Genel yönergeler için bkz. [Katman 1 Commerce geliştirme ortamında hata ayıklama](../e-commerce-extensibility/debug-tier-1.md).

Bir katman 1 ortamına karşı hata ayıklarken, site şimdi farklı bir Retail Server aradığı için, çapraz sunucu çağrıları içerik güvenlik ilkesiyle ilişkili çeşitli hatalara neden olabilir.

Aşağıdaki resimde, ürün ayrıntıları sayfasında bir varyant seçildiğinde oluşabilecek bir hata örneği gösterilmektedir.

![Ürün Ayrıntıları sayfasında bir varyant seçildiğinde oluşan hata](media/unhandled-rejection-error.jpg)

Aşağıdaki çizimde, tarayıcının hata ayıklama araçlarında (F12 geliştirici araçları) benzer bir hatanın örneği gösterilmektedir. Hata iletisi, içerik güvenlik ilkesi yönergesinin ihlalinden bahseder.

![Hata ayıklayıcı araçları hatası](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Çözünürlük

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Commerce site oluşturucuda sitenin içerik güvenliği ilkesini devre dışı bırakın

1. Üzerinde çalıştığınız siteyi seçin.
1. **Ayarlar**'ı ve daha sonra **Uzantılar**'ı seçin.
1. **İçerik güvenlik ilkesi** sekmesinde **içerik güvenlik ilkesini devre dışı bırak**'ı seçin.
1. **Kaydet ve yayınla** yı seçin.

> [!NOTE]
> İşletme-tüketici (B2C) oturumu açma, yerel bir geliştirme ortamında çalışmaz. Ancak, kullanıcı olarak oturum açmak gerektiğinde konuk olarak ödeme yapmayı kullanabilir veya sahte sayfa oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[E-ticaret çevrimiçi genişletilebilirlik geliştirmesini kullanmaya başlama](../e-commerce-extensibility/sdk-getting-started.md)

[E-ticaret sitesinde içerik güvenlik ilkesini (CSP) Yönetme](../manage-csp.md)
