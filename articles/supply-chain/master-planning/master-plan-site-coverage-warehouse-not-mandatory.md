---
title: "Tesis kapsamı için master planlama, ambar zorunlu değil"
description: "Bu konu, site boyutunun kapsam olduğu bir maddenin nasıl planlanacağını anlatır."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0b97f5f9a9a1447027e55d6c6b30253506caff70
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Tesis kapsamı için master planlama, ambar zorunlu değil

[!include [banner](../includes/banner.md)]

Bu konu, site boyutunun kapsam olduğu bir maddenin nasıl planlanacağını anlatır.

Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.
-   Ambar boyutu zorunluya göre ayarlanmamıştır. Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.
-   Tesis boyutu tedarik planlama için ayarlanmıştır.
-   Ambar boyutu tedarik planlama için ayarlanmamıştır. Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.

Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir. Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:
-   Madde karşılama, madde için tanımlanmıştır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.
-   Stok yenileme ilişkileri ambar için tanımlanmıştır. Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**. **Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.
-   Varsayılan sipariş türü Ürün, Satın alma siparişi veya Kanban olarak ayarlıdır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın. **Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü** alanına bakınız.

![Tesis kapsamı talebi ambar zorunlu değil    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>Ek kaynaklar
--------

[Master planlama ve birden çok tesis işlevi](master-plan-multisite-functionality.md)

[Master planlama - tesis kapsamı, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Master planlama - tesis ve ambar kapsamı, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Master planlama - ürün reçetesi sürümünün nasıl belirlendiği](master-plan-bom-version-determined.md)




