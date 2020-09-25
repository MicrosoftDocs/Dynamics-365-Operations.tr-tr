---
title: VALUE ER işlevi
description: Bu konu, VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745525"
---
# <a name="value-er-function"></a><span data-ttu-id="c0a3c-103">VALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="c0a3c-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0a3c-104">Bu `VALUE` işlevi, belirtilen dizeden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a3c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="c0a3c-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="c0a3c-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="c0a3c-106">Arguments</span></span>

<span data-ttu-id="c0a3c-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="c0a3c-107">`text`: *String*</span></span>

<span data-ttu-id="c0a3c-108">Bir sayısal değere dönüştürülmesi gereken dize değeri.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0a3c-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="c0a3c-109">Return values</span></span>

<span data-ttu-id="c0a3c-110">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="c0a3c-110">*Real*</span></span>

<span data-ttu-id="c0a3c-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c0a3c-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="c0a3c-112">Usage notes</span></span>

<span data-ttu-id="c0a3c-113">Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-), bir eksi işareti olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="c0a3c-114">Belirtilen dizenin sayısal olmayan karakterler içermesi durumunda bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0a3c-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0a3c-115">Example 1</span></span>

<span data-ttu-id="c0a3c-116">`VALUE ("1 234,56")`, özel durum oluşturur:</span><span class="sxs-lookup"><span data-stu-id="c0a3c-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0a3c-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c0a3c-117">Example 2</span></span>

<span data-ttu-id="c0a3c-118">`VALUE ("1234,56")`, **1234.56** döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0a3c-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c0a3c-119">Additional resources</span></span>

[<span data-ttu-id="c0a3c-120">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="c0a3c-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
