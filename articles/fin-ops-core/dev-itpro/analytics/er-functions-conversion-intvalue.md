---
title: INTVALUE ER işlevi
description: Bu konu, INTVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917730"
---
# <span data-ttu-id="84a55-103"><a name="INTVALUE">INTVALUE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="84a55-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84a55-104">Bu `INTVALUE` işlevi, belirtilen dizeyi temsil eden bir *Int* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="84a55-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="84a55-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="84a55-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="84a55-106">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="84a55-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="84a55-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="84a55-107">Arguments</span></span>

<span data-ttu-id="84a55-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="84a55-108">`text`: *String*</span></span>

<span data-ttu-id="84a55-109">Bir *Int* numarasına dönüştürülmesi gereken metin değeri.</span><span class="sxs-lookup"><span data-stu-id="84a55-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="84a55-110">`number`: *Gerçek* veya *tamsayı*</span><span class="sxs-lookup"><span data-stu-id="84a55-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="84a55-111">Bir *Int* numarasına dönüştürülmesi gereken sayısal *Gerçek* veya *Tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="84a55-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="84a55-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="84a55-112">Return values</span></span>

<span data-ttu-id="84a55-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="84a55-113">*Int*</span></span>

<span data-ttu-id="84a55-114">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="84a55-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="84a55-115">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="84a55-115">Usage notes</span></span>

<span data-ttu-id="84a55-116">Ondalık basamaklar kesilir.</span><span class="sxs-lookup"><span data-stu-id="84a55-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="84a55-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84a55-117">Example 1</span></span>

<span data-ttu-id="84a55-118">`INTVALUE ("100.77")`, *Int* **100** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="84a55-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="84a55-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="84a55-119">Example 2</span></span>

<span data-ttu-id="84a55-120">`INTVALUE (-100.77)`, *Int* **-100** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="84a55-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84a55-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="84a55-121">Additional resources</span></span>

[<span data-ttu-id="84a55-122">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="84a55-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
