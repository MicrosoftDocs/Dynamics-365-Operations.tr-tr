---
title: "Ürün numara terminolojisi"
description: "Bu konu, sabit biçimi [Ürün ana numarası - Yapılandırma - Boyut - Renk - Stil] ürün ana numarasını, etkin ürün boyutlarını ve istediğiniz metin ayırıcılarını da içeren bir hedeflenmiş biçimle değiştirmek için bir ürün numara terminolojisini nasıl ayarlayacağınızı açıklar. Kısıtlama tabanlı ürün yapılandırıcısı ile oluşturulan yapılandırmaları belirlemek için de bir terminoloji oluşturabilirsiniz. Bu terminolojiler istediğiniz öznitelikleri içerebilir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Ürün numara terminolojisi

[!include[banner](../includes/banner.md)]


Bu konu, sabit biçimi [Ürün ana numarası - Yapılandırma - Boyut - Renk - Stil] ürün ana numarasını, etkin ürün boyutlarını ve istediğiniz metin ayırıcılarını da içeren bir hedeflenmiş biçimle değiştirmek için bir ürün numara terminolojisini nasıl ayarlayacağınızı açıklar. Kısıtlama tabanlı ürün yapılandırıcısı ile oluşturulan yapılandırmaları belirlemek için de bir terminoloji oluşturabilirsiniz. Bu terminolojiler istediğiniz öznitelikleri içerebilir.

Yeni ürün çeşidi numarası terminolojisi, ürün çeşidi tanımlayıcılarınıza segmentler dahil etmenizi sağlar. Bu segmentler; ürün ana numarası, ürün boyutları, numara serileri, sabit metinler ve öznitelikler içerebilir. Bu işlev, bir satış siparişi veya satınalma siparişi oluşturduğunuzda belirli bir ürün çeşidini hızlı bir şekilde bulmanızı sağlar.

## <a name="nomenclature-of-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri terminolojisi
Ürün çeşitleri, ana ürünler için üç yapılandırma teknolojisinden birine göre oluşturulur:

-   Önceden tanımlanmış çeşitler
-   Kısıtlama tabanlı
-   Boyut tabanlı

Her ürün çeşidinin bir numarası vardır ve ürün çeşidi kimlik saptama terminolojisi, her ürün çeşidi numarasının dahil olacağı segmentleri seçmenizi sağlar. **Ürün terminolojisi** sayfasından aşağıdaki segmentleri seçebilirsiniz.

-   Ürün ana numarası
-   Numara serisi değeri
-   Metin sabiti
-   Ürün boyutları
    -   Yapılandırma
    -   Renk
    -   Ebat
    -   Stil

Ürün çeşidi kimlik saptama terminolojisi tanımlandıktan sonra bir ürün boyutu grubuyla ilişkilendirilebilir. Bunun sonucunda, bu ürün boyutu grubuna başvuran tüm ana ürünlere terminolojiye göre ürün çeşidi numarası atanır. Ana ürüne doğrudan bir ürün çeşidi kimlik saptama terminolojisi atamak da mümkündür. Bu durumda, bu ana ürüne ait olan ürün çeşitlerine terminolojiye göre ürün çeşidi numarası atanır.

### <a name="example"></a>Örnek

Bir tişört (TS1234), toplamda 24 olası ürün çeşidi olarak 3 farklı bedende (S, M, L), 4 farklı renkte (Kırmızı, Yeşil, Mavi, Sarı), ve 2 stilde (Polo, V) üretilir. Ürün çeşidi kimlik saptama terminolojisi aşağıdaki segmentlerle oluşturulur:

1.  Ürün ana numarası
2.  Metin sabiti: '-'
3.  Renk
4.  Metin sabiti: '-'
5.  Ebat
6.  Metin sabiti: '-'
7.  Stil

Kırmızı, Small beden, Polo tişörtün ürün çeşidi numarası TS1234-Kırmızı-Small-Polo olur.

## <a name="nomenclature-of-constraintbased-configurations"></a>Kısıtlama tabanlı yapılandırma terminolojisi
Kısıtlama tabanlı yapılandırmalar için, yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturulabilir. **Ürün terminolojisi** sayfasından aşağıdaki segmentleri seçebilirsiniz.

-   Numara serisi değeri
-   Metin sabiti
-   Öznitelik değeri 

Ürün yapılandırma modelindeki her bileşenin kendi yapılandırma terminolojisi olabilir. Yalnızca bileşene ait öznitelikler kullanılabilir. Alt bileşenlerden gelen öznitelikler veya kullanıcı gereksinimleri mevcut değildir.

### <a name="example"></a>Örnek

Ürün yapılandırma modelinin iki öznitelikli bir kök bileşeni vardır.

-   Malzeme (Plastik, Ahşap, Çelik)
-   Uzunluk (10...100)

Yapılandırma terminolojisi aşağıdaki segmentler kullanılarak tanımlanır:

1.  Öznitelik değeri: Malzeme
2.  Metin sabiti: "AAA"
3.  Öznitelik değeri: Uzunluk

Uzunluğu 78 olan ahşap bir malzemenin yapılandırma kodu AhşapAAA78 olur.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Boyut tabanlı yapılandırmaların terminolojisi
Boyut tabanlı yapılandırmalar için, yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturulabilir. **Ürün terminolojisi** sayfasından aşağıdaki segmentleri seçebilirsiniz.

-   Numara serisi değeri
-   Metin sabiti
-   Yapılandırma grubu maddesi

Ürün reçetesi (BOM) için bir yapılandırma terminolojisi oluşturulabilir.

### <a name="example"></a>Örnek

Ürün reçetesinin, 2 yapılandırma grubuna ayırılmış 4 ürün reçetesi satırı vardır.

-   Ürün reçetesi satırı: M0007, Standart dolap
    -   Yapılandırma grubu: Dolap
-   Ürün reçetesi satırı: M0008, Son teknolojili dolap
    -   Yapılandırma grubu: Dolap
-   Ürün reçetesi satırı: M0021, Ön ızgara dokuması
    -   Yapılandırma grubu: Ön ızgara
-   Ürün reçetesi satırı: M0022, Ön ızgara metali
    -   Yapılandırma grubu: Ön ızgara

Yapılandırma terminolojisi aşağıdaki segmentler kullanılarak tanımlanır:

1.  Yapılandırma grubu: Dolap
2.  Metin sabiti: "&"
3.  Yapılandırma grubu: Ön ızgara

Standart dolaplı ön ızgara dokuması yapılandırma kodu M0007&M0021 olur.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Ürün çeşitlerinin ve yapılandırmaların birleşiminin terminolojisi
Ana ürünün ürün çeşitlerini yapılandırmak için kısıtlama tabanlı veya boyut tabanlı yapılandırma teknolojisi kullandığınızda, ürün çeşitleri, yapılandırma boyutundan bir terminoloji içeren ürün çeşidi numaralarını alabilir. Çeşitleri yapılandırmak için şu adımları izleyin:

1.  **Ürün terminolojisi** sayfasında yapılandırma boyutu içeren bir ürün çeşidi numarası terminolojisi tanımlayın.
2.  Bu terminolojiyi yapılandırma boyutlu bir ürün boyut grubuna atayın.
3.  Ürün çeşitlerini yapılandırma amacıyla kullanılacak bileşenler veya ürün reçeteleri için bir yapılandırma terminolojisi tanımlayın.

### <a name="example-for-constraint-based-configurations"></a>Kısıtlama tabanlı yapılandırmalar için örnek

Bu örnekte, aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanabilirsiniz:

1.  Ürün ana numarası
2.  Metin sabiti '\_'
3.  Yapılandırma

Yapılandırma terminolojisi aşağıdaki segmentlerden oluşabilir:

1.  Öznitelik değeri: Malzeme
2.  Metin sabiti: "AAA"
3.  Öznitelik değeri: Uzunluk

Segmentler için aşağıdaki değerleri girebilirsiniz:

-   Ürün ana numarası = M0099
-   Malzeme = Plastik
-   Uzunluk = 12

Ürün çeşidi numarası M0099\_PlastikAAA12 olur.

### <a name="example-for-dimension-based-configurations"></a>Boyut tabanlı yapılandırmalar için örnek

Bu örnekte, aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanabilirsiniz.

1.  Ürün ana numarası
2.  Metin sabiti "//"
3.  Yapılandırma

Yapılandırma terminolojisi aşağıdaki segmentlerden oluşabilir:

1.  Yapılandırma grubu: Dolap
2.  Metin sabiti: "&"
3.  Yapılandırma grubu: Ön ızgara

Segmentler için aşağıdaki değerleri girebilirsiniz:

-   Ürün ana numarası = D0123
-   Dolap = M0008
-   Ön ızgara = M0022

Ürün çeşidi numarası D0123//M0008&M0022 olur.

## <a name="numbering-conflicts"></a>Çakışmaları numaralandırma
Benzersiz bir ürün çeşidi numarasının meydana gelmediği bir ürün çeşidi numarası terminolojisi ayarlanabilir. Örneğin etkin bir ürün boyutu, önceden tanımlı çeşit yapılandırma teknolojisini kullanan bir ana ürün terminolojisine dahil edilmezse böyle bir durum oluşabilir. Farklı yapılandırma teknolojileri için çakışmalar farklı şekillerde ele alınır.

### <a name="predefined-variants"></a>Önceden tanımlanmış çeşitler

Bir veya birden çok ürün çeşidinin aynı ürün çeşidi numarasını alacağı ürün çeşitlerini el ile veya otomatik olarak oluşturmayı denerseniz bir hata oluşur. Bunu önlemek için, ürün boyut grubundaki tüm etkin ürün boyutlarını kullanmalı veya ürün çeşit numaralarının benzersiz olmasını sağlamak için bir numara serisi eklemelisiniz.

### <a name="constraint-based-configurations"></a>Kısıtlama tabanlı yapılandırma

Terminolojiye bağlı olarak, sistem, yapılandırmaya benzersiz olmayan bir ürün numarası atama denemesinde bulunabilir. Bu durumda, sistem yapılandırma boyutu için ürün çeşidi numarası yerine numara serisi kullanır. Bu durumda, bir uyarı alırsınız. Bunu önlemek için, benzersizliği sağlamak adına terminolojiye yeterli öznitelikleri dahil etmelisiniz ve **Yeniden kullan** seçeneğinin bileşen için açık olduğuna emin olmalısınız.

### <a name="dimension-based-configurations"></a>Boyut tabanlı yapılandırmalar

Yapılandırma işlemi, sistemin terminolojiye göre bir yapılandırma değeri önereceği bir adım içerir. Bu adımda, yapılandırma değerini el ile değiştirebilirsiniz. Yapılandırmayı kaydettiğinizde sistem, yapılandırma değerinin benzersiz olup olmadığını kontrol eder. Değer benzersiz değilse bir hata görüntülenir. Yapılandırmayı kaydetmek için benzersiz bir yapılandırma değeri girmeniz gerekir.



<a name="see-also"></a>Ayrıca bkz.
--------

[Önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisi oluşturma (Görev kılavuzu)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Önceden yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisi oluşturma (Görev kılavuzu)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




