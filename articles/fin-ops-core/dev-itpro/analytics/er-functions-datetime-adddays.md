---
title: ADDDAYS ER işlevi
description: Bu konu, ADDDAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743387"
---
# <a name="adddays-er-function"></a><span data-ttu-id="3058d-103">ADDDAYS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="3058d-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3058d-104">`ADDDAYS` işlev, belirtilen başlangıç tarihinden önceki veya sonraki gün sayısı olan bir *tarih saat* değeri hesaplar.</span><span class="sxs-lookup"><span data-stu-id="3058d-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3058d-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3058d-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="3058d-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="3058d-106">Arguments</span></span>

<span data-ttu-id="3058d-107">`datetime`: *TarihSaat*</span><span class="sxs-lookup"><span data-stu-id="3058d-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="3058d-108">Başlangıç tarihini gösteren bir tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="3058d-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="3058d-109">`days`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="3058d-109">`days`: *Integer*</span></span>

<span data-ttu-id="3058d-110">`datetime` öncesinde veya sonrasında gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="3058d-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="3058d-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="3058d-111">Return values</span></span>

<span data-ttu-id="3058d-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="3058d-112">*DateTime*</span></span>

<span data-ttu-id="3058d-113">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="3058d-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3058d-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="3058d-114">Usage notes</span></span>

<span data-ttu-id="3058d-115">Gelecekteki bir tarihi veren pozitif bir `days` değer.</span><span class="sxs-lookup"><span data-stu-id="3058d-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="3058d-116">Negatif değer, geçmiş bir tarih verir.</span><span class="sxs-lookup"><span data-stu-id="3058d-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="3058d-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3058d-117">Example 1</span></span>

<span data-ttu-id="3058d-118">`ADDDAYS (NOW(), 7)` bugünden yedi gün sonraki tarih ve saati döndürür.</span><span class="sxs-lookup"><span data-stu-id="3058d-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="3058d-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3058d-119">Example 2</span></span>

<span data-ttu-id="3058d-120">`ADDDAYS (NOW(), -3)` bugünden üç gün önceki tarih ve saati döndürür.</span><span class="sxs-lookup"><span data-stu-id="3058d-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3058d-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3058d-121">Additional resources</span></span>

[<span data-ttu-id="3058d-122">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="3058d-122">Date and time functions</span></span>](er-functions-category-datetime.md)
