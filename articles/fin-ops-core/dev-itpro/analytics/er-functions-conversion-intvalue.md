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
ms.openlocfilehash: 5e06236bf1d158a4cf579b8b89cc0a5f7d815c38
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042674"
---
# <span data-ttu-id="1912f-103"><a name="INTVALUE">INTVALUE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="1912f-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1912f-104">Bu `INTVALUE` işlevi, belirtilen dizeyi temsil eden bir *Int* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="1912f-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1912f-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="1912f-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="1912f-106">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="1912f-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="1912f-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="1912f-107">Arguments</span></span>

<span data-ttu-id="1912f-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="1912f-108">`text`: *String*</span></span>

<span data-ttu-id="1912f-109">Bir *Int* numarasına dönüştürülmesi gereken metin değeri.</span><span class="sxs-lookup"><span data-stu-id="1912f-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="1912f-110">`number`: *Gerçek* veya *tamsayı*</span><span class="sxs-lookup"><span data-stu-id="1912f-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1912f-111">Bir *Int* numarasına dönüştürülmesi gereken sayısal *Gerçek* veya *Tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="1912f-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1912f-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="1912f-112">Return values</span></span>

<span data-ttu-id="1912f-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="1912f-113">*Int*</span></span>

<span data-ttu-id="1912f-114">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="1912f-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1912f-115">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="1912f-115">Usage notes</span></span>

<span data-ttu-id="1912f-116">Ondalık basamaklar kesilir.</span><span class="sxs-lookup"><span data-stu-id="1912f-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="1912f-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1912f-117">Example 1</span></span>

<span data-ttu-id="1912f-118">`INTVALUE ("100.77")`, *Int* **100** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1912f-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1912f-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1912f-119">Example 2</span></span>

<span data-ttu-id="1912f-120">`INTVALUE (-100.77)`, *Int* **-100** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1912f-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1912f-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1912f-121">Additional resources</span></span>

[<span data-ttu-id="1912f-122">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="1912f-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
