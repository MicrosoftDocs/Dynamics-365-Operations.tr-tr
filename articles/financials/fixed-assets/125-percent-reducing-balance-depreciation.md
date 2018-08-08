---
title: "Yüzde 125 azalan bakiyeli amortisman"
description: "Bu makale, amortismanın Yüzde 125 Azalan bakiye yöntemi hakkında genel bir bakış sağlar."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a>Yüzde 125 azalan bakiyeli amortisman

[!include [banner](../includes/banner.md)]

Bu makale, amortismanın Yüzde 125 Azalan bakiye yöntemi hakkında genel bir bakış sağlar.

Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%125 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir. Bu yüzde, sabit kıymetin servis ömrü temel alınarak hesaplanır. Örneğin, bir sabit kıymetin beş yıllık servis ömrü varsa, yüzde %25 (%125 ÷ 5) olarak hesaplanır.

%125 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir. **Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.

## <a name="select-a-depreciation-year"></a>Bir amortisman yılı seçin
**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz. Varsayılan değer **Takvim** seçeneğidir. 

Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler. Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.

### <a name="calendar"></a>Takvim

**Amortisman yılı** alanında varsayılan değer olan **Takvim** seçeneğini bırakabilirsiniz. 

**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller. Tipik olarak, amortisman tabanı, net defter değeri eksi ıskarta değeridir. Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur. 

Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :

-   **Yıllık** 31 Aralık'ta bir tutarı nakleder.
-   **Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.
-   **Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.
-   **Yarı yıllık** seçeneği takvim yarı yılında ( 30 Haziran ve 31 Aralık) yarı yıllık tutarı nakleder.
-   **Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.

### <a name="fiscal"></a>Mali

**Amortisman yılı** alanında **Mali** seçeneğini belirlerseniz, %125 azalan amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır. Mali takvimler, **Mali Takvimler** sayfasında ayarlanır. 

Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman, her mali dönem için otomatik olarak düzeltilir ve bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasındaki dönem ayarları tarafından belirlenir. 

Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:

-   **Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.
-   **Mali dönem**, mali yıl için hesaplanan toplam amortisman tutarını nakleder. Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.

## <a name="example-of-125-reducing-balance-depreciation"></a>%125 azalan bakiyeli amortisman örneği

|                                |        |
|--------------------------------|--------|
| Alım maliyeti               | 11.000 |
| Hurda değeri                  | 1.000  |
| Amortisman tabanı              | 10.000 |
| Servis ömrü yıl sayısı             | 5      |
| Yıllık amortisman yüzdesi | % 25    |

%125 azalan bakiye yöntemi, yüzde 125'ü servis ömrü yıl sayısına böler. Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.

| Dönem | Yıllık amortisman miktarının hesaplaması | Defter değeri                    | Yıl sonunda net defter değeri |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| Yıl 1 | (11.000 – 1.000) × %25 = 2.500                | (11.000 – 2.500) = 8.500      | (11.000 – 1.000 – 2.500) = 7.500      |
| 2. yıl | 7.500 × %25 = 1.875                           | (8.500 – 1.875) = 6.625       | (7.500 – 1.875) = 5.625               |
| 3. yıl | 5.625 × %25 = 1.406,25                        | (6.625 – 1.406,25) = 5.218,75 | (5.625 – 1.406,25) = 4.218,75         |

> [!NOTE] 
> Tipik olarak, %125 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.




