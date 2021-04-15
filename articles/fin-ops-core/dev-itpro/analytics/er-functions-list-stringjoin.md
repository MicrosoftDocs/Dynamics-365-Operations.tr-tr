---
title: STRINGJOIN ER işlevi
description: Bu konu, STRINGJOIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745533"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="08779-103">STRINGJOIN ER işlevi</span><span class="sxs-lookup"><span data-stu-id="08779-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08779-104">`STRINGJOIN` işlevi, belirtilen listedeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="08779-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="08779-105">Değerler belirtilen sınırlayıcı ile ayrılır.</span><span class="sxs-lookup"><span data-stu-id="08779-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="08779-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="08779-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="08779-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="08779-107">Arguments</span></span>

<span data-ttu-id="08779-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="08779-108">`list`: *Record list*</span></span>

<span data-ttu-id="08779-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="08779-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="08779-110">`field`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="08779-110">`field`: *Field*</span></span>

<span data-ttu-id="08779-111">*Dize* veri alanının geçerli yolu belirtilen listeyi yazın.</span><span class="sxs-lookup"><span data-stu-id="08779-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="08779-112">`delimiter`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="08779-112">`delimiter`: *String*</span></span>

<span data-ttu-id="08779-113">Alt dizeleri ayırmak için kullanılan sınırlayıcı.</span><span class="sxs-lookup"><span data-stu-id="08779-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="08779-114">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="08779-114">Return values</span></span>

<span data-ttu-id="08779-115">*Dize*</span><span class="sxs-lookup"><span data-stu-id="08779-115">*String*</span></span>

<span data-ttu-id="08779-116">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="08779-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="08779-117">Örnek</span><span class="sxs-lookup"><span data-stu-id="08779-117">Example</span></span>

<span data-ttu-id="08779-118">`SPLIT("abc" , 1)` veri kaynağı **DS** olarak girerseniz, ifade `STRINGJOIN (DS, DS.Value, "-")` **a-b-c** döndürür.</span><span class="sxs-lookup"><span data-stu-id="08779-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08779-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="08779-119">Additional resources</span></span>

[<span data-ttu-id="08779-120">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="08779-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]