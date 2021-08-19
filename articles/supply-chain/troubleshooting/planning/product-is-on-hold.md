---
title: Ürün hareketler için beklemede
description: Planlama emirlerini kesinleştirdikten sonra, maddenin hareketler için beklemede olduğunu bildiren bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752622"
---
# <a name="product-is-on-hold-for-transactions"></a>Ürün hareketler için beklemede

Hata kodu: SYS13295

## <a name="symptoms"></a>Belirtiler

Planlı siparişleri kesinleştirdikten sonra aşağıdaki hata iletisini alırsınız:

> %1 maddesi %2 hareketleri için durdurulmuş durumda.

## <a name="cause"></a>Nedeni

Engellenmiş maddeleri açıklarken, sistem *engellendi*, *durduruldu* ve *beklemede* terimlerini kullanır. Bu hata, maddenin varsayılan sipariş ayarlarında **Durduruldu** olarak ayarlandığı anlamına gelir.

Bir madde engellenirse ve bunu bir satınalma siparişine veya satış siparişi satırına eklerseniz, uyarı iletisi alırsınız. Bir madde engellendiğinde, satınalma siparişi veya satış siparişi satırıyla ilgili stok hareketleri, örneğin bir sevk irsaliyesini veya faturayı deftere naklederken, değiştirilemez. Satın alınan bir maddeyi engelleyebilir ve aynı zamanda satabilirsiniz. Bu durumda, **Durduruldu** onay kutusu bir satınalma siparişinde seçilir ancak madde stokta veya satış siparişinde engellenmez.

Aşağıda, bir madde numarasının satılmasını engellemeye neden olabilecek bazı koşullar yer almaktadır:

- Madde hala geliştirilme veya üretim aşamasındadır. Bu nedenle, satılmasını veya rezerve olmasını istemezsiniz.
- Birçok kusurlu madde aldınız ve maddenin satılabilmesi için hataların düzeltilmesi gerekiyor.

Bu tür durumlarda, sorun çözülünceye kadar maddeyi bloke edebilirsiniz.

Bir madde bloke edildiyse ve iade emri satırı oluşturduysanız bir ileti alırsınız. Bir madde dizisini veya lotunu bloke edemezsiniz. Maddenin bazı bölümlerinin bloke edilmesi gerekiyorsa bunları stoku taşıyarak veya maddenin o döneme ait tüm stokunu engelleyerek yapabilirsiniz.

## <a name="resolution"></a>Çözüm

- Madde için **Varsayılan sipariş ayarları** sayfasını açın ve **Durduruldu** onay kutusunu temizleyin.
