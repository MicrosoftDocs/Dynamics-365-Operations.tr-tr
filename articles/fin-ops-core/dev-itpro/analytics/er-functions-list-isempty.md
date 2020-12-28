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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dbba375104b57f9fb09ed4e330d85181ec0dff8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684895"
---
# <a name="isempty-er-function"></a><span data-ttu-id="de213-103">ISEMPTY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="de213-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de213-104">Belirtilen listede kayıt yoksa `ISEMPTY` işlevi bir **DOĞRU** *Boolean* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="de213-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="de213-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="de213-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="de213-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="de213-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="de213-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="de213-107">Arguments</span></span>

<span data-ttu-id="de213-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="de213-108">`list`: *Record list*</span></span>

<span data-ttu-id="de213-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="de213-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="de213-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="de213-110">Return values</span></span>

<span data-ttu-id="de213-111">*Boole*</span><span class="sxs-lookup"><span data-stu-id="de213-111">*Boolean*</span></span>

<span data-ttu-id="de213-112">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="de213-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="de213-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="de213-113">Example 1</span></span>

<span data-ttu-id="de213-114">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `ISEMPTY(DS)` ifadesi **yanlış** döndürür.</span><span class="sxs-lookup"><span data-stu-id="de213-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="de213-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="de213-115">Example 2</span></span>

<span data-ttu-id="de213-116">`ISEMPTY (SPLIT ("",1))` ifadesi **DOĞRU** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="de213-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de213-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="de213-117">Additional resources</span></span>

[<span data-ttu-id="de213-118">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="de213-118">List functions</span></span>](er-functions-category-list.md)
