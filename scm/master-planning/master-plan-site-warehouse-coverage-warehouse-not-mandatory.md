---
title: "Master planlama tesis ve ambar için kapsamı, zorunlu ambar"
description: "Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunlu değildir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3671024dc097c94638b1579d7cacc8447c49e97b
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Master planlama tesis ve ambar için kapsamı, zorunlu ambar

Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunlu değildir.

Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir. Bu ayar değiştirilemez.
-   Ambar boyutu zorunluya göre ayarlanmamıştır. Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.
-   Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır. Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir. Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.

Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir. Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:
-   Ambar El ile olarak ayarlanmıştır. ' I **Stok Yönetimi &gt;Kurulum &gt;Stok dökümü &gt;Ambarlar**. **Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.
-   Madde karşılama, madde için tanımlanmıştır. ' I **ürün bilgi yönetimi &gt;ürünleri&gt; ürünleri piyasaya**. Öğeyi seçin ve ardından eylem bölmesinde, üzerinde **Plan** sekmesini tıklatın, **Madde kapsamı**.
-   Stok yenileme ilişkileri ambar için tanımlanmıştır. ' I **Stok Yönetimi &gt;Kurulum &gt;Stok dökümü &gt;Ambarlar**. **Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.
-   Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır. ' I **ürün bilgi yönetimi &gt;ürünleri&gt; ürünleri piyasaya**. Öğeyi seçin ve ardından eylem bölmesinde, üzerinde **Plan** sekmesini tıklatın, **sipariş ayarları varsayılan**. **Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.

![Tesis ve ambar talebi, ambar zorunlu değil](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Ayrıca bkz.
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Master planlama - tesis ve ambar kapsamı, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Master planlama - tesis kapsamı, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Master planlama - tesis kapsamı, ambar zorunlu değil](master-plan-site-coverage-warehouse-not-mandatory.md)

[Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği](master-plan-bom-version-determined.md)


