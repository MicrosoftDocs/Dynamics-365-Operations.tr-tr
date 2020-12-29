---
title: Üretilen maddeler için sabit maliyetlerin itfası
description: Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 298b5cbbf955527edb399eae78a1c8e60a8b9ce3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439505"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Üretilen maddeler için sabit maliyetlerin itfası

[!include [banner](../includes/banner.md)]

Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır. 

Lot büyüklüğünü maliyetlendirme kavramı, bu sabit maliyetleri üretilen maddenin hesaplanan maliyetinde itfa etmek için kullanılır. Bu kavram muhasebe lot boyutunun da aralarında bulunduğu birkaç eş anlamlı sözcüğe sahiptir. Benzer şekilde, sabit maliyetlerin itfası kavramının da, orantılı sabit maliyetlerin de aralarında bulunduğu çeşitli eş anlamlı sözcükleri vardır.

Üretin bir madde için bir maliyetlendirme lotunun miktarı, bir ürün reçetesi (BOM) hesaplamasında kullanılır. Miktar, aşağıdaki şekilde gösterildiği gibi, ürün reçetesini nasıl başlattığınıza ve gerçekleştirdiğinize bağlıdır:

-   Maddenin ürün reçetesi hesaplamasındaki varsayılan hesaplama miktarı − Maddenin standart stok için sipariş miktarı, lot büyüklüğü maliyetlendirmesi için varsayılan olarak davranır, ancak varsayılan değer maddenin çoklu sipariş miktarını yansıtan miktardan büyük olabilir. Maddenin standart ve çoklu sipariş miktarı varsayılan sipariş ayarlarında veya tesise özgü sipariş ayarlarında tanımlanabilir.
-   Maddenin ürün reçetesi hesaplamasında belirtilen hesaplama miktarı − Belirtilen hesaplama miktarı maddenin lot büyüklüğü maliyetlendirmesi gibi davranır. Hesaplama miktarı başlangıçta maddenin standart sipariş miktarını kullanır, ancak varsayılan değer istenildiğinde el ile değiştirilebilir. Belirtilen hesaplama miktarı, belirli bir madde için maliyetlendirme lot boyutunu temsil eder ve ürün reçetesi hattı üretim türüne sahip üretilen bileşenler için. Bunun sebebi, bileşenin tam miktarda üretilecek olduğunun varsayılmasıdır. Üretilen diğer bileşenlere yönelik lot büyüklüğü maliyetlendirmesi maddenin BOM satır tipine sahip, her birinin standart sipariş miktarını yansıtır.
-   Maddenin ürün reçetesi hesaplamasında belirtilen siparişe göre üretim hesaplaması miktarı − Belirtilen hesaplama miktarı, ürün reçetesi hesaplamalarında siparişe göre üretim açılımı modu kullanıldığında madde ve maddenin üretilen bileşenleri için lot büyüklüğü hesaplaması gibi davranır. Üretilen bileşenlerin, üretime yönelik ürün reçetesi satır tipiyle üretilen bileşende olduğu gibi, tam miktarda üretileceği varsayılır.
-   Siparişe özel ürün reçetesi hesaplamasında belirtilen hesaplama miktarı − Siparişe özel ürün reçetesi hesaplaması, satış siparişi, satış teklifi veya servis siparişindeki bir satır maddesi için gerçekleştirilebilir. Belirtilen hesaplama miktarı, kaynak satır maddesindeki miktarı kullanır, ancak varsayılan miktar geçersiz kılınabilir. Siparişe özel ürün reçetesi hesaplamasının siparişe göre üretim mi, yoksa çok düzeyli açılım modu mu kullanacağı seçilebilir.

Üretilen maddenin hesaplanan miktarının itfa edilen sabit maliyetleri, belirlenmiş giderlere tabidir.





