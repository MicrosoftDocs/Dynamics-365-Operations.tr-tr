---
title: Favicon ekleme
description: Bu konu, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.
author: bicyclingfool
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697003"
---
# <a name="add-a-favicon"></a>Favicon ekleme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir tercih edilen simge, Web tarayıcısı sekmesinde, adres çubuğunda, gözatma geçmişinde ve diğer yerlerin yanı sıra yer imleri veya Sık Kullanılanlar'da gösterilen küçük bir grafik dosyasıdır. Markanızı temsil ettiğinden ve yeniden zorlayan ve sitenizi müşterilerinizin ziyaret ettiği diğer sitelerden ayırt etmenize yardımcı olacağından sitenize bir tercih edilen bir simge eklemeniz önerilir.

Sitenize çeşitli boyutlarda ve dosya türlerindeki birçok tercih edilebilir simge ekleyebilmenize rağmen bu konu, tek bir tercih edilen simgenin nasıl ekleneceğini göstermektedir. Ancak, aynı işlem ve yer, daha fazla tercih edilen simge eklemek için kullanılır.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Sitenizin varlık koleksiyonuna bir tercih simgesi yükleyin

Sitenizin varlık koleksiyonuna bir tercih simgesi yüklemek için aşağıdakileri takip edin.

1. **Varlıklar \> Yükle \> Varlıkları yükle**'ye gidin.
1. Yerel dosya sisteminizdeki tercih simgesini bulun ve seçin.
1. Bir başlık girin ve **Tamam**'ı seçin. 
1. Sağdaki özellik bölmesinde, tercih edilen simgenin ortak URL'sini kopyalayın.

> [!NOTE]
> **Yükledikten sonra varlıkları Yayınla** seçeneğini seçmezseniz, **varlıklar** sayfasına dönmeniz ve daha sonra yeniden öncelik simgesini el ile yayımlamanız gerekir.

## <a name="create-the-html-for-the-favicon"></a>Tercih simgesi için HTML oluşturun

Tercih edilen simgenin HTML'i oluşturmak için aşağıdaki HTML kod parçacığını kullanın. **Href** özniteliği için, **Tercih\_simgeniz\_için\_genel\_URL**'yi önceden kopyaladığınız ortak URL ile değiştirin.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Tercih simgesi için HTML'yi sayfalarınızın \<baş\> öğesine ekleyin

Sitenize bir tercih simgesi eklemek için, site sayfalarınızın **\<baş\>** öğesine herhangi bir türdeki HTML veya kod eklemek için kullanılan yordamın aynısını kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)

