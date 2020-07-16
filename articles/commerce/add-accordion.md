---
title: Akordiyon modülü
description: Bu konu akordiyon modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417266"
---
# <a name="accordion-module"></a>Akordiyon modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu akordiyon modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

Akordiyon modülleri, bir sayfadaki bilgileri veya modülleri daraltılabilir bir çekmece benzeri yetenek sağlayarak düzenlemek için kullanılan kapsayıcı benzeri modüllerdir. Bir akordiyon modülü herhangi bir sayfada kullanılabilir.

Her akordiyon modülü içinde bir veya daha fazla akordiyon madde modülü eklenebilir. Her bir akordiyon öğesi modülü daraltılabilir bir çekmeceyi gösterir. Her akordiyon madde modülü içinde bir veya daha fazla modülü eklenebilir. Bir akordiyon madde modülüne eklenebilecek modül türlerinde bir sınırlama yoktur.

Aşağıdaki resimde, bir mağazanın sık sorulan sorular (SSS) sayfasındaki bilgileri düzenlemek için kullanılan bir akordiyon modülü örneği gösterilmektedir.

![Akordiyon modülü örneği](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Akordiyon modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık | Metin | Bu özellik akordiyon modülü için isteğe bağlı bir metin başlığı belirtir. |
| Tümünü Genişlet | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlanırsa akordiyon modülündeki tüm öğelerin genişletilebileceği ve daraltılabilmesi için genişletme/daraltma işlevi açılır. |
| Etkileşim stili | **Bağımsız** veya **yalnızca bir öğeyi genişlet** | Bu özellik, akordiyon öğeler için etkileşimin stilini tanımlar. Değer **bağımsız** olarak ayarlandığında her bir akordiyon öğesi bağımsız olarak genişletilebilir veya daraltılabilir. Değer **yalnızca bir öğeyi genişletmek** üzere ayarlandıysa bir seferde yalnızca bir madde genişletilebilir. Öğeler genişletildiği gibi, önceden genişletilmiş öğeler daraltılmıştır. |

## <a name="accordion-item-module-properties"></a>Akordiyon madde modülü özellikleri

| Özellik adı | Değerler | Tanım |
|----------------|--------|-------------|
| Ünvan | Metin | Bu özellik akordiyon madde modülü için bir başlık metini belirtir. Başlık bölgesini seçerek, kullanıcılar bölümü genişletebilir veya daraltabilir. |
| Varsayılan olarak genişlet | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlanırsa sayfa yüklendiğinde akordiyon madde varsayılan olarak genişletilir. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>SSS sayfasına akordiyon modülü ekleme

SSS sayfaya akordiyon modülü eklemek ve özelliklerini site oluşturucuda ayarlamak için aşağıdaki adımları izleyin.

1. **Mağaza SSS** adlı yeni bir sayfa oluşturmak için **sayfalara** gidin ve Fabrikam pazarlama şablonunu (veya sınırlamaları olmayan tüm şablonları) kullanın.
1. **Varsayılan sayfada** **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **akordiyon** modülünü seçin ve **Tamam**'ı seçin.
1. Akordiyon modülünün Özellik bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.
1. **Başlık** iletişim kutusunda, **başlık metni** altında **sık sorulan soruları** girin. Daha sonra **Tamam**'ı seçin.
1. Akordiyon modülünün Özellik bölmesinde, **Tümünü Genişlet** onay kutusunu seçin ve sonra **etkileşim stili** alanında **bağımsız**'i seçin.
1. **Akordiyon** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **akordiyon madde** modülünü seçin ve **Tamam**'ı seçin.
1. Accordion madde modülünün Özellik bölmesinde, **başlık** altında başlık metnini girin (örneğin, **çalışma nasıl döner?**).
1. **Akordiyon madde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.
1. Metin bloğu modülünün Özellik bölmesinde bir paragraf metni girin (örneğin, **İadeler çağrı merkezi aracılığıyla işlenmelidir. İadeler için 1-800-FABRIKAM arayın. Ürünlerin 30 günlük bir iade ilkesi vardır. İadeler bu zaman çerçevesinde başlatılmalıdır.**).
1. **Akordiyon** yuvasında birkaç tane daha akordiyon madde modülü ekleyin. Her bir akordiyon madde modülünde içeriği olan bir metin bloğu modülü ekleyin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Sayfa, eklediğiniz içeriğe sahip bir akordiyon modülü gösterir.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Sekme modülü](add-tab.md)

[Metin bloğu modülü](add-content-rich-block.md)