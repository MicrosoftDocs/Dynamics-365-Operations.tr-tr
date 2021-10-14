---
title: Servis siparişi madde gereksinimleri
description: Bu konuda, servis siparişi madde gereksinimleri açıklanmaktadır.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae211cb24e3ed0e9e54643448ee378a20658ad89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573213"
---
# <a name="service-order-item-requirements"></a>Servis siparişi madde gereksinimleri

[!include [banner](../includes/banner.md)]

Müşterilerinize sağladığınız hizmetleri yönetmek ve izlemek için servis siparişi oluşturabilirsiniz. Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz. Bir madde gereksinimi hemen stoktan tüketilebilir ya da madde için üretim emri başlatabilirsiniz.

Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.

Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir. Bir servis siparişinde madde gereksinimi oluşturmak için, servis siparişinin bir projeye eklenmiş olması gerekir.

Bir servis siparişi için bir madde gereksinimi oluşturulur oluşturulmaz, bireysel servis siparişindeki **Proje**'den veya **Satış siparişi** formu üzerinden görüntülenebilir.

## <a name="view-an-item-requirement-from-a-service-order"></a>Bir servis siparişinden madde gereksinimi görüntüleme

1. **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.
1. **Gönder**'i ve ardından **Madde gereksinimi**'ni seçerek **Madde gereksinimleri** formunu açın.
1. Madde gereksiniminin servis siparişlerini görmek için **Proje** sekmesini seçin ve **Servis siparişi** alanını işaretleyin.

## <a name="delete-service-orders-with-item-requirements"></a>Madde gereksinimi olan servis siparişlerini silme

Bir servis siparişinde bir madde gereksinimi oluşturulmuşsa, servis siparişini silemezsini. Servis siparişini silebilmeniz için madde gereksinimini silmeniz gerekir.

1. **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.
1. **Gönder**'i ve ardından **Madde gereksinimi**'ni seçerek **Madde gereksinimleri** formunu açın. Bu form servis siparişinde oluşturulan tüm madde gereksinimlerini listeler.
1. Silinecek madde gereksinimini seçin ve ardından **Sil**'i seçin.

veya

1. **Proje yönetimi ve muhasebe** \> **Genel** \> **Projeler** \> **Tüm projeler**'e gidin.
1. Bir madde gereksiniminin oluşturulduğu servis siparişine sahip projeyi açın.
1. **Projeler** formunda sağ bölmede **Madde gereksinimleri**'ni seçin. **Madde gereksinimleri** formu seçili projeyle ilişkili madde gereksinimlerini listeler.
1. Silinecek madde gereksinimini seçin ve ardından **Sil**'i seçin.

## <a name="see-also"></a>Ayrıca bkz.

[Madde gereksinimleri (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]