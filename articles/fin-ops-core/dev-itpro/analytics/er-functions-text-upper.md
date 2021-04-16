---
title: UPPER ER işlevi
description: Bu konu, UPPER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749153"
---
# <a name="upper-er-function"></a><span data-ttu-id="fd698-103">UPPER ER işlevi</span><span class="sxs-lookup"><span data-stu-id="fd698-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd698-104">Bu `UPPER` işlev, büyük harflere dönüştürüldükten sonra bir *dize* değeri olarak belirtilen metin dizesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd698-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd698-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="fd698-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="fd698-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="fd698-106">Arguments</span></span>

<span data-ttu-id="fd698-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="fd698-107">`text`: *String*</span></span>

<span data-ttu-id="fd698-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="fd698-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd698-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="fd698-109">Return values</span></span>

<span data-ttu-id="fd698-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="fd698-110">*String*</span></span>

<span data-ttu-id="fd698-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fd698-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fd698-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="fd698-112">Example</span></span>

<span data-ttu-id="fd698-113">`UPPER ("Sample")`, **"ÖRNEK"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd698-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd698-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fd698-114">Additional resources</span></span>

[<span data-ttu-id="fd698-115">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="fd698-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]