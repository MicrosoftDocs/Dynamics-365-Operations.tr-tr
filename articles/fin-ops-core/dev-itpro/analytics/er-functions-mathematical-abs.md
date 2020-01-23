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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917109"
---
# <span data-ttu-id="262a5-103"><a name="ABS">ABS ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="262a5-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="262a5-104">`ABS` işlev, belirtilen sayının mutlak değeri (katsayı) bir *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="262a5-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="262a5-105">Diğer bir deyişle, işareti olmadan sayıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="262a5-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="262a5-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="262a5-106">Syntax</span></span>

```
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="262a5-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="262a5-107">Arguments</span></span>

<span data-ttu-id="262a5-108">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="262a5-108">`number`: *Real*</span></span>

<span data-ttu-id="262a5-109">Modülü bir mod olmasını istediğiniz sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="262a5-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="262a5-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="262a5-110">Return values</span></span>

<span data-ttu-id="262a5-111">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="262a5-111">*Real*</span></span>

<span data-ttu-id="262a5-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="262a5-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="262a5-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="262a5-113">Example</span></span>

<span data-ttu-id="262a5-114">`ABS (-1)`, **1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="262a5-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="262a5-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="262a5-115">Additional resources</span></span>

[<span data-ttu-id="262a5-116">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="262a5-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
