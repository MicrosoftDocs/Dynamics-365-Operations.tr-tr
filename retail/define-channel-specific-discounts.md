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
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Kanala özel indirimler tanımla

Perakendeciler sık sık farklı kanallara farklı iskontolar uygular. Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir. 

<a name="channel-specific-discounts"></a>Kanala özel indirimler
--------------------------

Perakendeciler genellikle farklı kanaldaki farklı indirimler sunmaktadır. Mayıs budur adres yerel Pazar koşullarına veya rakip Perakendeciler ile başa çıkmak için yapılması.

Perakende ve ticaret işlemleri için Microsoft Dynamics 365 kanal özel indirimler tanımlamak için fiyat gruplarını kullanır. Aşağıdaki varlıklardan biri veya daha fazlası için fiyat grupları atanabilir: kanallar, kataloglar, ilişkiler ve bağlılık programları. Bu makalede kanallar anlatılmaktadır, ancak aynı kavramlar katalog indirimleri, ilişkiler indirimleri ve bağlılık için indirimlerde de uygulanır.

## <a name="price-groups"></a>Fiyat grupları
\[Başlık ID = "eki\_256084" Hizala = "alignnone" width = "640"\][![fiyat grupları](./media/price-groups-1024x608.png)](./media/price-groups.png) grup bağlantıları için perakende fiyatı\[/altyazı\]

Yukarıdaki diyagramda (kanal, katalog, ilişki, müşteri, bağlılık programı kart) bir hareket olabilir varlıklar ve yapılandırılabilen çeşitli iskonto türleri arasındaki ilişkiyi göstermektedir. Kanal bir harekette bulunması garanti böylece tüm hareketleri bir kanalda gerçekleşir. Kalan varlıklar isteğe bağlıdır. Her ana veri sayfalarında ilgili fiyat grupları sayfasına gerektiği gibi fiyat grupları girebileceğiniz veya görüntüleyebileceğiniz bir bağlantı vardır. Bir fiyat grubu iskonto, fiyat ayarlamaları ve ticari sözleşmeleri için dört farklı türde varlıkları ilişkilendirmek için kullanılır. Bunları düzenli tutmak için fiyat gruplarının nasıl adlandıracağız bir strateji planı öneririz. Farklı türleri arasında ayrım yapmak için bir harf veya sayı önek veya sonek kullanmak için bir seçenek olacaktır. Örneğin, 1-xxxxx kanal fiyat grupları ve Katalog fiyat grupları için 2-xxxxx. Her birine iskonto ilişkilendirilmiş olabilecek her bir perakende varlığına odaklanan dört farklı sorgulama sayfası mevcuttur.

-   **Perakende kanalı fiyat grupları **- Bu sayfa her fiyat grubu için birbirine bağlı kanalların ve indirimlerin listesini gösterir.
-   **Katalog fiyat grupları **- Bu sayfa her fiyat grubu için birbirine bağlı katalogların ve indirimlerin listesini gösterir.
-   **Bağlılık fiyat grupları **- Bu sayfa her bağlılık programı için birbirine bağlı kanalların ve indirimlerin listesini gösterir.
-   **İlişki fiyat grupları **- Bu sayfa her bir ilişki için birbirine bağlı kanalların ve indirimlerin listesini gösterir.

## <a name="example-channel-discount-set-up"></a>Örnek kanal indirim ayarlama
Aşağıdaki örnek bir kanal iskonto ayarının kurulmasıyla ilgili görevleri gösterir.

1.  Bu örnekte **Houston** adlı bir kanal mevcuttur ve **Okula dönüş**adlı yeni bir indirim oluşturacaksınız.
2.  Fiyat ve iskonto stratejisi kanal indirimleri ihtimalini içerdiği için, bir kanal oluşturduğunuzda her zaman kanala özel bir fiyat grubu oluşturursunuz.
3.  Fiyat grubu **Houston-PG** mevcuttur ve bu, **Houston** kanalına atanmıştır.
4.  **Okula dönüş** yeni iskontosunu oluşturduktan sonra, **İndirim** sayfasının tepesindeki **Fiyat grupları** tıklamanız lazım. **İndirim fiyat grupları** sayfası açılacaktır. Bundan sonra **Yeni**'ye tıklayın ve **Houston-PG** fiyat grubunu seçin.
5.  Şimdi iskontoyu etkinleştirebilir ve kanala itebilirsiniz.

 

<a name="see-also"></a>Ayrıca bkz.
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


