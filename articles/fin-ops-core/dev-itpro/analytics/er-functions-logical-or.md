---
title: OR ER işlevi
description: Bu konu, OR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686990"
---
# <a name="or-er-function"></a><span data-ttu-id="121dc-103">OR ER işlevi</span><span class="sxs-lookup"><span data-stu-id="121dc-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="121dc-104">Belirtilen koşulların tümü yanlış ise, `OR` işlev **yanlış** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="121dc-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="121dc-105">Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="121dc-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="121dc-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="121dc-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="121dc-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="121dc-107">Arguments</span></span>

<span data-ttu-id="121dc-108">`condition 1`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="121dc-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="121dc-109">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="121dc-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="121dc-110">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="121dc-110">This argument is required.</span></span>

<span data-ttu-id="121dc-111">`condition N`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="121dc-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="121dc-112">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="121dc-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="121dc-113">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="121dc-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="121dc-114">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="121dc-114">Return values</span></span>

<span data-ttu-id="121dc-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="121dc-115">*Boolean*</span></span>

<span data-ttu-id="121dc-116">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="121dc-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="121dc-117">Örnek</span><span class="sxs-lookup"><span data-stu-id="121dc-117">Example</span></span>

<span data-ttu-id="121dc-118">`OR (1=2, "a"="a")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="121dc-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="121dc-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="121dc-119">Additional resources</span></span>

[<span data-ttu-id="121dc-120">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="121dc-120">Logical functions</span></span>](er-functions-category-logical.md)
