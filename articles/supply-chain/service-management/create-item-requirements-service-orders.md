---
title: Servis siparişleri için madde gereksinimleri oluşturma
description: Bu konuda, servis siparişleri için madde gereksinimlerinin nasıl oluşturulacağı açıklanmaktadır.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a92843a82093826822ab9865e43fee07d65e94c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677828"
---
# <a name="create-item-requirements-for-service-orders"></a>Servis siparişleri için madde gereksinimleri oluşturma

[!include [banner](../includes/banner.md)]

Müşterilerinize sağladığınız hizmetleri yönetmek ve izlemek için servis siparişi oluşturabilirsiniz. Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz. Bir madde gereksinimi hemen stoktan tüketilebilir ya da madde için üretim emri başlatabilirsiniz.

Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.

Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir. Bir servis siparişinde madde gereksinimi oluşturmak için, servis siparişinin bir projeye atanmış olması gerekir. Servis siparişi için madde gereksinimi oluşturduktan sonra madde gereksinimini seçilen projenin **Projeler** formundan görüntüleyebilirsiniz.

## <a name="create-an-item-requirement-for-a-service-order"></a>Servis siparişi için madde gereksinimi oluşturma

1. **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.
1. Madde gereksinimi oluşturmak istediğiniz servis siparişini seçin.
1. **Eylem Bölmesi**'nde, **Gönder** sekmesinde **Madde gereksinimi**'ni seçin.
1. **Madde gereksinimleri** formunda, gereken madde için bilgileri girin. Belirli alanlar hakkında daha fazla bilgi için bkz. [Madde gereksinimleri (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Servis sözleşmesi için madde gereksinimi oluşturma

1. **Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne gidin.
1. Madde gereksinimi oluşturmak istediğiniz servis sözleşmesini açın.
1. **Satırlar** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'yi seçin.
1. **Hareket türü** alanında **Madde**'yi seçin.
1. **Madde kurulumu** alanında **Madde gereksinimi**'ni seçin.
1. **Madde numarası** alanında, servis sözleşmesi için gereken maddeyi seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Ürün boyutları** sekmesindeki **Tesis** alanında, madde için stok tesisi seçin.
1. Sözleşme satırından servis siparişi oluşturmak için **Satırlar** hızlı sekmesinde **Servis siparişleri oluştur**'u seçin ve **Servis siparişleri oluştur** formuna ilgili bilgileri girin.

## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişlerini otomatik olarak oluşturma](create-service-orders-automatically.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
