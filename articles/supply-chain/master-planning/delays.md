---
title: Gecikmeler
description: Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.
author: t-benebo
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bda8d9fcf42727a1ef530dee5f58dbaf18d5022
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882561"
---
# <a name="delays"></a>Gecikmeler

[!include [banner](../includes/banner.md)]

Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.

Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir. 

Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez. Bu nedenle, sipariş gecikir. Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir.. Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar. Sipariş daha sonra bir gecikme tarihi alır. Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir. Master planlama ayrıca gecikme gün sayısını da hesaplar. 

Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz. 

Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz. Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz. 

**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz. Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir. 

> [!NOTE]
> Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken hareket *ileriye ayarlanmış bir hareket* olarak geçiyordu.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Birden çok ürün reçetesi düzeyi olan üretim kurulumunda sınırlı gecikmeler
Birden çok ürün reçetesi düzeyi olan bir üretim kurulumunda gecikmeler ile çalıştığınızda, yalnızca gecikmeye neden olan maddenin doğrudan üstündeki maddelerin (ürün reçetesi yapısında), master planlama çalıştırmasının bir parçası olarak güncelleştirileceği unutulmamalıdır. En üst düzey için planlanan sipariş onaylandığında veya kesinleştirildiğinde, ürün reçetesi yapısındaki diğer maddeler, ilk master planlama çalıştırılıncaya kadar uygulanan gecikmeyi alamaz. 

Bu bilinen sınırlamaya geçici bir çözüm bulmak için, ürün reçetesi yapısının üst kısmındaki üretim emirleri bir sonraki master planlama çalıştırılmadan önce onaylanabilir (veya kesinleştirilebilir). Bu şekilde, ertelenen onaylanmış planlı üretim emrinden gelen gecikme korunur ve tüm alt bileşenler de buna göre güncelleştirilir.
Eylem iletileri, ürün reçetesi yapısındaki başka gecikmelerden dolayı sonraki bir tarihe taşınabilecek planlı siparişleri tanımlamak için de kullanılabilir.

## <a name="desired-date"></a>İstenen tarih

**Planlanan siparişler** sayfasında, planlanan sipariş için **Gecikmeler** sekmesi, **İstenilen tarihtir**. Planlanan siparişin istenilen tarihi, **Net Gereksinim**'den hesaplanan **Talep edilen tarih**'e eşit olan gecikmeler için temel tarihtir. Planlanan sipariş bir BOM satırı, üretim satırı veya kanban satırıysa, istenilen tarih **Gereksinim tarihi** üzerine dayanır ve istenilen tarih **Planlanan sipariş** sayfasında görüntülenmez.

## <a name="additional-resources"></a>Ek kaynaklar

[Kapsam ayarları](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]