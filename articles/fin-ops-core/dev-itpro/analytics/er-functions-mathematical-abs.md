---
title: ABS ER işlevi
description: Bu konu, ABS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744611"
---
# <a name="abs-er-function"></a><span data-ttu-id="49319-103">ABS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="49319-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49319-104">`ABS` işlev, belirtilen sayının mutlak değeri (katsayı) bir *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="49319-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="49319-105">Diğer bir deyişle, işareti olmadan sayıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="49319-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="49319-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="49319-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="49319-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="49319-107">Arguments</span></span>

<span data-ttu-id="49319-108">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="49319-108">`number`: *Real*</span></span>

<span data-ttu-id="49319-109">Modülü bir mod olmasını istediğiniz sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="49319-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="49319-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="49319-110">Return values</span></span>

<span data-ttu-id="49319-111">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="49319-111">*Real*</span></span>

<span data-ttu-id="49319-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="49319-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="49319-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="49319-113">Example</span></span>

<span data-ttu-id="49319-114">`ABS (-1)`, **1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="49319-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49319-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="49319-115">Additional resources</span></span>

[<span data-ttu-id="49319-116">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="49319-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
