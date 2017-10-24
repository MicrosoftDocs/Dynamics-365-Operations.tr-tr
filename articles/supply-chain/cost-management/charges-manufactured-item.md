---
title: "Üretilen bir madde için giderleri görüntüleme"
description: "Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 66dbd107b47b8a064cbe2e284bcabea47c471089
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="display-charges-for-a-manufactured-item"></a>Üretilen bir madde için giderleri görüntüleme

[!include[banner](../includes/banner.md)]


Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır.

Maddenin giderlerinin hesaplanan tutarı, maddenin birim maliyeti ile görüntülenebilir. Ancak, masraflar bazen ayrı alanlar olarak görüntülenir ve maddenin birim maliyetlerine eklenmemiştir. Değişiklikler ayrı alanlar olarak görüntülendiğinde, bir alan toplam giderleri gösterir, diğer alan tutarı amorti etmekte kullanılan maliyetli lot miktarını gösterir. Örneğin, madde fiyat sayfası, giderleri iki farklı alan olarak gösterir. Ancak, Tüm sayfa, maddenin birim başına maliyetini ve birim maliyetlerine dahil edilen amorti edilmiş maliyetleri gösterir.

Üretilen bir maddeye ilişkin giderler standart maliyetler için maddenin birim maliyetine her zaman dahil edilir. Planlanan maliyetler için bu giderler isteğe bağlı olarak dahil edilebilir. Maliyet versiyonundaki bir ilke, üretilen bir maddenin maliyetine giderlerin dahil edilmesini zorunlu kılar. Bir maddenin maliyet kaydını etkinleştirdiğinizde, Madde fiyatı sayfasında görüntülenen, maddenin taban maliyet bilgileri için giderleri güncelleştirirsiniz. Giderler iki ayrı alanda gösterilir ve maddenin birim fiyatına dahil değildirler. Etkinleştirme farklı tesisleri yansıtsa da her etkinleştirme maddenin taban maliyet bilgilerini güncelleştirir. Bu nedenle, taban maliyet bilgisini bir referans bilgisi olarak görüntülemelisiniz.






