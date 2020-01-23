---
title: Üst bilgi modülü
description: Bu konu üstbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885490"
---
# <a name="header-module"></a>Üst bilgi modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu üstbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Üst bilgi modülü, bir sayfanın başlığında gösterilecek tüm modülleri barındırmak için kullanılan özel bir konteynerdir. Örneğin, site logonuzu, gezinti hiyerarşisine bağlantıları, sitedeki diğer sayfalara bağlantıları ve arama çubuğunu içerebilir.

Üst bilgi modülü, sitenin (yani bir masaüstü cihazı veya mobil cihaz) üzerinde göründüğü cihaz için otomatik olarak en iyi duruma getirilmiştir. Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.

## <a name="properties-of-a-header"></a>Üstbilginin özellikleri

Birçok konteyner gibi bir üstbilgi modülü de **başlık** ve **genişlik** için özellikleri destekler.

Üst bilgi modülü birden çok yuvaya sahip. Örneğin, bir bilgi iletisi, gezinme menüsü, logo, arama çubuğu, sepet simgesi, istek listesi simgesi ve hesap bilgileri için yuvalar vardır. Her yuva, belirli bir modül kümesini destekler.

## <a name="modules-that-are-available-in-a-header-module"></a>Üstbilgi modülünde kullanılabilen modüller

Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:

- **Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder. Kanal gezinme hiyerarşisi Dynamics 365 Retail'de yapılandırılabilir. Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür. Ek olarak, statik gezinti bağlantıları yapılandırılabilir ve e-ticaret sitesindeki diğer sayfalara göreli bağlantılar sağlanabilir. Üstbilginin kendisi sola, sağa veya ortaya hizalanabilir.
- **Sepet simgesi** – Sepet simgesi sepeti temsil eden özel bir simgedir. Başlıkta gösterilir ve sepetteki öğelerin sayısını belirtir. Sepet sayfasına bir bağlantı, bir simgenin simgesiyle etkileşimde bulunduklarında sepet sayfasına yönlendirilebilmeleri için, sepet simgesine eşlik etmelidir.
- **İstek listesi simgesi** – Son giriş listesi simgesi başlıkta gösterilir ve müşterinin istek listesine eklenen maddelerin sayısını belirtir. İstek listesi sayfasına bir bağlantı, bu simgesiyle etkileşimde bulunduklarında istek listesi sayfasına yönlendirilebilmeleri için, sepet simgesine eşlik etmelidir.
- **Oturum açma modülü** - Üstbilgide oturum açma modülü gösteriliyor. Müşterilerimiz, hesaplarına oturum açmalarını veya bir hesap için kaydolmasına olanak tanır. Müşteri önceden oturum açmışsa modül hesap sayfası, sipariş geçmişi sayfası veya başka bir sayfaya olan bağlantıları gösterecek şekilde konfigüre edilebilir.
- **Logo modülü** – Bu modül, perakendecileri ve markayı temsil eden logoyu gösterir. Bağlantısı olan bir görüntüdür. Bağlantı genellikle giriş sayfasına yeniden yönlendirilecek şekilde yapılandırılır, böylece müşteriler sitedeki herhangi bir sayfadan giriş sayfasına hızla dönebilir.
- **Uyarı** – Başlıkta bir uyarı görünür ve sitedeki tüm sayfalar için geçerli olan bir satır içi iletiyi göstermek için kullanılır. Örneğin, bir uyarı "Yıllık satış 2 günde bitiyor" gibi bir mesaj gösterebilir.
- **Arama çubuğu** – Arama çubuğu kullanıcıların ürün arayabilmeleri için arama terimleri girmesine izin verir. Modül, arama sonuçları sayfasının URL'siyle konfigüre edilmelidir. Sorgu dizesi parametresi yapılandırılabilir (varsayılan değer **"q"** dir). Arama çubuğu, otomatik önerme modülünün eklenmesi gereken bir autoönerme yuvasına sahiptir.
- **Otomatik öner** – otomatik öner modülü otomatik olarak önerilen sonuçları gösterir. Bu sonuçlar anahtar sözcükler, ürünler veya arama teriminin bulunduğu kategoriler olabilir.

## <a name="create-a-header-module"></a>Başlık modülü oluşturma

Bir üst bilgi modülü oluşturmak için şu adımları izleyin.

1. Üstbilgi modülü içeren bir sayfa parçası oluşturun.
1. Üstbilgi modülündeki yuvalara modüller ekleyin.
1. Her modülün ayarlarını güncelleştirin.
1. Sayfa parçasını kaydedin. 
1. Sayfayı giriş yapın ve yayımlayın.

Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.

1. Varsayılan sayfada üstbilgi modülünü içeren sayfa parçasını ana yuvadaki üstbilgiye ekleyin.
1. Şablonu kaydedin. 
1. Şablonu giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
