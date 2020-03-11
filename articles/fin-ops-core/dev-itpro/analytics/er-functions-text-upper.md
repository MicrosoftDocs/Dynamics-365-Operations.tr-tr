---
title: UPPER ER işlevi
description: Bu konu, UPPER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 77854d645ba5b65a2819437af510fcd67be6d99d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040952"
---
# <span data-ttu-id="71691-103"><a name="UPPER">UPPER ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="71691-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71691-104">Bu `UPPER` işlev, büyük harflere dönüştürüldükten sonra bir *dize* değeri olarak belirtilen metin dizesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="71691-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="71691-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="71691-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="71691-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="71691-106">Arguments</span></span>

<span data-ttu-id="71691-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="71691-107">`text`: *String*</span></span>

<span data-ttu-id="71691-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="71691-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="71691-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="71691-109">Return values</span></span>

<span data-ttu-id="71691-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="71691-110">*String*</span></span>

<span data-ttu-id="71691-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="71691-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="71691-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="71691-112">Example</span></span>

<span data-ttu-id="71691-113">`UPPER ("Sample")`, **"ÖRNEK"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="71691-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71691-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="71691-114">Additional resources</span></span>

[<span data-ttu-id="71691-115">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="71691-115">Text functions</span></span>](er-functions-category-text.md)
