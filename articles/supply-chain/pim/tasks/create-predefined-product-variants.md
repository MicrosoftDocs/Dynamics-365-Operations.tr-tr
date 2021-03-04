---
title: Önceden tanımlanmış ürün çeşitleri oluşturma
description: Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa9c6d4862a49bbf0b5ecbb8c0c3d573e0f49e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439298"
---
# <a name="create-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır. Bu yöntemi oluşturmak için kullanılan demo şirketi USMF'dir.


## <a name="create-a-product-master"></a>Ana ürün oluşturma
1. Ürün bilgi yönetimi > Ürünler > Ana ürünler'e git.
2. Yeni'ye tıklayın.
3. Ürün numarası alanında bir değer girin.
    * Bir ürün numarasının el ile girilmesi sadece ürün numarası alanı için hiçbir numarası dizisi ayarlanmamışsa gereklidir. Diğer bir deyişle, alan için bir numara serisi ayarlanmışsa bu adımı atlayın.  
4. Ürün adı alanına bir değer girin.
5. Ürün boyutu grubu alanına bir değer girin veya bir değer seçin.
    * SizeCol (Boyut ve Renk) ürün boyut grubunu seçin.  
6. Tamam'a tıklayın.

## <a name="add-product-dimensions"></a>Ürün boyutları ekleme
1. Ürün boyutları öğesini tıklayın.
    * Bu örnekte ürün boyutlarının nasıl el ile girileceği gösterilmiştir. Ayrıca, kullanmak istediğiniz ürün boyutu değerlerini içeren boyut, renk veya tarz grubunu seçebilirsiniz.  
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ebat alanına bir değer girin veya seçin.
5. İsim alanına bir değer yazın.
6. Yeni'yi tıklatın.
7. Listede, seçili satırı işaretleyin.
8. Ebat alanına bir değer girin veya seçin.
9. İsim alanına bir değer yazın.
10. Renkler sekmesini tıklatın.
11. Yeni'ye tıklayın.
12. Listede, seçili satırı işaretleyin.
13. Renk alanına bir değer girin veya buradan bir değer seçin.
14. İsim alanına bir değer yazın.
15. Yeni'yi tıklatın.
16. Listede, seçili satırı işaretleyin.
17. Renk alanına bir değer girin veya buradan bir değer seçin.
18. İsim alanına bir değer yazın.
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.

## <a name="generate-product-variants"></a>Ürün seçenekleri oluşturma
1. Ürün çeşitleri öğesini tıklayın.
2. Çeşit önerilerini tıklayın.
3. Tümünü seç'i tıklatın.
    * Bu örnekte tüm olası seçenekler dahil edilmiştir. Bu seçeneklerin oluşturulması için sadece olası ürün boyutu kombinasyonlarının bir alt kümesi kullanılacaksa, bireysel girişleri seçebilirsiniz.  
4. Oluştur'a tıklayın.
    * Ürün boyutu değerlerinin kombinasyonuna dayalı olarak tüm seçenekleriniz için açıklamalar oluşturabilirsiniz. Açıklamalar isteğe bağlıdır.  
5. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]