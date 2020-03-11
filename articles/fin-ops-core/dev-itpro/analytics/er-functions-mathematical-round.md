---
title: ROUND ER işlevi
description: Bu konu, ROUND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041619"
---
# <span data-ttu-id="b6180-103"><a name="ROUND">ROUND ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="b6180-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6180-104">`ROUND` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="b6180-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6180-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="b6180-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b6180-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b6180-106">Arguments</span></span>

<span data-ttu-id="b6180-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="b6180-107">`number`: *Real*</span></span>

<span data-ttu-id="b6180-108">Yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="b6180-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="b6180-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="b6180-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b6180-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="b6180-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6180-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b6180-111">Return values</span></span>

<span data-ttu-id="b6180-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="b6180-112">*Real*</span></span>

<span data-ttu-id="b6180-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="b6180-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6180-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="b6180-114">Usage notes</span></span>

<span data-ttu-id="b6180-115">Ondalık parametresinin değeri 0'dan (sıfır) büyükse, belirtilen sayı birçok `decimals` basamağa yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="b6180-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="b6180-116">`decimals` bağımsız değişkeni değeri **0** (sıfır) ise, belirtilen sayı en yakın tamsayıya yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="b6180-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="b6180-117">`decimals` bağımsız değişkeni değeri 0'dan (sıfır) küçükse, belirtilen sayı ondalık basamağın soluna yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="b6180-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="b6180-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6180-118">Example 1</span></span>

<span data-ttu-id="b6180-119">`ROUND (1200.767, 2)` iki ondalık basamağa yuvarlar ve **1200.77** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="b6180-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b6180-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b6180-120">Example 2</span></span>

<span data-ttu-id="b6180-121">`ROUND (1200.767, -3)`, 1.000'in en yakın katına yuvarlar ve **1000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="b6180-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6180-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b6180-122">Additional resources</span></span>

[<span data-ttu-id="b6180-123">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="b6180-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
