---
title: CONCATENATE ER işlevi
description: Bu konu, CONCATENATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569617"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="38d4c-103">CONCATENATE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="38d4c-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38d4c-104">Bu `CONCATENATE` işlev, bir dizeye katıldıktan sonra, belirtilen tüm metin dizelerini bir *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="38d4c-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d4c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="38d4c-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="38d4c-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="38d4c-106">Arguments</span></span>

<span data-ttu-id="38d4c-107">`text 1`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="38d4c-107">`text 1`: *String*</span></span>

<span data-ttu-id="38d4c-108">*Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="38d4c-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="38d4c-109">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="38d4c-109">This argument is required.</span></span>

<span data-ttu-id="38d4c-110">`text N`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="38d4c-110">`text N`: *String*</span></span>

<span data-ttu-id="38d4c-111">*Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="38d4c-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="38d4c-112">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="38d4c-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="38d4c-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="38d4c-113">Return values</span></span>

<span data-ttu-id="38d4c-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="38d4c-114">*String*</span></span>

<span data-ttu-id="38d4c-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="38d4c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="38d4c-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="38d4c-116">Example</span></span>

<span data-ttu-id="38d4c-117">`CONCATENATE ("abc", "def")`, **"abcdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="38d4c-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="38d4c-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="38d4c-118">Usage notes</span></span>

<span data-ttu-id="38d4c-119">`"abc" & "def"` ifadesi ayrıca **"abcdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="38d4c-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38d4c-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="38d4c-120">Additional resources</span></span>

[<span data-ttu-id="38d4c-121">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="38d4c-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]