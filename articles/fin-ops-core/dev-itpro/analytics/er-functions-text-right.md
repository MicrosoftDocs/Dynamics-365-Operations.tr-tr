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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682955"
---
# <a name="right-er-function"></a><span data-ttu-id="90846-103">RIGHT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="90846-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90846-104">Bu `RIGHT` işlevi belirtilen dizenin sonundan itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="90846-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="90846-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="90846-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="90846-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="90846-106">Arguments</span></span>

<span data-ttu-id="90846-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="90846-107">`text`: *String*</span></span>

<span data-ttu-id="90846-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="90846-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="90846-109">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="90846-109">`number`: *Integer*</span></span>

<span data-ttu-id="90846-110">Orijinal metnin sonundan itibaren döndürülmesi gereken karakter sayısı.</span><span class="sxs-lookup"><span data-stu-id="90846-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="90846-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="90846-111">Return values</span></span>

<span data-ttu-id="90846-112">*Dize*</span><span class="sxs-lookup"><span data-stu-id="90846-112">*String*</span></span>

<span data-ttu-id="90846-113">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="90846-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="90846-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="90846-114">Example</span></span>

<span data-ttu-id="90846-115">`RIGHT ("Sample", 3)`, **"ple"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="90846-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90846-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="90846-116">Additional resources</span></span>

[<span data-ttu-id="90846-117">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="90846-117">Text functions</span></span>](er-functions-category-text.md)
