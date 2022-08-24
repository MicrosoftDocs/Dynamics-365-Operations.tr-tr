---
title: Ortam kopyaladıktan sonra ürün ve kategoriler eksik
description: Bu makale, bir site ortamlar arasında veya aynı ortam içinde kopyalandıktan sonra ürün ve kategorilerin eksik olduğu durumlarda yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: d8df3f4cca6a7aaad98ffb7f2d284211a4f9589b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277919"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Ortam kopyaladıktan sonra ürün ve kategoriler eksik

[!include [banner](../../includes/banner.md)]

Bu makale, bir site ortamlar arasında veya aynı ortam içinde kopyalandıktan sonra ürün ve kategorilerin eksik olduğu durumlarda yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Bir site bir ortamdan diğerine veya aynı ortam içinde kopyalandıktan sonra, sitede ürünler ve Kategoriler eksik. Ürünler ve Kategoriler e-ticaret mağazasında ve Commerce Site Builder'daki **ürünler** sekmesinde yok.

## <a name="resolution"></a>Çözünürlük

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Kanal işletim birimi numarasını Commerce Site Builder'da yeni kopyalanmış bir siteyle eşleyin

Kanal işletim birimi numarasını (OUN) Commerce Site Builder'da yeni kopyalanmış bir siteyle eşlemek için aşağıdaki adımları izleyin.

1. Yeni kopyalanan siteyi seçin.
1. **Site Ayarları** altında, **Kanallar**'ı seçin.
1. Kanal adının yanındaki üç noktayı (**...**) seçin ve sonra **çevrimiçi mağaza kanalını Değiştir**'i seçin.
1. **Çevrimiçi mağaza kanalını Değiştir** iletişim kutusunda, yeni kopyalanan siteyle eşlenecek kanalı seçin ve **Tamam**'ı seçin.
1. **Kaydet ve yayınla** yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](../associate-site-online-store.md)
