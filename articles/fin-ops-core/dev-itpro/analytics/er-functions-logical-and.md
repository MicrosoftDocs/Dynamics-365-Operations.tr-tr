---
title: AND ER işlevi
description: Bu konu, AND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041843"
---
# <span data-ttu-id="1df3d-103"><a name="AND">AND ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="1df3d-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1df3d-104">Belirtilen koşulların tümü doğru ise, `AND` işlev *Boole* **DOĞRU** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1df3d-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="1df3d-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="1df3d-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df3d-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="1df3d-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="1df3d-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="1df3d-107">Arguments</span></span>

<span data-ttu-id="1df3d-108">`condition 1`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="1df3d-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="1df3d-109">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="1df3d-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="1df3d-110">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1df3d-110">This argument is required.</span></span>

<span data-ttu-id="1df3d-111">`condition N`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="1df3d-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="1df3d-112">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="1df3d-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="1df3d-113">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1df3d-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1df3d-114">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="1df3d-114">Return values</span></span>

<span data-ttu-id="1df3d-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="1df3d-115">*Boolean*</span></span>

<span data-ttu-id="1df3d-116">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="1df3d-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1df3d-117">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="1df3d-117">Usage notes</span></span>

<span data-ttu-id="1df3d-118">Mantıksal işlevlerin bağımsız değişkenlerinde, veri kaynağı başvurularını, sayısal ve metin değerlerini, Boole değerlerini, karşılaştırma işleçlerini ve diğer elektronik raporlama (ER) işlevlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df3d-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="1df3d-119">Ancak , tüm bağımsız değişkenlerin **doğru** veya **yanlış** *Boole* değeriyle değerlendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1df3d-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="1df3d-120">Örnek</span><span class="sxs-lookup"><span data-stu-id="1df3d-120">Example</span></span>

<span data-ttu-id="1df3d-121">`AND (1=1, "a"="a")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="1df3d-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="1df3d-122">`AND (1=2, "a"="a")`, **YANLIŞ** döndürür.</span><span class="sxs-lookup"><span data-stu-id="1df3d-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1df3d-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1df3d-123">Additional resources</span></span>

[<span data-ttu-id="1df3d-124">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="1df3d-124">Logical functions</span></span>](er-functions-category-logical.md)
