---
title: LEN ER işlevi
description: Bu konu, LEN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 394e07a7a573cc4462196b17440f8b0547d8dd48
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746327"
---
# <a name="len-er-function"></a><span data-ttu-id="3960e-103">LEN ER işlevi</span><span class="sxs-lookup"><span data-stu-id="3960e-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3960e-104">Bu `LEN` işlev, belirtilen dizedeki karakter sayısını bir *tamsayı* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="3960e-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3960e-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3960e-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="3960e-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="3960e-106">Arguments</span></span>

<span data-ttu-id="3960e-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="3960e-107">`text`: *String*</span></span>

<span data-ttu-id="3960e-108">Metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="3960e-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="3960e-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="3960e-109">Return values</span></span>

<span data-ttu-id="3960e-110">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="3960e-110">*Integer*</span></span>

<span data-ttu-id="3960e-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="3960e-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="3960e-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="3960e-112">Example</span></span>

<span data-ttu-id="3960e-113">`LEN ("Sample")`, **6** döndürür.</span><span class="sxs-lookup"><span data-stu-id="3960e-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3960e-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3960e-114">Additional resources</span></span>

[<span data-ttu-id="3960e-115">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="3960e-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]