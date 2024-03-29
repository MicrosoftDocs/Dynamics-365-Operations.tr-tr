---
title: Teslim al seçeneği sepette veya ürün ayrıntıları sayfalarında görünmüyor
description: Bu makale, sepet sayfasında veya ürün ayrıntıları sayfalarında mağazadan teslim alma seçeneği gözükmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 85d102d3442e19377912cb9562010778a0575db8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284616"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>"Teslim al" seçeneği sepette veya ürün ayrıntıları sayfalarında görünmüyor

[!include [banner](../../includes/banner.md)]

Bu makale, sepet sayfasında veya ürün ayrıntıları sayfalarında mağazadan teslim alma seçeneği gözükmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

**Teslim al** düğmesi sepet sayfasında veya ürün ayrıntıları sayfalarında görünmüyor.

Aşağıdaki resimde **Teslim al** düğmesini içeren bir sayfa örneği gösterilmektedir.

![Teslim al düğmesi.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Çözüm

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Commerce Site Builder'da BOPIS uzantısını etkinleştirme

Commerce Site Builder'da "çevrimiçi satın al, mağazadan teslim al" (BOPIS) uzantısını etkinleştirmek için aşağıdaki adımları izleyin.

1. Sitenizi seçin.
1. **Site Ayarları**'nı ve daha sonra **Uzantılar**'ı seçin.
1. **BOPIS'ı devre dışı bırak** seçeneğinin temizlenmiş olduğundan emin olun.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Commerce Headquarters'da teslimat şekillerini yapılandırma

Commerce Headquarters'da teslimat şekillerdini yapılandırmak için şu adımları izleyin.

1. **Tedarik ve kaynak \> Kurulum \> Teslimat şekilleri**'ne gidin.
1. **Müşteri teslim alma** teslimat şeklinin oluşturulduğundan ve ürün ve adreslerin buna atanmış olduğundan emin olun.
1. **Retail ve Commerce \> Headquarters kurulumu \> Parametreler**'e gidin.
1. Sol gezinti bölmesinde **Müşteri siparişleri**'ni seçin.
1. **Teslim alma teslimat şekli**'nin doğru yapılandırıldığından emin olun.

### <a name="configure-customer-orders-payments"></a>Müşteri siparişleri ödemelerini yapılandırma

Commerce Headquarters'da müşteri siparişleri ödemelerini yapılandırmak için şu adımları izleyin.

1. **Retail ve Commerce \> Headquarters kurulumu \> Parametreler**'e gidin.
1. Sol gezinti bölmesinde **Müşteri siparişleri**'ni seçin.
1. **Ödemeler** hızlı sekmesinde, **Ödeme koşullarının** ve **ödeme yönteminin** doğru ayarlandığından emin olun.

## <a name="additional-resources"></a>Ek kaynaklar

[BOPIS'i yapılandırma](../cpe-bopis.md)

[Müşteri sipairşleri için Çoklu malzeme çekme teslimat şekillerini etkinleştirme](../multiple-pickup-modes.md)

[Çok yönlü kanal Commerce siparişi ödemeleri](../dev-itpro/commerce-payments.md)

[Mağaza seçicisi modülü](../store-selector.md)
