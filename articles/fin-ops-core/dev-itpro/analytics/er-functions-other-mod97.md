---
title: MOD_97 ER işlevi
description: Bu konu, MOD_97 Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070541"
---
# <span data-ttu-id="8fa5a-103"><a name="MOD_97">MOD_97 ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="8fa5a-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fa5a-104">Bu `MOD_97` işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak MOD97 ifadesi olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa5a-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8fa5a-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8fa5a-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="8fa5a-106">Arguments</span></span>

<span data-ttu-id="8fa5a-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="8fa5a-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8fa5a-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8fa5a-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="8fa5a-109">Return values</span></span>

<span data-ttu-id="8fa5a-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="8fa5a-110">*String*</span></span>

<span data-ttu-id="8fa5a-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8fa5a-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="8fa5a-112">Example</span></span>

<span data-ttu-id="8fa5a-113">`MOD_97 ("VEND-200002")`, **"20000285"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8fa5a-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8fa5a-114">Additional resources</span></span>

[<span data-ttu-id="8fa5a-115">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="8fa5a-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
