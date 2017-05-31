---
title: "Yüzde 175 azalan bakiyeli amortisman"
description: "Bu makale, amortismanın Yüzde 175 Azalan bakiye yöntemi hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 40bbb07deb455d922244fc3856871cda7107543e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="175-percent-reducing-balance-depreciation"></a>Yüzde 175 azalan bakiyeli amortisman

[!include[banner](../includes/banner.md)]


Bu makale, amortismanın Yüzde 175 Azalan bakiye yöntemi hakkında genel bir bakış sağlar.

Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%175 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir. 

%175 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir. **Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.

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

**Amortisman yılı** alanında **Mali** seçeneğini belirlerseniz, %175 azalan bakiyeli amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır. Mali takvimler, **Mali Takvimler** sayfasında ayarlanır. Daha fazla bilgi için bkz. [Mali Takvimler, mali yıllar ve dönemler.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).

Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman, her mali dönem için otomatik olarak düzeltilir ve bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasındaki dönem ayarları tarafından belirlenir. 

Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:

-   **Yıllık** seçeneği, mali yıl için hesaplanan toplam amortisman tutarını, mali yılın son gününde nakleder.
-   **Mali dönem** seçeneği, mali yılın amortismanının toplam tutarını hesaplar. Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.

## <a name="example-of-175-reducing-balance-depreciation"></a>%175 azalan bakiyeli amortisman örneği
|                                |        |
|--------------------------------|--------|
| Alım maliyeti               | 11.000 |
| Hurda değeri                  | 1.000  |
| Amortisman tabanı              | 10.000 |
| Servis ömrü yıl sayısı             | 5      |
| Yıllık amortisman yüzdesi | %35    |

%175 azalan amortisman yöntemi, yüzde 175'ü servis ömrü yıl sayısına böler. Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.

| Dönem | Yıllık amortisman miktarının hesaplaması | Defter değeri                  | Yıl sonunda net defter değeri |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| Yıl 1 | (11.000 – 1.000) × %35 = 3.500                | 11.000 - 3.500 = 7.500      | 11.000 – 1.000 – 3.500 = 6.500        |
| 2. yıl | 6.500 × %35 = 2.275                           | 7.500 - 2.275 = 5.225       | 6.500 - 2.275 = 4.225                 |
| 3. yıl | 4.225 × %35 = 1.478,75                        | 5.225 - 1.478,75 = 3.746,25 | 4.225 - 1.478,75 = 2.746,25           |

> [!NOTE] 
> Tipik olarak, %175 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.




