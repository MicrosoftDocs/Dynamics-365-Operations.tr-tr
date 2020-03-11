---
title: LOWER ER işlevi
description: Bu konu, LOWER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041113"
---
# <span data-ttu-id="157f0-103"><a name="LOWER">LOWER ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="157f0-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="157f0-104">Bu `LOWER` işlev, küçük harflere dönüştürüldükten sonra bir *dize* değeri olarak belirtilen metin dizesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="157f0-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="157f0-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="157f0-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="157f0-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="157f0-106">Arguments</span></span>

<span data-ttu-id="157f0-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="157f0-107">`text`: *String*</span></span>

<span data-ttu-id="157f0-108">Metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="157f0-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="157f0-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="157f0-109">Return values</span></span>

<span data-ttu-id="157f0-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="157f0-110">*String*</span></span>

<span data-ttu-id="157f0-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="157f0-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="157f0-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="157f0-112">Example</span></span>

<span data-ttu-id="157f0-113">`LOWER ("Sample")`, **"Örnek"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="157f0-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="157f0-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="157f0-114">Additional resources</span></span>

[<span data-ttu-id="157f0-115">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="157f0-115">Text functions</span></span>](er-functions-category-text.md)
