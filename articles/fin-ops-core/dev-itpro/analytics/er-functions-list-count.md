---
title: COUNT ER işlevi
description: Bu konu, COUNT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687732"
---
# <a name="count-er-function"></a><span data-ttu-id="d1c42-103">COUNT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="d1c42-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1c42-104">Bu `COUNT` işlev, liste boş değilse, belirtilen listedeki kayıt sayısını gösteren bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="d1c42-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="d1c42-105">Liste boşsa, bu işlev **0** (sıfır) döndürür.</span><span class="sxs-lookup"><span data-stu-id="d1c42-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c42-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d1c42-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="d1c42-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d1c42-107">Arguments</span></span>

<span data-ttu-id="d1c42-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="d1c42-108">`list`: *Record list*</span></span>

<span data-ttu-id="d1c42-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="d1c42-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d1c42-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d1c42-110">Return values</span></span>

<span data-ttu-id="d1c42-111">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="d1c42-111">*Integer*</span></span>

<span data-ttu-id="d1c42-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="d1c42-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d1c42-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="d1c42-113">Example</span></span>

<span data-ttu-id="d1c42-114">`COUNT (SPLIT("abcd" , 3))`, **2** döndürür, çünkü bu örnekte kullanılan `SPLIT` işlev iki kayıttan oluşan bir liste oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1c42-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1c42-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d1c42-115">Additional resources</span></span>

[<span data-ttu-id="d1c42-116">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="d1c42-116">List functions</span></span>](er-functions-category-list.md)
