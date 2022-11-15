---
title: Tesis kapsamı için master planlama, ambar zorunlu
description: Bu makalede, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır. Ambar zorunlu bir boyuttur.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df58017c25737cc946d09bf86ff7ad8bd33f4176
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741053"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Tesis kapsamı için master planlama, ambar zorunlu

[!include [banner](../includes/banner.md)]

Bu makalede, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır. Ambar zorunlu bir boyuttur.

Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir. Bu ayar değiştirilemez.
-   Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.
-   Tesis boyutu tedarik planlama için ayarlanmıştır. Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir. Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.
-   Ambar boyutu tedarik planlama için ayarlanmamıştır. Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.

Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir. Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:
-   Madde karşılama, madde için tanımlanmıştır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.
-   Stok yenileme ilişkileri ambar için tanımlanmıştır. Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**. **Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.
-   Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın. **Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.

![Tesis kapsamı talebi ambar zorunlu.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Ek kaynaklar

- [Master planlama ve birden çok tesis işlevine genel bakış](master-plan-multisite-functionality.md)
- [Tesis ve ambar kapsamı için master planlama, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Tesis kapsamı için master planlama, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)
- [Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Ürün reçetesi sürümünü belirleme](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]