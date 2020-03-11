---
title: DAYOFYEAR ER işlevi
description: Bu konu, DAYOFYEAR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070679"
---
# <span data-ttu-id="0ddb6-103"><a name="DAYOFYEAR">DAYOFYEAR ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="0ddb6-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ddb6-104">`DAYOFYEAR` işlev, Ocak 1 ve belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddb6-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0ddb6-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="0ddb6-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="0ddb6-106">Arguments</span></span>

<span data-ttu-id="0ddb6-107">`date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="0ddb6-107">`date`: *Date*</span></span>

<span data-ttu-id="0ddb6-108">Gün sayısı hesaplaması için kullanılacak tarihi temsil eden bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ddb6-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="0ddb6-109">Return values</span></span>

<span data-ttu-id="0ddb6-110">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="0ddb6-110">*Integer*</span></span>

<span data-ttu-id="0ddb6-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0ddb6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0ddb6-112">Example 1</span></span>

<span data-ttu-id="0ddb6-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))`, **61** döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0ddb6-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0ddb6-114">Example 2</span></span>

<span data-ttu-id="0ddb6-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))`, **1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ddb6-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0ddb6-116">Additional resources</span></span>

[<span data-ttu-id="0ddb6-117">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="0ddb6-117">Date and time functions</span></span>](er-functions-category-datetime.md)
