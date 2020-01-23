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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917638"
---
# <span data-ttu-id="1443f-103"><a name="VALUE">VALUE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="1443f-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1443f-104">Bu `VALUE` işlevi, belirtilen dizeden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="1443f-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1443f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="1443f-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="1443f-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="1443f-106">Arguments</span></span>

<span data-ttu-id="1443f-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="1443f-107">`text`: *String*</span></span>

<span data-ttu-id="1443f-108">Bir sayısal değere dönüştürülmesi gereken dize değeri.</span><span class="sxs-lookup"><span data-stu-id="1443f-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="1443f-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="1443f-109">Return values</span></span>

<span data-ttu-id="1443f-110">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="1443f-110">*Real*</span></span>

<span data-ttu-id="1443f-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="1443f-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1443f-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="1443f-112">Usage notes</span></span>

<span data-ttu-id="1443f-113">Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-), bir eksi işareti olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1443f-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="1443f-114">Belirtilen dizenin sayısal olmayan karakterler içermesi durumunda bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1443f-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="1443f-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1443f-115">Example 1</span></span>

<span data-ttu-id="1443f-116">`VALUE ("1 234,56")`, özel durum oluşturur:</span><span class="sxs-lookup"><span data-stu-id="1443f-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="1443f-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1443f-117">Example 2</span></span>

<span data-ttu-id="1443f-118">`VALUE ("1234,56")`, **1234.56** döndürür.</span><span class="sxs-lookup"><span data-stu-id="1443f-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1443f-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1443f-119">Additional resources</span></span>

[<span data-ttu-id="1443f-120">Tür dönüştürme işlemleri</span><span class="sxs-lookup"><span data-stu-id="1443f-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
