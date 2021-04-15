---
title: OR ER işlevi
description: Bu konu, OR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: 9763cdbabfbaba1af433c1fd753b03982ecb550d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751751"
---
# <a name="or-er-function"></a><span data-ttu-id="e9488-103">OR ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e9488-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9488-104">Belirtilen koşulların tümü yanlış ise, `OR` işlev **yanlış** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9488-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="e9488-105">Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9488-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9488-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e9488-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="e9488-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e9488-107">Arguments</span></span>

<span data-ttu-id="e9488-108">`condition 1`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="e9488-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="e9488-109">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="e9488-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="e9488-110">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e9488-110">This argument is required.</span></span>

<span data-ttu-id="e9488-111">`condition N`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="e9488-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="e9488-112">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="e9488-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="e9488-113">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e9488-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9488-114">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e9488-114">Return values</span></span>

<span data-ttu-id="e9488-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="e9488-115">*Boolean*</span></span>

<span data-ttu-id="e9488-116">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="e9488-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="e9488-117">Örnek</span><span class="sxs-lookup"><span data-stu-id="e9488-117">Example</span></span>

<span data-ttu-id="e9488-118">`OR (1=2, "a"="a")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9488-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9488-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e9488-119">Additional resources</span></span>

[<span data-ttu-id="e9488-120">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="e9488-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]