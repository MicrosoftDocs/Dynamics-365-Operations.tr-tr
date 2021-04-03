---
title: COUNT ER işlevi
description: Bu konu, COUNT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567904"
---
# <a name="count-er-function"></a><span data-ttu-id="90fbe-103">COUNT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="90fbe-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90fbe-104">Bu `COUNT` işlev, liste boş değilse, belirtilen listedeki kayıt sayısını gösteren bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="90fbe-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="90fbe-105">Liste boşsa, bu işlev **0** (sıfır) döndürür.</span><span class="sxs-lookup"><span data-stu-id="90fbe-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="90fbe-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="90fbe-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="90fbe-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="90fbe-107">Arguments</span></span>

<span data-ttu-id="90fbe-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="90fbe-108">`list`: *Record list*</span></span>

<span data-ttu-id="90fbe-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="90fbe-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="90fbe-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="90fbe-110">Return values</span></span>

<span data-ttu-id="90fbe-111">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="90fbe-111">*Integer*</span></span>

<span data-ttu-id="90fbe-112">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="90fbe-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="90fbe-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="90fbe-113">Example</span></span>

<span data-ttu-id="90fbe-114">`COUNT (SPLIT("abcd" , 3))`, **2** döndürür, çünkü bu örnekte kullanılan `SPLIT` işlev iki kayıttan oluşan bir liste oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90fbe-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90fbe-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="90fbe-115">Additional resources</span></span>

[<span data-ttu-id="90fbe-116">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="90fbe-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]