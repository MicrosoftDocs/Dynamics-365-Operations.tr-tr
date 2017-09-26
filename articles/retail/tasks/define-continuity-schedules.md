--- 
title: " Süreklilik zamanlamaları tanımlama"
description: "Bu konu süreklilik programının ayarlanmasını gösterir (aksi takdirde tekrarlanan siparişler olarak bilinir)."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f51cb4fc093db60f03bbe6d2133f61ef90046155
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="define-continuity-schedules"></a> Süreklilik zamanlamaları tanımlama

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu konu süreklilik programının ayarlanmasını gösterir (aksi takdirde tekrarlanan siparişler olarak bilinir). Bu konu, demo verilerinde USRT şirketini kullanır.


## <a name="create-continuity-program"></a>Süreklilik programı oluşturma
1. Perakende ve ticaret > Süreklilik > Süreklilik programları'na gidin.
2. Yeni'ye tıklayın.
3. Planlama kodu alanına süreklilik planı kodunu yazın.
4. Sipariş başlangıç alanında 'İlk olay'ı seçin.
    * Bir müşteri süreklilik programı için yeni bir sipariş verirse, ürünü nakliye edileceği iki yol vardır:  1. İlk olay: süreklilik programındaki ilk ürün sevk edilir.  2. Geçerli olay: Geçerli ürün sevk edilir. Örneğin, programdaki üç ay içinde müşteri programdaki üçüncüyü alır.  
5. Sipariş başlangıç tarihi komutu için Evet'i seçin.
6. Satır ekle'ye tıklayın.
7. Madde numarası alanında ilk ürün için madde numarasını ('0013') girin.
8. "CP" yazın.
9. İlk ürünün sipariş için kullanılabilir olacağı tarihi girin.
10. Satır ekle'ye tıklayın.
11. Madde numarası alanına '0014' yazın.
12. Tarih aralık kodu alanında değeri temizleyerek alanı boşaltın.
    * Bu yordam için tarih aralığını temizleyin. Tarihi ilk öğenin başlangıç tarihinden artırımlı olarak ayarlayın.  
13. Buraya ürünlerin sevk edildiği aralığı girin. "30" yazın.
    * Aylık program için aralık olarak 30 gün girin.  
14. Satır ekle'ye tıklayın.
15. Madde numarası alanına '0015' yazın.
16. "Son" yazın.
17. Kaydet'e tıklayın.

## <a name="assign-to-continuity-item"></a>Süreklilik maddesine atama
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. '0016' maddesini seçin.
    * Bu yordam için 0016 madde numarasını seçin. Normalde çağrı merkezinde bir satış siparişi verildiğinde uygulanan ek süreklilik iş mantığı olan bir serbest bırakılan ürünü oluşturursunuz.  
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Düzenle öğesine tıklayın.
5. Satış bölümünü genişletin veya daraltın.
6. Bu maddenin temsil ettiği süreklilik programını buraya girin. Daha önce oluşturduğunuz Planlama kodunu yazın.
    * Bu madde bir çağrı merkezinde satıldığında, seçili süreklilik programından ek iş mantığı uygulanır.  
7. Kaydet'e tıklayın.


