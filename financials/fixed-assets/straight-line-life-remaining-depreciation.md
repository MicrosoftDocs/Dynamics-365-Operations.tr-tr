---
title: "Sabit kalan ömür amortismanı"
description: "Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: 9b690b80f148e7ccecba19850bd78c81216d8658
ms.lasthandoff: 03/31/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Sabit kalan ömür amortismanı

Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar.

Bir sabit kıymek amortisman profili ayarladığınızda ve **Amortisman profilleri** sayfasındaki **Yöntem** alanından **Kalan düz çizgi yaşamı** öğesini seçtiğinizde amortisman profiline atanan sabit kıymetlerin amortismanı kıymetin kalan hizmet ömrüne dayalı olacaktır. Amortisman tutarı genellikle her amortisman döneminde aynı olur. Düz çizgi kalan ömür amortismanı ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir. **Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.

## <a name="select-a-depreciation-year"></a>Bir amortisman yılı seçin
**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz. Varsayılan değer **Takvim** seçeneğidir. Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler. Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.

### <a name="calendar"></a>Takvim

Seçerseniz **Takvim** içinde ***Amortisman yılı*** alan, bir yılın 1 Ocak-31 Aralık kabul edilir, farklı mali takvimi tanýmladýðýnýz olsa bile. **Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller. Tipik olarak, amortisman tabanı, net defter değeri eksi hurda değeridir. Bu konunun devamındaki örnekte, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur. Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :

-   **Yıllık** 31 Aralık'ta bir tutarı nakleder.
-   **Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.
-   **Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.
-   **Altı Aylık** seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.
-   **Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.

Örneğin, **Yıllık** seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir. **Aylık** seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının on ikide biri oranında nakleder

### <a name="fiscal"></a>Mali

**Amortisman yılı** alanından **Mali Yıl** seçimini yaparsanız düz çizgi kalan yaşam amortismanı kullanılır Amortisman, kalan mali yıllar temel alınarak hesaplanır. Örneğin, 1 Temmuz 2015 30 Haziran 2016 aracılığıyla mali yıl için amortisman hesaplaması 1 Temmuz tarihinde başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman her mali dönem için ayarlanır. Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir. Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:

-   **Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.
-   **Mali dönem** seçeneği, mali yılın amortismanının toplam tutarını hesaplar. Bu tutar daha sonra, defter için belirtilen mali takvim için**Mali takvimler** sayfasında tanımlanan mali dönemlere aktarılır.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Değişmeyen bir sabit kıymet için düz çizgi amortisman örneği
Bir sabit kıymet aşağıdaki özelliklere sahiptir.

|                     |        |
|---------------------|--------|
| Alım maliyeti    | 11.000 |
| Hurda değeri       | 1.000  |
| Amortisman tabanı   | 10.000 |
| Servis ömrü yıl sayısı  | 5      |
| Yıllık amortisman | 2.000  |

Amortisman tutarı her yıl aynıdır: (Edinme maliyeti – Hurda değeri) ÷ Servis ömrü yıl

| Dönem | Yıllık amortisman miktarının hesaplaması | Yıl sonunda net defter değeri |
|--------|-----------------------------------------------|---------------------------------------|
| Yıl 1 | (11.000 – 1.000) ÷ 5 = 2.000                  | 9.000                                 |
| 2. yıl | (9.000 – 1.000) ÷ 4 = 2.000                   | 7.000                                 |
| 3. yıl | (7.000 – 1.000) ÷ 3 = 2.000                   | 5.000                                 |
| Yıl 4 | (5.000 – 1.000) ÷ 2 = 2.000                   | 3.000                                 |
| Yıl 5 | (3.000 – 1.000) ÷ 1 = 2.000                   | 1.000                                 |




