---
title: ROUNDDOWN ER işlevi
description: Bu konu, ROUNDDOWN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686894"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="4159d-103">ROUNDDOWN ER işlevi</span><span class="sxs-lookup"><span data-stu-id="4159d-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4159d-104">`ROUNDDOWN` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı aşağı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="4159d-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="4159d-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="4159d-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="4159d-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="4159d-106">Arguments</span></span>

<span data-ttu-id="4159d-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="4159d-107">`number`: *Real*</span></span>

<span data-ttu-id="4159d-108">Aşağı yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="4159d-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="4159d-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="4159d-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="4159d-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="4159d-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="4159d-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="4159d-111">Return values</span></span>

<span data-ttu-id="4159d-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="4159d-112">*Real*</span></span>

<span data-ttu-id="4159d-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="4159d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4159d-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="4159d-114">Usage notes</span></span>

<span data-ttu-id="4159d-115">Bu işlev [YUVARLA](er-functions-mathematical-round.md) işlevi gibi davranır ancak belirtilen sayıyı daima aşağı doğru (sıfıra doğru) yuvarlar.</span><span class="sxs-lookup"><span data-stu-id="4159d-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="4159d-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4159d-116">Example 1</span></span>

<span data-ttu-id="4159d-117">`ROUNDDOWN (1200.767, 2)` iki ondalık basamağa aşağı yuvarlar ve **1200.76** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="4159d-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="4159d-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4159d-118">Example 2</span></span>

<span data-ttu-id="4159d-119">`ROUNDDOWN (1700.767, -3)`, 1.000'in en yakın katına aşağı yuvarlar ve **1000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="4159d-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4159d-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4159d-120">Additional resources</span></span>

[<span data-ttu-id="4159d-121">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="4159d-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
