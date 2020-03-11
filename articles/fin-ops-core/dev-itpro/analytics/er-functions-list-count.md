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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042217"
---
# <span data-ttu-id="67c9a-103"><a name="COUNT">COUNT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="67c9a-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67c9a-104">Bu `COUNT` işlev, liste boş değilse, belirtilen listedeki kayıt sayısını gösteren bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="67c9a-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="67c9a-105">Liste boşsa, bu işlev **0** (sıfır) döndürür.</span><span class="sxs-lookup"><span data-stu-id="67c9a-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="67c9a-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="67c9a-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="67c9a-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="67c9a-107">Arguments</span></span>

<span data-ttu-id="67c9a-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="67c9a-108">`list`: *Record list*</span></span>

<span data-ttu-id="67c9a-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="67c9a-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="67c9a-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="67c9a-110">Return values</span></span>

<span data-ttu-id="67c9a-111">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="67c9a-111">*Integer*</span></span>

<span data-ttu-id="67c9a-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="67c9a-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="67c9a-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="67c9a-113">Example</span></span>

<span data-ttu-id="67c9a-114">`COUNT (SPLIT("abcd" , 3))`, **2** döndürür, çünkü bu örnekte kullanılan `SPLIT` işlev iki kayıttan oluşan bir liste oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67c9a-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67c9a-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="67c9a-115">Additional resources</span></span>

[<span data-ttu-id="67c9a-116">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="67c9a-116">List functions</span></span>](er-functions-category-list.md)
