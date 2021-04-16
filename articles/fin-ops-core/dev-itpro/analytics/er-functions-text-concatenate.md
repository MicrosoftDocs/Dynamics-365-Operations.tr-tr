---
title: CONCATENATE ER işlevi
description: Bu konu, CONCATENATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746495"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="2c753-103">CONCATENATE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="2c753-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c753-104">Bu `CONCATENATE` işlev, bir dizeye katıldıktan sonra, belirtilen tüm metin dizelerini bir *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c753-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c753-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2c753-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="2c753-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="2c753-106">Arguments</span></span>

<span data-ttu-id="2c753-107">`text 1`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2c753-107">`text 1`: *String*</span></span>

<span data-ttu-id="2c753-108">*Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="2c753-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="2c753-109">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2c753-109">This argument is required.</span></span>

<span data-ttu-id="2c753-110">`text N`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2c753-110">`text N`: *String*</span></span>

<span data-ttu-id="2c753-111">*Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="2c753-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="2c753-112">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2c753-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c753-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="2c753-113">Return values</span></span>

<span data-ttu-id="2c753-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2c753-114">*String*</span></span>

<span data-ttu-id="2c753-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="2c753-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2c753-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="2c753-116">Example</span></span>

<span data-ttu-id="2c753-117">`CONCATENATE ("abc", "def")`, **"abcdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c753-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c753-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="2c753-118">Usage notes</span></span>

<span data-ttu-id="2c753-119">`"abc" & "def"` ifadesi ayrıca **"abcdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c753-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c753-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2c753-120">Additional resources</span></span>

[<span data-ttu-id="2c753-121">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="2c753-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]