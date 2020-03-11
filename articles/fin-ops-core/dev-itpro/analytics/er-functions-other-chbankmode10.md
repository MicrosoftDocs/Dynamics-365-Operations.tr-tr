---
title: CH_BANK_MOD_10 ER işlevi
description: Bu konu, CH_BANK_MOD_10 Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 808e328bfcc35c96091da9a69850429b82a71070
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070587"
---
# <span data-ttu-id="fa0e3-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="fa0e3-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa0e3-104">Bu `CH_BANK_MOD_10` işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak MOD10 ifadesi olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa0e3-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0e3-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="fa0e3-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="fa0e3-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="fa0e3-106">Arguments</span></span>

<span data-ttu-id="fa0e3-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="fa0e3-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="fa0e3-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fa0e3-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="fa0e3-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="fa0e3-109">Return values</span></span>

<span data-ttu-id="fa0e3-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="fa0e3-110">*String*</span></span>

<span data-ttu-id="fa0e3-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fa0e3-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fa0e3-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="fa0e3-112">Example</span></span>

<span data-ttu-id="fa0e3-113">`CH_BANK_MOD_10 ("VEND-200002")`, **3** döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa0e3-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa0e3-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fa0e3-114">Additional resources</span></span>

[<span data-ttu-id="fa0e3-115">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="fa0e3-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
