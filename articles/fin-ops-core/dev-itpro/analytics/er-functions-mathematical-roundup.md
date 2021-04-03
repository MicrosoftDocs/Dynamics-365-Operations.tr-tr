---
title: ROUNDUP ER işlevi
description: Bu konu, ROUNDUP Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d23a984bd59c4d2d37c407e3fcfed9c7017dcc7f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569347"
---
# <a name="roundup-er-function"></a><span data-ttu-id="f1ed7-103">ROUNDUP ER işlevi</span><span class="sxs-lookup"><span data-stu-id="f1ed7-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1ed7-104">`ROUNDUP` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yukarı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ed7-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="f1ed7-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="f1ed7-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="f1ed7-106">Arguments</span></span>

<span data-ttu-id="f1ed7-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="f1ed7-107">`number`: *Real*</span></span>

<span data-ttu-id="f1ed7-108">Yukarı yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="f1ed7-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="f1ed7-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="f1ed7-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1ed7-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="f1ed7-111">Return values</span></span>

<span data-ttu-id="f1ed7-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="f1ed7-112">*Real*</span></span>

<span data-ttu-id="f1ed7-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f1ed7-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="f1ed7-114">Usage notes</span></span>

<span data-ttu-id="f1ed7-115">Bu işlev [YUVARLA](er-functions-mathematical-round.md) işlevi gibi davranır ancak belirtilen sayıyı daima yukarı doğru (sıfırdan uzağa doğru) yuvarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="f1ed7-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1ed7-116">Example 1</span></span>

<span data-ttu-id="f1ed7-117">`ROUNDUP (1200.763, 2)` iki ondalık basamağa yukarı yuvarlar ve **1200.77** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f1ed7-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f1ed7-118">Example 2</span></span>

<span data-ttu-id="f1ed7-119">`ROUNDUP (1200.767, -3)`, 1.000'in en yakın katına yukarı yuvarlar ve **2000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1ed7-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f1ed7-120">Additional resources</span></span>

[<span data-ttu-id="f1ed7-121">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="f1ed7-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]