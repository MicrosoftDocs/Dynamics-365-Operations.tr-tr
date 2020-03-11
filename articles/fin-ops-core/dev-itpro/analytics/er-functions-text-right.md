---
title: RIGHT ER işlevi
description: Bu konu, RIGHT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040883"
---
# <span data-ttu-id="422e6-103"><a name="RIGHT">RIGHT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="422e6-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="422e6-104">Bu `RIGHT` işlevi belirtilen dizenin sonundan itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="422e6-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="422e6-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="422e6-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="422e6-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="422e6-106">Arguments</span></span>

<span data-ttu-id="422e6-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="422e6-107">`text`: *String*</span></span>

<span data-ttu-id="422e6-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="422e6-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="422e6-109">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="422e6-109">`number`: *Integer*</span></span>

<span data-ttu-id="422e6-110">Orijinal metnin sonundan itibaren döndürülmesi gereken karakter sayısı.</span><span class="sxs-lookup"><span data-stu-id="422e6-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="422e6-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="422e6-111">Return values</span></span>

<span data-ttu-id="422e6-112">*Dize*</span><span class="sxs-lookup"><span data-stu-id="422e6-112">*String*</span></span>

<span data-ttu-id="422e6-113">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="422e6-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="422e6-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="422e6-114">Example</span></span>

<span data-ttu-id="422e6-115">`RIGHT ("Sample", 3)`, **"ple"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="422e6-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="422e6-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="422e6-116">Additional resources</span></span>

[<span data-ttu-id="422e6-117">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="422e6-117">Text functions</span></span>](er-functions-category-text.md)
