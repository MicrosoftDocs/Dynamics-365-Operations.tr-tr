---
title: Sekme modülü
description: Bu makale sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 91c79ca1b70a776352ef99d854397ada34c548e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276986"
---
# <a name="tab-module"></a>Sekme modülü

[!include [banner](includes/banner.md)]

Bu makale sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Sekme modülleri, sekmelerdeki bir site sayfasındaki bilgileri düzenlemek için kullanılan kapsayıcı benzeri modüllerdir. Bunlar, bilgilerin sekmelerde sunulması gereken her sayfada kullanılabilir.

Her sekme modülü içinde bir veya daha fazla sekme madde modülü eklenebilir. Her sekme öğesi modülü tek bir sekmeyi temsil eder. Her sekme madde modülünde, bir veya daha fazla modül eklenebilir. Bir sekme madde modülüne eklenebilecek modül türlerinde bir sınırlama yoktur.

Aşağıdaki resimde site sayfasında kullanılan bir sekme modülü örneği gösterilmektedir. Bu örnekte, **Sevkiyat** sekmesi seçili.

![Sekme modülü örneği.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Sekme modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık | Metin | Bu özellik sekme modülü için isteğe bağlı bir metin başlığı belirtir. |
| Etkin sekme dizini | Sayı | Bu özellik, sayfa yüklendiğinde varsayılan olarak etkin olması gereken sekmeyi belirtir. Herhangi bir değer sağlanmazsa, ilk sekme öğesi varsayılan olarak etkindir. |

## <a name="tab-item-module-properties"></a>Sekme madde modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Ünvan | Metin | Bu özellik sekme madde modülü için bir başlık metini belirtir. |

## <a name="add-a-tab-module-to-a-page"></a>Sayfaya sekme modülü ekleme

Bir sayfaya sekme modülü eklemek ve özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Mağaza politikaları sayfası** adlı yeni bir sayfa oluşturmak için sayfalara gidin ve Fabrikam pazarlama şablonunu kullanın.
1. **Varsayılan sayfada** **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusundaki **Sekme** modülünü seçin ve **Tamam**'ı seçin.
1. Sekme modülünün Özellik bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.
1. **Başlık** iletişim kutusunda, **başlık metni** altında başlık metni girin (örneğin, **ilkeler**). Daha sonra **Tamam**'ı seçin.
1. **Sekme** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Sekme öğesi** modülünü seçin ve **Tamam**'ı seçin.
1. Sekme madde modülünün Özellik bölmesinde, **başlık** altında başlık metnini girin (örneğin, **Teslimat**).
1. **Sekme öğesi** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Metin bloğu** modülünü seçin ve **Tamam**'ı seçin.
1. Metin bloku modülünün özellik panosunda, **Zengin metin** altına mtein paragrafı girin.
1. **Sekme** yuvasında, başlıkları olan birkaç sekme öğesi modülü ekleyin. Her bir sekme madde modülünde içeriği olan bir metin bloğu modülü ekleyin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Sayfa, sekme öğesi modülleri içeren bir sekme modülünü gösterir eklediğiniz içeriğe sahip.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Kapsayıcı modülü](add-container-module.md)

[Akordeon modülü](add-accordion.md)

[Metin bloğu modülü](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
