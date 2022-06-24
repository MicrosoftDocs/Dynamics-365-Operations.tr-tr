---
title: Amortisman defteri yükseltmeye genel bakış
description: Bu makalede, Sabit kıymetlerdeki geçerli defter işlevi açıklanmaktadır. Bu özellik, önceki sürümlerde kullanılabilir olan değer modeli işlevselliğini temel alır ancak önceden yalnızca amortisman defterlerinde sunulan tüm işlevsellikleri de içerir.
author: moaamer
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 784ec32ae886ef7ea9342b085f893eeeec761961
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855505"
---
# <a name="depreciation-book-upgrade-overview"></a>Amortisman defteri yükseltmeye genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede, Sabit kıymetlerdeki geçerli defter işlevi açıklanmaktadır. Bu özellik, önceki sürümlerde kullanılabilir olan değer modeli işlevselliğini temel alır ancak önceden yalnızca amortisman defterlerinde sunulan tüm işlevsellikleri de içerir. Değer modeli işlevselliği ve amortisman defteri işlevselliği bir defter olarak bilinen tek bir kavramda birleştirilmiştir. Defter işlevi, tüm organizasyonunuzun sabit kıymet süreçleri için tek bir sayfa, sorgu ve rapor kümesi kullanmanızı sağlar. Bu makalede, yükseltme öncesinde dikkate almanız gereken bazı bilgiler sağlanmaktadır. 

Yükseltme işlemi var olan kurulumunuzu ve var olan tüm hareketlerinizi yeni defter yapısına taşır. Değer modelleri oldukları gibi genel muhasebeye nakleden defterler olarak kalır. Amortisman defterleri Genel muhasebeye naklet seçeneği Hayır olarak ayarlanmış bir deftere taşınır. Amortisman defteri günlük adları deftere nakil katmanı Yok ile ayarlanmış bir genel muhasebe günlük adına taşınır. Amortisman defteri hareketleri, Sabit kıymet hareketlerine taşınacaktır.

Veri yükseltmesini çalıştırmadan önce, amortisman defteri günlük satırlarını hareket fişlerine yükseltmek için kullanabileceğiniz iki seçeneği ve fiş serileri için kullanılacak numara serisini anlamanız gerekir.

1. Seçenek: **Sistem tarafından tanımlanan numara serisi** - Bu, yükseltme performansını en iyi duruma getirmek için varsayılan seçenektir. Yükseltme numara serisi çerçevesini kullanmaz, bunun yerine fişleri küme tabanlı bir yaklaşım ile tahsis eder. Yükseltmeden sonra, yeni numara serisi **Sonraki numara kümesi** ile yükseltme hareketlerine uygun şekilde dayanarak oluşturulacaktır. Varsayılan olarak, kullanılan numara serisi FADBUpgr\#\#\#\#\#\#\#\#\# biçiminde olacaktır. Bu yaklaşımı kullanırken biçimi ayarlayabilmeniz için birkaç parametre vardır:

-   **Numara serisi kodu** – Numara serisini belirlemek için kod. Yükseltme tarafından oluşturulacağından, bu numara serisi kodu mevcut olamaz.
    -   Sabit adı: **NumberSequenceDefaultCode**
    -   Varsayılan değer: "FADBUpgr"
-   **Ön Ek**: Fiş numaraları için ön ek olarak kullanılacak sabit dize değeri.
    -   Sabit adı: **NumberSequenceDefaultParameterPrefix**
    -   Varsayılan değer: "FADBUpgr"
-   **Alfasayısal uzunluk** – Numara serisinin alfasayısal kesiminin uzunluğu.
    -   Sabit adı: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Varsayılan değer: 9
-   **Başlangıç numarası** - Numara serisinde kullanılacak ilk numara.
    -   Sabit adı: **NumberSequenceDefaultParameterStartNumber**
    -   Varsayılan değer: 1

Seçenek 2: **Mevcut kullanıcı tarafından belirlenmiş numara serisi** - Bu seçenek, bu yükseltme için kullanılacak numara serisini tanımlamanıza izin verir. Bu seçeneği, gelişmiş numara serisi yapılandırmasına ihtiyaç duyarsanız kullanın. Bir numara serisini kullanmak için, ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans yükseltme sınıfını aşağıdaki bilgilerle değiştirmelisiniz:

-   **Numara serisi kodu** – Numara serisinin kodu.
    -   Sabit adı: **NumberSequenceExistingCode**
    -   Varsayılan değer: Varsayılan değer yoktur, bu değer numara serisi koduna güncelleştirilmelidir.
-   **Paylaşılan numara serisi** – Numara serisinin kapsamını tanımlayan Boole değeri. Tüm şirketler arasında paylaşılan numara serileri için "true", şirkete özel kapsam için "false" değerini kullanın. "False" kullanırken, belirtilen ada sahip numara serisi, amortisman defteri hareketleri içeren her şirkette mevcut olmalıdır. Paylaşılan numara serileri, amortisman defter hareketleri içeren her bölümde mevcuttur.
    -   Sabit adı: **NumberSequenceExistingIsShared**
    -   Varsayılan değer: true

Parametreler ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans sınıfının başında yer alır. 

*// Fiş tahsisatı için tercih edilebilir yaklaşım belirtin* 
 *// true, mevcut bir numara serisi kodu kullanmak istiyorsanız* 
 *// false, sistem tarafından tanımlanan numara serisini (varsayılan) kullanmaya niyetliyseniz* const boolean NumberSequenceUseExistingCode = false;  

*// Sistem tarafından tanımlanan numara serisi yaklaşımını kullanırsanız, numara serisi için parametreleri belirtin.*
 *// Bu parametrelerle yeni bir numara serisi oluşturulur.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Mevcut numara serisi yaklaşımını kullanıyorsanız, mevcut numara serisi kodunu belirtin.* 
 *// Fiş tahsisatı mevcut numara serileri için satır satır gidecektir.* const str NumberSequenceExistingCode = ''; *// Mevcut numara serisi kodunun kapsamını belirtin* 
 *// true, belirtilen numara serisi paylaşımlıysa* 
 *// false, belirtilen numara serisi şirket başına ise* 
 *// Varsayılan sistem tanımlı numara serisi, belirtilen kapsama sahip bir numara serisi kodu bulunmazsa kullanılacaktır.* const boolean NumberSequenceExistingIsShared = true; 

Sabitler değiştirildikten sonra sınıfı içeren projeyi yeniden oluşturun. 

Sistem tarafından oluşturulan bir numara serisi yaklaşımı kullanırken (seçenk 1), yükseltme fiş numaralarını yükseltme komut doyası parametrelerinde belirtildiği üzere tahsis etmek için set tabanlı işlem kullanır. Ayrıca tahsisattan sonra belirtilen parametrelerle yeni bir numara serisi oluşturacaktır. 

Kullanıcı tarafından tanımlanan var olan numara serisi yaklaşımı (2. seçenek) kullanılırken, veri yükseltme işlemi belirtilen kapsama sahip numara serisinin her bölüm ve şirket için amortisman defteri hareketlerinde var olup olmadığını denetler. Mevcut değilse, yükseltme fiş numaralarını, numara serisinde belirtildiği gibi numara serisi çerçevesini kullanarak satır satır tahsis edecektir. Numara serisi belirtilen kapsamla mevcut değilse, yükseltme varsayılan sistem tanımlı numara serisi yaklaşımını, fiş numaralarını tahsis etmek için kullanacaktır ve tahsisat sonunda belirtilen varsayılan parametrelere sahip yeni bir numara serisi oluşturacaktır.

İki yaklaşımda da veri yükseltme komut dosyası eski amortisman defteri günlük adları için oluşturulan yeni genel muhasebe günlük adlarındaki **Fiş serisi** alanının numara serisini kullanır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
