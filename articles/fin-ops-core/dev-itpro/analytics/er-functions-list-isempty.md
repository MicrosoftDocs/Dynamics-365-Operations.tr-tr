---
title: ISEMPTY ER işlevi
description: Bu konu, ISEMPTY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745141"
---
# <a name="isempty-er-function"></a><span data-ttu-id="d3545-103">ISEMPTY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="d3545-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3545-104">Belirtilen listede kayıt yoksa `ISEMPTY` işlevi bir **DOĞRU** *Boolean* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3545-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="d3545-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3545-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3545-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d3545-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="d3545-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d3545-107">Arguments</span></span>

<span data-ttu-id="d3545-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="d3545-108">`list`: *Record list*</span></span>

<span data-ttu-id="d3545-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="d3545-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3545-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d3545-110">Return values</span></span>

<span data-ttu-id="d3545-111">*Boole*</span><span class="sxs-lookup"><span data-stu-id="d3545-111">*Boolean*</span></span>

<span data-ttu-id="d3545-112">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="d3545-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d3545-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3545-113">Example 1</span></span>

<span data-ttu-id="d3545-114">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `ISEMPTY(DS)` ifadesi **yanlış** döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3545-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d3545-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d3545-115">Example 2</span></span>

<span data-ttu-id="d3545-116">`ISEMPTY (SPLIT ("",1))` ifadesi **DOĞRU** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3545-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3545-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d3545-117">Additional resources</span></span>

[<span data-ttu-id="d3545-118">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="d3545-118">List functions</span></span>](er-functions-category-list.md)
