---
title: TRIM ER işlevi
description: Bu konu, TRIM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560049"
---
# <a name="trim-er-function"></a><span data-ttu-id="21ce6-103">TRIM ER işlevi</span><span class="sxs-lookup"><span data-stu-id="21ce6-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21ce6-104">`TRIM` işlevi, belirtilen metin dizesini baştaki ve sondaki boşluklar kesildikten ve sözcükler arasındaki birden fazla boşluk kaldırıldıktan sonra *Dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="21ce6-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ce6-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="21ce6-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="21ce6-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="21ce6-106">Arguments</span></span>

<span data-ttu-id="21ce6-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="21ce6-107">`text`: *String*</span></span>

<span data-ttu-id="21ce6-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="21ce6-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="21ce6-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="21ce6-109">Return values</span></span>

<span data-ttu-id="21ce6-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="21ce6-110">*String*</span></span>

<span data-ttu-id="21ce6-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="21ce6-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="21ce6-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="21ce6-112">Example</span></span>

<span data-ttu-id="21ce6-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")`, **"Örnek metin"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="21ce6-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21ce6-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="21ce6-114">Additional resources</span></span>

[<span data-ttu-id="21ce6-115">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="21ce6-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]