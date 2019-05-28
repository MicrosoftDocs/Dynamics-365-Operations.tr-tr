---
title: Yüzde 200 azalan bakiyeli amortisman
description: Bu makalede, yüzde 200 amortisman bilanço azaltma yöntemine genel bakış sunulmuştur.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec51f9e12e31e81c56fab9e82d0fc18d45beb5e6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569325"
---
# <a name="200-percent-reducing-balance-depreciation"></a>Yüzde 200 azalan bakiyeli amortisman

[!include [banner](../includes/banner.md)]

Bu makalede, yüzde 200 amortisman bilanço azaltma yöntemine genel bakış sunulmuştur.

Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%200 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir. Yüzde, sabit kıymetin servis ömrü temel alınarak hesaplanır. Örneğin, bir sabit kıymetin beş yıllık servis ömrü varsa, yüzde 40 (%200 ÷ 5) olarak hesaplanır. 

Bu yöntem çift azalan bakiye olarak da bilinir.

%200 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir. **Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçtiğiniz değere bağlı olarak değişir.

## <a name="select-a-depreciation-year"></a>Bir amortisman yılı seçin
**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz. Varsayılan değer **Takvim** seçeneğidir. 

Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler. Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.

### <a name="calendar"></a>Takvim

**Amortisman yılı** alanında varsayılan değer olan **Takvim** seçeneğini bırakabilirsiniz. 

**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller. Tipik olarak, amortisman net defter değeri eksi ıskarta değeridir. Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur. 

Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :

-   **Yıllık** 31 Aralık'ta bir tutarı nakleder.
-   **Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.
-   **Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.
-   **Yarı yıllık** seçeneği takvim yarı yılında ( 30 Haziran ve 31 Aralık) yarı yıllık tutarı nakleder.
-   **Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.

### <a name="fiscal"></a>Mali

**Amortisman** yılı alanında **Mali** seçeneğini belirlerseniz, %200 azalan bakiyeli amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır. Mali takvimler, **Mali Takvimler** sayfasında ayarlanır. 

Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman her dönem için ayarlanır. Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir. 

Amortisman yılı olarak **Mali** seçildiğinde, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:

-   **Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.
-   **Mali dönem**, mali yıl için hesaplanan toplam amortisman tutarını nakleder. Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.

## <a name="example-of-200-reducing-balance-depreciation"></a>%200 azalan bakiyeli amortisman örneği

|                                |        |
|--------------------------------|--------|
| Alım maliyeti               | 11.000 |
| Hurda değeri                  | 1.000 |
| Amortisman tabanı              | 10.000 |
| Servis ömrü yıl sayısı             | 5      |
| Yıllık amortisman yüzdesi | %40    |

%200 azalan bakiye yöntemi, yüzde 200'ü servis ömrü yıl sayısına böler. Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.

| Dönem | Yıllık amortisman miktarının hesaplaması | Defter değeri             | Yıl sonunda net defter değeri |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| Yıl 1 | (11.000 – 1.000) × %40 = 4.000                | 11.000 – 4.000 = 7.000 | 11.000 – 1.000 – 4.000 = 6.000        |
| 2. yıl | 6.000 × %40 = 2.400                           | 7.000 – 2.400 = 4.600  | 6.000 – 2.400 = 3.600                 |
| 3. yıl | 3.600 × %40 = 1.440                           | 4.600 – 1.440 = 3.160  | 3.600 – 1.440 = 2.160                 |

> [!NOTE] 
> Tipik olarak, %200 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.



