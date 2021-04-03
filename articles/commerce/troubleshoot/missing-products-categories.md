---
title: Ortam kopyaladıktan sonra ürün ve kategoriler eksik
description: Bu konu, bir site ortamlar arasında veya aynı ortam içinde kopyalandıktan sonra ürün ve kategorilerin eksik olduğu durumlarda yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585581"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Ortam kopyaladıktan sonra ürün ve kategoriler eksik

[!include [banner](../../includes/banner.md)]

Bu konu, bir site ortamlar arasında veya aynı ortam içinde kopyalandıktan sonra ürün ve kategorilerin eksik olduğu durumlarda yardımcı olabilecek sorun giderme kılavuzu sağlar.

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
