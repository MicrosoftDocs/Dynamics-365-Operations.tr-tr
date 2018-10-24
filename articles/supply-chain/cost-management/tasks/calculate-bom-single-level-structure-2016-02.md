--- 
title: "Tek düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)"
description: "Bu yordam, Maliyetlendirme tablosunu temel alan, tek düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f74f8e4efc4474693f0a5b543c1300c3b64ecda0
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Tek düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


