---
title: INDEX ER işlevi
description: Bu konu, INDEX Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087763"
---
# <a name="index-er-function"></a><span data-ttu-id="19f4e-103">INDEX ER işlevi</span><span class="sxs-lookup"><span data-stu-id="19f4e-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19f4e-104">Bu `INDEX` işlev, belirtilen listede belirtilen sayısal dizin kullanılarak seçilen bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="19f4e-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="19f4e-105">Dizin listedeki kayıtların aralığı dışında ise bir özel durum oluşur.</span><span class="sxs-lookup"><span data-stu-id="19f4e-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f4e-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="19f4e-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="19f4e-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="19f4e-107">Arguments</span></span>

<span data-ttu-id="19f4e-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="19f4e-108">`list`: *Record list*</span></span>

<span data-ttu-id="19f4e-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="19f4e-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="19f4e-110">`index`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="19f4e-110">`index`: *Integer*</span></span>

<span data-ttu-id="19f4e-111">İstenen kaydın belirtilen listedeki konumunu gösteren sayısal dizin.</span><span class="sxs-lookup"><span data-stu-id="19f4e-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="19f4e-112">Bu işlev için tek tabanlı numaralandırma kullanıldığından, belirtilen listenin ilk kaydını döndürmek için **1** değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="19f4e-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="19f4e-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="19f4e-113">Return values</span></span>

<span data-ttu-id="19f4e-114">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="19f4e-114">*Container (record)*</span></span>

<span data-ttu-id="19f4e-115">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="19f4e-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="19f4e-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19f4e-116">Example 1</span></span>

<span data-ttu-id="19f4e-117">*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `DS.Value` ifadesi, bu kayıt listesinin ikinci kaydı için **B** döndürür.</span><span class="sxs-lookup"><span data-stu-id="19f4e-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="19f4e-118">Bu ifade `INDEX (SPLIT ("A|B|C", "|"), 2).Value` **"B"** metin değerini de döndürür.</span><span class="sxs-lookup"><span data-stu-id="19f4e-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="19f4e-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="19f4e-119">Example 2</span></span>

<span data-ttu-id="19f4e-120">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'yi girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `INDEX (SPLIT ("A|B|C", "|"), 4).Value` ifadesi istisna oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19f4e-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19f4e-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="19f4e-121">Additional resources</span></span>

[<span data-ttu-id="19f4e-122">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="19f4e-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
