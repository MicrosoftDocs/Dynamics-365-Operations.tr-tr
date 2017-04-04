---
title: "Eylem Araması"
description: "Bu makalede, Microsoft Dynamics 365 işlemleri için eylem arama işlevleri açıklanır. Eylem Arama Bul ve bir sayfada çalışma Eylemler yardımcı olur."
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
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Eylem Araması

Bu makalede, Microsoft Dynamics 365 işlemleri için eylem arama işlevleri açıklanır. Eylem Arama Bul ve bir sayfada çalışma Eylemler yardımcı olur.

<a name="introduction"></a>Giriş
------------

Sayfaları Microsoft Dynamics 365 işlemleri için öncelikle eylem bölmeleri, sayfanın en üstünde görünen standart eylem bölmesi hem sayfasının çeşitli bölümlerine görünen araç çubukları üzerindeki komutları ortaya çıkarır. Önceki sürümlerinde, Alt tuşu ile bir dizi harf tuşlarına basarak herhangi bir eylem bölmesi düğmesini hızlı erişim anahtarı ipucu özelliği sağlar. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Dynamics 365 işlemleri için geçerli sürümünde, anahtar ipuçları artık kullanılabilir ancak, eylem arama özelliği tarafından değiştirildi. Bu yeni özellik, görünen herhangi bir Eylem Bölmesinden bir düğmeyi hızla aramanıza ve düğmeyi çalıştırmanıza olanak sağlar.

## <a name="using-action-search"></a>Eylem aramasını kullanma
Eylem arama özelliğini kullanmak için aşağıdaki adımları izleyin.

1.  Eylem bölmesinde, **eylem arama** alanına tıklayın. (**Eylem arama** alanı bir büyüteç simgesi içerir.)
2.  Çalıştırmak istediğiniz düğmenin adını bir bölümünü veya tümünü yazın. Düğmenin "yolu." sözcükleri kullanarak da arama yapabilirsiniz (Daha fazla bilgi için bu makalenin sonraki bölümüne bakın.) Genellikle, iki ile dört karakter yazdıktan sonra bir düğme Sonuçlar listesinin en üstüne yakın görünür.
3.  Sonuçlar listesinde (fare ya da klavyenizi kullanarak) düğmeyi bulun ve çalıştırın.

Düğmeyi çalıştırdıktan sonra, çalışmaya devam edebilmeniz için sayfadaki son konumunuz yeniden ön plana geçer. 

[![Eylem arama alanı](./media/action-search-field.png)](./media/action-search-field.png)

Eylem aramasını Ctrl+/ veya Alt+Q tuşuna basarak da başlatabilirsiniz. Sayfadaki son konumunuzu yeniden ön plana almak için klavye kısayoluna tekrar basın.

## <a name="understanding-the-results-list"></a>Sonuç listesini anlama
Genellikle, operasyonlar için Dynamics 365 içinde hem konumu hem de tamamen bu düğmenin amacını anlamak için bir düğme bağlamında bilmelisiniz. Bu nedenle, ek bilgi sonuçlar listesindeki her öğe için tam olarak anlamanıza yardımcı olmak için görüntülenecek düğmeleri listesinde gösterilir. Özellikle, düğmenin "yol"u gösterilir. Bu yol, ilgili olarak, aşağıdaki Kullanıcı Arabirimi öğelerini içerebilir:

-   Eylem Bölmesi öğesi
-   Düğme grubu
-   Menü düğmesi (düğme bir menü düğmesi içinde ise)
-   Menü ayırıcı (düğme bir menü düğmesi içindeki adlandırılmış bir grup içinde ise)
-   Sayfadaki grup veya öğe (örneğin, bir Hızlı Sekmenin adı)

Örneğin, **eylem arama** alanına **top** yazdınız ve şimdi sonuçlar listesini inceliyorsunuz. Adlı bir düğme ilk girişi **toplam**, vurgulanır. Bir düğme yolunu **satış sipariş**&gt;**Görünüm** de gösterilir. **Satış siparişi** karşılık gelen yolun bir parçası **satış siparişi** eylem bölmesinde, Genel sekmesinde ve **Görünüm** karşılık gelen yolun bir parçası **Görünüm** o sekmesindeki grup. Benzer şekilde, yolunu **toplam iskonto** düğmesini (**satmak**&gt;**Hesapla**) Bu düğme bulunan bildirir **Hesapla** üzerinde Grup **satmak** sekmesinde eylem bölmesinin. Bu nedenle, bu bilgileri (Bu düğme sonuçlar listesinde öğesini seçerseniz) tam olarak hangi düğme eylemi aramada tetiklenip anlamanıza yardımcı olur. 

[![Eylem-arama-alan-ile-veri](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Önceki örnekte, eylem arama bir sayfanın en üstündeki standart Eylem Bölmesi'nden sonuçları göstermiştir. Bununla birlikte, eylem arama sayfada başka yerlerde bulunan görünür araç çubuklarından sonuçları da gösterir. Örneğin, aradığınız **, eldeki stok** üzerinde bulunan düğme **satış siparişi satırları** hızlı. Bu durumda, sonuçlar listesinde düğme yolunu (**satış siparişi satırları**&gt;**stok**&gt;**Görünüm**) Bu düğme altında bulunduğunu bildirir **Görünüm** üzerinde başlık **stok** menü düğmesinde **satış siparişi satırları** hızlı. 

[![üzerinde-eldeki-stok](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Eylem arama - Gezinti arama karşılaştırması
Eylem Arama Bul ve bir sayfada eylemleri çalıştırmak için ise, bulmak ve işlemleri için Dynamics 365 sayfalarında gezinme için bir ayrı bir arama mekanizması yoktur. Bu özellik hakkında daha fazla bilgi için bkz: [Gezinti arama](navigation-search.md) makale.


