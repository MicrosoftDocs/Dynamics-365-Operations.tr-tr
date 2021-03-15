---
title: Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil
description: Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunlu değildir.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd3614e52da72e32e6781bc8da7c9e2b3162832
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970418"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil

[!include [banner](../includes/banner.md)]

Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunlu değildir.

Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir. Bu ayar değiştirilemez.
-   Ambar boyutu zorunluya göre ayarlanmamıştır. Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.
-   Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır. Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir. Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.

Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir. Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:
-   Ambar El ile olarak ayarlanmıştır. Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**. **Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.
-   Madde karşılama, madde için tanımlanmıştır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve sonra Eylem Bölmesi'ndeki **Plan** sekmesinde, **Madde kapsamı** seçeneğini tıklatın.
-   Stok yenileme ilişkileri ambar için tanımlanmıştır. Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**. **Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.
-   Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve sonra Eylem Bölmesi'ndeki **Plan** sekmesinde, **Varsayılan sipariş ayarları** seçeneğini tıklatın. **Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.

![Tesis ve ambar talebi, ambar zorunlu değil](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>Ek kaynaklar
--------

[Master planlama ve birden çok tesis işlevine genel bakış](master-plan-multisite-functionality.md)

[Tesis kapsamı için master planlama, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Tesis ve ambar kapsamı için master planlama, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil](master-plan-site-coverage-warehouse-not-mandatory.md)

[Ürün reçetesi sürümünü belirleme](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]