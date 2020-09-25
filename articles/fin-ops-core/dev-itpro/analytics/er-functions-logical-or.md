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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744635"
---
# <a name="or-er-function"></a><span data-ttu-id="87b94-103">OR ER işlevi</span><span class="sxs-lookup"><span data-stu-id="87b94-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87b94-104">Belirtilen koşulların tümü yanlış ise, `OR` işlev **yanlış** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="87b94-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="87b94-105">Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="87b94-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b94-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="87b94-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="87b94-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="87b94-107">Arguments</span></span>

<span data-ttu-id="87b94-108">`condition 1`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="87b94-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="87b94-109">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="87b94-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="87b94-110">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="87b94-110">This argument is required.</span></span>

<span data-ttu-id="87b94-111">`condition N`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="87b94-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="87b94-112">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="87b94-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="87b94-113">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="87b94-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="87b94-114">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="87b94-114">Return values</span></span>

<span data-ttu-id="87b94-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="87b94-115">*Boolean*</span></span>

<span data-ttu-id="87b94-116">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="87b94-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="87b94-117">Örnek</span><span class="sxs-lookup"><span data-stu-id="87b94-117">Example</span></span>

<span data-ttu-id="87b94-118">`OR (1=2, "a"="a")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="87b94-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87b94-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="87b94-119">Additional resources</span></span>

[<span data-ttu-id="87b94-120">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="87b94-120">Logical functions</span></span>](er-functions-category-logical.md)
