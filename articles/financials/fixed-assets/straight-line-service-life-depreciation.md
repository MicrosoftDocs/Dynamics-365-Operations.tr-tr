---
title: "Sabit servis ömrü amortismanı"
description: "Bu makalede amortismanın Düz çigi hizmet ömrü yöntemine genel bir bakış sunulmuştur."
author: ShylaThompson
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb5715855c7e240cddf4fd264a4b26ca09a2f6c4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="straight-line-service-life-depreciation"></a>Sabit servis ömrü amortismanı

[!include [banner](../includes/banner.md)]

Bu makalede amortismanın Düz çigi hizmet ömrü yöntemine genel bir bakış sunulmuştur.

Bir sabit kıymet amortisman profili ayarladığınızda ve Amortisman profilleri sayfasında Yöntem alanında Sabit servis ömrü öğesini seçtiğinizde bu amortisman profilinin atanmış olduğu kıymetlerin amortismanı kıymetin toplam servis ömrüne dayalı olarak hesaplanır. Bu, genellikle her amortisman dönemindeki aynı amortisman tutarı olur. 

Kalan sabit amortisman servis ömrüne ve sabit amortisman servis ömrüne göre hesaplanan amortisman tutarı arasındaki fark, sabit kıymet için deftere nakledilen bir düzeltme olduğunda ortaya çıkar . 

Sabit servis ömrü amortismanını ayarlamak için, Amortisman profilleri sayfasında Amortisman yılı ve Dönem sıklığı alanlarındaki seçenekleri de belirlemeniz gerekir.

## <a name="select-a-depreciation-year"></a>Amortisman yılının seçilmesi
Amortisman profilleri sayasındaki Amortisman yılı alanından Takvim Yılı veya Mali Yıl seçimi yapabilirsiniz. Seçiminiz, Dönem sıklığı alanında bulunan seçenekleri tanımlar. Varsayılan seçenek Takvim yılıdır.

### <a name="calendar"></a>Takvim

Takvim seçersiniz, mali dönem takvimini farklı şekilde tanımlamış olsanız bile, bir yılın 1 Ocak ile 31 Aralık arasındaki süre olduğu varsayılacaktır. 

Takvim seçeneği tipik olarak her yıl 1 Ocak itibariyle net defter değerinden hurda değeri çıkarılarak hesaplanan amortisman temelini günceller. Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur. 

Takvim seçimini yaparsanız, amortisman artışı nakil tarihleri ve takvim yılı genelindeki tutarları belirleyen Dönem sıklığı alanında şu seçenekler mevcut olacaktır:
-   Yıllık 31 Aralık'ta bir tutarı nakleder.
-   Aylık seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.
-   Üç aylık seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.
-   Altı Aylık seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.
-   Günlük seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.

Örneğin, Yıllık seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir. Aylık seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının 1/12'si oranında nakleder

### <a name="fiscal"></a>Mali

Amortisman yılı alanında Mali yıl seçimini yaparsanız, sabit servis ömrü amortismanı kullanılır. Defterin mali takvimine ya da Genel muhasebe sayfasında seçilen mali takvime göre tanımlanan mali yıl temel alınarak hesaplanır. Mali takvimler, Mali takvimler sayfasında ayarlanır.

Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman her mali dönem için otomatik olarak ayarlanır. Bir sonraki mali yılın uzunluğu, Mali takvimler formunda yeni bir mali yıl oluşturduğunuzda belirlenen mali dönemlere dayalı olacaktır. 

Mali yıl seçimini yaparsanız Dönem sıklığı alanında şu seçenekler kullanılabilir:
-   Yıllık, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.
-   Mali dönem, mali takvimin Mali takvimler formunda tanımlanan dönemlere tahakkuk edilen mali yıla ilişkin toplam amortisman tutarını hesaplar.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Örnek: Değişmeyen bir sabit kıymet için sabit amortisman
Bir sabit kıymetin aşağıdaki özelliklere sahip olduğunu düşünelim.

|                     |        |
|---------------------|--------|
| Alım maliyeti    | 11.000 |
| Hurda değeri       | 1.000  |
| Amortisman tabanı   | 10.000 |
| Servis ömrü yıl sayısı  | 5      |
| Yıllık amortisman | 2.000  |

Her yıl aynı amortisman tutarını elde edersiniz. (Alım maliyeti - Hurda değeri) / Servis ömrü yıl sayısı

| Dönem | Yıllık amortisman miktarı hesaplaması | Yılın sonundaki net defter değeri |
|--------|-------------------------------------------|---------------------------------------|
| Yıl 1 | (11.000 - 1.000) / 5 = 2.000              | 9.000                                 |
| Yıl 2 | (11.000 - 1.000) / 5 = 2.000              | 7.000                                 |
| Yıl 3 | (11.000 - 1.000) / 5 = 2.000              | 5.000                                 |
| Yıl 4 | (11.000 - 1.000) / 5 = 2.000              | 3.000                                 |
| Yıl 5 | (11.000 - 1.000) / 5 = 2.000              | 1.000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a> Örnek: Değiştirilmiş bir sabit kıymet için sabit amortisman

2. yılda aynı sabit kıymete 4.000 tutarında bir alım düzeltmesi eklediğinizi varsayalım. 

Alım düzeltmesinin servis ömrü, sabit kıymetinkiyle aynıdır ve alım anında başlar. 5.yılın sonunda bir net defter değeri varlığını sürdürür; bu, alım düzeltmesinin net defter değerine karşılık gelir. Döneme göre amortisman aşağıdaki tabloda gösterildiği şekilde hesaplanır.

| Dönem | Yıllık amortisman miktarı hesaplaması | Yıl sonunda net defter değeri |
|--------|-------------------------------------------|---------------------------------------|
| Yıl 1 | 10.000 / 5 = 2.000                        | 11.000 - 2.000 = 9.000                |
| 2. yıl | 4.000 (alım düzeltmeleri)            | 9.000 + 4.000 =13.000                 |
| 2. yıl | 14.000 / 5 = 2.800                        | 13.000 - 2.800 = 10.200               |
| 3. yıl | 14.000 / 5 = 2.800                        | 10.200 - 2.800 = 7.400                |
| Yıl 4 | 14.000 / 5 = 2.800                        | 7.400 - 2.800 = 4.600                 |
| Yıl 5 | 14.000 / 5 = 2.800                        | 4.600 - 2.800 = 1.800                 |
| Yıl 6 | Kalan 800\*                           | 1.800 – 800 = 1.000                   |

\*Kalan tutar amortisman miktarından az olduğundan, yalnızca kalan tutar eksi hurda değeri alınmıştır.






