---
title: Kanala özel indirimler tanımla
description: Perakendeciler sık sık farklı kanallara farklı iskontolar uygular. Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 36b2d8f96f8545f9fa792e42c639b03e1e14e8ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213758"
---
# <a name="define-channel-specific-discounts"></a>Kanala özel iskontolar tanımlama

[!include [banner](includes/banner.md)]

Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir.

## <a name="channel-specific-discounts"></a>Kanala özel indirimler

Perakendeciler sık sık farklı kanallara farklı iskontolar sunar. Bunun nedeni, yerel piyasa koşullarına yanıt vermek veya rakip perakendecilerle başa çıkmaya çalışmak olabilir.

Commerce, fiyat gruplarını kanal özel indirimleri tanımlamak için kullanır. Aşağıdaki varlıklardan biri veya daha fazlası için fiyat grupları atanabilir: kanallar, kataloglar, ilişkiler ve bağlılık programları. Bu makalede kanallar anlatılmaktadır, ancak aynı kavramlar katalog indirimleri, ilişkiler indirimleri ve bağlılık için indirimlerde de uygulanır.

## <a name="price-groups"></a>Fiyat grupları

[![Fiyat grupları](./media/price-groups-1024x608.png)](./media/price-groups.png)

Yukarıdaki diyagram, bir hareket üzerinde bulunabilen varlıklar (kanal, katalog, ilişki, müşteri, bağlılık programı kartı) arasındaki ilişkiyi ve yapılandırılabilen çeşitli iskonto türlerini gösterir. Tüm hareketler bir kanal içerisinde gerçekleşir, böylece kanalın hareket üzerinde bulunması garanti edilir. Kalan varlıklar isteğe bağlıdır. Her ana veri sayfalarında ilgili fiyat grupları sayfasına gerektiği gibi fiyat grupları girebileceğiniz veya görüntüleyebileceğiniz bir bağlantı vardır. Bir fiyat grubu, dört farklı tipte varlığı iskontolara, fiyat ayarlamalarına ve ticari anlaşmalara ilişkilendirmek için kullanılır. Fiyat gruplarınızı organize etmek için onları nasıl adlandıracağınıza dair bir strateji planlamanızı öneririz. Bir seçenek, farklı türler arasında ayrım yapabilmek için bir harf veya sayı ön veya son eki kullanmak olabilir. Örneğin, kanal fiyat grupları için 1-xxxxx ve katalog fiyat grupları için 2-xxxxx. Her birine iskonto ilişkilendirilmiş olabilecek her bir Commerce varlığına odaklanan dört farklı sorgulama sayfası mevcuttur.

- **Commerce kanalı fiyat grupları** – Bu sayfa her fiyat grubu için birbirine bağlı kanalların ve indirimlerin listesini gösterir.
- **Katalog fiyat grupları** – Bu sayfa her fiyat grubu için birbirine bağlı katalogların ve indirimlerin listesini gösterir.
- **Bağlılık fiyat grupları** – Bu sayfa her bağlılık programı için birbirine bağlı kanalların ve indirimlerin listesini gösterir.
- **İlişki fiyat grupları** – Bu sayfa her bir ilişki için birbirine bağlı kanalların ve indirimlerin listesini gösterir.

## <a name="example-channel-discount-set-up"></a>Örnek kanal indirim ayarlama

Aşağıdaki örnek bir kanal iskonto ayarının kurulmasıyla ilgili görevleri gösterir.

1. Bu örnekte **Houston** adlı bir kanal mevcuttur ve **Okula dönüş** adlı yeni bir indirim oluşturacaksınız.
2. Fiyat ve iskonto stratejisi kanal indirimleri ihtimalini içerdiği için, bir kanal oluşturduğunuzda her zaman kanala özel bir fiyat grubu oluşturursunuz.
3. Fiyat grubu **Houston-PG** mevcuttur ve bu, **Houston** kanalına atanmıştır.
4. **Okula dönüş** yeni iskontosunu oluşturduktan sonra, **İndirim** sayfasının tepesindeki **Fiyat grupları** tıklamanız lazım. **İndirim fiyat grupları** sayfası açılacaktır. Bundan sonra **Yeni**'ye tıklayın ve **Houston-PG** fiyat grubunu seçin.
5. Şimdi iskontoyu etkinleştirebilir ve kanala itebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Fiyat ayarlamaları ve iskontolar](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]