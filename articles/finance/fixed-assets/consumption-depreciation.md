---
title: Tüketim esasına göre amortisman
description: Bu makalede, amortismanın Tüketim yöntemi hakkında genel bir bakış verilmektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e78e2481724aede93ecb997d95a0ef8032618bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989039"
---
# <a name="consumption-depreciation"></a>Tüketim esasına göre amortisman

[!include [banner](../includes/banner.md)]

Bu makalede, amortismanın Tüketim yöntemi hakkında genel bir bakış verilmektedir.

Sabit kıymetler için bir amortisman profili ayarladıysanız ve **Amortisman profilleri** sayfasındaki **Yöntem** alanında **Tüketim** seçeneğini işaretlerseniz, sabit kıymetler kullanımlarına göre amortisman profili atanır. **Amortisman profilleri** sayfasında yüzdeleri ve aralıkları ayarlamak zorunda değilsiniz. Tüketim yöntemini kullanan bir amortisman profili oluşturduktan sonra yöntemi çeşitli şekillerde ayarlayabilirsiniz.

## <a name="set-up-and-use-consumption-depreciation"></a>Tüketim amortismanını ayarlayın ve kullanın
1.  **Amortisman profilleri** sayfasında, bir amortisman profili oluşturun. Tüketim hesaplamaları için amortisman profilinin bir kimlik ve bir adı olmalıdır ve **Yöntemi** alanından **Tüketim** seçilmelidir.
2.  **Tüketim faktörleri** sayfasında, tüketim faktörlerini ayarlama. Her tüketim faktörünün bir kimliği ve bir adı ve bir yüzde ya da bir miktar olarak belirtilmiş bir tüketim faktörü olmalıdır.
3.  **Tüketim birimleri** sayfası, tüketim birimleri ayarlama. Her tüketim biriminin bir kimliği ve bir adı olmalıdır. Amortisman birimleri, **Tüketim amortismanı** sayfasında tüketim amortismanını hesaplamak için kullanılır. Birimlere örnek olarak, kilometre (km), kilogram (kg) ve saat verilebilir.
4.  **Sabit kıymetler** sayfası üzerinde, sabit kıymetleri tek ayarlayın. Her bir sabit kıymet için değer modelleri ve amortisman profilleri olan amortisman defterleri seçin. Eğer sabit kıymetlerinizden herhangi biri Tüketim yöntemine dayalı amortisman modelleri kullanıyorsa, tüketim amortismanı için değer modelleri ve amortisman defterleri ayarlamanız gerekir. Bu ayar ya **Değer modelleri** sayfasındaki **Amortisman** sekmesinde ya da **Amortisman profili** sayfasında **Genel** hızlı sekmesinde yapılır.. Çok sayıda sabit kıymet için aynı değer modelini kullanabilirsiniz. Amortisman profilleri, her sabit kıymet için seçtiğiniz değer modeli veya amortisman defterinin bir parçasıdır. Amortisman profillerini doğrudan **Sabit kıymetler** sayfasında ekleyemez veya değiştirmezsiniz. Amortisman profillerini yalnızca **amortisman defterleri** sayfa değiştirebilirsiniz.
5.  **Değer modelleri** sayfasi veya **Amortisman defterleri** sayfasında, **Tüketim esasına göre amortisman** alan grubunda, aşağıdaki alanlara bilgileri girin:
    -   Tüketim faktörü
    -   Birim
    -   Birim amortisman
    -   Tahmini tüketim

    **Deftere nakledilen tüketim** alanı deftere sabit kıymet ve değer modelinin birleşimi için veya amortisman defter için nakledilmiş tüketim amortismanını birimleriyle gösterir. Bu alandaki değeri el ile güncelleştiremezsiniz.

## <a name="examples"></a>Örnekler
### <a name="example-1"></a>Örnek 1

Aşağıdaki tüketim faktörü 31 Ocak için oluşturulmuştur:

-   Miktar 1,000'dir.
-   Sabit kıymet için belirtilmiş birim amortisman fiyatı 1,5'tur.

31 Ocak Amortisman teklifi aşağıdaki gibidir: Miktar × Birim amortismanı 1.000 × 1,5 = 1.500 Eğer sabit kıymet için belirtilen faktör bir yüzde faktörüyse, **Tüketim tahmini** alanındaki sabit kıymet için değer modeli tahminin miktarı, seçilen bitiş tarihi için ayarlanmış oran ile çarpılır. Sonuçta elde edilen miktar sonra dönem için amortisman miktarı olarak önerilir.

### <a name="example-2"></a>Örnek 2

Aşağıdaki tüketim amortismanına yönelik faktör, 31 Ocak için oluşturulmuştur:

-   Yüzde, yüzde 10'dur.
-   Sabit kıymet için belirtilmiş birim amortisman fiyatı 1,5'tur.
-   Sabit kıymetin tahmini miktarı 2.000'dir.

31 Ocak tarihindeki amortisman teklifi aşağıdaki gibidir: Tahmini miktarı x Yüzde × Birim amortisman 2,000 × ,10 × 1,5 = 300



