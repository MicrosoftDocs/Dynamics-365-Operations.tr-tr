---
title: STRINGJOIN ER işlevi
description: Bu konu, STRINGJOIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917201"
---
# <span data-ttu-id="7da45-103"><a name="STRINGJOIN">STRINGJOIN ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="7da45-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7da45-104">`STRINGJOIN` işlevi, belirtilen listedeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7da45-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="7da45-105">Değerler belirtilen sınırlayıcı ile ayrılır.</span><span class="sxs-lookup"><span data-stu-id="7da45-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da45-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7da45-106">Syntax</span></span>

```
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="7da45-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7da45-107">Arguments</span></span>

<span data-ttu-id="7da45-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7da45-108">`list`: *Record list*</span></span>

<span data-ttu-id="7da45-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7da45-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7da45-110">`field`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="7da45-110">`field`: *Field*</span></span>

<span data-ttu-id="7da45-111">*Dize* veri alanının geçerli yolu belirtilen listeyi yazın.</span><span class="sxs-lookup"><span data-stu-id="7da45-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="7da45-112">`delimiter`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="7da45-112">`delimiter`: *String*</span></span>

<span data-ttu-id="7da45-113">Alt dizeleri ayırmak için kullanılan sınırlayıcı.</span><span class="sxs-lookup"><span data-stu-id="7da45-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="7da45-114">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7da45-114">Return values</span></span>

<span data-ttu-id="7da45-115">*Dize*</span><span class="sxs-lookup"><span data-stu-id="7da45-115">*String*</span></span>

<span data-ttu-id="7da45-116">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="7da45-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7da45-117">Örnek</span><span class="sxs-lookup"><span data-stu-id="7da45-117">Example</span></span>

<span data-ttu-id="7da45-118">`SPLIT("abc" , 1)` veri kaynağı **DS** olarak girerseniz, ifade `STRINGJOIN (DS, DS.Value, "-")` **a-b-c** döndürür.</span><span class="sxs-lookup"><span data-stu-id="7da45-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7da45-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7da45-119">Additional resources</span></span>

[<span data-ttu-id="7da45-120">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="7da45-120">List functions</span></span>](er-functions-category-list.md)
