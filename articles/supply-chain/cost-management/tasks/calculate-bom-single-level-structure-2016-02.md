--- 
title: "Tek düzeyli yapı kullanarak ürün reçetesini hesaplama (yalnızca Şubat 2016)"
description: "Bu yordam, Maliyetlendirme tablosunu temel alan, tek düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e6829238b244cc01b070fde6acdf37bdaeb9670
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>Tek düzeyli yapı kullanarak ürün reçetesini hesaplama (yalnızca Şubat 2016)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, Maliyetlendirme tablosunu temel alan, tek düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir. Bu, Ürün reçetesi hesaplaması serisindeki altıncı görevdir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.

1. Serbest bırakılan ürünler öğesine gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Ürün BOM_1 öğesini seçin.  
3. Eylem Bölmesinde Yönet'e tıklayın.
4. Madde fiyatı'na tıklayın.
5. Madde maliyetini hesapla'ya tıklayın.
    * Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.  
6. Maliyetlendirme sürümü alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bu tanıtım için, 10'u seçin. Bu, bileşenlere maliyet fiyatını eklemek için kullanılan aynı maliyetlendirme sürümüdür.  
7. Tamam'a tıklayın.
8. Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.
    * Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.    Maliyetin bileşimi buradadır:  •    10 ITEM_A'dan, 10 ITEM_B'den ve 10 BOM_2'den türetilir. Bu durumda, BOM_2 için ayrıntı bulunmamaktadır çünkü 10'un standart maliyeti olarak girilmiş ve hesaplama sonunda yapılmamıştır.  •  Hazırlık süresinden, sabit bir maliyet olan 7 ve çalışma zamanı işleminden (İşlem) ek olarak 7 türetilmiştir.  •   Dolaylı maliyetlere karşılık gelen başka tutarlar da vardır.  
9. @SysTaskRecorder:_RequestClose


