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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683293"
---
# <a name="abs-er-function"></a><span data-ttu-id="24e51-103">ABS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="24e51-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24e51-104">`ABS` işlev, belirtilen sayının mutlak değeri (katsayı) bir *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="24e51-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="24e51-105">Diğer bir deyişle, işareti olmadan sayıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="24e51-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e51-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="24e51-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="24e51-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="24e51-107">Arguments</span></span>

<span data-ttu-id="24e51-108">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="24e51-108">`number`: *Real*</span></span>

<span data-ttu-id="24e51-109">Modülü bir mod olmasını istediğiniz sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="24e51-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="24e51-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="24e51-110">Return values</span></span>

<span data-ttu-id="24e51-111">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="24e51-111">*Real*</span></span>

<span data-ttu-id="24e51-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="24e51-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="24e51-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="24e51-113">Example</span></span>

<span data-ttu-id="24e51-114">`ABS (-1)`, **1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="24e51-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24e51-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="24e51-115">Additional resources</span></span>

[<span data-ttu-id="24e51-116">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="24e51-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
