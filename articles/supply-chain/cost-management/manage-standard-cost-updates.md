---
title: Maliyet güncelleştirmelerini yönetme
description: Standart maliyet verilerindeki güncelleştirmeler iki farklı yaklaşımla yönetilebilir - tek sürümlü yaklaşım ve iki sürümlü yaklaşım.
author: AndersGirke
manager: tfehr
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7beeafa6d0bb22a687278ccebc3127409e1ee0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439351"
---
# <a name="manage-standard-cost-updates"></a>Maliyet güncelleştirmelerini yönetme

[!include [banner](../includes/banner.md)]

Standart maliyet verilerindeki güncelleştirmeler iki farklı yaklaşımla yönetilebilir - tek sürümlü yaklaşım ve iki sürümlü yaklaşım. 

Tek sürümlü yaklaşım, tüm maliyet kayıtlarını içeren tek bir maliyetlendirme sürümünü kullanır. Bu kayıtlar orijinal maliyetleri ve tüm maliyet güncelleştirmelerini içerir.

İki sürümlü yaklaşım, orijinal maliyetlerin kayıtlarını içeren bir sürümü ve tüm maliyet güncelleştirmelerini içeren ikinci bir sürümü kullanır. İki versiyonlu yaklaşımın birincil avantajı, maliyet güncelleştirmelerinin, orijinal maliyetlendirme versiyonunu etkilemeden ayrı bir maliyetlendirme versiyonunda net bir şekilde açıklanması ve izlenmesidir. İki sürümlü yaklaşım, her artımlı güncelleştirmenin artımlı maliyet kayıtlarını içeren ayrı bir maliyetlendirme sürümünün bulunduğu birden fazla artımlı güncelleştirmeyi belirlemek için kullanılabilir. 

**Örnek** 

Aşağıdaki örnekte, bir üretim ortamında standart maliyetleri güncelleştirmek için bir sürümlü ve sürümlü yaklaşımların nasıl kullanılabileceği gösterilmiştir. Örneğin, yeni maddeleri veya hata düzeltmelerini gösteren güncelleştirmeler. Tek maliyetlendirme sürümünün geçerli yıl için standart maliyetleri temsil ettiğini varsayalım. Bu sürüm için tanımlayıcı 2016-STD'dir. Sürüm 2016-STD tüm maddeler için geçerli etkin maliyetleri içerir. Ek olarak, 2016 yılının başında bilinen rota ile ilgili maliyet kategorileri ve gider hesaplama formüllerini içerir. 2016-STD, özgün maliyet sürümüdür.

-   **Maliyet verileri güncelleştirmeleri için tek sürümlü yaklaşım** - Tek sürümlü yaklaşımda, orijinal 2016-STD maliyetlendirme sürümü tüm maliyet kayıtlarını içerir. Maliyet güncelleştirmeleri 2016-STD içerisinde kaydedilir ve "Beklemede" durumuna ayarlanır Bekleyen maliyetler yeni satın alınan maddeler için el ile girilmiş olabilir veya düzeltmeleri yansıtmak için üretilmiş bir madde için hesaplanmış olabilir. Tek versiyonlu yaklaşım kullanıldığında ürün reçetesi hesaplamaları, tüm etkin maliyetler maliyetlendirme versiyonunda yer aldığından geri dönüş veri kaynağı gerektirmez. Beklemede olan maliyetler etkin duruma geldiğinde, 2016-STD orijinal maliyetlendirme sürümü yeniden tüm geçerli etkin maliyetleri kapsar.
-   **Maliyet verileri güncelleştirmeleri için iki sürümlü yaklaşım** − İki sürümlü yaklaşım, yalnızca maliyet güncelleştirmelerini içeren ek bir maliyetlendirme sürümü gerektirir. Bu sürüm için tanımlayıcı 2016-STD-CHANGES'dir. Maliyet güncelleştirmeleri 2016-STD-CHANGES içerisinde kaydedilir ve "Beklemede" durumuna ayarlanır. İki sürümlü yaklaşımda, üretilen maddeler için bekleyen maliyetlerin ürün reçetesi hesaplamaları bir geri dönüş veri kaynağı gerektirir. Bunun nedeni, ek maliyetlendirme sürümü olan 2016-STD-CHANGES'ın yalnızva bir maliyet verisi alt grubu içermesidir. Her ikisi de 2016-STD-CHANGES içinde yer almayan maliyet verilerinin kaynağını tanımladığından, geri dönüş etkin maliyetler veya maliyetlendirme versiyonu 2016-STD olarak ifade edilir. Bekleyen maliyetler etkinleştirildikten sonra, maliyetlendirme versiyonu 2016-STD-CHANGES güncelleştirmeleri yansıtan geçerli etkin maliyetleri içerirken, orijinal maliyetlendirme versiyonu 2016-STD'ye dokunulmaz. İki versiyonlu yaklaşım kullanıldığında, orijinal maliyetlendirme sürümü için durdurma ilkelerinin güncelleştirmeleri önleyecek şekilde ayarlanması gerekir. Belirtilen başlangıç tarihi ve güncelleştirmelere izin vermek için durdurma ilkelerinin seçimli kullanımı dışında, ek maliyetlendirme sürümü için aynı ilkeler ayarlanmalıdır. Belirtilen başlangıç tarihi, planlanan etkinleştirme tarihini yansıtmak için her toplu değişiklikle güncelleştirilmelidir.

Bu örnekte 2016 yılı boyunca güncelleştirmeleri yönetmek için bir ek maliyetlendirme versiyonu kullanılmıştır. Her toplu güncelleştirme için ayrı bir versiyon gibi birden fazla ek maliyetlendirme versiyonu da kullanılabilirdi. Birden fazla maliyetlendirme kullanıldığında, etkin maliyetler birden fazla maliyetlendirme sürümüne dağıtılacağından geri dönüşün etkin maliyetler şeklinde ifade edilmesi gerekir.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]