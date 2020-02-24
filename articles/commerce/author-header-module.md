---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025721"
---
# <a name="header-module"></a>Üst bilgi modülü


[!include [banner](includes/banner.md)]

Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce'te sayfa üst bilgisi; başlık, gezinti menüsü, arama, promosyon başlığı ve tanımlama bilgisi izin modülleri gibi birden çok modülü kapsar. 

Üst bilgi modülü bir site logosu, gezinti hiyerarşisine bağlantılar, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu içerir. Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir. Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.

## <a name="properties-of-a-header-module"></a>Üst bilgi modülünün özellikleri

Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler. 

**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır. Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md). 

**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.

## <a name="modules-that-are-available-in-a-header-module"></a>Üstbilgi modülünde kullanılabilen modüller

Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:

- **Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder. Kanal gezinme hiyerarşisi Dynamics 365 Commerce'de yapılandırılabilir. Gezinti menüsünde, Retail Server gezinti menüsü öğelerini ve statik menü öğelerini bir kaynak olarak belirtmek için kullanılan bir **Gezinti Kaynağı** özelliği vardır. Statik menü öğeleri kaynak olarak belirtilirse, sitedeki diğer sayfalara göreli bağlantılar sağlanabilir. Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür. 
- **Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir. **Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir. Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır. Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.

## <a name="create-a-header-module-for-a-page"></a>Sayfa için üst bilgi modülü oluşturma

Bir üst bilgi modülü oluşturmak için şu adımları izleyin.

1. **Üst bilgi parçası** olarak adlandırılan bir parça oluşturun ve buna bir kapsayıcı modülü ekleyin.
1. Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.
1. Kapsayıcı modülüne promosyon başlığı ve tanımlama bilgisi izin modülleri ekleyin.
1. Parçaya başka bir kapsayıcı modülü ekleyin ve **Genişlik** özelliğinin ayarını **Kapsayıcıya sığdır** yapın.
1. İkinci kapsayıcı modülüne bir üst bilgi modülü ekleyin.
1. Üst bilgi modülünün **Gezinti menüsü** yuvasında bir gezinti menüsü modülü ekleyin. 
1. Gezinti menüsü modülünün özellik bölmesinde, gezinti menüsü modülünün özelliklerini yapılandırın.
1. Üst bilgi modülünün **Arama** yuvasında bir arama modülü ekleyin. 
1. Arama modülünün özellik bölmesinde, arama modülünün özelliklerini yapılandırın. 
1. Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın. 

Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.

1. Varsayılan sayfanın **Ana** yuvasında, üst bilgi modülünü içeren üst bilgi sayfa parçasını üst bilgiye ekleyin.
1. Şablonu kaydedin, düzenlemeyi bitirin ve sonra yayınlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
