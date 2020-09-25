---
title: INDEX ER işlevi
description: Bu konu, INDEX Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745196"
---
# <a name="index-er-function"></a><span data-ttu-id="914da-103">INDEX ER işlevi</span><span class="sxs-lookup"><span data-stu-id="914da-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="914da-104">Bu `INDEX` işlev, belirtilen listede belirtilen sayısal dizin kullanılarak seçilen bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="914da-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="914da-105">Dizin listedeki kayıtların aralığı dışında ise bir özel durum oluşur.</span><span class="sxs-lookup"><span data-stu-id="914da-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="914da-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="914da-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="914da-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="914da-107">Arguments</span></span>

<span data-ttu-id="914da-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="914da-108">`list`: *Record list*</span></span>

<span data-ttu-id="914da-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="914da-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="914da-110">`index`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="914da-110">`index`: *Integer*</span></span>

<span data-ttu-id="914da-111">İstenen kaydın belirtilen listedeki konumunu gösteren sayısal dizin.</span><span class="sxs-lookup"><span data-stu-id="914da-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="914da-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="914da-112">Return values</span></span>

<span data-ttu-id="914da-113">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="914da-113">*Container (record)*</span></span>

<span data-ttu-id="914da-114">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="914da-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="914da-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="914da-115">Example 1</span></span>

<span data-ttu-id="914da-116">*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `DS.Value` ifadesi, bu kayıt listesinin ikinci kaydı için **B** döndürür.</span><span class="sxs-lookup"><span data-stu-id="914da-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="914da-117">Bu ifade `INDEX (SPLIT ("A|B|C", "|"), 2).Value` **"B"** metin değerini de döndürür.</span><span class="sxs-lookup"><span data-stu-id="914da-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="914da-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="914da-118">Example 2</span></span>

<span data-ttu-id="914da-119">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'yi girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `INDEX (SPLIT ("A|B|C", "|"), 4).Value` ifadesi istisna oluşturur.</span><span class="sxs-lookup"><span data-stu-id="914da-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="914da-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="914da-120">Additional resources</span></span>

[<span data-ttu-id="914da-121">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="914da-121">List functions</span></span>](er-functions-category-list.md)
