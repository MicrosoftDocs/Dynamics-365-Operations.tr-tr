---
title: CURCREDREF ER işlevi
description: Bu konu, CURCREDREF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567628"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="e0af5-103">CURCREDREF ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e0af5-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0af5-104">Bu `CURCREDREF` işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0af5-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0af5-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e0af5-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="e0af5-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e0af5-106">Arguments</span></span>

<span data-ttu-id="e0af5-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="e0af5-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="e0af5-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="e0af5-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="e0af5-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e0af5-109">Return values</span></span>

<span data-ttu-id="e0af5-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e0af5-110">*String*</span></span>

<span data-ttu-id="e0af5-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="e0af5-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e0af5-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="e0af5-112">Example</span></span>

<span data-ttu-id="e0af5-113">`CURCredRef ("VEND-200002")`, **"2200002"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0af5-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0af5-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e0af5-114">Additional resources</span></span>

[<span data-ttu-id="e0af5-115">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="e0af5-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]