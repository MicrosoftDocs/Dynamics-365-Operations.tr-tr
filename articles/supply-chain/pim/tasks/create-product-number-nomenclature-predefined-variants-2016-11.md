---
title: Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu makale, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887326"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu makale, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yeni ürün numara terminolojisi, Renk ve Boyut ürün boyut grubuna atanmıştır. Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.


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