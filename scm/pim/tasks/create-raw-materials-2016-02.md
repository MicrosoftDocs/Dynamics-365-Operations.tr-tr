--- 
title: "Hammadde oluşturma (yalnızca Şubat 2016)"
description: "Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: a20a2c720af7c981cced231c0f863a1bd8283f2c
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="create-raw-materials-february-2016-only"></a>Hammadde oluşturma (yalnızca Şubat 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır. Ürün Reçetesi hesaplama serisindeki üçüncü görevdir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-the-first-material"></a>İlk malzemeyi oluşturma
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Ürün numarası alanında bir değer girin.
    * Bu örnek için, ITEM_A girin.  
4. Model grubu alanına bir değer girin veya bir değer seçin.
    * STD öğesini seçin. STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.  
5. Ürün grubu alanında bir değer girin veya bir değer seçin.
    * Örneğin, Ses'i seçin. Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.  
6. Stok boyutu grubu alanına bir değer girin veya bir değer seçin.
    * SiteWH'yi seçin. Tanıtım için yalnızca Tesis ve Ambar kullanılır.  
7. İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.
    * Bu örnek için izleme boyutları kullanılmaz. Hiçbiri'ni seçin.  
8. Tamam'a tıklayın.
9. Eylem Bölmesinde, Stok yönetimi'ne tıklayın.
10. Varsayılan sipariş ayarlarına tıklayın.
11. Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
12. Stok tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
13. Satış tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
14. Sayfayı kapatın.
15. Sayfayı kapatın.
16. Listede, seçili satırdaki bağlantıya tıklayın.
    * ITEM_A öğesine tıklayın.  
17. Maliyetleri yönet bölümünü genişletin.
18. Maliyet grubu alanına bir değer girin.
    * Bu örnek için M2 yazın.  
19. Eylem Bölmesinde Yönet'e tıklayın.
20. Madde fiyatı'na tıklayın.
21. Yeni'ye tıklayın.
22. Sürüm alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Standart maliyet maliyetlendirme türü olan 10'u seçin.  
23. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
24. Fiyat alanına bir sayı girin.
    * Bu örnek için, 10 yazın.  
25. Kaydet'e tıklayın.
26. Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.
27. Sayfayı kapatın.
28. Sayfayı kapatın.

## <a name="create-the-second-material"></a>İkinci malzemeyi oluşturma
1. Yeni'ye tıklayın.
2. Ürün numarası alanında bir değer girin.
    * Bu örnek için, ITEM_B yazın.  
3. Model grubu alanına bir değer girin veya bir değer seçin.
    * STD öğesini seçin. STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.  
4. Ürün grubu alanında bir değer girin veya bir değer seçin.
    * Örneğin, Ses'i seçin. Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.  
5. Stok boyutu grubu alanına bir değer girin veya bir değer seçin.
    * SiteWH'yi seçin. Bu örnek için yalnızca Tesis ve Ambar kullanılır.  
6. İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.
    * Bu örnek için izleme boyutları kullanılmaz. Hiçbiri'ni seçin.  
7. Tamam'a tıklayın.
8. Eylem Bölmesinde, Stok yönetimi'ne tıklayın.
9. Varsayılan sipariş ayarlarına tıklayın.
10. Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
11. Stok tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
12. Satış tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
13. Sayfayı kapatın.
14. Sayfayı kapatın.
15. Listede, seçili satırdaki bağlantıya tıklayın.
    * ITEM_B öğesine tıklayın.  
16. Maliyetleri yönet bölümünü genişletin.
17. Maliyet grubu alanına bir değer girin.
    * Bu örnek için M2 yazın.  
18. Eylem Bölmesinde Yönet'e tıklayın.
19. Madde fiyatı'na tıklayın.
20. Yeni'ye tıklayın.
21. Sürüm alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, 10'u seçin. Bu, Standart maliyet maliyetlendirme türüdür.  
22. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
23. Fiyat alanına bir sayı girin.
    * Tanıtım için, 10 yazın.  
24. Kaydet'e tıklayın.
25. Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.
26. Sayfayı kapatın.
27. Sayfayı kapatın.

## <a name="create-the-third-material"></a>Üçüncü malzemeyi oluşturma
1. Yeni'ye tıklayın.
2. Ürün numarası alanında bir değer girin.
    * Tanıtım için, ITEM_C yazın.  
3. Model grubu alanına bir değer girin veya bir değer seçin.
    * STD öğesini seçin. STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.  
4. Ürün grubu alanında bir değer girin veya bir değer seçin.
    * Örneğin, Ses'i seçin. Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.  
5. Stok boyutu grubu alanına bir değer girin veya bir değer seçin.
    * SiteWH'yi seçin. Tanıtım için yalnızca Tesis ve Ambar kullanılır.  
6. İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.
    * Bu örnek için izleme boyutları kullanılmaz. Hiçbiri'ni seçin.  
7. Tamam'a tıklayın.
8. Eylem Bölmesinde, Stok yönetimi'ne tıklayın.
9. Varsayılan sipariş ayarlarına tıklayın.
10. Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
11. Stok tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
12. Satış tesisi alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
13. Sayfayı kapatın.
14. Sayfayı kapatın.
15. Listede, seçili satırdaki bağlantıya tıklayın.
    * ITEM_C öğesine tıklayın.  
16. Maliyetleri yönet bölümünü genişletin.
17. Maliyet grubu alanına bir değer girin.
    * Bu örnek için M1 yazın.  
18. Eylem Bölmesinde Yönet'e tıklayın.
19. Madde fiyatı'na tıklayın.
20. Yeni'ye tıklayın.
21. Sürüm alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, 10'u seçin. Bu, Standart maliyet maliyetlendirme türüdür.  
22. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i seçin.  
23. Fiyat alanına bir sayı girin.
    * Bu örnek için, 10 yazın.  
24. Kaydet'e tıklayın.
25. Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.
26. Sayfayı kapatın.
27. Sayfayı kapatın.


