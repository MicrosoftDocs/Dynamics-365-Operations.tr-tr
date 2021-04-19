---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b14178431b281daa827749781dd16481f8bfb74
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799936"
---
# <a name="header-module"></a>Üst bilgi modülü

[!include [banner](includes/banner.md)]

Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.

Dynamics 365 Commerce'de sayfa üstbilgisi başlık, promosyon başlığı ve tanımlama bilgisi izin modüllerini içeren bir sayfa parçası olarak yapılandırılır. 

Üst bilgi modülünde bir site logosu, gezinti hiyerarşisinin bağlantıları, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü modülü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu bulunur. Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir. Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.

Aşağıdaki resimde giriş sayfasında kullanılan bir üstbilgi modülü örneği gösterilmektedir.

![üstbilgi modülü örneği](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Üst bilgi modülünün özellikleri

Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler. 

**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır. Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md). 

**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.

## <a name="modules-that-are-available-within-a-header-module"></a>Üstbilgi modülünde kullanılabilen modüller

Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:

- **Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder. Daha fazla bilgi için bkz. [Gezinti menüsü modülleri](nav-menu-module.md).

- **Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir. **Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir. Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır. Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.

- **Sepet simgesi** - Sepet simgesi modülü, belirli bir zamanda sepetteki öğelerin sayısını gösteren sepet simgesini temsil eder. Daha fazla bilgi için bkz. [Sepet simgesi modülü](cart-icon-module.md).

- **Site seçici** - Site seçici modülü kullanıcıların pazar, bölgeler ve yerel ayarlara göre, önceden tanımlanmış farklı sitelere göz atmasına olanak tanır. Daha fazla bilgi için bkz. [Site seçici modülü](site-selector.md).

- **Mağaza Seçici** - Mağaza seçici modülü, bir üstbilgi modülünün mağaza seçici yuvasına dahil edilebilir. Kullanıcıların yakındaki mağazalara göz atmasına ve onları bulmasına olanak tanır. Kullanıcılar tercih edilen bir mağaza da belirtebilirler. Bu mağaza üst bilgide görüntülenecektir. Mağaza seçici modülü üst bilgi modülüne dahil edildiğinde, **Mod** özelliği **Mağaza bul** olarak ayarlanmalıdır. Daha fazla bilgi için bkz. [Mağaza seçici modülü](store-selector.md).

> [!NOTE]
> - Üst bilgi modüllerinde sepet simgesi modülünü kullanma desteği Dynamics 365 Commerce 10.0.11 sürümünde bulunabilir.
> - Üst bilgi modüllerinde site seçici modülünü kullanma desteği Dynamics 365 Commerce 10.0.14 sürümünde bulunabilir.
> - Üst bilgi modüllerinde mağaza seçici modülünü kullanma desteği Dynamics 365 Commerce 10.0.15 sürümünde bulunabilir.

## <a name="create-a-header-fragment-for-a-page"></a>Sayfa için üst bilgi parçası oluşturma

Bir üst bilgi parçası oluşturmak için şu adımları izleyin.

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda **Kapsayıcı** modülünü seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.
1. **Varsayılan kapsayıcı** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Ekranı doldur** olarak ayarlayın.
1. **Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Tanımlama bilgisi izni**, **Üst bilgi** ve **Promosyon başlığı** modüllerini seçin ve **Tamam**'ı seçin.
1. **Promosyon başlığı** modülünün özellikler bölmesinde, **İleti ekle**'yi seçin ve sonra **İleti**'yi seçin.
1. **İleti** iletişim kutusunda promosyon içeriği için metin ve bağlantı ekleyin ve **Tamam**'ı seçin.
1. **Tanımlama bilgisi izni** modülünün özellikler bölmesinde, bir metin ve site gizlilik sayfasına bağlantı ekleyin ve yapılandırın.
1. Başlık modülünü içeren **Gezinti menüsü** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Gezinti meüsü** modülünü seçin ve **Tamam**'ı seçin.
1. Gezinti menü modülünün özellik bölmesinde, **Gezinme menüsü kaynağı** altında, **Retail Server** öğesini seçin.
1. Gezinti menüsü modülünün özellik bölmesinde, **Statik menü öğeleri** altında, **Menü öğesi ekle**'yi seçin ve sonra **Menü öğesini** seçin. 
1. **Menü öğesi** iletişim kutusunda **Menü Öğesi Metni** altında "İletişim"i girin.
1. **Menü öğesi** iletişim kutusunda **Menü Öğesi Bağlantı hedefi** altından **Bağlantı ekle**'yi seçin.
1. **Bağlantı ekle** iletişim kutusunda sitenin "İletişim" sayfası için URL seçin ve **Tamam**'ı seçin.  
1. **Menü öğesi** iletişim kutusunda **Tamam**'ı seçin.
1. Başlık modülünü içeren **Ara** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Ara** modülünü seçin ve **Tamam**'ı seçin.
1. Arama modülünün özellik bölmesinde, özelliklerini yapılandırın.
1. Başlık modülünü içeren **Sepet simgesi** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Sepet simgesi** modülünü seçin ve **Tamam**'ı seçin.
1. Sepet simgesi modülünün özellik bölmesinde, özelliklerini yapılandırın. Kullanıcılar üzerinde gezinirken, sepet simgesinin bir sepet Özeti (mini sepet olarak da bilinir) göstermesini istiyorsanız, **mini sepeti göster**'i seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

Üstbilginin her sayfada göründüğünden emin olmak için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.

1. **Varsayılan sayfanın** **üstbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Kapsayıcı modülü](add-container-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Promosyon başlığı modülü](add-alert.md)

[Gezinti Menüsü modülleri](nav-menu-module.md) 

[Tanımlama bilgisi izni](cookie-consent-module.md)

[Alt bilgi modülü](author-footer-module.md)

[Site seçici modülü](site-selector.md)

[Mağaza seçicisi modülü](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]