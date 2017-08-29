---
title: "Sağdan sola doğru okunan dilde mali boyutlar ve ana hesaplar"
description: "Bu konu, sağdan sola doğru okunan bir dil kullandığınızda ve finansal boyutlar ve ana hesaplar ayarlamanız gerektiğinde değerlendirmeniz gereken bazı uygulama kararlarını açıklar."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: e28d3b318c2efa0b9d0da1154692f8e64c553e64
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Sağdan sola doğru okunan dilde mali boyutlar ve ana hesaplar

[!include[banner](../includes/banner.md)]


Bu konu, sağdan sola doğru okunan bir dil kullandığınızda ve finansal boyutlar ve ana hesaplar ayarlamanız gerektiğinde değerlendirmeniz gereken bazı uygulama kararlarını açıklar.

Mali boyutları ve ana hesaplar bir uygulama için planlama aşamasının anahtar bileşenleridir. Mali boyutlar ve ana hesaplar sistemde oluşturulduktan sonra **Hesap yapıları yapılandır**, **Gelişmiş kural yapıları** ve **Uygulamaları tümleştirmek için mali boyut yapılandırması** sayfalarında kullanılır. Bu sayfalarda tanımlanan sıra, sistemde veri girişi ve tüketim için kullanılır. Sistemdeki bazı yerlerde mali boyutlar ve ana hesaplar ayrı alanlarda görünür. Ancak, günlükler gibi diğer yerlerde mali boyutlar ve ana hesaplar tek bir dize olarak görünür.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Sağdan sola doğru okunan bir sistemde mali boyutları ve ana hesapları ayarlamanın en iyi yöntemleri

-   Hesap planları için ayraç seçtiğinizde çift ayraç seçeneklerinden birini belirleyin: çift tire (--), çift çubuk (||) veya çift nokta (..) veya çift alt çizgi (\_\_).
-   Mali boyut ve ana hesap değerleri oluşturduğunuzda yalnızca sayıları ve sağdan sola dil karakterlerini kullanın.
-   Seçili hesap planı ayracını mali boyut ve ana hesap değerlerinde kullanmaktan kaçının.

Bu en iyi yöntemleri izleyerek sistemde kullanıcı tanımlı sıranın tutarlı gösterimini garanti altına almaya yardımcı olursunuz.




