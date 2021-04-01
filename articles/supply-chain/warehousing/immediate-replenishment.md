---
title: Anlık stok yenileme
description: Bu konu, bir yerleşim yönergesi stok tahsis etmek için başarısız olduğunda stok yenileme için anlık stok yenilemeyi nasıl kullanabileceğinizi açıklar.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 3def95ac272a424591ed4382d5cd5841bc663654
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235400"
---
# <a name="immediate-replenishment"></a>Anlık stok yenileme

[!include [banner](../includes/banner.md)]

Anlık stok yenileme bir yerleşim yönergesi satırı stok tahsis etmek için başarısız olduktan hemen sonra stoğu yenilemenize olanak tanır. Stok yenileme yerleşim yönergesi kurulumundaki tek bir satırı temel alır. Stok bu satır tarafından belirtilen ölçü biriminde elde yoksa, bu ölçü birimi için stok yenileme anında gerçekleştirilir.

Anlık stok yenileme, stok tahsisatının yerleşim yönergesinde birçok satırı temel aldığı ve talebin tahsisat sonunda toplanıp yerleşim yönergesinin son satırı tarafından belirtilen ölçüm biriminde yenilendiği yönteme bir alternatif sağlar.

Anlık stok yenileme kullanmanın avantajları stok yenilemenin belirli birimlere göre sınırlandırılabilmesi be miktarın belirli yerleşimlere yönlendirilebilmesidir.

## <a name="business-scenario"></a>İş senaryosu

Örneğin, "kutu" ve "her" ölçüm birimi için ayrı malzeme çekme alanlarına sahip bir ambarınız bulunuyor olsun. Mümkün olduğu kadar çok kutu çekerek malzeme çekme sürecini en iyi duruma getirmek ve bir kutudan az olan kalan miktarı "her" alanından çekmek istiyorsunuz.

Bu durumda, anında stok yenileme kullanabilirsiniz. Yerleşim yönergesinde, kutular için anlık stok yenileme ayarlayarak talep stok yenilemesinin talep miktarı için çekilebilecek kutular eksik olduğunda kullanılmasını sağlayabilirsiniz. Bu şekilde, malzeme çekme işlemini en iyi duruma getirerek çekme işleminin mümkün olduğunca çok kutuyu içermesini sağlarsınız. Anlık stok yenileme kutular için stok yenileme oluşturur ve talep geçilmez, böylece miktarlar "her" ölçü biriminde çekilir. Başka bir deyişle, "her" ölçü birimiyle (diğer bir deyişle, bir kutudan az olan miktarlar) çekilmesi gereken miktarlar "her" alanından çekilir. "Kutu" alanında bir yetersizlik oluşursa, toplam talep dışında olabildiğince çok kutu çekebilirsiniz. Kalan miktarlar daha sonra "her" alanından çekilir.

## <a name="where-it-applies"></a>Uygulandığı yerler

Anında stok yenileme, stok yenileme şablonunun ayarlandığı bir yerleşim yönergesi satırı için tahsisatın başarısız olması durumunda dalga yürütme sırasında kullanılır.

## <a name="set-up-immediate-replenishment"></a>Anlık stok yenileme ayarlama

- **Ambar yönetimi** \> **Kurulum** \> **Yerleşim yönergeleri**'ne gidin ve **Satırlar** sekmesinde **Anlık stok yenileme şablonu** listesinde dalga talebi için bir stok yenileme şablonu seçin.

Stok yenileme şablonu, yerleşim yönergesi satırı özel bir ölçüm birimi tahsis etmede başarısız olursa kullanılır.

## <a name="troubleshooting"></a>Sorun giderme

Bir yerleşim yönergesi satırı için anlık stok yenileme seçilir ancak bu yerleşim yönergesi satırı için talep stok yenileme şablonları kullandığınızda stok yenileme işi oluşturulmazsa, iki ana nedenin araştırılması gerekir:

- Uygulanan talep stok yenileme şablonunun doğru yerleşim şablonlarıyla ve **Stok yenileme** türünde iş şablonları ile kullanılmak üzere ayarlandığından emin olun.
- Talep stok yenileme şablonunun stok yenileme için eldeki stoğu aradığı yerleşimlerde yeterli eldeki stok bulunduğundan emin olun.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]