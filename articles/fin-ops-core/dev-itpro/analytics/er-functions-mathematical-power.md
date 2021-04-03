---
title: POWER ER işlevi
description: Bu konu, POWER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570434"
---
# <a name="power-er-function"></a><span data-ttu-id="14eec-103">POWER ER işlevi</span><span class="sxs-lookup"><span data-stu-id="14eec-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14eec-104">`POWER` işlev, belirtilen pozitif sayıyı belirtilen güce yükseltme sonucunu gösteren *gerçek* bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="14eec-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="14eec-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="14eec-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="14eec-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="14eec-106">Arguments</span></span>

<span data-ttu-id="14eec-107">`number`: *Gerçek* veya *tamsayı*</span><span class="sxs-lookup"><span data-stu-id="14eec-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="14eec-108">Belirtilen üsse yükseltilmiş sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="14eec-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="14eec-109">`power`: *Gerçek* veya *tamsayı*</span><span class="sxs-lookup"><span data-stu-id="14eec-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="14eec-110">Belirli bir gücü temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="14eec-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="14eec-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="14eec-111">Return values</span></span>

<span data-ttu-id="14eec-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="14eec-112">*Real*</span></span>

<span data-ttu-id="14eec-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="14eec-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="14eec-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14eec-114">Example 1</span></span>

<span data-ttu-id="14eec-115">`POWER (10, 2)`, **100** döndürür.</span><span class="sxs-lookup"><span data-stu-id="14eec-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="14eec-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="14eec-116">Example 2</span></span>

<span data-ttu-id="14eec-117">`POWER (4, 0.5)`, **2** döndürür.</span><span class="sxs-lookup"><span data-stu-id="14eec-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14eec-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="14eec-118">Additional resources</span></span>

[<span data-ttu-id="14eec-119">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="14eec-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]