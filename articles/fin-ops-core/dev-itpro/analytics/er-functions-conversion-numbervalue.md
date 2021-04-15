---
title: NUMBERVALUE ER işlevi
description: Bu konu, NUMBERVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755360"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="8ecac-103">NUMBERVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="8ecac-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ecac-104">Bu `NUMBERVALUE` işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ecac-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="8ecac-105">Dönüştürme sırasında, belirtilen ondalık ve basamak gruplandırma ayırıcıları dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="8ecac-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ecac-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8ecac-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="8ecac-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="8ecac-107">Arguments</span></span>

<span data-ttu-id="8ecac-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="8ecac-108">`text`: *String*</span></span>

<span data-ttu-id="8ecac-109">Bir *Gerçek* numarasına dönüştürülmesi gereken metin değeri.</span><span class="sxs-lookup"><span data-stu-id="8ecac-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="8ecac-110">`decimal separator`: Dize</span><span class="sxs-lookup"><span data-stu-id="8ecac-110">`decimal separator`: String</span></span>

<span data-ttu-id="8ecac-111">Ondalık ayırıcısı.</span><span class="sxs-lookup"><span data-stu-id="8ecac-111">A decimal separator.</span></span> <span data-ttu-id="8ecac-112">Ondalık sayının tamsayı ve kesirli kısımlarını ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8ecac-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="8ecac-113">`digit grouping separator`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="8ecac-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="8ecac-114">Basamak gruplandırma ayırıcısı.</span><span class="sxs-lookup"><span data-stu-id="8ecac-114">A digit grouping separator.</span></span> <span data-ttu-id="8ecac-115">Binler ayırıcısı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8ecac-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ecac-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="8ecac-116">Return values</span></span>

<span data-ttu-id="8ecac-117">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="8ecac-117">*Real*</span></span>

<span data-ttu-id="8ecac-118">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="8ecac-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8ecac-119">Örnek</span><span class="sxs-lookup"><span data-stu-id="8ecac-119">Example</span></span>

<span data-ttu-id="8ecac-120">`NUMBERVALUE( "1 234,56", ",", " ")`, **1234.56** döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ecac-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ecac-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8ecac-121">Additional resources</span></span>

[<span data-ttu-id="8ecac-122">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="8ecac-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]