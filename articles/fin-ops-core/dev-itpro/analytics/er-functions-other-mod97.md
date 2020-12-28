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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e4e40fbd953b31225ccc0f54912b26933ccc48
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680650"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="21c3c-103">MOD_97 ER işlevi</span><span class="sxs-lookup"><span data-stu-id="21c3c-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21c3c-104">Bu `MOD_97` işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak MOD97 ifadesi olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="21c3c-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="21c3c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="21c3c-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="21c3c-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="21c3c-106">Arguments</span></span>

<span data-ttu-id="21c3c-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="21c3c-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="21c3c-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="21c3c-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="21c3c-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="21c3c-109">Return values</span></span>

<span data-ttu-id="21c3c-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="21c3c-110">*String*</span></span>

<span data-ttu-id="21c3c-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="21c3c-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="21c3c-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="21c3c-112">Example</span></span>

<span data-ttu-id="21c3c-113">`MOD_97 ("VEND-200002")`, **"20000285"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="21c3c-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21c3c-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="21c3c-114">Additional resources</span></span>

[<span data-ttu-id="21c3c-115">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="21c3c-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
