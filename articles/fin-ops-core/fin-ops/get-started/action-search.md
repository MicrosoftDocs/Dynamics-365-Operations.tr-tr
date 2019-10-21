---
title: Eylem arama
description: Bu makale, eylem arama işlevini açıklar. Eylem arama, bir sayfadaki eylemleri bulmanıza ve çalıştırmanıza yardımcı olur.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d01247aa356625cb759306e5ead2afd3cdeb840f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191328"
---
# <a name="action-search"></a>Eylem arama

[!include [banner](../includes/banner.md)]

Bu makale, eylem arama işlevini açıklar. Eylem arama, bir sayfadaki eylemleri bulmanıza ve çalıştırmanıza yardımcı olur.

## <a name="introduction"></a>Giriş

Sayfalar, başlıca Eylem Panoları üzerindeki komutları ortaya çıkartır: sayfanın üzerinde görünen standart Eylem Panosu ve sayfanın çeşitli yerlerinde görünen araç çubukları. Önceki sürümlerde, Anahtar İpuçları özelliği, Eylem Panosu üzerindeki herhangi bir düğmeye, Alt tuşu ve daha sonra bir dizi harfe basarak hızla erişmenize izin veriyordu.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Anahtar İpuçları artık kullanılamaz, ancak yerine eylem arama özelliği getirilmiştir. Bu yeni özellik, görünen herhangi bir Eylem Bölmesinden bir düğmeyi hızla aramanıza ve düğmeyi çalıştırmanıza olanak sağlar.

## <a name="using-action-search"></a>Eylem aramasını kullanma

Eylem arama özelliğini kullanmak için aşağıdaki adımları izleyin.

1. Eylem bölmesinde, **eylem arama** alanına tıklayın. (**Eylem arama** alanı bir büyüteç simgesi içerir.)
2. Çalıştırmak istediğiniz düğmenin adının tamamını veya bir kısmını yazın. Düğmenin "yolu" üzerindeki kelimeleri de kullanarak arayabilirsiniz. (Daha fazla bilgi için, bu makalenin sonraki bölümüne bakın.) Genellikle bir düğme, siz iki - dört karakter arasında yazdığınızda sonuç listesinin üstüne yakın bir yerde görünür.
3. Sonuçlar listesinde (fare ya da klavyenizi kullanarak) düğmeyi bulun ve çalıştırın.

Düğmeyi çalıştırdıktan sonra, çalışmaya devam edebilmeniz için sayfadaki son konumunuz yeniden ön plana geçer.

[![eylem-arama-alanı](./media/action-search-field.png)](./media/action-search-field.png)

Eylem aramasını Ctrl+/ veya Alt+Q tuşuna basarak da başlatabilirsiniz. Sayfadaki son konumunuzu yeniden ön plana almak için klavye kısayoluna tekrar basın.

## <a name="understanding-the-results-list"></a>Sonuç listesini anlama

Bir düğmenin amacını tamamen anlamak için çoğu zaman bu düğmenin hem konumunu hem de bağlamını bilmeniz gerekir. Bu nedenle, size tam olarak hangi düğmenin listede göründüğünü anlamanıza yardımcı olmak için her bir öğe için ek bilgiler sonuç sayfasında görüntülenir. Özellikle, düğmenin "yol"u gösterilir. Bu yol, ilgili olarak, aşağıdaki Kullanıcı Arabirimi öğelerini içerebilir:

- Eylem Bölmesi öğesi
- Düğme grubu
- Menü düğmesi (düğme bir menü düğmesi içinde ise)
- Menü ayırıcı (düğme bir menü düğmesi içindeki adlandırılmış bir grup içinde ise)
- Sayfadaki grup veya öğe (örneğin, bir Hızlı Sekmenin adı)

Örneğin, **eylem arama** alanına **top** yazdınız ve şimdi sonuçlar listesini inceliyorsunuz. Bir düğme için ilk girişte **Toplamlar** adına sahiptir ve vurgulanır. **Satış siparişi** &gt; **Görünüm** düğme yolu da gösterilir. Yolun **Satış siparişi** parçasına karşılık gelen **Satış siparişi** sekmesi, Eylem bölmesinde ve yolun **Görüntüle** parçasına karşılık gelen o sekmede **Görüntüle** grubunda. Benzer şekilde **Toplam indirim** düğmesi (**Sat** &gt; **Hesapla**), bu düğmenin **Hesapla** grubunda, Eylem bölmesinin **Sat** sekmesinde olduğunu size belirtir. Bu nedenle, bu bilgi size tam olarak hangi düğmenin hangi eylem arama tarafından tetiklendiğini anlamanıza yardımcı olur (düğmeyi sonuç listesinden seçerseniz).

[![eylem-arama-alan-ile-veri](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Önceki örnekte, eylem arama bir sayfanın en üstündeki standart Eylem Bölmesi'nden sonuçları göstermiştir. Bununla birlikte, eylem arama sayfada başka yerlerde bulunan görünür araç çubuklarından sonuçları da gösterir. Örneğin **Satış siparişleri satırı** hızlı sekmesi üzerindeki **Eldeki stok** düğmesini arıyorsanız. Bu durumda, sonuç sayfasındaki düğme yolu (**Satış siparişi satırları** &gt; **Stok** &gt; **Görünüm**), bu düğmenin **Satış siparişleri satırları** hızlı sekmesi üzerindeki **Stok** menü düğmesindeki **Görünüm** başlığı altında bulunduğunu belirtir.

[![eldeki-stok](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Eylem arama - Gezinti arama karşılaştırması

Eylem arama ile bir sayfadaki eylemleri bulup çalıştırma amaçlanırken, sayfaları bulup gezinmek için ayrı bir arama mekanizması bulunur. Bu özellik hakkında daha fazla bilgi için, bkz. [Gezinti arama](navigation-search.md) makalesi.
