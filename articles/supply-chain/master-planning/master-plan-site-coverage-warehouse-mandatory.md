---
title: Tesis kapsamı için master planlama, ambar zorunlu
description: Bu konuda, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır. Ambar zorunlu bir boyuttur.
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72240e7db8ec914220cb8f8f1185a91a304ff66b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977975"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Tesis kapsamı için master planlama, ambar zorunlu

[!include [banner](../includes/banner.md)]

Bu konuda, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır. Ambar zorunlu bir boyuttur.

Bu master planlama senaryosu aşağıdaki koşulları kapsar:

-   Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir. Bu ayar değiştirilemez.
-   Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.
-   Tesis boyutu tedarik planlama için ayarlanmıştır. Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir. Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.
-   Ambar boyutu tedarik planlama için ayarlanmamıştır. Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.

Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir. Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:
-   Madde karşılama, madde için tanımlanmıştır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.
-   Stok yenileme ilişkileri ambar için tanımlanmıştır. Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**. **Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.
-   Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır. **Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın. **Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.

![Tesis kapsamı talebi ambar zorunlu](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>Ek kaynaklar
--------

[Master planlama ve birden çok tesis işlevine genel bakış](master-plan-multisite-functionality.md)

[Tesis ve ambar kapsamı için master planlama, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Tesis kapsamı için master planlama, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Ürün reçetesi sürümünü belirleme](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]