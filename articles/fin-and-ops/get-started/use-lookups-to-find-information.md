---
title: "Bilgi bulmak için aramaları kullanma"
description: "Microsoft Dynamics 365 for Finance and Operations'taki birçok alanda, doğru veya istediğiniz değeri bulmanıza yardımcı olabilecek aramalar vardır. Bu denetimleri daha kullanışlı hale getiren ve kullanıcıları daha üretken hale getiren aramalara çeşitli geliştirmeler eklendi. Bu konuda, bu yeni arama özellikleri hakkında bilgi edineceksiniz ve sistemdeki aramalardan en iyi sonucu almak için bazı yararlı ipuçları edineceksiniz."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a5d0a9edd2cb5747fc799c6fdca45dd9ba5720f7
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="use-lookups-to-find-information"></a>Bilgi bulmak için aramaları kullanma

[!include[banner](../includes/banner.md)]


Microsoft Dynamics 365 for Finance and Operations'taki birçok alanda, doğru veya istediğiniz değeri bulmanıza yardımcı olabilecek aramalar vardır. Bu denetimleri daha kullanışlı hale getiren ve kullanıcıları daha üretken hale getiren aramalara çeşitli geliştirmeler eklendi. Bu konuda, bu yeni arama özellikleri hakkında bilgi edineceksiniz ve sistemdeki aramalardan en iyi sonucu almak için bazı yararlı ipuçları edineceksiniz.  

<a name="responsive-lookups"></a>Duyarlı aramalar
------------------

Finance and Operations'ın önceki sürümlerinde, bir arama denetimiyle etkileşim kurarken, kullanıcının açılır menüyü açmak için açık bir eylem yapması gerekir. Bu, denetimin geçerli değerine göre aramayı filtrelemek için denetimde bir yıldız (\*) yazarak, açılır menü düğmesine tıklayarak veya **Alt**+**Aşağı ok** klavye kısayollarını kullanarak yapılmış olabilir Arama denetimleri, geçerli web uygulamalarıyla daha uyumlu olması için aşağıdaki şekilde değiştirildi:

-   Arama açılır menüleri artık yazarken hafif bir duraklamadan sonra otomatik olarak açılır ve içerikleri arama denetiminin değerine göre filtrelenmiş haldedir.
    -   Yıldız işareti (\*) yazdıktan sonra açılır menünün otomatik açıldığı eski davranışın kullanımdan kaldırıldığına dikkat edin.
-   Arama açılır menü açıldıktan sonra şunlar olur:
    -   İmleç, denetimin değerinde değişiklik yapmaya devam edebilmeniz için (açılır menüye odaklama yerine) arama denetiminde kalır. Ancak, kullanıcı açılır menüdeki satırları değiştirmek ve açılır menüdeki geçerli satırı seçmek üzere giriş yapmak için **Yukarı ok**'u ve **Aşağı ok**'u kullanmaya devam edebilir.
    -   Arama denetiminin değerinde değişiklik yapıldıktan sonra açılır menünün içeriği ayarlanır.

Örneğin **Şehir** adlı bir arama alanı düşünün. 

Odak **Şehir** (City) alanındayken, "col" gibi birkaç harf yazarak istediğiniz şehir için arama başlatabilirsiniz.  Siz yazmayı durdurduktan sonra arama "col" ile başlayan şehirler filtre edilerek gösterilmiş halde otomatik olarak açılır. 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Bu noktada imleç hala arama alanındadır. Değer "colum" olacak şekilde yazmaya devam ederseniz, arama içeriği denetimdeki son değeri yansıtacak şekilde otomatik olarak ayarlanır. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Odak arama denetiminde olsa da, seçmek istediğiniz satırı vurgulamak için **Yukarı ok** veya **Aşağı ok** tuşlarını da kullanabilirsiniz. **Enter** tuşuna basarsanız, vurgulanmış satır aramada seçilir ve denetimin değeri güncelleştirilir. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Koddan daha fazlasını yazma
Veri girerken kullanıcıların, bir varlığı temsil eden bir tanımlayıcı yerine, bir müşteri veya satıcı gibi bir varlığı tanımlamaya çalışması doğaldır. Finance and Operations'ın geçerli sürümünde birçok aramada (tümünde değil) bağlamsal veri girişine artık izin veriliyor. Bu güçlü özellik kullanıcının arama denetiminde kodu veya karşılık gelen adı yazmasına izin veriyor. 

Örneğin bir satış siparişi oluştururken **Müşteri hesabı** alanını düşünün. Bu alanda müşteri için **Hesap kodu** gösterilir ancak bir kullanıcı satış siparişi oluştururken genellikle **Hesap kodu** yerine **Hesap adı** girmeyi tercih edecektir (örneğin "ABD-003" yerine "Forest Wholesales").

Kullanıcı arama denetimine bir **Hesap kodu** girmeye başladığı zaman açılır menü önceki bölümde açıklandığı şekilde otomatik olarak açılır ve kullanıcı aramayı aşağıda gösterildiği gibi görür.

[![Müşteri hesap kodu girildiğinde bağlamsal arama](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Ancak, kullanıcı artık bir **Hesap adının** baş kısmını da girebilir. Bu algılandığı zaman kullanıcı aşağıdaki aramayı görecektir. Aramada **Ad** (Name) sütununun ilk sütun olacak şekilde nasıl taşındığına ve aramanın **Ad** sütununa göre nasıl sıralanıp filtrelendiğine dikkat edin.

[![Müşteri adı girildiğinde bağlamsal arama](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Daha gelişmiş filtreleme ve sıralama için kılavuz sütun başlıklarını kullanma
Önceki iki bölümde ele alınan arama geliştirmeleri kullanıcının bir aramada **Kod** veya **Alan** alanının "ile başlar" şeklinde aranmasına göre satırlar arasında gezinme yeteneğini büyük ölçüde geliştiriyor. Bununla birlikte, doğru satırı bulmak için daha gelişmiş filtrelemenin (veya sıralamanın) gerekli olduğu durumlar vardır. Böyle durumlarda kullanıcının arama içinde kılavuz sütun başlıklarında filtreleme ve sıralama seçeneklerini kullanması gerekir. Örneğin, bir satış siparişi satırı girerken ürün olarak doğru "kabloyu" bulması gereken bir çalışan düşünün. "Kablo" ile başlayan ürün adı olmadığı için, **Madde numarası** denetimine "kablo" yazmak yardımcı olmaz. 

![emptyitemlookup](./media/emptyitemlookup.png) 

Bunun yerine, kullanıcı arama denetiminin değerini temizlemeli, arama açılır menüsünü açmalı ve aşağıda gösterildiği gibi ızgara sütun başlığını kullanarak açılır menüyü filtrelemelidir. Bir kullanıcı sütun başlığına fareyle tıklayarak veya dokunarak o sütunun filtreleme ve sıralama seçeneklerine erişebilir. Klavye kullananlar için, kullanıcının odağı açılır menüye getirmesi için, doğru sütuna gelmek üzere ikinci kez **Alt**+**Aşağı** **oka** basması, ardından **Ctrl**+**G** tuşlarına basarak ızgara sütunu başlığının açılır menüsünü açması gerekir. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Filtre uygulandıktan sonra (aşağıdaki resme bakın) kullanıcı her zamanki gibi satırı bulup seçebilir. 

![filtereditemlookup](./media/filtereditemlookup.png)



