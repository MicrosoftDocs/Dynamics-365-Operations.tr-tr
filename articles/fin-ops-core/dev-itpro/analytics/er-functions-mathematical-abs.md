---
title: ABS ER işlevi
description: Bu konu, ABS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565796"
---
# <a name="abs-er-function"></a><span data-ttu-id="10257-103">ABS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="10257-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10257-104">`ABS` işlev, belirtilen sayının mutlak değeri (katsayı) bir *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="10257-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="10257-105">Diğer bir deyişle, işareti olmadan sayıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="10257-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="10257-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="10257-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="10257-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="10257-107">Arguments</span></span>

<span data-ttu-id="10257-108">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="10257-108">`number`: *Real*</span></span>

<span data-ttu-id="10257-109">Modülü bir mod olmasını istediğiniz sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="10257-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="10257-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="10257-110">Return values</span></span>

<span data-ttu-id="10257-111">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="10257-111">*Real*</span></span>

<span data-ttu-id="10257-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="10257-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="10257-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="10257-113">Example</span></span>

<span data-ttu-id="10257-114">`ABS (-1)`, **1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="10257-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10257-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="10257-115">Additional resources</span></span>

[<span data-ttu-id="10257-116">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="10257-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]