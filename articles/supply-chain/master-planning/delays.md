---
title: Gecikmeler
description: Bu konu, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/20/2019
ms.locfileid: "878322"
---
# <a name="delays"></a>Gecikmeler

[!include [banner](../includes/banner.md)]

Bu konu, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.

Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir. 

Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez. Bu nedenle, sipariş gecikir. Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir.. Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar. Sipariş daha sonra bir gecikme tarihi alır. Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir. Master planlama ayrıca gecikme gün sayısını da hesaplar. 

Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz. 

Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz. Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz. 

**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz. Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir. 

> [!NOT}: Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken işlem *ileriye ayarlanmış bir işlem* olarak geçiyordu.

## <a name="desired-date"></a>İstenen tarih

**Planlanan siparişler** sayfasında, planlanan sipariş için **Gecikmeler** sekmesi, **İstenilen tarihtir**. Planlanan siparişin istenilen tarihi, **Net Gereksinim**'den hesaplanan **Talep edilen tarih**'e eşit olan gecikmeler için temel tarihtir. Planlanan sipariş bir BOM satırı, üretim satırı veya kanban satırıysa, istenilen tarih **Gereksinim tarihi** üzerine dayanır ve istenilen tarih **Planlanan sipariş** sayfasında görüntülenmez.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Kapsam ayarları](coverage-settings.md)
