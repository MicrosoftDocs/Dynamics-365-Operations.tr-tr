---
title: Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007553"
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

