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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042079"
---
# <span data-ttu-id="26c13-103"><a name="INDEX">INDEX ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="26c13-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26c13-104">Bu `INDEX` işlev, belirtilen listede belirtilen sayısal dizin kullanılarak seçilen bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="26c13-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="26c13-105">Dizin listedeki kayıtların aralığı dışında ise bir özel durum oluşur.</span><span class="sxs-lookup"><span data-stu-id="26c13-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c13-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="26c13-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="26c13-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="26c13-107">Arguments</span></span>

<span data-ttu-id="26c13-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="26c13-108">`list`: *Record list*</span></span>

<span data-ttu-id="26c13-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="26c13-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="26c13-110">`index`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="26c13-110">`index`: *Integer*</span></span>

<span data-ttu-id="26c13-111">İstenen kaydın belirtilen listedeki konumunu gösteren sayısal dizin.</span><span class="sxs-lookup"><span data-stu-id="26c13-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="26c13-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="26c13-112">Return values</span></span>

<span data-ttu-id="26c13-113">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="26c13-113">*Container (record)*</span></span>

<span data-ttu-id="26c13-114">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="26c13-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="26c13-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26c13-115">Example 1</span></span>

<span data-ttu-id="26c13-116">*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `DS.Value` ifadesi, bu kayıt listesinin ikinci kaydı için **B** döndürür.</span><span class="sxs-lookup"><span data-stu-id="26c13-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="26c13-117">Bu ifade `INDEX (SPLIT ("A|B|C", "|"), 2).Value` **"B"** metin değerini de döndürür.</span><span class="sxs-lookup"><span data-stu-id="26c13-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="26c13-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="26c13-118">Example 2</span></span>

<span data-ttu-id="26c13-119">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'yi girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `INDEX (SPLIT ("A|B|C", "|"), 4).Value` ifadesi istisna oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26c13-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26c13-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="26c13-120">Additional resources</span></span>

[<span data-ttu-id="26c13-121">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="26c13-121">List functions</span></span>](er-functions-category-list.md)
