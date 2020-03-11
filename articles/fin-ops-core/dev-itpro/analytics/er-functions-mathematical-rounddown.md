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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92150bb23e76f82907e0f3e8f0738b25801958bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041582"
---
# <span data-ttu-id="76d70-103"><a name="ROUNDDOWN">ROUNDDOWN ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="76d70-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76d70-104">`ROUNDDOWN` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı aşağı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="76d70-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d70-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="76d70-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="76d70-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="76d70-106">Arguments</span></span>

<span data-ttu-id="76d70-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="76d70-107">`number`: *Real*</span></span>

<span data-ttu-id="76d70-108">Aşağı yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="76d70-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="76d70-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="76d70-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="76d70-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="76d70-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="76d70-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="76d70-111">Return values</span></span>

<span data-ttu-id="76d70-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="76d70-112">*Real*</span></span>

<span data-ttu-id="76d70-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="76d70-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="76d70-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="76d70-114">Usage notes</span></span>

<span data-ttu-id="76d70-115">Bu işlev [YUVARLA](er-functions-mathematical-round.md) işlevi gibi davranır ancak belirtilen sayıyı daima aşağı doğru (sıfıra doğru) yuvarlar.</span><span class="sxs-lookup"><span data-stu-id="76d70-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="76d70-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76d70-116">Example 1</span></span>

<span data-ttu-id="76d70-117">`ROUNDDOWN (1200.767, 2)` iki ondalık basamağa aşağı yuvarlar ve **1200.76** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="76d70-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="76d70-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76d70-118">Example 2</span></span>

<span data-ttu-id="76d70-119">`ROUNDDOWN (1700.767, -3)`, 1.000'in en yakın katına aşağı yuvarlar ve **1000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="76d70-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76d70-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="76d70-120">Additional resources</span></span>

[<span data-ttu-id="76d70-121">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="76d70-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
