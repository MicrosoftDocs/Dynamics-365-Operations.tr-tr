---
title: NOW ER işlevi
description: Bu konu, NOW Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042355"
---
# <span data-ttu-id="e5762-103"><a name="NOW">NOW ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="e5762-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5762-104">`NOW` işlev, geçerli uygulama sunucusu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5762-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5762-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e5762-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="e5762-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e5762-106">Return values</span></span>

<span data-ttu-id="e5762-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="e5762-107">*DateTime*</span></span>

<span data-ttu-id="e5762-108">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="e5762-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="e5762-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="e5762-109">Example</span></span>

<span data-ttu-id="e5762-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarih/saat değerini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5762-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5762-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e5762-111">Additional resources</span></span>

[<span data-ttu-id="e5762-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="e5762-112">Date and time functions</span></span>](er-functions-category-datetime.md)
