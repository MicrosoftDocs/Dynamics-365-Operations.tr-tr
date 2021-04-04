---
title: ROUNDDOWN ER işlevi
description: Bu konu, ROUNDDOWN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567152"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="15b94-103">ROUNDDOWN ER işlevi</span><span class="sxs-lookup"><span data-stu-id="15b94-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15b94-104">`ROUNDDOWN` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı aşağı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="15b94-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b94-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="15b94-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="15b94-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="15b94-106">Arguments</span></span>

<span data-ttu-id="15b94-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="15b94-107">`number`: *Real*</span></span>

<span data-ttu-id="15b94-108">Aşağı yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="15b94-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="15b94-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="15b94-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="15b94-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="15b94-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="15b94-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="15b94-111">Return values</span></span>

<span data-ttu-id="15b94-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="15b94-112">*Real*</span></span>

<span data-ttu-id="15b94-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="15b94-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="15b94-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="15b94-114">Usage notes</span></span>

<span data-ttu-id="15b94-115">Bu işlev [YUVARLA](er-functions-mathematical-round.md) işlevi gibi davranır ancak belirtilen sayıyı daima aşağı doğru (sıfıra doğru) yuvarlar.</span><span class="sxs-lookup"><span data-stu-id="15b94-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="15b94-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15b94-116">Example 1</span></span>

<span data-ttu-id="15b94-117">`ROUNDDOWN (1200.767, 2)` iki ondalık basamağa aşağı yuvarlar ve **1200.76** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="15b94-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="15b94-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="15b94-118">Example 2</span></span>

<span data-ttu-id="15b94-119">`ROUNDDOWN (1700.767, -3)`, 1.000'in en yakın katına aşağı yuvarlar ve **1000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="15b94-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15b94-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="15b94-120">Additional resources</span></span>

[<span data-ttu-id="15b94-121">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="15b94-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]