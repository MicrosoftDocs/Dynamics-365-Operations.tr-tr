---
title: Giriş sayfasına genel bakış
description: Bu konu Microsoft Dynamics 365 Commerce'te giriş sayfası hakkında bilgi sağlar.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ebc8b4ebd3720815cdaaab708fbfdd8302cbea1
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817766"
---
# <a name="home-page-overview"></a>Giriş sayfasına genel bakış

[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 Commerce'te giriş sayfası hakkında bilgi sağlar.

## <a name="overview"></a>Genel Bakış

Giriş sayfası, alışverişçilerin bir e-ticaret sitesini ziyaret ettiklerinde gideceği varsayılan sayfasıdır. Tipik olarak bu sayfa, ürünler ve promosyonlar için pazarlama modüllerinin bir birleşimini kullanarak servis talebi kullanır. Alışverişçileri bağlı tutmak için ana sayfa, görüntü ve metinle zengin olmalıdır.

Aşağıdaki çizimde, modül kitaplığı ve "Fabrikam" teması kullanılarak oluşturulmuş bir ana sayfa örneği gösterilmektedir.

![Giriş sayfası örneği](./media/Homepage2.PNG)

Giriş sayfanın üst bölümünde, perakendecinin müşterilerin göz atmasını istediği tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır. Giriş sayfanın alt bölümünde, bir müşterilerin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.

Giriş sayfasının ana bölümü, ürünleri, kategorileri veya yükseltmeleri çeşitli Dynamics 365 Commerce modüller kullanarak vurgulayabilir:

- **Hero** – Genel olarak, ana bölümün başındaki ilk öğe, depodaki yeni ürünleri ve promosyonları vurgulayan bir veya daha fazla "kahraman" görüntüsü gösterir. Birden çok Hero görüntü varsa, kullanıcıların onlara gözatabilmeleri için bir döngü modülü içinde barındırılır.

    Aşağıdaki şekilde, ana bölümdeki ilk öğenin "Yeni Varış" adı adlı bir içerik blokunun hero modülü olduğu giriş sayfası örneği gösterilmektedir.

    ![Hero modülü örneği](./media/Hero.PNG)

- **Özellik** - İçerik bloku modülünün özellik düzeni, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır. Özellik düzenleri bağımsız olarak kullanılabilir veya bir döngü modül içinde barındırılabilir.

    Aşağıdaki resimde, özellik düzenine sahip bir içerik bloğu modülü örneği gösterilmektedir.

    ![Özellik modülleri örnekleri](./media/Feature.PNG)

- **Kutucuk** – bir içerik bloku modülü kutucuk düzeni, çok sütunlu bir düzende bir görüntü ve metin bileşimi kullanarak birden fazla ürün veya ürün kategorisini sergileyerek kullanılır. Bu konunun başlarında görünen bir giriş sayfası gösterimde, **Alışveriş kadınlar**, **Alışveriş erkek** ve **Alışveriş Aksesuarları** kalemlerin üç sütunlu düzeni için içerik yerleşim modülü kullanılır.
- **Video oynatıcı** – Bir video oynatıcı modülü giriş sayfasındaki video içeriğini sergileyebilecek şekilde kullanılabilir. Bu konunun yukarısında görünen bir giriş sayfasının resmi bir video oynatıcı modülü içerir.
- **Metin bloku** – İçerik zengin blok modülü, giriş sayfasındaki metin içeriğini tek sütunlu veya birden çok sütunlu düzende göstermek için kullanılabilir.
- **Ürün önerileri** – Ürün önerileri modülleri, giriş sayfasında **yeni**, **trend** ve **en iyi satış** gibi listeleri göstermek için kullanılır. Bu listeler, ürünleri alışveriş eğilimlerine göre görüntüler ve bunlar algoritmik oluşturulabilir veya el ile başlatılabilir. Müşterilerin önde gelen ürünleri bulmasına ve alışveriş yapmaya devam etmesine yardımcı olurlar.

    Aşağıdaki çizimde giriş sayfasındaki ürün önerileri modüllerinin bir örneği gösterilmektedir.

    ![Ürün öneri modüllerine örnekler](./media/Recommendations.PNG)

> [!NOTE]
> Burada listelenen tüm modüller herhangi bir site sayfasında kullanılabilir. Ancak, müşteriler siteyle ilk kez etkileşimde bulunduğu için, giriş sayfasındaki yerleşimleri önemlidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün ayrıntıları sayfalarına genel bakış](quick-tour-pdp.md)

[Sepet ve ödeme sayfalarına genel bakış](quick-tour-cart-checkout.md)

[Hesap yönetimi sayfalarına genel bakış](quick-tour-account-management.md)
