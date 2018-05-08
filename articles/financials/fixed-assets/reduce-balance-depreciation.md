---
title: "Bakiyeli amortismanı azaltma"
description: "Bu makale, amortismanın Azalan bakiye yöntemi hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29bc8cd02d98479197d7e5f5664b9859c03893b3
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="reduce-balance-depreciation"></a>Bakiyeli amortismanı azaltma

[!include [banner](../includes/banner.md)]

Bu makale, amortismanın Azalan bakiye yöntemi hakkında genel bir bakış sağlar.

Bir sabit kıymet amortisman profili oluşturduğunuzda ve Amortisman profilleri sayfasındaki Yöntem alanından Azalan bilançoyu seçtiğinizde, bu amortisman profilinin atandığı kıymetler her amortisman döneminde aynı yüzdeyle amortismana ayrılır.

Azalan bilanço amortismanını ayarlamak için Amortisman profilleri sayfasındaki Genel FastTab altındaki alanlardan seçimler yapmalısınız. Öncelikle, Amortisman yılı alanından bir yıl seçin. Seçiminize bağlı olarak, aşağıdaki bölümlerde anlatıldığı şekilde, Dönem sıklığı alanında farklı seçenekler görüntülenecektir. 

Ayrıca, amortisman profili için Yüzde alanına bir değer girmeniz gerekir. Tam amortisman seçeneğini belirlerseniz kalan amortisman, son amortisman dönemini temel alınır ve bu, büyük bir tutar olabilir. Bazı ülkeler/bölgeler doğrusal amortisman yöntemine geçiş özelliğini kullanmaz. Alternatif amortisman yönteminin tutarı birincil amortisman profili tutarına eşit veya daha büyükse değişim gerçekleştirilir ve alınan amortisman tutarı alternatif yöntemin tutarı olarak kabul edilir. 

Bir kıymet yüzde hesaplamasına dayanarak tamamen amortismana ayrılmayacağından, bir kıymeti tamamen amortismana ayırmak için Tam amortisman seçeneği belirlemelisiniz.

## <a name="select-a-depreciation-year"></a>Amortisman yılının seçilmesi
Amortisman profilleri sayasındaki Amortisman yılı alanından Takvim Yılı veya Mali Yıl seçimi yapabilirsiniz. Seçiminiz, Dönem sıklığı alanında bulunan seçenekleri tanımlar. Varsayılan seçenek Takvim yılıdır.

### <a name="calendar"></a>Takvim

Takvim seçeneği tipik olarak her yıl 1 Ocak itibariyle net defter değerinden hurda değeri çıkarılarak hesaplanan amortisman temelini günceller. Bu konunun ilerleyen bölümlerinde verilen azalan bilanço amortismanı örneğinde, amortismana esas olan değer, hesaplama sütunundaki ilk ifadenin payıdır. 

Takvim seçimini yaparsanız, amortisman artışı nakil tarihleri ve takvim yılı genelindeki tutarları belirleyen Dönem sıklığı alanında şu seçenekler mevcut olacaktır:

-   31 Aralık tarihindeki yıllık nakiller.
-   Aylık seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.
-   Üç aylık seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.
-   Altı Aylık seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.
-   Günlük seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.

Örneğin, Yıllık seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir. Aylık seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının 1/12'si oranında nakleder

### <a name="fiscal"></a>Mali

Amortisman yılı alanından Mali Yıl seçimini yaparsanız düz çizgi amortisman yöntemi kullanılır. Defter sayfasında seçilen mali takvim için Mali takvimler sayfasında ayarlanan mali yıl temel alınarak hesaplanır. Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman her mali dönem için ayarlanır. Bir sonraki mali yılın uzunluğu, Mali takvimler sayfasında yeni bir mali yıl oluşturduğunuzda belirlenen mali dönemlere dayalı olacaktır.


Mali yıl seçimini yaparsanız Dönem sıklığı alanında şu seçenekler kullanılabilir:

-   Yıllık seçeneği, mali yılın son gününde mali yıl için tek bir tutar olarak hesaplanan toplam amortisman tutarını nakleder.
-   Mali dönem, Defter sayfasında seçilen mali takvim için veya bir sabit kıymet defteri için seçilen mali takvim için tanımlanan mali dönemlere aktarılan mali yıl için hesaplanan toplam amortisman tutarını nakleder.

## <a name="example-of-reducing-balance-depreciation"></a>Azalan bakiye amortismanı örneği

Sabit kıymet alım fiyatının 11.000, ıskarta değerinin 1.000 ve amortisman yüzde faktörünün 30 olduğunu varsayalım. 

Amortismana esas olan değerin yüzde 30'u (net defter değeri eksi hurda değeri), Azalan bakiye yöntemini kullanılarak önceki amortisman döneminin sonunda hesaplanır. İlk üç yıla yönelik amortisman aşağıdaki tabloda gösterilmiştir.

| Dönem | Yıllık amortisman miktarı hesaplaması | Yıl sonunda net defter değeri |
|--------|-------------------------------------------|---------------------------------------|
| Yıl 1 | (11.000 - 1.000) \* %30 = 3.000           | (11.000 - 1.000) - 3.000 = 7.000      |
| 2. yıl | (7.000 - 1.000) \* %30 = 1.800            | (7.000 -1.800) = 5.200                |
| 3. yıl | (5.200 - 1.000) \* %30 = 1.260            | (5.200 - 1.260) = 3.940               |


-






