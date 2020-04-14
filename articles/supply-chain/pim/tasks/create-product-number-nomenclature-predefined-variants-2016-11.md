---
title: Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150068"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yeni ürün numara terminolojisi, Renk ve Boyut ürün boyut grubuna atanmıştır. Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.


## <a name="create-a-product-number-nomenclature"></a>Ürün numara terminolojisi oluşturma
1. **Ürün çeşidi model tanımı**'nı seçin.
2. **Ürün terminolojisi**'ni seçin.
3. **Yeni**'yi seçin.
4. **Ad** alanına, örneğin `ColorSize` gibi hedef ürün boyut grubunu tanımlamaya yardımcı olacak bir terminoloji adı girin.
5. **Tanım** alanına bir değer girin.
6. **Ekle**'yi seçin.
7. **Ürün ana numarası** seçin.
8. **Ekle**'yi seçin.
9. **Metin sabiti** seçin.
10. **Metin** alanına bir değer yazın.
11. **Ekle**'yi seçin.
12. **Renk** seçin.
13. **Ekle**'yi seçin.
14. **Metin sabiti** seçin.
15. **Metin** alanına bir değer yazın.
16. **Ekle**'yi seçin.
17. **Boyut** seçin.
18. Sayfayı kapatın.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Ana ürüne terminoloji atama
1. **Ürün boyut grupları**'nı seçin.
2. **SizeCol ürün boyut grubunu** seçin.
3. **Düzenle** öğesini seçin.
4. **Terminolojiyi kullan** alanında **Evet**'i seçin.
5. **Ürün çeşidi numara terminolojisi** alanında bir değer girin veya seçin.
6. Sayfayı kapatın.

