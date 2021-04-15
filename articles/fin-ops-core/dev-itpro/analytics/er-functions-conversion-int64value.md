---
title: INT64VALUE ER işlevi
description: Bu konu, INT64VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755408"
---
# <a name="int64value-er-function"></a><span data-ttu-id="6bcf2-103">INT64VALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="6bcf2-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bcf2-104">Bu `INT64VALUE` işlevi, belirtilen dizeyi temsil eden bir *Int64* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6bcf2-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="6bcf2-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="6bcf2-106">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="6bcf2-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="6bcf2-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="6bcf2-107">Arguments</span></span>

<span data-ttu-id="6bcf2-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="6bcf2-108">`text`: *String*</span></span>

<span data-ttu-id="6bcf2-109">Bir *Int64* numarasına dönüştürülmesi gereken metin değeri.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="6bcf2-110">`number`: *Gerçek* veya *tamsayı*</span><span class="sxs-lookup"><span data-stu-id="6bcf2-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="6bcf2-111">Bir *Int64* numarasına dönüştürülmesi gereken sayısal *Gerçek* veya *Tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="6bcf2-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="6bcf2-112">Return values</span></span>

<span data-ttu-id="6bcf2-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="6bcf2-113">*Int64*</span></span>

<span data-ttu-id="6bcf2-114">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6bcf2-115">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="6bcf2-115">Usage notes</span></span>

<span data-ttu-id="6bcf2-116">Ondalık basamaklar kesilir.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="6bcf2-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bcf2-117">Example 1</span></span>

<span data-ttu-id="6bcf2-118">`INT64VALUE ("22565422744")`, *Int64* **22565422744** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6bcf2-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6bcf2-119">Example 2</span></span>

<span data-ttu-id="6bcf2-120">`INT64VALUE ( VALUE("22565422744.77"))`, *Int64* **22565422744** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bcf2-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6bcf2-121">Additional resources</span></span>

[<span data-ttu-id="6bcf2-122">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="6bcf2-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]