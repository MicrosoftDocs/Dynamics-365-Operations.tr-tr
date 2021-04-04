---
title: ADDDAYS ER işlevi
description: Bu konu, ADDDAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 85ad6508c0d16796efbf1ad81e25d74365de8f30
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570784"
---
# <a name="adddays-er-function"></a><span data-ttu-id="bfb01-103">ADDDAYS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="bfb01-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfb01-104">`ADDDAYS` işlev, belirtilen başlangıç tarihinden önceki veya sonraki gün sayısı olan bir *tarih saat* değeri hesaplar.</span><span class="sxs-lookup"><span data-stu-id="bfb01-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb01-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="bfb01-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="bfb01-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="bfb01-106">Arguments</span></span>

<span data-ttu-id="bfb01-107">`datetime`: *TarihSaat*</span><span class="sxs-lookup"><span data-stu-id="bfb01-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="bfb01-108">Başlangıç tarihini gösteren bir tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="bfb01-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="bfb01-109">`days`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="bfb01-109">`days`: *Integer*</span></span>

<span data-ttu-id="bfb01-110">`datetime` öncesinde veya sonrasında gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="bfb01-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="bfb01-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="bfb01-111">Return values</span></span>

<span data-ttu-id="bfb01-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="bfb01-112">*DateTime*</span></span>

<span data-ttu-id="bfb01-113">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="bfb01-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bfb01-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="bfb01-114">Usage notes</span></span>

<span data-ttu-id="bfb01-115">Gelecekteki bir tarihi veren pozitif bir `days` değer.</span><span class="sxs-lookup"><span data-stu-id="bfb01-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="bfb01-116">Negatif değer, geçmiş bir tarih verir.</span><span class="sxs-lookup"><span data-stu-id="bfb01-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="bfb01-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bfb01-117">Example 1</span></span>

<span data-ttu-id="bfb01-118">`ADDDAYS (NOW(), 7)` bugünden yedi gün sonraki tarih ve saati döndürür.</span><span class="sxs-lookup"><span data-stu-id="bfb01-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="bfb01-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bfb01-119">Example 2</span></span>

<span data-ttu-id="bfb01-120">`ADDDAYS (NOW(), -3)` bugünden üç gün önceki tarih ve saati döndürür.</span><span class="sxs-lookup"><span data-stu-id="bfb01-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfb01-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bfb01-121">Additional resources</span></span>

[<span data-ttu-id="bfb01-122">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="bfb01-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]