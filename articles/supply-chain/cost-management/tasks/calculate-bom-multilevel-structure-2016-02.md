---
title: Çok düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)
description: Bu yordam, Maliyetlendirme tablosunu temel alan, çok düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859f7b7c828dcdad1aa836044d2cc26847630f1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821429"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Çok düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)

[!include [banner](../../includes/banner.md)]

Bu yordam, Maliyetlendirme tablosunu temel alan, çok düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir. Ürün reçetesi hesaplaması serisindeki yedinci görevdir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.

1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Ürün BOM_1 öğesini seçin.  
3. Eylem Bölmesinde Yönet'e tıklayın.
4. Madde fiyatı'na tıklayın.
5. Madde maliyetini hesapla'ya tıklayın.
    * Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.  
6. Maliyetlendirme sürümü alanına bir değer girin veya buradan bir değer seçin.
    * Planlanan maliyet türü ve Açılım modu Çok Düzeyli olduğu için, Maliyetlendirme sürümü 20'yi seçin.   Çok düzeyli açılım modu, planlanan maliyetler ve benzetimler içindir. Standart maliyet için kullanılmaz.  
7. Tamam'a tıklayın.
8. Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.
    * Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.  Bu durumda, BOM_2'nin hammadde, işlem bu serinin ilk görev kılavuzunda etkinleştirilen 10 standart maliyeti yerine, toplam 29,40 genel gider dikkate alınarak hesaplandığına dikkat edin.  
9. Maliyetlendirme tablosu sekmesine tıklayın.
    * Maliyetlendirme tablosu sekmesine geçildiğinde, her maliyet grubunun toplam tutarları önceki görev kılavuzunda yapılan hesaplamalardan farklıdır.  
10. Düzey alanında "Çoklu" seçeneğini belirtin.
    * Çoklu seçenek belirlendiğinde, maliyetler 10'un M1 maliyet grubundan (ITEM_C) ve 15,60'ın da maliyet grubu L2 iken üretiminden türetildiği BOM_2 bileşimine göre sınıflandırılır. Dolaylı maliyetler de değişiklik gösterir.  
11. Sayfayı kapatın.
12. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]