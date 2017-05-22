---
title: "Eylem Araması"
description: "Bu makalede, Microsoft Dynamics 365 for Operations&quot;daki arama işlevi eylemi açıklanmaktadır. Eylem arama, bir sayfadaki eylemleri bulmanıza ve çalıştırmanıza yardımcı olur."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2ff12088d432d3e8693dfd9662cb0ead82fd0191
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="action-search"></a>Eylem Araması

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Operations'daki arama işlevi eylemi açıklanmaktadır. Eylem arama, bir sayfadaki eylemleri bulmanıza ve çalıştırmanıza yardımcı olur.

<a name="introduction"></a>Giriş
------------

Microsoft Dynamics 365 for Operations'taki sayfalar, başlıca Eylem Panoları üzerindeki komutları ortaya çıkartır, hem sayfanın üzerinde görünen standart Eylem Panosu hem de sayfanın çeşitli yerlerinde görünen araç çubukları. Önceki sürümlerde, Anahtar İpuçları özelliği, Eylem Panosu üzerindeki herhangi bir düğmeye, Alt tuşu ve daha sonra bir dizi harfe basarak hızla erişmenize izin veriyordu. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Ancak, Dynamics 365 for Operations'ın güncel sürümünde, Tuş İpuçları artık kullanılmamakta olup yerine eylem arama özelliği gelmiştir. Bu yeni özellik, görünen herhangi bir Eylem Bölmesinden bir düğmeyi hızla aramanıza ve düğmeyi çalıştırmanıza olanak sağlar.

## <a name="using-action-search"></a>Eylem aramasını kullanma
Eylem arama özelliğini kullanmak için aşağıdaki adımları izleyin.

1.  Eylem bölmesinde, **eylem arama** alanına tıklayın. (**Eylem arama** alanı bir büyüteç simgesi içerir.)
2.  Çalıştırmak istediğiniz düğmenin adının tamamını veya bir kısmını yazın. Düğmenin "yolu" üzerindeki kelimeleri de kullanarak arayabilirsiniz. (Daha fazla bilgi için, bu makalenin sonraki bölümüne bakın.) Genellikle bir düğme, siz iki - dört karakter arasında yazdığınızda sonuç listesinin üstüne yakın bir yerde görünür.
3.  Sonuçlar listesinde (fare ya da klavyenizi kullanarak) düğmeyi bulun ve çalıştırın.

Düğmeyi çalıştırdıktan sonra, çalışmaya devam edebilmeniz için sayfadaki son konumunuz yeniden ön plana geçer. 

[![eylem-arama-alanı](./media/action-search-field.png)](./media/action-search-field.png)

Eylem aramasını Ctrl+/ veya Alt+Q tuşuna basarak da başlatabilirsiniz. Sayfadaki son konumunuzu yeniden ön plana almak için klavye kısayoluna tekrar basın.

## <a name="understanding-the-results-list"></a>Sonuç listesini anlama
Dynamics 365 for Operations içerisinde bir düğmenin amacını tamamen anlamak için çoğu zaman bu düğmenin hem konumunu hem de bağlamını bilmeniz gerekir. Bu nedenle, size tam olarak hangi düğmenin listede göründüğünü anlamanıza yardımcı olmak için her bir öğe için ek bilgiler sonuç sayfasında görüntülenir. Özellikle, düğmenin "yol"u gösterilir. Bu yol, ilgili olarak, aşağıdaki Kullanıcı Arabirimi öğelerini içerebilir:

-   Eylem Bölmesi öğesi
-   Düğme grubu
-   Menü düğmesi (düğme bir menü düğmesi içinde ise)
-   Menü ayırıcı (düğme bir menü düğmesi içindeki adlandırılmış bir grup içinde ise)
-   Sayfadaki grup veya öğe (örneğin, bir Hızlı Sekmenin adı)

Örneğin, **eylem arama** alanına **top** yazdınız ve şimdi sonuçlar listesini inceliyorsunuz. Bir düğme için ilk girişte **Toplamlar** adına sahiptir ve vurgulanır. **Satış siparişi** &gt; **Görünüm** düğme yolu da gösterilir. **Satış siparişi**, Eylem Panosunda **Satış siparişi**'ne karşılık gelen yolun parçasıdır ve yolun **Görünüm** parçası, o sekmedeki **Görünüm** grubuna karşılık gelir. Benzer şekilde, **Toplam iskonto** düğmesinin yolu (**Sat** &gt; **Hesapla**), bu düğmenin Eylem Panosu üzerindeki **Satış** sekmesinde bulunan **Hesapla** grubu üzerinde bulunduğunu bildirir. Bu nedenle, bu bilgi size tam olarak hangi düğmenin hangi eylem arama tarafından tetiklendiğini anlamanıza yardımcı olur (düğmeyi sonuç listesinden seçerseniz). 

[![eylem-arama-alan-ile-veri](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Önceki örnekte, eylem arama bir sayfanın en üstündeki standart Eylem Bölmesi'nden sonuçları göstermiştir. Bununla birlikte, eylem arama sayfada başka yerlerde bulunan görünür araç çubuklarından sonuçları da gösterir. Örneğin **Satış siparişleri satırı** hızlı sekmesi üzerindeki **Eldeki stok** düğmesini arıyorsanız. Bu durumda, sonuç sayfasındaki düğme yolu (**Satış siparişi satırları** &gt; **Stok** &gt; **Görünüm**), bu düğmenin **Satış siparişleri satırları** hızlı sekmesi üzerindeki **Stok** menü düğmesindeki **Görünüm** başlığı altında bulunduğunu belirtir. 

[![eldeki-stok](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Eylem arama - Gezinti arama karşılaştırması
Eylem arama ile bir sayfadaki eylemleri bulup çalıştırma amaçlanırken, Dynamics 365 for Operations'ta sayfaları bulup gezinmek için ayrı bir arama mekanizması bulunur. Bu özellik hakkında daha fazla bilgi için, bkz. [Gezinti arama](navigation-search.md) makalesi.



