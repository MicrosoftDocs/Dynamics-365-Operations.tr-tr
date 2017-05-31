---
title: "Alan açıklamalarını görüntüleme ve dışarı aktarma"
description: "Bu makalede, alan açıklamalarının nasıl görüntüleneceği ve açıklamaları dışa aktarmak için Alan açıklamalarının nasıl kullanılacağı açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cd84c03baa4f7a9d38e380c37ed2020ee3387954
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="view-and-export-field-descriptions"></a>Alan açıklamalarını görüntüleme ve dışarı aktarma

[!include[banner](../includes/banner.md)]


Bu makalede, alan açıklamalarının nasıl görüntüleneceği ve açıklamaları dışa aktarmak için Alan açıklamalarının nasıl kullanılacağı açıklanmaktadır.

Microsoft Dynamics 365 for Operations'ın karmaşık alanlarından bazıları için açıklamaları bulunur. Bu açıklamalar, alanın üzerine geldiğinizde görünür. Ayrıca, **Alan açıklamaları** sayfasından alan açıklamalarını görüntüleyebilir ve dışa aktarabilirsiniz. 

Tüm sayfaların alan açıklamaları yoktur. Kullanımı belirgin olan alanların değil, yalnızca daha karmaşık alanların açıklamalarını sağlamak istiyoruz. Bu nedenle, bazı sayfalarda alan açıklamaları bulunmaz, bazı sayfalarda birkaç açıklama vardır ve parametre sayfaların çoğunda olduğu gibi daha karmaşık sayfalarda birçok açıklama vardır. 

Microsoft Dynamics 365 for Operations geliştirme ortamına erişiminiz varsa yeni alan açıklamalarınızı ekleyebilirsiniz ve mevcut açıklamaları özelleştirebilirsiniz. Örneğin, bir alan açıklamasına şirkete özgü bilgiler ekleyebilirsiniz. Daha fazla bilgi için, [Alanı özelleştirme yardımı](/dynamics365/operations/dev-itpro/user-interface/customize-field-help) sayfasına bakın.

## <a name="see-field-descriptions-in-the-user-interface"></a>Kullanıcı arabirimindeki alan açıklamalarına bakın
Alanın üzerine getirerek alan açıklamaları görüntüleyebilirsiniz. Açıklama yoksa, üzerine getirdiğinizde alan adını görürsünüz. (Not: 7.0.0 sürümünde alan açıklamaları yalnızca **Alan açıklamaları** sayfasında görüntülenebilir.) Aşağıdaki şekilde, **Sayım sırasında madde kilitlemesi** alanına fare imlecini getirdiğiniz zaman görünen alan açıklaması gösterilmektedir. 

[![Alan açıklaması örneği](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Alan açıklamaları sayfasını kullanarak alan yardımını görüntüleme ve dışa aktarma
**Alan açıklamaları** sayfası, alan açıklamalarını görüntülemenizi ve dışarı aktarmanızı sağlar. Tek seferde bir sayfa için mevcut olan açıklamaları görebilirsiniz.

### <a name="view-the-descriptions-for-a-page"></a>Bir sayfanın açıklamalarını görüntüleme

Bir sayfanın açıklamalarını görüntülemek için, aşağıdaki adımı izleyin.

-   **Sayfa seç** alanında, sayfanın adını yazın. Alternatif olarak, tüm sayfaların bir listesini açmak için oka tıklayın ve ardından listeye göz atın veya filtreleyin.

Kullanıcı arabiriminde (UI) gösterilen sayfa adını (örneğin, **Müşteriler**) veya bir sayfaya sağ tıkladığınızda görebileceğiniz (örneğin, **CustTable**) kod adını (AOT adı) kullanabilirsiniz. 

Sayfalar listesini filtrelemenin çeşitli yolları hakkında daha fazla bilgi için bu makalenin ilerisindeki "Sayfa arama" bölümüne bakın. 

**Açıklama olmayan alanları ekle** seçeneğini **Evet** olarak ayarlarsanız, sayfadaki tüm alanlar, alan açıklaması olmasa bile gösterilir.

### <a name="export-the-descriptions-for-a-page"></a>Bir sayfanın açıklamalarını dışarı aktarma

Bir sayfanın açıklamalarını dışa aktarmak için, aşağıdaki adımları izleyin.

1.  **Sayfa seçin** alanından bir sayfa seçin.
2.  Sağ üst köşedeki **Microsoft Office'te aç** düğmesine tıklayın ve ardından **FieldDescriptionTmp** öğesine tıklayın.

### <a name="searching-for-a-page"></a>Sayfa arama

**Sayfa seçin** alanında sayfa aramanın çeşitli yolları vardır. Çoğu durumda, açılır listeyi açmak için **Sayfa seçin** alanındaki oka tıklamanız ve ardından filtrelenmiş sayfa listesinden seçim yapmanız gerekir.

-   Adın bir bölümünü yazın ve ardından filtrelenmiş sayfa listesinden seçim yapmak için açılır listeyi açın.
-   Açılır listeyi açın ve ardından listenin en üstündeki **Sayfa adı** başlığına veya **Sayfa AOT adı** başlığına tıklayın. **Sayfa adı şununla başlar** gibi gelişmiş filtreleme seçeneklerini kullanabileceğiniz bir iletişim görüntülenir.
-   Sayfanın tam adını yazın. Bu seçeneği kullandığınızda, alan açıklamaları gösterilse bile açılır listeyi açıp listedeki diğer sayfalara da bakmanızı öneririz.
    -   Ad için tek bir eşleşme varsa bu sayfanın alan açıklamaları gösterilir.
    -   Birden fazla tam eşleşme varsa hiçbir açıklama gösterilmez. Açılır listeyi açıp istediğiniz sayfayı seçmelisiniz.
    -   Yazdığınız ad, başka bir sayfanın adının parçası ise sayfanızın açıklamalarını görürsünüz. Ancak, açılır listeyi açarsanız bu adı içeren ek sayfaları da görürsünüz.

Örneğin ****Sayfa seçin**** alanında **Sayım** yazarken hiçbir açıklama gösterilmez. Açılır listeyi açın ve adı **Sayım** olan iki sayfa ve adı, "Sayım" kelimesini içeren birkaç sayfa olduğunu görün. AOT adı **InventJournalCount** olan sayfayı seçerseniz, bu sayfanın alan açıklamaları gösterilir. Ancak açılır listeyi yeniden açarsanız listenin artık AOT adında "InventJournalCount" geçen tüm sayfaları içerdiğini görürsünüz.

## <a name="troubleshooting"></a>Sorun Giderme
Bu bölüm, alan açıklamalarını kullanırken karşılaşabileceğiniz sorunları gidermenize yardımcı olacak bilgiler içerir.

### <a name="i-cant-find-a-field-description"></a>Bir alanın açıklamasını bulamıyorum

Daha karmaşık alanların açıklamalarını eklemeye devam ediyoruz. Belirli bir alanla ilgili yardım gereksiniminiz varsa bu konuya yorum ekleyerek bize bildirin.

### <a name="the-field-description-isnt-helpful"></a>Alan açıklaması yardımcı olmuyor

Bu konuya yorum ekleyerek bize bildirin. Yapabiliyorsanız ihtiyacınız olan ek bilgileri açıklayın.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Alan açıklamaları sayfasında bir alanı bulamıyorum

Bir sayfadaki tüm alanları görüntülemek için **Açıklama olmayan alanları dahil et** seçeneğini **Evet** olarak ayarlayın. Doğru sayfayı seçtiğinizi doğrulamak için **Sayfa seçin** alanına tıklayın. Yazdığınız ad, başka bir alan adının parçası ise, daha uzun ada sahip olan sayfayı seçmiş olabilirsiniz.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Alan açıklamaları sayfasında bir sayfayı bulamıyorum.

Sayfaları aramanın çeşitli yolları hakkında daha fazla bilgi için, bu makalede daha önceki "Sayfa arama" bölümüne bakın. Sayfanın tam adını yazdıysanız ve aynı adlı birden fazla sayfa varsa alan açıklamaları gösterilemeyebilir. **Sayfa seçin** alanındaki oka tıklayarak kullanılabilir sayfaların filtrelenmiş bir listesini açın.

<a name="see-also"></a>Ayrıca bkz.
--------

[Alanı özelleştirme yardımı](/dynamics365/operations/dev-itpro/user-interface/customize-field-help)





