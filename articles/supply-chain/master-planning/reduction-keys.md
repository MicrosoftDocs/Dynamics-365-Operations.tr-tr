---
title: "Azaltma anahtarları"
description: "Bu makalelerde bir azaltma anahtarının nasıl ayarlanacağını gösteren örnekler verilmiştir. Çeşitli azaltma anahtarı ayarları ve her birinin sonuçları hakkında da bilgiler içerir. Bir zzaltma anahtarını, tahmin gereksinimlerinin nasıl azaltılacağını tanımlamak için kullanabilirsiniz."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 30634b0af343ad171c385a95c4ba0934180f70cf
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="reduction-keys"></a>Azaltma anahtarları

[!include[banner](../includes/banner.md)]


Bu makalelerde bir azaltma anahtarının nasıl ayarlanacağını gösteren örnekler verilmiştir. Çeşitli azaltma anahtarı ayarları ve her birinin sonuçları hakkında da bilgiler içerir. Bir zzaltma anahtarını, tahmin gereksinimlerinin nasıl azaltılacağını tanımlamak için kullanabilirsiniz.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Örnek 1: Yüzde - Azaltma anahtarı tahmin azaltma ilkesi
---------------------------------------------------------------

Bu örnek bir azaltma anahtarının, talep tahmini gereksinimlerini azaltma anahtarı tarafından tanımlanan yüzdelere ve dönemlere göre nasıl azalttığını gösterir.

1.  **Azaltma anahtarları** sayfasında aşağıdaki satırları ayarlayın.
    | Değiştirme | Birim  | Yüzde |
    |--------|-------|---------|
    | 1      | Ay | 100     |
    | 2      | Ay | 75      |
    | 3      | Ay | 50      |
    | 4      | Ay | 25      |

2.  Azaltma anahtarını ürünün kapsam grubuna bağlayın.
3.  **Ana planlar** sayfasında, **Azaltma ilkesi** alanında **Yüzde - azaltma anahtarı**'nı seçin.
4.  Aylık 1.000 parçalık bir talep tahmini oluşturun.

Tahmin planını 1 Ocak'ta çalıştırırsanız, talep tahmini gereksinimleri **Azaltma anahtarları** sayfasında ayarladığınız yüzdelere göre tüketilir. Aşağıdaki gereksinim miktarları ana plana transfer edilir.

| Ay                | Gerekli parça sayısı |
|----------------------|---------------------------|
| Ocak              | 0                         |
| Şubat             | 250                       |
| Mart                | 500                       |
| Nisan                | 750                       |
| Mayıs - Aralık arası | 1.000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Örnek 2: Hareketler azaltma anahtarı tahmini azaltma ilkesi
Bu örnek, azaltma anahtarı tarafından tanımlanan dönemler boyunca gerçekleşen fiili siparişlerin talep tahmini gereksinimlerini nasıl azalttığını gösterir.

-   **Ana planlar** sayfasında, **Azaltma ilkesi** alanında **Hareketler - azaltma anahtarı**'nı seçin.

Aşağıdaki satış siparişleri 1 Ocak'tadır.

| Ay    | Gerekli parça sayısı |
|----------|--------------------------|
| Ocak  | 956                      |
| Şubat | 1.176                    |
| Mart    | 451                      |
| Nisan    | 119                      |

Aylık 1.000 parçalık aynı talep tahminini kullanıyorsanız, aşağıdaki gereksinim miktarları ana planlamaya aktarılır.

| Ay                | Gerekli parça sayısı |
|----------------------|---------------------------|
| Ocak              | 44                        |
| Şubat             | 0                         |
| Mart                | 549                       |
| Nisan                | 881                       |
| Mayıs - Aralık arası | 1.000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Örnek 3: Hareketler dinamik dönem tahmini azaltma ilkesi
Çoğu durumda, hareketlerin haftalık, aylık ve benzeri tahmin dönemlerinde talep tahminini azaltabilmesi için sistemler ayarlanır. Bu dönemler azaltma anahtarında tanımlanır. Ancak, iki tahmin satırı arasındaki süre bir dönemi*gösterebilir*.

1.  Aşağıdaki tarihler ve miktarlar için bir talep tahmin oluşturun.
    | Tarih       | Talep tahmini |
    |------------|-----------------|
    | 1 Ocak  | 1.000           |
    | 5 Ocak  | 500             |
    | 12 Ocak | 1.000           |

    Bu tahminde, tahmin tarihleri arasında açıkça bir dönem yoktur: birinci ve ikinci tarihler arasında dört günlük bir süre; ikinci ve üçüncü tarihler arasında yedi günlük bir süre vardır. Bu süre çeşitliliği dinamik periyotları oluşturur.
2.  Aşağıdaki satış siparişi satırlarını oluşturun.
    | Tarih                             | Satış siparişi miktarı |
    |----------------------------------|----------------------|
    | Önceki yılın 15 Aralık tarihi | 500                  |
    | 3 Ocak                        | 100                  |
    | 10 Ocak                       | 200                  |

Tahmin aşağıdaki gibi azaltılır:

-   İlk satış siparişi dönem içinde değildir, böylece hiçbir tahmini azaltmaz.
-   İkinci satış siparişi 1 Ocak - 5 Ocak aralığındadır, böylece 1 Ocak için tahmini 100 azaltır.
-   Üçüncü satış siparişi 5 Ocak - 12 Ocak aralığındadır, böylece 5 Ocak için tahmini 200 azaltır.

Aşağıdaki planlı sipariş tahmini karşılamak için oluşturulur.

| Talep tahmini tarihi | Azaltılmış miktar |
|----------------------|------------------|
| 1 Ocak            | 900              |
| 5 Ocak            | 300              |
| 12 Ocak           | 1.000            |

**Hareketler - dinamik dönem** azaltmasına ilişkin bir örnek şöyledir:

-   Tahmin gereksinimleri, dinamik dönem sırasında gerçekleşen fiili sipariş hareketleriyle azaltılır. Dinamik dönem, geçerli tahmin tarihlerini kapsar ve bir sonraki tahmin başlangıcında sona erer.
-   Bu yöntem bir azaltma anahtarı kullanmaz.
-   Bu seçenek kullanıldığında, aşağıdaki davranış ortaya çıkar:
    -   Tahmin tümüyle azaltıldıysa, geçerli tahminin tahmin gereksinimleri 0 (sıfır) olur.
    -   Gelecekte başka bir tahmin yoksa, girilen son tahmindeki tahmin gereksinimleri azaltılır.
    -   Zaman dilimleri, tahmin azaltma hesaplamasına eklenir.
    -   Artı günler, tahmin azaltma hesaplamasına eklenir.
    -   Fiili sipariş hareketlerinin tahmin gereksinimlerini aşması durumunda, kalan hareketler sonraki tahmin dönemine iletilmez.


<a name="see-also"></a>Ayrıca bkz.
--------

[Master planlar](master-plans.md)




