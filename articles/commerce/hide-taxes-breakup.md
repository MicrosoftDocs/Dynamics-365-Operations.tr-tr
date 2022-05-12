---
title: Sipariş özetlerindeki vergi sonu bilgilerini gizle
description: Bu konu, Microsoft Dynamics 365 Commerce'teki sepet, teslim alma, sipariş onayı ve sipariş ayrıntıları sayfalarındaki satış özetlerinin vergi döküm bilgilerinin nasıl gizleneceğini açıklamaktadır.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645227"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Sipariş özetlerindeki vergi sonu bilgilerini gizle

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'teki sepet, teslim alma, sipariş onayı ve sipariş ayrıntıları sayfalarındaki satış özetlerinin vergi döküm bilgilerinin nasıl gizleneceğini açıklamaktadır.

Varsayılan olarak, Dynamics 365 Commerce'teki sepet, teslim alma, sipariş onayı ve sipariş ayrıntıları sayfalarındaki satış özetlerinin vergi döküm bilgileri görüntülenir. Commerce 10.0.27 sürümünden itibaren, Commerce site oluşturucuda sipariş özetlerinde vergi döküm bilgilerini gizlemenize olanak tanıyan bir seçenek bulunur.

Aşağıdaki örnekte, iki sipariş özeti örneği gösterilmektedir. İlki, vergi dökümü bilgilerini gösterirken ikincisinde bu gizlenmiştir.

![Vergi dökümü bilgilerinin gösterildiği ve gizlendiği sepet örnekleri.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Sipariş özetlerinde vergi döküm bilgilerini gizleme seçeneği yalnızca e-ticaret kanalındaki **Fiyatlar satış vergisini dahil eder** seçeneği, Commerce genel merkezinde **Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'da **Evet** olarak ayarlandığında kullanılabilir. 
> - Varsayılan olarak, Site oluşturucuda **Vergi dökümünü sipariş özetinde göster** seçeneği etkinleştirilmiştir.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Sipariş özetlerindeki vergi sonu bilgilerini gizle

Sipariş özetlerindeki vergi sonu bilgilerini gizlemek için aşağıdaki adımları izleyin.

1. Commerce site oluşturucuda güncelleştirmek istediğiniz siteye gidin.
1. **Site ayarları \> uzantılarına** gidin.
1. **Sipariş özetinde vergi dökümünü göster** onay kutusunu temizleyin.

Sipariş özetleri içinde vergi döküm bilgilerini göstermek için, **Sipariş özetinde vergi dökümünü göster** onay kutusunu seçin.  

Aşağıdaki şekil, site oluşturucuda **Sipariş özetinde vergi dökümünü göster** onay kutusunun vurgulanmış ve seçilmiş olduğunu gösterir.

![Site oluşturucuda, sipariş özetinde vergi dökümünü göster seçeneği.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Satış vergisine genel bakış](/finance/general-ledger/indirect-taxes-overview)

[Çevrimiçi siparişler için satış vergisini yapılandırma](sales-tax-config.md)

[Sorun giderme: Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı](troubleshoot/tax-miscalculated-online-order.md)
