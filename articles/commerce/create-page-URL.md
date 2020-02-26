---
title: URL sayfası oluşturma
description: Bu konu, sitenizde sayfa URL'SI oluşturmaya yönelik temel kavramları ve yordamları kapsamaktadır.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 588cbedb077fab0663d3d62fc4a8b8ed915635b3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001933"
---
# <a name="create-a-page-url"></a>URL sayfası oluşturma


[!include [banner](includes/banner.md)]

Bu konu, sitenizde sayfa URL'SI oluşturmaya yönelik temel kavramları ve yordamları kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Sitenizdeki bir sayfaya işaret eden tam veya mutlak URL, farklı bölümlerden oluşur. Örneğin, URL `https://www.contoso.com/en-us/contactus` aşağıdaki bölümlerden oluşur:

- `https://www.contoso.com` – HTTP iletişim kuralı ve sitenin etki alanı.
- `/en-us`– Sitenin dil yolu.
- `/contactus` – **Bize Ulaşın** sayfasının göreli URL'si. Göreli URL, URL *bilgi* olarak da bilinir.

Siteyi kurarken sitenizin etki alanını ve isteğe bağlı dil yolunu kurarsınız. Sitenin ayarlarındaki çevrimiçi mağazalar sayfası yoluyla sitenize başka etki alanları ve dil yolları ekleyebilirsiniz.

Bir sayfanın URL adresi, site geliştirme ortamında bağımsız bir varlık olarak bulunur. Sayfa URL'si iki bölümden oluşur: URL bilgisinin temsil ettiği bir ad ve sitenizdeki veya dış sitedeki bir sayfaya işaretçi. Sayfa URL'Si Ayrıca, sitenizdeki veya dış sitedeki başka bir sayfaya yeniden yönlendirme işlevi görecek şekilde de yapılandırılabilir.

## <a name="create-a-page-url"></a>URL sayfası oluşturma

Sayfa URL'leri oluşturmanın iki yolu vardır:

- Otomatik olarak, bir sayfa oluşturduğunuzda
- El ile, **URL'ler** sayfasından

### <a name="create-a-page-url-when-you-create-a-page"></a>Sayfa oluştururken sayfa URL'Si oluşturma

Yeni sayfa oluştururken **URL** alanında bir ad sağlarsanız, **URL'ler** sayfasında otomatik olarak bu sayfaya işaret eden bir sayfa URL'si oluşturulur. URL'yi ve işaret eden sayfayı yayımladıktan sonra, site kullanıcıları (müşterileriniz) URL ile ilişkilendirilmiş olan sayfaya erişebilir.

> [!NOTE]
> İşaret ettiği sayfayı yayımlamadan bir URL'yi yayımlarsanız, site kullanıcıları sayfaya erişmeye çalıştıklarında bir 404 hatası alırlar. Bir sayfayı üzerinde işaret eden bir URL'yi yayımlamadan yayımlarsanız, sayfaya bir URL kullanılarak erişilemez.

### <a name="manually-create-a-page-url"></a>Manuel olarak sayfa URL'si oluşturma

Yeni sayfalar oluşturduğunuzda, bir sayfa URL'si belirtmeniz gerekmez. URL alanını boş bırakırsanız, sayfa bağlantısız durumda oluşturulur. Bu durumda, yayımlanmış olsa bile, müşteriler sayfaya erişemez. Sayfayı erişilebilir duruma getirmek için, URL'yi el ile oluşturmanız ve sayfaya bağlamanız gerekir.

Bir sayfa için sayfa URL'sini manuel oluşturmak için, aşağıdaki adımları izleyin.

1. **URL'ler** sayfasında, **Yeni**'yi seçin.
1. URL ile ilişkilendirileceği site sayfasını seçin.
1. Bir URL bilgisi girin ve **Tamam**'ı seçin.

Bu noktada, URL Taslak durumundadır. Site kullanıcılarının ilişkili sayfaya erişebilmesi için önce bu sitenin yayımlanması gerekir.

## <a name="update-a-page-url"></a>Sayfa URL'si güncelleme

Sayfa URL'sinin hedef sayfasını güncelleştirmek için, aşağıdaki adımları izleyin.

1. **URL'ler** sayfasında güncelleştirilecek URL'yi seçin.
1. Sağdaki özellik bölmesinde hedef sayfa alanının yanında üç nokta düğmesini (**...**) seçin.
1. İletişim kutusunda , farklı bir sayfa seçin ve **Tamam**'ı tıklatın.
1. URL'yi kaydet ve yayınlayın.

## <a name="redirect-a-page-url"></a>Sayfa URL'sini yeniden yönlendir

Bazen, belirli bir URL'yi istediklerinde müşterilerinizin farklı sayfaları görüntülemesini isteyebilirsiniz. Bu durumlarda, en iyi ve en kolay yaklaşım genellikle sayfa URL'sinin işaret ettiği sayfayı değiştirir. Ancak, HTTP 301 veya 3023 isteklerinin bir URL'yi farklı bir URL'ye yeniden yönlendirmek için yasal sebeplere sahip olabilirsiniz.

Bir URL'Yi farklı bir URL'ye yeniden yönlendirmek için, aşağıdaki adımları izleyin.

1. **URL'ler** sayfasında güncelleştirilecek URL'yi seçin.
1. Sağdaki Özellik bölmesinde **yeniden yönlendir**'i seçin.
1. Yeniden yönlendirme için hedef seçin:

    - Sitenizdeki başka bir sayfayı işaret etmek için, **Dahili URL** seçin, üç nokta düğmesini (**...**) ve sonra yeniden yönlendirilecek URL 'yi seçin.
    - Harici bir sitesindeki sayfayı işaret etmek için **Harici URL** seçeneğini belirleyin ve sonra o sayfanın tam URL'sini girin. İletişim kuralını eklediğinizden emin olun. Örneğin `https://domain.com/new/page` yazın. URL zaten dahili bir URL'ye yeniden yönlendiriyorsa, harici bir URL girmek için **seçimi temizle**'yi seçmelisiniz.

1. Bir yeniden yönlendirme türü seçin:

    - **Kalıcı yeniden yönlendirme (301)** – içeriğinizin kalıcı olarak taşınmakta olduğunu ve önceki URL'sini geri döndürmeyinizi biliyorsanız bu seçeneği belirleyin. Arama motorları, yeniden yönlendirme URL'sinin arama motoru iyileştirme (SEO) değerini, yeni URL'yi göstermek üzere kendi kayıtlarını yönlendirmekte olan URL'ye atayacaktır. 
    - **Geçici yeniden yönlendirme (302)** – akışı, arama altyapılarını güncelleştirmeden yeniden yönlendirmek için bu seçeneği belirleyin. Bu yaklaşım genellikle içerik önceki URL'sine geri dönürseniz kullanılır.

1. Yeniden yönlendirmeyi uygulamaya hazır olduğunuzda, URL'yi kaydedin ve yayınlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Site gezintisini özelleştirme](customize-site-navigation.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Sitenize dil ekleme](add-languages-to-site.md)
