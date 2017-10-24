---
title: El ile amortisman
description: "Bu makalede, el ile amortisman yöntemi hakkında genel bir bakış verilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e43b9397dd4e362eff9d78f302732e6bcc53d1db
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="manual-depreciation"></a>El ile amortisman

[!include[banner](../includes/banner.md)]


Bu makalede, el ile amortisman yöntemi hakkında genel bir bakış verilmektedir.

Sabit kıymet amortisman profilini ayarlayıp **Amortisman profilleri** sayfasının **Yöntem** alanındaki **El ile** seçeneğini işaretlediğinize, amortisman profiline atanan sabit kıymetlerin amortismanı, takvim yılında her aralık için girdiğiniz yüzdeyle saptanır. Yüzdeler ayarladığını aralıklar **Amortisman profilleri** sayfasının **Dönem sıklığı** alanındaki **Genel** hızlı sekmesinde seçtiğiniz değere göre deftere nakledilir. Seçebileceğiniz değerler şunlardır:

-   Yıllık
-   Aylık
-   Üç aylık
-   Yarım yıllık
-   Günlük

Dönem sıklığını seçtikten sonra, **El ile girilen planlar**'ı seçin ve her bir deftere nakletme sıklığı için yüzdeler ayarlayın. El ile yapılan planlamalar ve deftere nakledilen aralıklar, bu makalenin devamında aşağıdaki örneklerde gösterildiği gibi amortisman tutarını tanımlar. El ile amortisman her zaman alım fiyatının bir yüzdesi olarak hesaplanır. El ile amortisman için, amortismanın aralıklarına girdiğiniz yüzdeler, toplam yüzde 100'e tamamlanmak zorunda değildir. El ile amortisman, **Defterler**'de genellikle özel amaçlar için (örneğin, vergi) periyodik olmayan amortismanları belirlemek için kullanılan, esnek bir amortisman yöntemidir.

## <a name="examples"></a>Örnekler
Alım fiyatı: 11.000,00 Beklenen ıskarta değeri: 1.000,00 Aşağıdaki tablo, **Sabit kıymet amortisman profili planları** sayfasında ayarlamış olduğunuz aralıklar ve yüzdeleri gösterir.

| Aralık numarası | Yüzde |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Aşağıdaki tablo, her aralık için amortismanın nasıl hesaplandığını gösterir.

|  Aralık numarası | Yıllık amortisman miktarının hesaplaması | Aralık sonunda net defter değeri |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11.000 – 1.000) × %10 = 1.000                | 10.000 (11.000 – 1.000)                   |
| 2                | (11.000 – 1.000) × %50 = 5.000                | 5.000 (10.000 – 5.000)                    |
| 3                | (11.000 – 1.000) × %8 = 800                   | 4.200 (5.000 – 800)                       |

**Dönem sıklığı** alanında **Aylık** seçeneğini işaretlerseniz , el ile 12 planlama aralığı ayarlarsınız. Aşağıdaki tablo, ilk iki aralık için amortisman tutarlarını gösterir.

| Aralık | Amortisman tutarı            |
|----------|--------------------------------|
| Ocak  | (11.000 – 1.000) × %10 = 1.000 |
| Şubat | (11.000 – 1.000) × %50 = 5.000 |

****Dönem sıklığı** alanında** **Yarım Yıllık** seçeneğini işaretlerseniz , el ile en fazla iki planlama aralığı ayarlarsınız. Aşağıdaki tablo, bu iki aralık için amortisman tutarlarını gösterir.

| Aralık    | Amortisman tutarı            |
|-------------|--------------------------------|
| 30 Haziran     | (11.000 – 1.000) × %10 = 1.000 |
| 31 Aralık | (11.000 – 1.000) × %50 = 5.000 |

Tüm aralıkların yüzde toplamı 100 olmak zorunda değildir. Ancak, **Sabit kıymet amortisman profili planları** sayfasındaki **Toplam yüzde** alanındaki değer **100** değilse bir ileti alırsınız.




