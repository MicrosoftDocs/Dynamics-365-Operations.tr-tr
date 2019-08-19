---
title: Rotalar oluşturma (Şubat 2016)
description: Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844573"
---
# <a name="create-routes-february-2016"></a>Rotalar oluşturma (Şubat 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır. Ürün reçetesi hesaplaması serisindeki beşinci görevdir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-route-for-a-semi-finished-product"></a>Yarı mamul bir ürün için rota oluşturma
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
    * BOM_2 madde numarasını seçin.  
3. Eylem Bölmesinde, Mühendis öğesine tıklayın.
4. Rota'ya tıklayın.
5. Yeni'ye tıklayın.
6. Rota ve rota sürümü'ne tıklayın.
7. Açıklama alanına bir değer girin.
    * Bu örnek için, ROUTE_2 yazın.  
8. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i girin veya seçin.  
9. Tamam'a tıklayın.
10. Yeni'ye tıklayın.
11. Operasyon alanında bir değer girin veya bir değer seçin.
    * Bu örnek için Derleme seçeneğini belirtin.  
12. Çalışma süresi alanında bir sayı girin.
    * Örneğin 1 yazın. Çalışma zamanları genellikle madde için hesaplanan fiyatın parçasıdır.  
13. Rota grubu alanında bir değer girin veya bir değer seçin.
    * Bu örnek için, Std seçeneğini belirtin.  
14. Kurulum sekmesine tıklayın.
15. Kurulum kategorisi alanında bir değer girin veya seçin.
    * Bu örnek için Derleme seçeneğini belirtin.  
16. Zaman sekmesini tıklatın.
17. Hazırlık süresi alanına bir sayı girin.
    * Bu örnek için, 1 yazın. Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.  
18. Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.
19. Onayla’yı tıklatın.
20. Rotayı da onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.
21. Tamam'a tıklayın.
22. Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.
23. Etkinleştir'i tıklatın.
24. Sayfayı kapatın.
25. Sayfayı kapatın.

## <a name="create-a-route-for-a-finished-product"></a>Tamamlanmış bir ürün için rota oluşturma
1. Listede, seçili satırdaki bağlantıya tıklayın.
    * BOM_1 madde numarasını seçin.  
2. Eylem Bölmesinde, Mühendis öğesine tıklayın.
3. Rota'ya tıklayın.
4. Yeni'ye tıklayın.
5. Rota ve rota sürümü'ne tıklayın.
6. Açıklama alanına bir değer girin.
    * Bu örnek için, ROUTE_1 yazın.  
7. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * Bu örnek için, Tesis 1'i girin veya seçin.  
8. Tamam'a tıklayın.
9. Yeni'ye tıklayın.
10. Operasyon alanında bir değer girin veya bir değer seçin.
    * Bu örnek için, Ambalaj seçeneğini belirtin.  
11. Çalışma süresi alanında bir sayı girin.
    * Bu örnek için, 1 yazın.  
12. Rota grubu alanında bir değer girin veya bir değer seçin.
    * Bu örnek için, Std seçeneğini belirtin.  
13. Kurulum sekmesine tıklayın.
14. Kurulum kategorisi alanında bir değer girin veya seçin.
    * Bu örnek için, Ambalaj seçeneğini belirtin.  
15. Zaman sekmesini tıklatın.
16. Hazırlık süresi alanına bir sayı girin.
    * Bu örnek için, 1 yazın.  
17. Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.
18. Onayla’yı tıklatın.
19. Tamam'a tıklayın.
20. Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.
21. Etkinleştir'i tıklatın.
22. Sayfayı kapatın.
23. Sayfayı kapatın.

## <a name="enable-automatic-consumption-of-setup-time"></a>Hazırlık süresinin otomatik tüketimini etkinleştirme
1. Üretim denetimi > Kurulum > Rotalar > Rota grupları öğesine gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Listede, Std seçeneğini belirtin.  
3. Düzenle öğesine tıklayın.
4. Hazırlık süresi alanında, Evet'i seçin.
    * Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.  
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.

