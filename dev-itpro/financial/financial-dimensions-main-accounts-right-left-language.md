---
title: "Sağdan sola doğru okunan dilde mali boyutlar ve ana hesaplar"
description: "Bu konu, Microsoft Dynamics 365 for Operations uygulamasında sağdan sola doğru okunan bir dil kullandığınızda değerlendirmeniz gereken bazı uygulama kararlarını açıklar."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0a2fcbbc91960e0602f42d89ca5e46b8d51f98d6
ms.openlocfilehash: da5c53ddf113daf19a9832cf59f7a231a00b3367
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Sağdan sola doğru okunan dilde mali boyutlar ve ana hesaplar

Bu konu, Microsoft Dynamics 365 for Operations uygulamasında sağdan sola doğru okunan bir dil kullandığınızda değerlendirmeniz gereken bazı uygulama kararlarını açıklar.

Mali boyutları ve ana hesaplar bir uygulama için planlama aşamasının anahtar bileşenleridir. Mali boyutlar ve ana hesaplar sistemde oluşturulduktan sonra **Hesap yapıları yapılandır**, **Gelişmiş kural yapıları** ve **Uygulamaları tümleştirmek için mali boyut yapılandırması** sayfalarında kullanılır. Bu sayfalarda tanımlanan sıra, sistemde veri girişi ve tüketim için kullanılır. Sistemdeki bazı yerlerde mali boyutlar ve ana hesaplar ayrı alanlarda görünür. Ancak, günlükler gibi diğer yerlerde mali boyutlar ve ana hesaplar tek bir dize olarak görünür.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Sağdan sola doğru okunan bir sistemde mali boyutları ve ana hesapları ayarlamanın en iyi yöntemleri

-   Hesap için ayırıcı seçtiğinizde, ayırıcı çift seçeneklerden birini seçin: çift tire (-), çift çubuk (|) veya çift nokta (.) veya çift alt çizgi (\_\_).
-   Mali boyut ve ana hesap değerleri oluşturduğunuzda yalnızca sayıları ve sağdan sola dil karakterlerini kullanın.
-   Seçili hesap planı ayracını mali boyut ve ana hesap değerlerinde kullanmaktan kaçının.

Bu en iyi yöntemleri izleyerek sistemde kullanıcı tanımlı sıranın tutarlı gösterimini garanti altına almaya yardımcı olursunuz.


