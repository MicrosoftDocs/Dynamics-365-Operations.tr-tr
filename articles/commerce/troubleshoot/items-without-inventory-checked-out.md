---
title: Stoğu olmayan maddeler ödeme sayfasına yönlendirilebiliyor
description: Bu konu, müşterilerin stoğu olmayan maddeleri alışveriş sepetlerine ekleyebildiği ve ödeme sayfasına ilerleyebildiği durumlarda yardımcı olan sorun giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585571"
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
