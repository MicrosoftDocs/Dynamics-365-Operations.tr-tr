---
title: "Amortisman defteri yükseltmeye genel bakış"
description: "Önceki sürümlerde, sabit kıymetler - değer modelleri ve amortisman defterleri için iki değerleme kavram vardı. Microsoft Dynamics 365 for Operations sürüm 1611 ile, değer modeli işlevselliği ve amortisman defteri işlevselliği bir defter olarak bilinen tek bir kavramda birleştirilmiştir. Bu konu yükseltme işleminde dikkate alınması gereken bazı noktaları ele alır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Amortisman defteri yükseltmeye genel bakış

Önceki sürümlerde, sabit kıymetler - değer modelleri ve amortisman defterleri için iki değerleme kavram vardı. Microsoft Dynamics 365 for Operations sürüm 1611 ile, değer modeli işlevselliği ve amortisman defteri işlevselliği bir defter olarak bilinen tek bir kavramda birleştirilmiştir. Bu konu yükseltme işleminde dikkate alınması gereken bazı noktaları ele alır. 

Yükseltme işlemi var olan kurulumunuzu ve var olan tüm hareketlerinizi yeni defter yapısına taşır. Değer modelleri oldukları gibi genel muhasebeye nakleden defterler olarak kalır. Amortisman defterleri **Genel muhasebeye naklet** seçeneği **Hayır** olarak ayarlanmış bir deftere taşınır. Amortisman defteri günlük adlarını taşınabilir bir genel muhasebe günlüğü deftere nakil katmanı ayarlanmış olan **yok**. Amortisman defteri hareketleri için sabit kıymet hareketlerini taşınacaktır. 

Veri yükseltmesini çalıştırmadan önce, amortisman defteri günlük satırlarını hareket fişlerine yükseltmek için kullanabileceğiniz iki seçeneği ve fiş serileri için kullanılacak numara serisini anlamanız gerekir. 

1. Seçenek: **Sistem tarafından tanımlanan numara serisi** - Bu, yükseltme performansını en iyi duruma getirmek için varsayılan seçenektir. Yükseltme numara serisi çerçevesini kullanmaz, bunun yerine fişleri küme tabanlı bir yaklaşım ile tahsis eder. Yükseltme sonrasında, yeni numara serisi ile oluşturulacak **numara tandır** uygun şekilde yükseltilen hareketlere dayalı. Varsayılan olarak, FADBUpgr içinde kullanılan numara serisi olacak\#\#\#\#\#\#\#\#\# biçimi. Bu yaklaşım kullanırken biçimini ayarlamak için kullanabileceğiniz birkaç parametre vardır:

-   **Numara sırası kodu** – tanımlayan numara serisi kodu. Yükseltme tarafından oluşturulacağından, bu numara serisi kodu bulunamaz.
    -   Sabit adı: **NumberSequenceDefaultCode**
    -   Varsayılan değer: "FADBUpgr"
-   **Önek** – Fiş numaraları için önek olarak kullanılacak sabit dize değeri.
    -   Sabit adı: **NumberSequenceDefaultParameterPrefix**
    -   Varsayılan değer: "FADBUpgr"
-   **Alfasayısal uzunluk** – Numara serisinin alfasayısal kesiminin uzunluğu.
    -   Sabit adı: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Varsayılan değer: 9
-   **Başlangıç numarası** - Numara serisinde kullanılacak ilk numara.
    -   Sabit adı: ** NumberSequenceDefaultParameterStartNumber **
    -   Varsayılan değer: 1

Seçenek 2: **varolan kullanıcı tanımlı numara serisi** -bu seçenek yükseltme için kullanılacak numara serisini tanımlamanıza izin verir. Gelişmiş numara sırası yapılandırma gerekiyorsa bu seçeneği kullanmayı düşünün. Bir numara serisi kullanmak için yükseltme sınıf ReleaseUpdateDB70 değiştirmek\_FixedAssetJournalDepBookRemovalDepBookJournalTrans aşağıdaki bilgilerle:

-   **Numara serisi kodu** – Numara serisinin kodu.
    -   Sabit adı: ** NumberSequenceExistingCode **
    -   Varsayılan değer: Varsayılan değer yoktur, bu değer numara serisi koduna güncelleştirilmelidir.
-   **Paylaşılan numara serisi** – Numara serisinin kapsamını tanımlayan Boole değeri. Tüm şirketler arasında paylaşılan numara serileri için "true", şirkete özel kapsam için "false" değerini kullanın. "False" kullanırken, belirtilen ada sahip bir numara sırası amortisman defteri hareketlerini içeren her şirkette bulunması gerekir. Amortisman defteri hareketleri içeren her bölümün paylaşılan numara serileri mevcut.
    -   Sabit adı: ** NumberSequenceExistingIsShared **
    -   Varsayılan değer: true

Parametreler ReleaseUpdateDB70 başında bulunan\_FixedAssetJournalDepBookRemovalDepBookJournalTrans sınıf. 

*Fişleri ayırma tercih bir yaklaşım belirtmek*<ph id="t1">
</ph>*/ / true, varolan bir numara sırası kodu kullanmak isterseniz*<ph id="t2">
</ph>*/ / yanlış, sistem tarafından tanımlanan numara sırası (varsayılan) kullanmayı düşünüyorsanız,* boolean const NumberSequenceUseExistingCode = false;  

*Sistem tarafından tanımlanan numara sırası yaklaşımı kullanarak, numara serisi için parametreleri belirtin. *<ph id="t3">
</ph>*/ / Bu parametrelerle yeni bir numara serisi oluşturulacaktır.* Str const NumberSequenceDefaultCode = 'FADBUpgr'; str const NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*Mevcut numara serisi yaklaşımı kullanarak, varolan bir numara sırası kodu belirtin. *<ph id="t4">
</ph>*/ / Fiş tahsisat satır satır gider için numara serileri mevcut.* Str const NumberSequenceExistingCode = ''; */ / Mevcut numara serisi kodu kapsamını belirtmek*<ph id="t5">
</ph>*/ / belirtilen numara sırasındaki paylaşılan, doğru*<ph id="t6">
</ph>*/ / yanlış belirtilen numara sırasındaki her şirket ise*<ph id="t7">
</ph>*/ / varsayılan sistem tarafından tanımlanan numara serisinden bir numara sırası kodu ile belirtilen kapsam bulunamazsa, kullanılacak.* const boolean NumberSequenceExistingIsShared = true; 

Sabitler değiştirildikten sonra sınıfı içeren projeyi yeniden oluşturun. 

Sistem tarafından oluşturulan numara sırası yaklaşım (seçenek 1) kullanırken, yükseltme yükseltme komut dosyası parametreleri belirtilen fiş numaraları ayırmaya kümesi tabanlı işleme kullanır. Belirtilen parametrelerle ayırmadan sonra da yeni bir numara sırası oluşturur. 

Kullanıcı tarafından tanımlanan var olan numara serisi yaklaşımı (2. seçenek) kullanılırken, veri yükseltme işlemi belirtilen kapsama sahip numara serisinin her bölüm ve şirket için amortisman defteri hareketlerinde var olup olmadığını denetler. Yükseltme yoksa, satır satır işleme müteselsil numara sırası Framework'ü kullanarak belirtildiği gibi fiş numaraları tahsis etmek amacıyla kullanır. Numara sırası ile belirtilen kapsam yoksa yükseltme fiş numaraları tahsis etmek amacıyla varsayılan sistem tarafından tanımlanan numara sırası yaklaşımı kullanacaksınız ve yeni bir numara sırası ayırmadan sonra belirtilen varsayılan parametreler ile oluşturur.

İki yaklaşımda da veri yükseltme komut dosyası eski amortisman defteri günlük adları için oluşturulan yeni genel muhasebe günlük adlarındaki **Fiş serisi** alanının numara serisini kullanır.


