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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042631"
---
# <span data-ttu-id="dcb12-103"><a name="VALUE">VALUE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="dcb12-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcb12-104">Bu `VALUE` işlevi, belirtilen dizeden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="dcb12-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb12-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="dcb12-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="dcb12-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="dcb12-106">Arguments</span></span>

<span data-ttu-id="dcb12-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="dcb12-107">`text`: *String*</span></span>

<span data-ttu-id="dcb12-108">Bir sayısal değere dönüştürülmesi gereken dize değeri.</span><span class="sxs-lookup"><span data-stu-id="dcb12-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="dcb12-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="dcb12-109">Return values</span></span>

<span data-ttu-id="dcb12-110">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="dcb12-110">*Real*</span></span>

<span data-ttu-id="dcb12-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="dcb12-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dcb12-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="dcb12-112">Usage notes</span></span>

<span data-ttu-id="dcb12-113">Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-), bir eksi işareti olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dcb12-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="dcb12-114">Belirtilen dizenin sayısal olmayan karakterler içermesi durumunda bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcb12-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="dcb12-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcb12-115">Example 1</span></span>

<span data-ttu-id="dcb12-116">`VALUE ("1 234,56")`, özel durum oluşturur:</span><span class="sxs-lookup"><span data-stu-id="dcb12-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="dcb12-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dcb12-117">Example 2</span></span>

<span data-ttu-id="dcb12-118">`VALUE ("1234,56")`, **1234.56** döndürür.</span><span class="sxs-lookup"><span data-stu-id="dcb12-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dcb12-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="dcb12-119">Additional resources</span></span>

[<span data-ttu-id="dcb12-120">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="dcb12-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
