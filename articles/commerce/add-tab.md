---
title: Sekme modülü
description: Bu konu sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 9062e584d159e0f1986c46140d535f06f5d2817af048f30e812f9049bd52d4f6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723299"
---
# <a name="tab-module"></a>Sekme modülü

[!include [banner](includes/banner.md)]

Bu konu sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

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
1. **Varsayılan sayfada** **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **sekme** modülünü seçin ve **Tamam**'ı seçin.
1. Sekme modülünün Özellik bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.
1. **Başlık** iletişim kutusunda, **başlık metni** altında başlık metni girin (örneğin, **ilkeler**). Daha sonra **Tamam**'ı seçin.
1. **Sekme** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **sekme madde** modülünü seçin ve **Tamam**'ı seçin.
1. Sekme madde modülünün Özellik bölmesinde, **başlık** altında başlık metnini girin (örneğin, **Teslimat**).
1. **Sekme madde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.
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