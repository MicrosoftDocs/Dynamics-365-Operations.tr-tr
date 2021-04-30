---
title: ROUNDAMOUNT ER işlevi
description: Bu konu, ROUNDAMOUNT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: 7dfc7817eab68e9dd70ce84e68f26d14fd8cf1df
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891221"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="7a9a9-103">ROUNDAMOUNT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="7a9a9-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a9a9-104">`ROUNDAMOUNT` işlev, belirtilen yuvarlama kuralına göre başka sayının en yakın katına belirtilen sayının yuvarlanmasının sonucu olarak *gerçek* bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a9a9-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7a9a9-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="7a9a9-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7a9a9-106">Arguments</span></span>

<span data-ttu-id="7a9a9-107">`number`: *Tam* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="7a9a9-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="7a9a9-108">Yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="7a9a9-109">`decimals`: *Tam* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="7a9a9-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="7a9a9-110">`number` parametre değerinin bir katına yuvarlanması gereken sayı.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="7a9a9-111">`round rule`: *Numaralandırma değeri*</span><span class="sxs-lookup"><span data-stu-id="7a9a9-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="7a9a9-112">Yuvarlama kuralını tanımlayan **RoundOffType** sabit listesinin numaralandırma değeri.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="7a9a9-113">Bu numaralandırma aşağıdaki değerleri sağlar:</span><span class="sxs-lookup"><span data-stu-id="7a9a9-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="7a9a9-114">Normal (normal)</span><span class="sxs-lookup"><span data-stu-id="7a9a9-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="7a9a9-115">Aşağı (AŞAĞIYUVARLA)</span><span class="sxs-lookup"><span data-stu-id="7a9a9-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="7a9a9-116">Yukarı yuvarlama (YukarıYuvarla)</span><span class="sxs-lookup"><span data-stu-id="7a9a9-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="7a9a9-117">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7a9a9-117">Return values</span></span>

<span data-ttu-id="7a9a9-118">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="7a9a9-118">*Real*</span></span>

<span data-ttu-id="7a9a9-119">Sonuçta elde edilen sayısal değer `decimals` parametrenin belirttiği değerin bir katları olur ve `number` parametre tarafından belirtilen değere en yakın değerdir.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7a9a9-120">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="7a9a9-120">Usage notes</span></span>

<span data-ttu-id="7a9a9-121">`number` parametre sıfır olduğunda bu işlev her zaman sıfır döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="7a9a9-122">`decimals` parametre sıfır olduğunda, bu işlev varsayılan yuvarlama değerine yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="7a9a9-123">`round rule` parametre, **RoundOffType.Ordinary** olarak ayarlandığında, varsayılan yuvarlama değeri **0,01**'dir.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="7a9a9-124">Aksi durumda, varsayılan yuvarlama değeri **1,0**'dir.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="7a9a9-125">`round rule` parametre, **RoundOffType.Ordinary** olarak ayarlandığında bu işlev normal olarak en yakın yuvarlama miktarına yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="7a9a9-126">`round rule` parametre, **RoundOffType.RoundDown** olarak ayarlandığında bu işlev sıfıra en yakın yuvarlama miktarına yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="7a9a9-127">`round rule` parametre, **RoundOffType.RoundUp** olarak ayarlandığında bu işlev sıfırdan en uzak en yakın yuvarlama miktarına yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="7a9a9-128">`round rule` parametresi **RoundOffType.Ordinary** olarak ayarlandığında, bu işlev [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel işlevi ve [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ işlevi gibi davranır.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a9a9-129">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="7a9a9-129">Remarks</span></span>

<span data-ttu-id="7a9a9-130">Sayısal değeri belirtilen sayıda ondalık basamağa yuvarlamak için [ROUND](er-functions-mathematical-round.md) işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="7a9a9-131">Örnek</span><span class="sxs-lookup"><span data-stu-id="7a9a9-131">Example</span></span>

<span data-ttu-id="7a9a9-132">**model.RoundOff** parametresi **RoundOffType.Ordinary** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="7a9a9-133">**model.RoundOff** parametresi **RoundOffType.RoundDown** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="7a9a9-134">**model.RoundOff** parametresi **RoundOffType.RoundUp** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4 döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a9a9-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a9a9-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7a9a9-135">Additional resources</span></span>

[<span data-ttu-id="7a9a9-136">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="7a9a9-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="7a9a9-137">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="7a9a9-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]