---
title: NULLDATETIME ER işlevi
description: Bu konu, NULLDATETIME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 9e1aaed3e85fc99d6451577d19e834afd37ad008
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743555"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="e13ad-103">NULLDATETIME ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e13ad-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e13ad-104">`NULLDATETIME` işlev,eşgüdümlü evrensel saat (Greenwich Saati \[GMT\]) içinde **boş** tarih/zaman değerini (1 Ocak, 1900) gösteren bir *tarih saat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e13ad-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="e13ad-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e13ad-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="e13ad-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e13ad-106">Return values</span></span>

<span data-ttu-id="e13ad-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="e13ad-107">*DateTime*</span></span>

<span data-ttu-id="e13ad-108">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="e13ad-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="e13ad-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="e13ad-109">Example</span></span>

<span data-ttu-id="e13ad-110">`DATETIMEFORMAT( NULLDATETIME(), "O")`, Saat dilimi değerine sahip bir uygulama kullanıcısı tarafından başlatılan bir işlem sırasında çağrıldığında **1900-01-01T 00:00:00.0000000+00:00** dize değerini döndürür, **dil ve ülke/bölge tercihleri** bölümünde **Eşgüdümlü Evrensel Saat** (GMT).</span><span class="sxs-lookup"><span data-stu-id="e13ad-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e13ad-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e13ad-111">Additional resources</span></span>

[<span data-ttu-id="e13ad-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="e13ad-112">Date and time functions</span></span>](er-functions-category-datetime.md)
