---
title: Gecikmeler
description: "Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 84682e08da6da8928004c7971cd2c2a3725446c0
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="delays"></a>Gecikmeler

[!include[banner](../includes/banner.md)]


Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.

Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir. 

Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez. Bu nedenle, sipariş gecikir. Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir.. Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar. Sipariş daha sonra bir gecikme tarihi alır. Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir. Master planlama ayrıca gecikme gün sayısını da hesaplar. 

Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz. 

Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz. Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz. 

**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz. Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir. 

**Not:** Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken işlem *ileriye ayarlanmış bir işlem* olarak geçiyordu.

<a name="see-also"></a>Ayrıca bkz.
--------

[Kapsam ayarları](coverage-settings.md)




