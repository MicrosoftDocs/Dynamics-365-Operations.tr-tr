---
title: "Master planlama tesis ve ambar için kapsamı, zorunlu ambar"
description: "Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunludur."
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Master planlama tesis ve ambar için kapsamı, zorunlu ambar

Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunludur.

Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.
-   Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.
-   Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır. Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir. Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.

Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir. Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:
-   The warehouse is set to **Manual**. ' I **Stok Yönetimi &gt;Kurulum &gt;Stok dökümü &gt;Ambarlar**. **Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.
-   Madde karşılama, madde için tanımlanmıştır. ' I **ürün bilgi yönetimi &gt;ürünleri&gt; ürünleri piyasaya**. Öğeyi seçin ve ardından eylem bölmesinde, üzerinde **Plan** sekmesini tıklatın, **Madde kapsamı**.
-   Stok yenileme ilişkileri ambar için tanımlanmıştır. ' I **Stok Yönetimi &gt;Kurulum &gt;Stok dökümü &gt;Ambarlar**. **Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.
-   Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır. ' I **ürün bilgi yönetimi &gt;ürünleri&gt; ürünleri piyasaya**. Öğeyi seçin ve ardından eylem bölmesinde, üzerinde **Plan** sekmesini tıklatın, **sipariş ayarları varsayılan**. **Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.

![Tesis ve ambar kapsamı talep et, ambar zorunlu](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Ayrıca bkz.
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Master planlama - tesis kapsamı, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Master planlama - tesis kapsamı, ambar zorunlu değil](master-plan-site-coverage-warehouse-not-mandatory.md)

[Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği](master-plan-bom-version-determined.md)


