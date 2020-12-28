---
title: NUMBERVALUE ER işlevi
description: Bu konu, NUMBERVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3eec6dc5a472f366c9029456fe05cf1e431e1c5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685991"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="0799a-103">NUMBERVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="0799a-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0799a-104">Bu `NUMBERVALUE` işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0799a-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="0799a-105">Dönüştürme sırasında, belirtilen ondalık ve basamak gruplandırma ayırıcıları dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="0799a-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="0799a-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0799a-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="0799a-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="0799a-107">Arguments</span></span>

<span data-ttu-id="0799a-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="0799a-108">`text`: *String*</span></span>

<span data-ttu-id="0799a-109">Bir *Gerçek* numarasına dönüştürülmesi gereken metin değeri.</span><span class="sxs-lookup"><span data-stu-id="0799a-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="0799a-110">`decimal separator`: Dize</span><span class="sxs-lookup"><span data-stu-id="0799a-110">`decimal separator`: String</span></span>

<span data-ttu-id="0799a-111">Ondalık ayırıcısı.</span><span class="sxs-lookup"><span data-stu-id="0799a-111">A decimal separator.</span></span> <span data-ttu-id="0799a-112">Ondalık sayının tamsayı ve kesirli kısımlarını ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0799a-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="0799a-113">`digit grouping separator`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="0799a-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="0799a-114">Basamak gruplandırma ayırıcısı.</span><span class="sxs-lookup"><span data-stu-id="0799a-114">A digit grouping separator.</span></span> <span data-ttu-id="0799a-115">Binler ayırıcısı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0799a-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="0799a-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="0799a-116">Return values</span></span>

<span data-ttu-id="0799a-117">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="0799a-117">*Real*</span></span>

<span data-ttu-id="0799a-118">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="0799a-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="0799a-119">Örnek</span><span class="sxs-lookup"><span data-stu-id="0799a-119">Example</span></span>

<span data-ttu-id="0799a-120">`NUMBERVALUE( "1 234,56", ",", " ")`, **1234.56** döndürür.</span><span class="sxs-lookup"><span data-stu-id="0799a-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0799a-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0799a-121">Additional resources</span></span>

[<span data-ttu-id="0799a-122">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="0799a-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
