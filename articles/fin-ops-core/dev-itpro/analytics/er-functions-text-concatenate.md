---
title: CONCATENATE ER işlevi
description: Bu konu, CONCATENATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 1a21140e5636ebd96eca4be90308c915e77510e1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743915"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="41451-103">CONCATENATE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="41451-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41451-104">Bu `CONCATENATE` işlev, bir dizeye katıldıktan sonra, belirtilen tüm metin dizelerini bir *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="41451-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="41451-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="41451-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="41451-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="41451-106">Arguments</span></span>

<span data-ttu-id="41451-107">`text 1`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="41451-107">`text 1`: *String*</span></span>

<span data-ttu-id="41451-108">*Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="41451-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="41451-109">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="41451-109">This argument is required.</span></span>

<span data-ttu-id="41451-110">`text N`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="41451-110">`text N`: *String*</span></span>

<span data-ttu-id="41451-111">*Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="41451-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="41451-112">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="41451-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="41451-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="41451-113">Return values</span></span>

<span data-ttu-id="41451-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="41451-114">*String*</span></span>

<span data-ttu-id="41451-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="41451-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="41451-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="41451-116">Example</span></span>

<span data-ttu-id="41451-117">`CONCATENATE ("abc", "def")`, **"abcdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="41451-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="41451-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="41451-118">Usage notes</span></span>

<span data-ttu-id="41451-119">`"abc" & "def"` ifadesi ayrıca **"abcdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="41451-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41451-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="41451-120">Additional resources</span></span>

[<span data-ttu-id="41451-121">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="41451-121">Text functions</span></span>](er-functions-category-text.md)
