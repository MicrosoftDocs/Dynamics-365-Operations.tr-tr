---
title: Sağdan sola doğru okunan dillerde mali boyutlar ve ana hesaplar
description: Bu konu, sağdan sola doğru okunan bir dil kullandığınızda ve mali boyutlar ve ana hesaplar ayarlamanız gerektiğinde vermeniz gereken kararları açıklar.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 508f4ed4de367770acddc77a6ff5e7e36fd20729
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748149"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Sağdan sola doğru okunan dillerde mali boyutlar ve ana hesaplar

[!include [banner](../includes/banner.md)]

Bu konu, sağdan sola doğru okunan bir dil kullandığınızda ve finansal boyutlar ve ana hesaplar ayarlamanız gerektiğinde değerlendirmeniz gereken bazı uygulama kararlarını açıklar.

Mali boyutları ve ana hesaplar bir uygulama için planlama aşamasının anahtar bileşenleridir. Mali boyutlar ve ana hesaplar sistemde oluşturulduktan sonra **Hesap yapıları yapılandır**, **Gelişmiş kural yapıları** ve **Uygulamaları tümleştirmek için mali boyut yapılandırması** sayfalarında kullanılır. Bu sayfalarda tanımlanan sıra, sistemde veri girişi ve tüketim için kullanılır. Sistemdeki bazı yerlerde mali boyutlar ve ana hesaplar ayrı alanlarda görünür. Günlükler gibi diğer yerlerde mali boyutlar ve ana hesaplar tek bir dize olarak görünür.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Sağdan sola doğru okunan bir sistemde mali boyutları ve ana hesapları ayarlamanın en iyi yöntemleri

- Hesap planları için sınırlayıcı seçtiğinizde çift sınırlayıcı seçeneklerinden birini belirleyin: çift tire (`--`), çift çubuk (`||`), çift nokta (`..`) veya çift alt çizgi (`\\`).
- Mali boyut ve ana hesap değerleri oluşturduğunuzda yalnızca sayıları ve sağdan sola dil karakterlerini kullanın.
- Seçili hesap planı ayracını mali boyut ve ana hesap değerlerinde kullanmaktan kaçının.

Bu en iyi yöntemleri izleyerek sistemde kullanıcı tanımlı sıranın tutarlı gösterimini garanti altına almaya yardımcı olursunuz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]