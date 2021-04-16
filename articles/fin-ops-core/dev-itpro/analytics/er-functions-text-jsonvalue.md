---
title: JSONVALUE ER işlevi
description: Bu konu, JSONVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746375"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="ad8e4-103">JSONVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="ad8e4-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad8e4-104">`JSONVALUE` işlevi, verileri, belirtilen koda göre skaler bir değer çıkarmak için belirtilen yolla erişilen JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırın.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="ad8e4-105">Sonra da bir *dize* değeri olarak ayıklanan skalar değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad8e4-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ad8e4-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="ad8e4-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="ad8e4-107">Arguments</span></span>

<span data-ttu-id="ad8e4-108">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-108">`input`: *String*</span></span>

<span data-ttu-id="ad8e4-109">JSON verileri içeren *Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="ad8e4-110">`path`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-110">`path`: *String*</span></span>

<span data-ttu-id="ad8e4-111">JSON verileri sklar değeri tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="ad8e4-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ad8e4-112">Return values</span></span>

<span data-ttu-id="ad8e4-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-113">*String*</span></span>

<span data-ttu-id="ad8e4-114">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ad8e4-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="ad8e4-115">Example</span></span>

<span data-ttu-id="ad8e4-116">**JsonField** veri kaynağı, aşağıdaki veriyi JSON biçiminde içerir: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="ad8e4-117">Bu durumda `JSONVALUE (JsonField, "BuildNumber")` ifadesi, *dize* veri türünün şu değerini döndürür: **"7.3.1234.1".**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad8e4-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ad8e4-118">Additional resources</span></span>

[<span data-ttu-id="ad8e4-119">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="ad8e4-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]