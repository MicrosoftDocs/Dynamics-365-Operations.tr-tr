---
title: "Stok konumları"
description: "Stok konumları ile temel depolama (WSM I) birlikte kullanılarak maddelerin nerede depolandıkları ve maddelerin bir WMS I ambarında nereden çekildikleri belirlenir."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 95d93c9d471cc86877f35340693c171958db71df
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="inventory-locations"></a>Stok konumları

[!include[banner](../includes/banner.md)]


Stok konumları ile temel depolama (WSM I) birlikte kullanılarak maddelerin nerede depolandıkları ve maddelerin bir WMS I ambarında nereden çekildikleri belirlenir.

Bu konu, Stok yönetimi modülündeki özellikler için geçerlidir. Ambar yönetimi modülündeki özellikler için geçerli değildir.

Konum terimi, maddelerin depolandığı ve çekildiği yeri ifade eder.

Her yerleşim için, maddenin yerleştirildiği yer de belirtilebilir. Varsayılan olarak bunlar aynıdır. Maddeler genellikle bir yerleşimin aynı yönünden çekilir veya yerleştirilirler ancak her zaman durum böyle olmaz. Örneğin aktif depoların raflarında saklanan maddeler bir koridordan yerleştirilir ve diğer koridordan çekilir. Ana giriş genellikle koordinatları ile belirlenen bir konum adı tarafından verilir: ambar, koridor, dolap, raf ve depo gözü. Bu isim veya kimlik el ile girilebilir veya konum koordinatlarından üretilebilir—örneğin, Stok konumları sayfasındaki koridor 1, dolap 2, raf 3, bölme 4 için 01-02-03-4.
Yerleşim özellikleri

Bir yerleşim aşağıdaki özelliklere sahiptir:
-   Boyut (yükseklik, genişlik, derinlik ve dolayısıyla hacim)
-   Ambar, koridor, dolap, raf ve bölme pozisyonu
-   Konum türü (toplu yerleşim, malzeme çekme konumu, giriş noktası, çıkış noktası, üretim giriş konumu, inceleme konumu veya kanban süpermarketi)

Çevrimiçi sistemlerde operatörün belirli bir madde için doğru yerleşimi seçtiğini doğrulamak için bir denetim metni kullanılabilir. Bu denetim metni el ile veya varsayılan olarak oluşturulabilir.

## <a name="sort-codes"></a>Sıralama kodları
Malzeme çekme hatlarını en iyi şekilde idare edebilmek için, malzeme çekme sırası da dahil olmak üzere maddelerin stoktan çekilmesi için gerekli bilgilerin detaylarını içeren sıralama kodlarını kullanın. Sıralama kodları koridor veya diğer koordinatlara göre tanımlanabilir veya yerleşim noktasına el ile atanabilir.

## <a name="blocked-locations"></a>Kullanım dışı bırakılan yerleşimler
Bazen bir yerleşimi, örneğin onarımlar için bir süre için kullanım dışı bırakmanız gerekir. Bazen de, yalnızca giriş veya çıkışı engellemek isteyebilirsiniz.

## <a name="tree-structure"></a>Ağaç yapısı

Stok konumları sayfasında, ambar düzenini ağaç yapısında stok konumlarının yapısına göre tanımlı bir görüntüleme formatında görüntüleyebilirsiniz.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Ambar formu üzerinden stok konumlarını muhafaza etme

Konumları bir ambardan diğerine kopyalamak ve sihirbaz üzerinden konum oluşturmak mümkündür. Sihirbazı çalıştırmadan önce, Ambar sayfasında varsayılan konum adlarını tanımladığınızdan emin olun.



<a name="see-also"></a>Ayrıca bkz.
--------

[Yeni bir ambar düzeni oluştur (Görev kılavuzu)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-new-warehouse-layout)

