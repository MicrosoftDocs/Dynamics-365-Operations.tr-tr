---
title: Stoğu olmayan maddeler ödeme sayfasına yönlendirilebiliyor
description: Bu konu, müşterilerin stoğu olmayan maddeleri alışveriş sepetlerine ekleyebildiği ve ödeme sayfasına ilerleyebildiği durumlarda yardımcı olan sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018470"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Stoğu olmayan maddeler ödeme sayfasına yönlendirilebiliyor

[!include [banner](../../includes/banner.md)]

Bu konu, müşterilerin stoğu olmayan maddeleri alışveriş sepetlerine ekleyebildiği ve ödeme sayfasına ilerleyebildiği durumlarda yardımcı olan sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Kullanıcılar elde stoğu olmayan bir maddeyi sepetine ekleyebiliyor ve ödeme sayfasına ilerleyebiliyor.

## <a name="resolution"></a>Çözünürlük

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Commerce Site Builder'da stokta yok hatalarını göster özelliğini etkinleştirin

Commerce Site Builder'da **stokta yok hatalarını göster** özelliğini etkinleştirmek için şu adımları izleyin.

1. Üzerinde çalıştığınız siteyi seçin.
1. Soldaki gezinti bölmesinde **Sayfalar** seçin.
1. Açmak için **cartpage**'i seçin.
1. **Sepet 1** yuvasını seçin , **Düzenle**'yi seçin ve sonra Özellikler bölmesinde **Stokta yok hatalarını göster** onay kutusunu seçin.
1. Sayfayı kaydedip yayınlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Stok ayarlarını uygulama](../inventory-settings.md)

[Perakende kanalları için stok kullanılabilirliğini hesaplama](../calculated-inventory-retail-channels.md)

[Stok arabellekleri ve stok düzeyleri yapılandırma](../inventory-buffers-levels.md)
