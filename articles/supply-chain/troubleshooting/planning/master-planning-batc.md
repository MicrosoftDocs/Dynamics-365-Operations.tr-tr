---
title: Master planlama maddelerini ilgili karşılama grubu değerlerine göre filtreleyemiyorsunuz
description: Master planlama maddelerini ilgili karşılama grubu değerlerine göre filtreleyemiyorsunuz.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9750a73f0962179512c5e21a614a276c313ff975b7494f31589ca936886ecf6e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781405"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Master planlama maddelerini ilgili karşılama grubu değerlerine göre filtreleyemiyorsunuz

KB numarası: 4612572

## <a name="symptoms"></a>Belirtiler

Madde karşılama tablosundaki ilgili kayıtların değerlerini temel alarak, master planlama toplu işlemine dahil edilecek maddelere filtre uygulamak istiyorsunuz. (Örneğin, öğeleri **Satıcı** ve/veya **Karşılama grubu** değerlerine göre maddeleri filtrelemek istiyorsunuz). Toplu işlemin filtre kurulumu, **Maddeler** tablosundan **Madde kapsamı** tablosuna bir birleştirme oluşturmanıza ve ardından sorgunuzdaki madde karşılama tablosundan alan değerlerini belirtmenize olanak tanır. Ancak, bu kurulumu tamamladıktan sonra, sistem yalnızca madde karşılama tablosundan belirtilen alan değerleriyle eşleşen maddeler için değil, tüm madde kapsamı için planlı siparişler oluşturur.

## <a name="resolution"></a>Çözüm

Toplu işlem filtresi yalnızca maddelere filtre yapabilir. **Madde kapsama** tablosuna bir birleştirme ekleyebilmenize rağmen, bu tabloya karşı yaptığınız filtre ayarları sorgu çıktısını etkilemez. Çalışma zamanında, sistem tüm karşılama grupları ve filtre uygulanmış maddelerin sahip olduğu tüm varyasyonlar için planlama çalıştırır. Bir madde zaten çalıştırmaya dahil edildikten sonra, madde filtresine dahil edilen tüm karşılama grupları planlama çıktısını etkilemez.
