---
title: Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258887"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir. Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır. Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.


## <a name="create-a-product-number-nomenclature"></a>Ürün numara terminolojisi oluşturma
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün terminolojisi'ne tıklayın.
3. Yeni'ye tıklayın.
4. İsim alanına bir değer yazın.
5. Açıklama alanına bir değer girin.
6. Ekle öğesini tıklatın.
7. Ana ürün numarası'na tıklayın.
8. Ekle öğesini tıklatın.
9. Metin sabiti'ne tıklayın.
10. Listede, seçili satırı işaretleyin.
11. Metin alanına bir değer yazın.
12. Ekle öğesini tıklatın.
13. Yapılandırma'ya tıklayın.
14. Sayfayı kapatın.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Ana ürüne, ürün numara terminolojisi atama
1. Ana ürünler'e tıklayın.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ürün numarası alanında "D" değeriyle filtreleyin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Düzenle'ye tıklayın.
5. Terminoloji kullan alanında Evet'i seçin.
6. Ürün çeşidi numara terminolojisi alanında bir değer girin veya seçin.
7. Sayfayı kapatın.
8. Sayfayı kapatın.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Ürün yapılandırma model bileşeni için terminoloji oluşturma
1. Ürün yapılandırma modelleri'ne tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Düzenle'ye tıklayın.
5. Konfigürasyon terminolojisini kullan alanında Evet'i seçin.
6. Ekle öğesini tıklatın.
7. Öznitelik değeri'ne tıklayın.
8. Listede, seçili satırı işaretleyin.
9. Öznitelik alanına bir değer girin veya seçin.
10. Ekle öğesini tıklatın.
11. Metin sabiti'ne tıklayın.
12. Listede, seçili satırı işaretleyin.
13. Metin alanına bir değer yazın.
14. Ekle öğesini tıklatın.
15. Öznitelik değeri'ne tıklayın.
16. Listede, seçili satırı işaretleyin.
17. Öznitelik alanına bir değer girin veya seçin.
18. Ekle öğesini tıklatın.
19. Metin sabiti'ne tıklayın.
20. Listede, seçili satırı işaretleyin.
21. Metin alanına bir değer yazın.
22. Ekle öğesini tıklatın.
23. Öznitelik değeri'ne tıklayın.
24. Listede, seçili satırı işaretleyin.
25. Öznitelik alanına bir değer girin veya seçin.
26. Ekle öğesini tıklatın.
27. Metin sabiti'ne tıklayın.
28. Listede, seçili satırı işaretleyin.
29. Metin alanına bir değer yazın.
30. Ekle öğesini tıklatın.
31. Öznitelik değeri'ne tıklayın.
32. Listede, seçili satırı işaretleyin.
33. Öznitelik alanına bir değer girin veya seçin.
34. Ekle öğesini tıklatın.
35. Metin sabiti'ne tıklayın.
36. Listede, seçili satırı işaretleyin.
37. Metin alanına bir değer yazın.
38. Ekle öğesine tıklayın.
39. Numara serisi değeri'ne tıklayın.
40. Listede, seçili satırı işaretleyin.
41. Numara sırası alanında, bir değer girin veya seçin.
42. Sayfayı kapatın.
43. Sayfayı kapatın.
44. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]