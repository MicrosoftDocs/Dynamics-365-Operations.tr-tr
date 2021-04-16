---
title: ISEMPTY ER işlevi
description: Bu konu, ISEMPTY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750448"
---
# <a name="isempty-er-function"></a><span data-ttu-id="0c73f-103">ISEMPTY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="0c73f-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c73f-104">Belirtilen listede kayıt yoksa `ISEMPTY` işlevi bir **DOĞRU** *Boolean* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c73f-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="0c73f-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c73f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c73f-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0c73f-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="0c73f-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="0c73f-107">Arguments</span></span>

<span data-ttu-id="0c73f-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="0c73f-108">`list`: *Record list*</span></span>

<span data-ttu-id="0c73f-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="0c73f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c73f-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="0c73f-110">Return values</span></span>

<span data-ttu-id="0c73f-111">*Boole*</span><span class="sxs-lookup"><span data-stu-id="0c73f-111">*Boolean*</span></span>

<span data-ttu-id="0c73f-112">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="0c73f-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c73f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c73f-113">Example 1</span></span>

<span data-ttu-id="0c73f-114">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `ISEMPTY(DS)` ifadesi **yanlış** döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c73f-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c73f-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0c73f-115">Example 2</span></span>

<span data-ttu-id="0c73f-116">`ISEMPTY (SPLIT ("",1))` ifadesi **DOĞRU** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c73f-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c73f-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0c73f-117">Additional resources</span></span>

[<span data-ttu-id="0c73f-118">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="0c73f-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]