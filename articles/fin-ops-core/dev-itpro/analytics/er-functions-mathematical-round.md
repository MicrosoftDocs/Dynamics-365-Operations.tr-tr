---
title: ROUND ER işlevi
description: Bu konu, ROUND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570410"
---
# <a name="round-er-function"></a><span data-ttu-id="3c65f-103">ROUND ER işlevi</span><span class="sxs-lookup"><span data-stu-id="3c65f-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c65f-104">`ROUND` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c65f-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c65f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3c65f-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="3c65f-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="3c65f-106">Arguments</span></span>

<span data-ttu-id="3c65f-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="3c65f-107">`number`: *Real*</span></span>

<span data-ttu-id="3c65f-108">Yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="3c65f-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="3c65f-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="3c65f-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="3c65f-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="3c65f-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c65f-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="3c65f-111">Return values</span></span>

<span data-ttu-id="3c65f-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="3c65f-112">*Real*</span></span>

<span data-ttu-id="3c65f-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="3c65f-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3c65f-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="3c65f-114">Usage notes</span></span>

<span data-ttu-id="3c65f-115">Ondalık parametresinin değeri 0'dan (sıfır) büyükse, belirtilen sayı birçok `decimals` basamağa yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="3c65f-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="3c65f-116">`decimals` bağımsız değişkeni değeri **0** (sıfır) ise, belirtilen sayı en yakın çift tamsayıya yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="3c65f-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="3c65f-117">`decimals` bağımsız değişkeni değeri 0'dan (sıfır) küçükse, belirtilen sayı ondalık basamağın soluna yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="3c65f-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="3c65f-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c65f-118">Example 1</span></span>

<span data-ttu-id="3c65f-119">`ROUND (1200.767, 2)` iki ondalık basamağa yuvarlar ve **1200.77** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c65f-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3c65f-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3c65f-120">Example 2</span></span>

<span data-ttu-id="3c65f-121">`ROUND (1200.767, -3)`, 1.000'in en yakın katına yuvarlar ve **1000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c65f-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="3c65f-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3c65f-122">Example 3</span></span>

<span data-ttu-id="3c65f-123">`ROUND (1200.5, 0)`, en yakın çift tamsayıya yuvarlanır ve **1200** değerini döndürür, `ROUND (1201.5, 0)` de aynısını yapar ve **1202** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c65f-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c65f-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3c65f-124">Additional resources</span></span>

[<span data-ttu-id="3c65f-125">Matematiksel işlevler</span><span class="sxs-lookup"><span data-stu-id="3c65f-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]