---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411262"
---
# <a name="header-module"></a>Üst bilgi modülü

[!include [banner](includes/banner.md)]

Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce'te sayfa üst bilgisi; başlık, gezinti menüsü, arama, promosyon başlığı ve tanımlama bilgisi izin modülleri gibi birden çok modülü kapsar. 

Üst bilgi modülü bir site logosu, gezinti hiyerarşisine bağlantılar, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu içerir. Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir. Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.

Aşağıdaki resimde giriş sayfasında kullanılan bir üstbilgi modülü örneği gösterilmektedir.

![üstbilgi modülü örneği](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Üst bilgi modülünün özellikleri

Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler. 

**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır. Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md). 

**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.

## <a name="modules-that-are-available-in-a-header-module"></a>Üstbilgi modülünde kullanılabilen modüller

Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:

- **Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder. Kanal gezinme hiyerarşisi Dynamics 365 Commerce'de yapılandırılabilir. Gezinti menüsünde, Retail Server gezinti menüsü öğelerini ve statik menü öğelerini bir kaynak olarak belirtmek için kullanılan bir **Gezinti Kaynağı** özelliği vardır. Statik menü öğeleri kaynak olarak belirtilirse, sitedeki diğer sayfalara göreli bağlantılar sağlanabilir. Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür. 

- **Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir. **Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir. Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır. Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.

- **Sepet simgesi** - Sepet simgesi modülü, belirli bir zamanda sepetteki öğelerin sayısını gösteren sepet simgesini temsil eder. Daha fazla bilgi için bkz. [Sepet simgesi modülü](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Sayfa için üst bilgi modülü oluşturma

Bir üst bilgi modülü oluşturmak için şu adımları izleyin.

1. **Sayfa Parçaları**'na gidin ve yeni parçası oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa parçası** iletişim kutusunda **Konteyner** modülünü seçin, sayfa parçası için bir ad girin ve sonra **Tamam**'ı seçin.
1. **Varsayılan kapsayıcı** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Konteyneri doldur** olarak ayarlayın.
1. **Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Promosyon başlığı** ve **Çerez izni** modüller'i seçin, ve **Tamam**'ı seçin.
1. **Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Konteyneri doldur** olarak ayarlayın.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Başlık** modülünü seçin ve **Tamam**'ı seçin.
1. Başlık modülünü içeren **Gezinti menüsü** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Gezinti meüsü** modülünü seçin ve **Tamam**'ı seçin.
1. Gezinti menüsü modülünün özellik bölmesinde, özelliklerini yapılandırın.
1. Başlık modülünü içeren **Ara** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Ara** modülünü seçin ve **Tamam**'ı seçin.
1. Arama modülünün özellik bölmesinde, özelliklerini yapılandırın.
1. Başlık modülünü içeren **Sepet simgesi** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Sepet simgesi** modülünü seçin ve **Tamam**'ı seçin.
1. Sepet simgesi modülünün özellik bölmesinde, özelliklerini yapılandırın. Kullanıcılar üzerinde gezinirken, sepet simgesinin bir sepet Özeti (mini sepet olarak da bilinir) göstermesini istiyorsanız, **mini sepeti göster**'i seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.

1. **Varsayılan sayfanın** **üstbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
