---
title: INTVALUE ER işlevi
description: Bu konu, INTVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755384"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="7727a-103">INTVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="7727a-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7727a-104">Bu `INTVALUE` işlevi, belirtilen dizeyi temsil eden bir *Int* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7727a-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="7727a-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="7727a-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="7727a-106">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="7727a-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="7727a-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7727a-107">Arguments</span></span>

<span data-ttu-id="7727a-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="7727a-108">`text`: *String*</span></span>

<span data-ttu-id="7727a-109">Bir *Int* numarasına dönüştürülmesi gereken metin değeri.</span><span class="sxs-lookup"><span data-stu-id="7727a-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="7727a-110">`number`: *Gerçek* veya *tamsayı*</span><span class="sxs-lookup"><span data-stu-id="7727a-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="7727a-111">Bir *Int* numarasına dönüştürülmesi gereken sayısal *Gerçek* veya *Tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="7727a-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="7727a-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7727a-112">Return values</span></span>

<span data-ttu-id="7727a-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="7727a-113">*Int*</span></span>

<span data-ttu-id="7727a-114">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="7727a-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7727a-115">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="7727a-115">Usage notes</span></span>

<span data-ttu-id="7727a-116">Ondalık basamaklar kesilir.</span><span class="sxs-lookup"><span data-stu-id="7727a-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="7727a-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7727a-117">Example 1</span></span>

<span data-ttu-id="7727a-118">`INTVALUE ("100.77")`, *Int* **100** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7727a-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7727a-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7727a-119">Example 2</span></span>

<span data-ttu-id="7727a-120">`INTVALUE (-100.77)`, *Int* **-100** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7727a-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7727a-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7727a-121">Additional resources</span></span>

[<span data-ttu-id="7727a-122">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="7727a-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]