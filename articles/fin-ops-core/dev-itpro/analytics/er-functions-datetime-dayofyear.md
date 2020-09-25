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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745501"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="79005-103">DAYOFYEAR ER işlevi</span><span class="sxs-lookup"><span data-stu-id="79005-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79005-104">`DAYOFYEAR` işlev, Ocak 1 ve belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.</span><span class="sxs-lookup"><span data-stu-id="79005-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="79005-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="79005-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="79005-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="79005-106">Arguments</span></span>

<span data-ttu-id="79005-107">`date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="79005-107">`date`: *Date*</span></span>

<span data-ttu-id="79005-108">Gün sayısı hesaplaması için kullanılacak tarihi temsil eden bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="79005-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="79005-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="79005-109">Return values</span></span>

<span data-ttu-id="79005-110">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="79005-110">*Integer*</span></span>

<span data-ttu-id="79005-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="79005-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="79005-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79005-112">Example 1</span></span>

<span data-ttu-id="79005-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))`, **61** döndürür.</span><span class="sxs-lookup"><span data-stu-id="79005-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="79005-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="79005-114">Example 2</span></span>

<span data-ttu-id="79005-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))`, **1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="79005-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79005-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="79005-116">Additional resources</span></span>

[<span data-ttu-id="79005-117">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="79005-117">Date and time functions</span></span>](er-functions-category-datetime.md)
