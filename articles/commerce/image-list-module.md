---
title: Görüntü listesi modülü
description: Bu konu görüntü listesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b7e070bfe562bb1a28b10d4632725b53a090cda4
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638842"
---
# <a name="image-list-module"></a>Görüntü listesi modülü

[!include [banner](includes/banner.md)]

Bu konu görüntü listesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Görüntü listesi modülü, site sayfalarına kolayca resim koleksiyonu (dizisi) eklemek için kullanılabilir. Dizideki her görüntü, paragraf metni ve bağlantı URL'leriyle yapılandırılabilir. Görüntü listesi modülü, marka logoları veya logolar içeren bir liste görüntülemek için en uygun yöntemdir.

> [!IMPORTANT]
> - Görüntü listesi modülü, Dynamics 365 Commerce 10.0.20 sürümünden itibaren Commerce modülünde kullanılabilir.
> - Görüntü listesi modülü Adventure Works temalarında görüntülenir.

Aşağıdaki örnekte bir görüntü listesi modülünün, Adventure Works işletme ile müşteri arası (B2C) site sayfasında logoları içeren bir metin listesi görüntülediği bir örnek gösterilmektedir.

![Logoları içeren bir metin listesi görüntüleyen resim listesi modülü örneği](./media/Image_list.PNG)

Aşağıdaki örnekte bir görüntü listesi modülünün, Adventure Works işletmeler arası (B2B) site sayfasında marka logoları görüntülediği bir örnek gösterilmektedir.

![Marka logolarını görüntüleyen görüntü listesi modülü örneği](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Görüntü listesi modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık       | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Görüntü listesi modülü için metin başlığı. |
| Görüntü listesi    | Görüntüler, metin ve URL'ler | Dizideki her öğe, paragraf metni ve URL ile birlikte gelen bir görüntüdür. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Yeni sayfaya görüntü listesi modülü ekleme

Yeni sayfaya görüntü listesi modülü eklemek ve Commerce site oluşturucuda gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin ve sitenizin giriş sayfası için pazarlama şablonunu açın (veya yeni bir pazarlama şablonu oluşturun).
1. Varsayılan sayfada **Ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Görüntü listesi** modülünü ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve sitenin giriş sayfasını açın (veya pazarlama şablonunu kullanarak yeni bir giriş sayfası oluşturun).
1. Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Görüntü listesi**'ni ve **Tamam**'ı seçin.
1. Görüntü listesi modülünün özellik bölmesinde bir başlık ekleyin (örneğin, **Markalarımız**).
1. Görüntü listesi öğesi ekleyin ve bir görüntü, paragraf metni ve yeniden yönlendirme URL'si belirtin.
1. Görüntü listesi öğesi modüllerini gereksinim duyduğunuz şekilde ekleyin ve yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Adventure Works teması](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
