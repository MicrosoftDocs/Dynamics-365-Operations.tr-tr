---
title: "Bilgi bulmak için arama kullanma"
description: "İşlemler için Microsoft Dynamics 365 içinde birçok alanları kolayca doğru veya istenen değeri bulmanıza yardımcı olabilir arama sahiptir. Bu denetimler daha kullanışlı yapabilir ve kullanıcıların daha verimli aramalar için çeşitli geliştirmeler eklenmiştir. Bu konuda bu yeni arama özellikleri hakkında bilgi edineceksiniz ve sistemdeki en iyi kullanım dışı aramaları almak için bazı yararlı ipuçları alacaksınız."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Bilgi bulmak için arama kullanma

İşlemler için Microsoft Dynamics 365 içinde birçok alanları kolayca doğru veya istenen değeri bulmanıza yardımcı olabilir arama sahiptir. Bu denetimler daha kullanışlı yapabilir ve kullanıcıların daha verimli aramalar için çeşitli geliştirmeler eklenmiştir. Bu konuda bu yeni arama özellikleri hakkında bilgi edineceksiniz ve sistemdeki en iyi kullanım dışı aramaları almak için bazı yararlı ipuçları alacaksınız.  

<a name="responsive-lookups"></a>Duyarlı aramalar
------------------

Arama denetimi ile kullanılırken işlemleri için Dynamics 365 önceki sürümlerinde, kullanıcı açılan menüsünü açmak için açık bir eylem etmesi gerekir. Bu yıldız yazarak olabilir (\*) kullanarak veya denetime denetim geçerli değerini temel alarak arama filtre uygulamak için aşağı açılan düğmesini tıklatarak **Alt**+**aşağı ok** klavye kısayolu. Arama denetimleri geçerli web uygulamaları ile daha iyi hizalamak için aşağıdaki şekilde değiştirildi:

-   Arama açılan menüleri şimdi açılır otomatik olarak, açılan ile yazarak, hafif duraklamadan sonra menü içeriklerini arama denetimin değerine göre filtre.
    -   Unutmayın eski yıldız yazdıktan sonra açılan otomatik olarak açma davranışını (\*) düşürülmüştür.
-   Arama açılan menü açtıktan sonra aşağıdaki olur:
    -   İmlecin (odak açılan menü taşımak) yerine arama denetimi içinde kalır böylece denetimin değeri değişiklik yapmak devam edebilirsiniz. Ancak, kullanıcı hala kullanabilirsiniz **yukarı ok** ve **aşağı ok** aþaðý açýlan menüsünden satır değiştirme ve geçerli satır aşağı açılan menüden seçmek için girin.
    -   Arama denetimin değeri için herhangi bir değişiklik yapıldıktan sonra açılır menüsünün içeriğini ayarlar.

Örneğin, adlı bir arama alanı düşünün **Şehir**. 

Odak olduğunda **Şehir** alan, "süt" gibi birkaç harf yazarak istediğiniz şehir arayan başlayabilir  Yazmayı bırakın sonra arama "süt" ile başlayan bu şehirler için filtre otomatik olarak açılır. 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Bu noktada, hala arama alanında imlecidir. "Sütu" değeri olacak şekilde yazmaya devam ederseniz, arama içeriği denetimi son değeri yansıtacak şekilde otomatik olarak ayarlanır. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Odak arama denetimi yine olsa da kullanabilirsiniz **yukarı ok** veya **aşağı ok** tuşlarını kullanarak seçmek istediğiniz satırı vurgulayın. Basarsanız **Enter** vurgulanmış satıra aramasından seçilir ve denetimin değeri güncelleştirilir. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Birden çok kimlik yazmakta
Veri girerken, kullanıcıların bir müşteri veya satıcı, adı yerine bir tanımlayıcıyı temsil eden varlık açısından gibi bir varlık tanımlamak denemek doğaldır. Dynamics 365 işlemleri için geçerli sürümünde, çoğu (ancak tüm) aramaları artık bağlamsal veri girişine olanak verir. Bu güçlü özellik kullanıcı kimliği veya karşılık gelen ad arama denetimi yazmak izin verir. 

Örneğin, düşünün **müşteri hesabı** alan bir satış siparişi oluştururken. Bu alanda gösterilir **hesap kimliği** müşteri, ancak bir kullanıcı genellikle girmek tercih için bir **hesap adı** yerine bir **hesap kimliği** "Orman Wholesales" yerine "ABD-003." gibi bir satış siparişi oluştururken, bu alan için

Kullanıcı girmeye başladı, bir **hesap kimliği** arama denetimine, önceki bölümde açıklandığı şekilde otomatik olarak açılan menüyü açar ve kullanıcı arama aşağıda gösterildiği gibi görür.

[![Müşteri hesap kodu girildiğinde, bağlamsal arama](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Ancak, kullanıcı başına da şimdi girebilirsiniz bir **hesap adı** de. Algılanırsa, kullanıcı şu arama bakın. Bildirimi nasıl **adı** sütun ilk sütunda arama olarak taşındığı ve arama nasıl sıralanmış ve filtre temel **adı** sütun.

[![Müşteri adı girildiğinde, bağlamsal arama](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Daha gelişmiş filtreleme ve sıralama için kılavuz sütun başlıklarını kullanma
Büyük ölçüde önceki iki bölümde ele alınan arama geliştirmeleri satırları bir "ile başlar" arama üzerinde temel alan bir arama gitmek için bir kullanıcının yeteneklerini geliştirmek **ID** veya **adı** arama alanındaki. Ancak, içinde daha gelişmiş filtreleme (veya sıralama) doğru satır bulmak için gerekli durumlar vardır. Bu durumda, kullanıcının arama içinde kılavuz sütun üstbilgileri filtreleme ve sıralama seçeneklerini kullanmak gerekir. Örneğin, bir satış siparişi satırına girerek bir ürün olarak "kablo" sağ bulmak için gereken çalışan düşünün. "Kablo" içine yazmaya **madde numarası** "kablo" ile başlayan hiçbir ürün adları gibi denetim yardımcı değil 

![emptyitemlookup](./media/emptyitemlookup.png) 

Bunun yerine, kullanıcının arama denetiminin değerini temizleyin, arama açılır menüsünü açın ve aşağıda gösterildiği gibi filtre kılavuz sütun başlığını kullanarak açılan menüsü gerekir. Fare (veya dokunma) bir kullanıcı yalnızca tıklatın (dokunmatik filtreleme ve sıralama seçenekleri için o sütundaki erişmek için herhangi bir sütun başlığını veya). Klavye kullanıcı için kullanıcının yalnızca basın gerekir **Alt**+**aşağı****oku** sonra kullanıcı sekme için doğru sütunu ve tuşuna basarak açılan menüye, odağı taşımak için ikinci kez **Ctrl**+**G** kılavuz sütun başlığındaki açılan menüsünü açmak için. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

(Aşağıdaki resme bakın) filtre uygulandıktan sonra bulmak ve her zamanki şekilde satır seçin. 

![filtereditemlookup](./media/filtereditemlookup.png)


