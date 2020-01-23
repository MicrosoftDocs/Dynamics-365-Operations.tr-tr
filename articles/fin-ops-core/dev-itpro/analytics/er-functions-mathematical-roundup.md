---
title: ROUNDUP ER işlevi
description: Bu konu, ROUNDUP Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917063"
---
# <span data-ttu-id="98972-103"><a name="ROUNDUP">ROUNDUP ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="98972-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98972-104">`ROUNDUP` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yukarı yuvarladıktan sonra *Gerçek* değer olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="98972-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="98972-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="98972-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="98972-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="98972-106">Arguments</span></span>

<span data-ttu-id="98972-107">`number`: *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="98972-107">`number`: *Real*</span></span>

<span data-ttu-id="98972-108">Yukarı yuvarlama gereken sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="98972-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="98972-109">`decimals`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="98972-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="98972-110">Ondalık basamak sayısını temsil eden sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="98972-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="98972-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="98972-111">Return values</span></span>

<span data-ttu-id="98972-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="98972-112">*Real*</span></span>

<span data-ttu-id="98972-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="98972-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98972-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="98972-114">Usage notes</span></span>

<span data-ttu-id="98972-115">Bu işlev [YUVARLA](er-functions-mathematical-round.md) işlevi gibi davranır ancak belirtilen sayıyı daima yukarı doğru (sıfırdan uzağa doğru) yuvarlar.</span><span class="sxs-lookup"><span data-stu-id="98972-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="98972-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98972-116">Example 1</span></span>

<span data-ttu-id="98972-117">`ROUNDUP (1200.763, 2)` iki ondalık basamağa yukarı yuvarlar ve **1200.77** sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="98972-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="98972-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="98972-118">Example 2</span></span>

<span data-ttu-id="98972-119">`ROUNDUP (1200.767, -3)`, 1.000'in en yakın katına yukarı yuvarlar ve **2000** döndürür.</span><span class="sxs-lookup"><span data-stu-id="98972-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98972-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="98972-120">Additional resources</span></span>

[<span data-ttu-id="98972-121">Matematik işlevi</span><span class="sxs-lookup"><span data-stu-id="98972-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
