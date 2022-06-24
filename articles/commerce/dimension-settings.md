---
title: Ürün boyutları için görüntü ayarlarını uygulama
description: Bu makale, ürün boyutlarının görüntü ayarlarını kapsar ve Microsoft Dynamics 365 Commerce'de bunların nasıl uygulanacağını açıklar.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7575e205a9732259b00e424f66eeadfe8c659ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899187"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Ürün boyutları için görüntü ayarlarını uygulama

[!include [banner](includes/banner.md)]


Bu makale, ürün boyutlarının görüntü ayarlarını kapsar ve Microsoft Dynamics 365 Commerce'de bunların nasıl uygulanacağını açıklar.

Dynamics 365 Commerce, ürün çeşitlerini ayırt etmek için boyut, stil ve renk boyutlarını destekler. Boyutlar genellikle boyutlar için "Küçük", "Orta" ve "Büyük" ve renkler için "Siyah" ve "Kahverengi" gibi metin değerleri olarak gösterilir. Ancak, bir ürün birçok varyasyonu destekliyorsa her varyasyon için görüntüyü görüntülemek için birden fazla seçim gerektiğinden, ürün varyasyonlarına göz atmak zor olabilir. Ürün varyasyonlarına göz atmayı kolaylaştırmak için, Commerce'in 10.0.20 sürümü, boyutları renk örneği olarak göstermek için görüntüleri ve onaltılık (onaltılık) kodları kullanabilir.

Commerce site oluşturucusunda, boyut ayarları **Site Ayarlar \> Uzantılar \> Boyut Ayarları** altında tanımlanır. Aşağıdaki resimde, site oluşturucudaki boyut ayarlarına bir örnek gösterilmektedir.

![Commerce site oluşturucusunda site ayarları örneği.](./dev-itpro/media/swatch_site_settings.PNG)

İki boyut ayarı kullanılabilir:

- **Görüntü olarak görüntülenecek boyutlar** – Ürün ayrıntıları sayfaları (PDP'ler) ve arama sonuç listesi sayfaları gibi e-ticaret sitesi sayfalarında hangi boyutların renk örneği olarak görünmesi gerektiğini belirtin. Renk, boyut ve stil boyutlarının herhangi bir birleşimi renk örneği olarak gösterilebilir. Renk örneği olarak görüntülenmek üzere bir boyut seçilirse, Commerce modülü işleme, altıgen kod renk örneğinin kullanılabilir bir yapılandırmasını arar. Her iki kod yapılandırılmamışsa, sistem mantığı bir görüntü URL'si renk örneğinin yapılandırmalarını arar. Ne bir altıgen kod ne de bir resim URL'si yapılandırılmamışsa, metin gösterilir.

    Aşağıdaki resimde, bir e-ticaret sitesindeki PDP'nin renk ve boyut örnekleri içerdiği bir örnek gösterilmektedir. Bu örnekte, renk boyutu için bir altıgen kod yapılandırılır. Bu nedenle, renk örnekleri renk olarak gösterilir. Ancak, boyut boyutu için bir altıgen kod veya resim URL'si yapılandırılmaz. Bu nedenle, metin gösterilir.

    ![E-ticaret ürün ayrıntıları sayfasında renk örneği olarak gösterilen renk boyutu örneği.](./dev-itpro/media/swatch_pdp.png)

- **Ürün kartında görüntülenecek boyutlar** – Listelerde ve liste sayfalarında gösterilen ürün kartlarında hangi boyutların görünleneceğini belirtin. Boyutun ürün kartında görünebilmesi için önce bu ayarın bu boyut için etkinleştirilmesi gerekir. **Görüntü olarak görüntülenecek Boyutlar** ayarı da etkinleştirilmelidir. Ürün kartlarındaki renk örneği seçimi davranışı renk boyutu için en iyi duruma getirilmiştir. Diğer boyutlar için renk örneği seçim davranışını özelleştirmek için bir görünüm uzantısı gerekebilir.

    Aşağıdaki resimde, bir e-ticaret sitesindeki liste sayfasının renk örnekleri içeren ürün kartları içerdiği bir örnek gösterilmektedir.

    ![E-ticaret liste sayfasında renk örneği olarak gösterilen renk boyutu örneği.](./dev-itpro/media/swatch_searchresults.PNG)

Ürün boyutlarını site sayfalarında renk örneği olarak gösterilecek şekilde yapılandırma hakkında bilgi için bkz. [Ürün boyutu değerlerini renk örneği olarak görünecek şekilde yapılandırma](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Arama sonuçları modülü](search-result-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Ürün boyutu değerlerini renk örneği olarak görünecek şekilde yapılandırma](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
