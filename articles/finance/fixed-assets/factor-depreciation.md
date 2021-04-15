---
title: Faktör amortisman
description: Bu makale, faktör amortisman yöntemi hakkında genel bir bakış sağlar.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8adfc91251ba1707c688fac6da04adaa9af1a47f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815704"
---
# <a name="factor-depreciation"></a>Faktör amortisman

[!include [banner](../includes/banner.md)]

Bu makale, faktör amortisman yöntemi hakkında genel bir bakış sağlar.

Faktörler, kıymetlere amortisman uygulamak için kullanılan yüzdelerdir. Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **Faktör**'ü seçtiğinizde, artan paylı, azalan paylı, eşit paylı amortisman ayarlayabilirsiniz:

-   Artan paylı amortismanda, amortisman tutarı her amortisman döneminde artar.
-   Azalan paylı amortismanda, dönem başına amortisman tutarı zaman içinde azalır.
-   Eşit paylı amortismanda, amortisman her dönem için aynıdır.

Aşağıdaki kurallar ve örnekler, her tip amortisman için faktörleri nasıl ayarlayacağınızı gösterir. 

> [!NOTE] 
> **Yöntem** alanında **Faktör**'ü seçtiğinizde, **Faktör** alanı ve **Aralık** alanı görüntülenir.

## <a name="progressive-depreciation"></a>Artan paylı amortisman
**Faktör** alanındaki değer **50**'den büyüktür.

### <a name="example"></a>Örnek

Alım fiyatı 100.000, faktör 70, hizmet ömrü 10 yıl ve amortisman 1 Ocak'ta başlıyor. Amortisman tutarları ve net defter değeri tutarları yalnızca hizmet ömrünün ilk altı yılı için gösterilir.

| Yıl | Dönem      | Amortisman tutarı | Net defter değeri tutarı |
|------|-------------|---------------------|-----------------------|
| 1    | 31 Aralık | 307,69              | 99.692,31             |
| 2    | 31 Aralık | 1.447,21            | 98.245,10             |
| 3    | 31 Aralık | 3.104,50            | 95.140,60             |
| 4    | 31 Aralık | 5.150,21            | 89.990,39             |
| 5    | 31 Aralık | 7.522,95            | 82.467,44             |
| 6    | 31 Aralık | 10.184,06           | 72.283,38             |

## <a name="digressive-depreciation"></a>Azalan paylı amortisman
**Faktör** alanındaki değer **50**'den küçüktür.

### <a name="example"></a>Örnek

Alım fiyatı 100.000, faktör 20, hizmet ömrü 10 yıl ve amortisman 1 Ocak'ta başlıyor. Amortisman tutarları ve net defter değeri tutarları yalnızca hizmet ömrünün ilk altı yılı için gösterilir.

| Yıl | Dönem      | Amortisman tutarı | Net defter değeri tutarı |
|------|-------------|---------------------|-----------------------|
| 1    | 31 Aralık | 56.080,43           | 43.919,57             |
| 2    | 31 Aralık | 10.665,70           | 33.253,87             |
| 3    | 31 Aralık | 7.156,22            | 26.097,65             |
| 4    | 31 Aralık | 5.538,06            | 20.559,59             |
| 5    | 31 Aralık | 4.579,89            | 15.979,70             |
| 6    | 31 Aralık | 3.937,36            | 12.042,34             |

## <a name="straight-line-depreciation"></a>Eşit paylı amortisman
**Faktör** alanındaki değer **50**'ye eşittir. Bu durumda, amortisman her dönemde aynıdır ve [Sabit servis ömrü amortismanı](straight-line-service-life-depreciation.md) içinde açıklandığı gibi, diğer alanlarda belirttiğiniz değerlerin etkilerini değerlendirmeniz gerekir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]