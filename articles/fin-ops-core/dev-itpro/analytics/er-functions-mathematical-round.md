---
title: ROUND ER işlevi
description: Bu konu, ROUND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683268"
---
# <a name="round-er-function"></a><span data-ttu-id="ba7d2-103">ROUND ER işlevi</span><span class="sxs-lookup"><span data-stu-id="ba7d2-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba7d2-104">`ROUND` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7d2-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ba7d2-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="ba7d2-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="ba7d2-106">Arguments</span></span>

<span data-ttu-id="ba7d2-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="ba7d2-107">`number`: *Real*</span></span>

<span data-ttu-id="ba7d2-108">Yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="ba7d2-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="ba7d2-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="ba7d2-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba7d2-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ba7d2-111">Return values</span></span>

<span data-ttu-id="ba7d2-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="ba7d2-112">*Real*</span></span>

<span data-ttu-id="ba7d2-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ba7d2-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="ba7d2-114">Usage notes</span></span>

<span data-ttu-id="ba7d2-115">Ondalık parametresinin değeri 0'dan (sıfır) büyükse, belirtilen sayı birçok `decimals` basamağa yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="ba7d2-116">`decimals` bağımsız değişkeni değeri **0** (sıfır) ise, belirtilen sayı en yakın çift tamsayıya yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="ba7d2-117">`decimals` bağımsız değişkeni değeri 0'dan (sıfır) küçükse, belirtilen sayı ondalık basamağın soluna yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="ba7d2-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba7d2-118">Example 1</span></span>

<span data-ttu-id="ba7d2-119">`ROUND (1200.767, 2)` iki ondalık basamağa yuvarlar ve **1200.77** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ba7d2-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ba7d2-120">Example 2</span></span>

<span data-ttu-id="ba7d2-121">`ROUND (1200.767, -3)`, 1.000'in en yakın katına yuvarlar ve **1000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="ba7d2-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ba7d2-122">Example 3</span></span>

<span data-ttu-id="ba7d2-123">`ROUND (1200.5, 0)`, en yakın çift tamsayıya yuvarlanır ve **1200** değerini döndürür, `ROUND (1201.5, 0)` de aynısını yapar ve **1202** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba7d2-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ba7d2-124">Additional resources</span></span>

[<span data-ttu-id="ba7d2-125">Matematiksel işlevler</span><span class="sxs-lookup"><span data-stu-id="ba7d2-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)
