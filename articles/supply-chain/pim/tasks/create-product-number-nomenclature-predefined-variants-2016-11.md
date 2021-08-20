---
title: Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fada426b03aa8a908c3351932a288c911cb8c60fa13ccbfbfd0ceed232759a88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736052"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yeni ürün numara terminolojisi, Renk ve Boyut ürün boyut grubuna atanmıştır. Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.


## <a name="create-a-product-number-nomenclature"></a>Ürün numara terminolojisi oluşturma

1. **Ürün bilgi yönetimi \> Kurulum \> Ürün terminolojisi**'ne gidin.
1. **Yeni**'yi seçin.
1. **Ad** alanına, örneğin `ColorSize` gibi hedef ürün boyut grubunu tanımlamaya yardımcı olacak bir terminoloji adı girin.
1. **Tanım** alanına bir değer girin.
1. **Ekle**'yi seçin.
1. **Ürün ana numarası** seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Renk** seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Boyut** seçin.
1. Sayfayı kapatın.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Ana ürüne terminoloji atama

1. **Ürün boyut grupları**'nı seçin.
2. **SizeCol ürün boyut grubunu** seçin.
3. **Düzenle** öğesini seçin.
4. **Terminolojiyi kullan** alanında **Evet**'i seçin.
5. **Ürün çeşidi numara terminolojisi** alanında bir değer girin veya seçin.
6. Sayfayı kapatın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]