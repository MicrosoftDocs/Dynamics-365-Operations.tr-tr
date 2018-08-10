---
title: Gecikmeler
description: "Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a>Gecikmeler

[!include [banner](../includes/banner.md)]

Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.

Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir. 

Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez. Bu nedenle, sipariş gecikir. Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir.. Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar. Sipariş daha sonra bir gecikme tarihi alır. Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir. Master planlama ayrıca gecikme gün sayısını da hesaplar. 

Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz. 

Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz. Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz. 

**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz. Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir. 

**Not:** Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken işlem *ileriye ayarlanmış bir işlem* olarak geçiyordu.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Kapsam ayarları](coverage-settings.md)




