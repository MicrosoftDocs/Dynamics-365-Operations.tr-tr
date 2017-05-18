---
title: "Kanala özel indirimler tanımla"
description: "Perakendeciler sık sık farklı kanallara farklı iskontolar uygular. Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 6e52ba4bdb8e879959ff886010092914332e6e12
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="define-channel-specific-discounts"></a>Kanala özel indirimler tanımla

[!include[banner](includes/banner.md)]


Perakendeciler sık sık farklı kanallara farklı iskontolar uygular. Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir. 

<a name="channel-specific-discounts"></a>Kanala özel indirimler
--------------------------

Perakendeciler sık sık farklı kanallara farklı iskontolar sunar. Bunun sebebi yerel piyasa koşullarına yanıt vermek veya rakip perakendecilerle başa çıkmak için olabilir.

Microsoft Dynamics 365 for Operations'ta perakende ve ticaret, kanala özel indirimleri tanımlamak için fiyat gruplarını kullanır. Aşağıdaki varlıklardan biri veya daha fazlası için fiyat grupları atanabilir: kanallar, kataloglar, ilişkiler ve bağlılık programları. Bu makalede kanallar anlatılmaktadır, ancak aynı kavramlar katalog indirimleri, ilişkiler indirimleri ve bağlılık için indirimlerde de uygulanır.

## <a name="price-groups"></a>Fiyat grupları

[![Fiyat grupları](./media/price-groups-1024x608.png)](./media/price-groups.png)

Yukarıdaki diyagram, bir hareket üzerinde bulunabilen varlıklar (kanal, katalog, ilişki, müşteri, bağlılık programı kartı) arasındaki ilişkiyi ve yapılandırılabilen çeşitli iskonto türlerini gösterir. Tüm hareketler bir kanal içerisinde gerçekleşir, böylece kanalın hareket üzerinde bulunması garanti edilir. Kalan varlıklar isteğe bağlıdır. Her ana veri sayfalarında ilgili fiyat grupları sayfasına gerektiği gibi fiyat grupları girebileceğiniz veya görüntüleyebileceğiniz bir bağlantı vardır. Bir fiyat grubu, dört farklı tipte varlığı iskontolara, fiyat ayarlamalarına ve ticari anlaşmalara ilişkilendirmek için kullanılır. Fiyat gruplarınızı organize etmek için onları nasıl adlandıracağınıza dair bir strateji planlamanızı öneririz. Bir seçenek, farklı türler arasında ayrım yapabilmek için bir harf veya sayı ön veya son eki kullanmak olabilir. Örneğin, kanal fiyat grupları için 1-xxxxx ve katalog fiyat grupları için 2-xxxxx. Her birine iskonto ilişkilendirilmiş olabilecek her bir perakende varlığına odaklanan dört farklı sorgulama sayfası mevcuttur.

-   **Perakende kanalı fiyat grupları**- Bu sayfa her fiyat grubu için birbirine bağlı kanalların ve indirimlerin listesini gösterir.
-   **Katalog fiyat grupları**- Bu sayfa her fiyat grubu için birbirine bağlı katalogların ve indirimlerin listesini gösterir.
-   **Bağlılık fiyat grupları**- Bu sayfa her bağlılık programı için birbirine bağlı kanalların ve indirimlerin listesini gösterir.
-   **İlişki fiyat grupları**- Bu sayfa her bir ilişki için birbirine bağlı kanalların ve indirimlerin listesini gösterir.

## <a name="example-channel-discount-set-up"></a>Örnek kanal indirim ayarlama
Aşağıdaki örnek bir kanal iskonto ayarının kurulmasıyla ilgili görevleri gösterir.

1.  Bu örnekte **Houston** adlı bir kanal mevcuttur ve **Okula dönüş**adlı yeni bir indirim oluşturacaksınız.
2.  Fiyat ve iskonto stratejisi kanal indirimleri ihtimalini içerdiği için, bir kanal oluşturduğunuzda her zaman kanala özel bir fiyat grubu oluşturursunuz.
3.  Fiyat grubu **Houston-PG** mevcuttur ve bu, **Houston** kanalına atanmıştır.
4.  **Okula dönüş** yeni iskontosunu oluşturduktan sonra, **İndirim** sayfasının tepesindeki **Fiyat grupları** tıklamanız lazım. **İndirim fiyat grupları** sayfası açılacaktır. Bundan sonra **Yeni**'ye tıklayın ve **Houston-PG** fiyat grubunu seçin.
5.  Şimdi iskontoyu etkinleştirebilir ve kanala itebilirsiniz.

 

<a name="see-also"></a>Ayrıca bkz.
--------

[Fiyat ayarlamaları ve iskontolar](price-adjustments-discounts.md)




