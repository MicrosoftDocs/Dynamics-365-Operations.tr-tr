---
title: Ürün çeşidi numaraları ve adlarının terminolojisi
description: Bu konu, ürün numaraları terminolojisini, sabit [Ana ürün numarası - Yapılandırma - Ebat - Renk - Stil] biçimini değiştirmek için nasıl ayarlayabileceğinizi açıklar.
author: roxanadiaconu
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 0ccb2ed2a143735c199c36f2da357996ad3fbff3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812848"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Ürün çeşidi numaraları ve adlarının terminolojisi

[!include [banner](../includes/banner.md)]

Bu konu, ürün numaraları terminolojisini, sabit [Ana ürün numarası - Yapılandırma - Ebat - Renk - Stil] biçimini değiştirmek için nasıl ayarlayabileceğinizi açıklar. Yeni terminoloji, ana ürün numarası, etkin ürün boyutları ve tercihiniz olan metin ayırıcılarını içeren hedeflenmiş bir biçime sahiptir. Ürün adları için bir terminoloji de oluşturabilirsiniz. Son olarak, kısıtlama tabanlı ürün yapılandırıcısı ile oluşturulan yapılandırmaları belirlemek için bir terminoloji oluşturabilirsiniz. Bu terminolojiler istediğiniz öznitelikleri içerebilir.

Ürün çeşidi numaraları ve ürün çeşit adları için yeni terminoloji, ürün çeşitleri için kimlik tanımlayıcıları içerisinde bölümler dahil etmenize de izin verir. Bu bölümler, ana ürün numarası ve adı, ürün boyut kimlikleri ve adları, numara serileri, sabit metinler ve öznitelikleri içerebilir. Bu işlev, bir satış siparişi veya bir satınalma siparişi oluşturduğunuzda belirli bir ürün çeşidini hızlı bir şekilde bulmanızı sağlar. **Ürün terminolojisi** sayfasını kullanarak hem ürün çeşit numaraları hem de ürün çeşit adları için terminolojiler oluşturabilirsiniz. Bu sayfayı açmak için **Ürün bilgi yönetimi** &gt; **Kurulum** üzerine tıklayın.

## <a name="nomenclature-of-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri terminolojisi
Ürün çeşitleri, ana ürünler için üç yapılandırma teknolojisinden birine göre oluşturulur:

-   Önceden tanımlanmış çeşitler
-   Kısıtlama tabanlı
-   Boyut tabanlı

Her ürün çeşidinin bir numarası ve adı vardır ve ürün çeşidi kimlik saptama terminolojileri, her ürün çeşidi numarasının veya adının dahil olacağı segmentleri seçmenizi sağlar. **Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:

-   Ürün ana numarası
-   Ana ürün adı
-   Numara serisi değeri
-   Metin sabiti
-   Ürün boyutları
    -   Yapılandırma kodu veya adı
    -   Renk kodu veya adı
    -   Beden kodu veya adı
    -   Stil kodu veya adı

Bir ürün çeşidi kimlik saptama numarası terminolojisini tanımladıktan sonra, bunu bir ürün boyutu grubu ile ilişkilendirebilirsiniz. Bu ürün boyutu grubuna başvuran tüm ana ürünlere daha sonra, terminolojiye uygun olarak bir ürün çeşidi numarası atanacaktır. Ancak, ürün çeşidi adı terminolojileri, ürün boyut grupları ile ilişkilendirilemez. Ayrıca bir ürün çeşidini kimlik saptama terminolojisini doğrudan ana ürüne de atayabilirsiniz. Bu durumda, ana ürüne ait ürün çeşitlerine ürün çeşidi numaraları ve adları, terminolojilere uygun bir biçimde atanacaktır.

### <a name="example"></a>Örnek

Bir tişört (TS1234), üç bedende (S, M, L), dört renkte (Kırmızı, Yeşil, Mavi, Sarı) ve iki stilde (Polo, V yaka) üretilmektedir. Bu nedenle, 24 ürün çeşidi mümkündür (= 3 x 4 x 2). Aşağıdaki bölümlere sahip bir ürün çeşidi numarası terminolojisi oluşturabilirsiniz:

1.  Ürün ana numarası
2.  Metin sabiti: "-"
3.  Renk
4.  Metin sabiti: "-"
5.  Ebat
6.  Metin sabiti: "-"
7.  Stil

Bu durumda, kırmızı, small bir polo tişört için ürün çeşidi numarası TS1234-Kırmızı-Small-Polo olacaktır.

## <a name="nomenclature-of-constraint-based-configurations"></a>Kısıtlama tabanlı yapılandırma terminolojisi
Kısıtlama tabanlı yapılandırmalar için yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturabilirsiniz. **Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:

-   Numara serisi değeri
-   Metin sabiti
-   Öznitelik değeri

Ürün yapılandırma modelindeki her bileşenin kendi yapılandırma terminolojisi olabilir. Yalnızca bileşene ait olan öznitelikler kullanılabilir. Alt bileşenlerden gelen öznitelikler veya kullanıcı gereksinimleri kullanılamaz.

### <a name="example"></a>Örnek

Bir ürün yapılandırma modeli, iki özniteliğe sahip bir kök bileşene sahiptir:

-   Malzeme (Plastik, Ahşap, Çelik)
-   Uzunluk (10...100)

Aşağıdaki bölümlere sahip bir yapılandırma terminolojisi oluşturabilirsiniz:

1.  Öznitelik değeri: Malzeme
2.  Metin sabiti: "AAA"
3.  Öznitelik değeri: Uzunluk

Bu durumda, 78 uzunluğuna sahip ahşap malzeme için yapılandırma kodu WoodAAA78 olacaktır.

## <a name="nomenclature-of-dimension-based-configurations"></a>Boyut tabanlı yapılandırmaların terminolojisi
Boyut tabanlı yapılandırmalar için yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturabilirsiniz. **Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:

-   Numara serisi değeri
-   Metin sabiti
-   Konfigürasyon grubu maddesi

Ürün reçetesi (BOM) için bir yapılandırma terminolojisi oluşturulabilirsiniz.

### <a name="example"></a>Örnek

Bir ürün reçetesi, iki farklı yapılandırma grubuna ayrılmış dört ürün reçetesi satırına sahiptir:

-   Ürün reçetesi satırı: M0007, Standart dolap
    -   Yapılandırma grubu: Dolap
-   Ürün reçetesi satırı: M0008, Son teknolojili dolap
    -   Yapılandırma grubu: Dolap
-   Ürün reçetesi satırı: M0021, Ön ızgara dokuması
    -   Yapılandırma grubu: Ön ızgara
-   Ürün reçetesi satırı: M0022, Ön ızgara metali
    -   Yapılandırma grubu: Ön ızgara

Aşağıdaki bölümlere sahip bir yapılandırma terminolojisi oluşturabilirsiniz:

1.  Yapılandırma grubu: Dolap
2.  Metin sabiti: "&"
3.  Yapılandırma grubu: Ön ızgara

Bu durumda, ön ızgara dokumasına sahip standart bir dolap için yapılandırma kodu M0007&M0021 olur.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Ürün çeşitlerinin ve yapılandırmalarının birleşimi için terminoloji
Kısıtlama tabanlı yapılandırma teknolojisi ya da boyut tabanlı yapılandırma teknolojisini, bir ana ürün için ürün çeşitlerini yapılandırmakta kullandığınızda, ürün çeşidi için ürün çeşidi numaraları, yapılandırma boyutundaki terminolojiyi içerebilir. Çeşitleri yapılandırmak için şu adımları izleyin.

1.  **Ürün terminolojisi** sayfası üzerinde, yapılandırma boyutunu içeren bir ürün çeşidi numarası terminolojisi tanımlayın.
2.  Terminolojiyi, yapılandırma boyutuna sahip bir boyut grubuna atayın.
3.  Ürün çeşitlerini yapılandırma amacıyla kullanılacak bileşenler veya ürün reçeteleri için bir yapılandırma terminolojisi tanımlayın.

Ürün çeşidi adları için terminolojiler de oluşturabilirsiniz. Ürün çeşidi adları, yapılandırma kodunu veya adını içermek üzere de yapılandırılabilir.

### <a name="example-for-constraint-based-configurations"></a>Kısıtlama tabanlı yapılandırmalar için örnek

Bu örnek için aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanırsınız:

1.  Ürün ana numarası
2.  Metin sabiti "\_"
3.  Yapılandırma

Yapılandırma terminolojisi aşağıdaki segmentlerden oluşur:

1.  Öznitelik değeri: Malzeme
2.  Metin sabiti: "AAA"
3.  Öznitelik değeri: Uzunluk

Segmentler için aşağıdaki değerleri girersiniz:

-   Ürün ana numarası = **M0099**
-   Malzeme = **Plastik**
-   Uzunluk = **12**

Bu durumda, ürün çeşidi numarası M0099\_PlastikAAA12 olacaktır.

### <a name="example-for-dimension-based-configurations"></a>Boyut tabanlı yapılandırmalar için örnek

Bu örnek için aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanırsınız:

1.  Ürün ana numarası
2.  Metin sabiti "//"
3.  Yapılandırma

Yapılandırma terminolojisi aşağıdaki segmentlerden oluşur:

1.  Yapılandırma grubu: Dolap
2.  Metin sabiti: "&"
3.  Yapılandırma grubu: Ön ızgara

Segmentler için aşağıdaki değerleri girersiniz:

-   Ürün ana numarası = **D0123**
-   Dolap = **M0008**
-   Ön ızgara = **M0022**

Bu durumda, ürün çeşidi numarası D0123//M0008&M0022 olacaktır.

## <a name="numbering-conflicts"></a>Çakışmaları numaralandırma
Bazı durumlarda, ayarladığınız bir ürün çeşidi numarası terminolojisi, benzersiz ürün çeşidi numaraları oluşturmayabilir. Örneğin etkin bir ürün boyutu, önceden tanımlı çeşit yapılandırma teknolojisini kullanan bir ana ürün terminolojisine dahil edilmezse ürün çeşidi numaraları benzersiz olmaz. Bu çakışmayı nasıl çözeceğiniz, yapılandırma teknolojisine bağlıdır.

### <a name="predefined-variants"></a>Önceden tanımlanmış çeşitler

Ürün çeşitlerini el ile oluşturmaya çalıştığınızda veya otomatik ürün çeşitleri oluşturduğunuzda bir hata ortaya çıkar ve birden fazla ürün çeşidi aynı ürün çeşidi numarasına sahip olur. Bu durumun önüne geçmek için tüm etkin ürün boyutlarını ürün boyutu grubunda kullanmalısınız. Alternatif olarak, ürün çeşit numarasının benzersiz olduğunu garanti etmeye yardımcı olmak için bir numara serisi ekleyin.

### <a name="constraint-based-configurations"></a>Kısıtlama tabanlı yapılandırma

Terminolojiye bağlı olarak, sistem, yapılandırmaya benzersiz olmayan bir ürün numarası atama denemesinde bulunabilir. Bu durumda, sitem yapılandırma boyutu için numara serisini ürün numarası olarak kullanır ve bir uyarı alırsınız. Bu durumu engellemek için benzersiz ürün çeşidi numaralarını garanti etmeye yardımcı olmak için terminolojide yeterli sayıda öznitelik dahil etmelisiniz. Ayrıca **Yeniden kullan** seçeneğinin bileşen için açık olduğundan emin olmalısınız.

### <a name="dimension-based-configurations"></a>Boyut tabanlı yapılandırmalar

Yapılandırma işleminin bir adımında, sistem terminolojiye göre bir yapılandırma değeri önerir. Bu adımda, yapılandırma değerini el ile değiştirebilirsiniz. Yapılandırmayı kaydettiğinizde sistem, yapılandırma değerinin benzersiz olduğunu doğrular. Girmiş olduğunuz değer benzersiz değilse, bir hata iletisi alırsınız. Yapılandırmayı kaydetmek için, benzersiz bir yapılandırma değeri girmeniz gerekir.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisi oluşturma](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]