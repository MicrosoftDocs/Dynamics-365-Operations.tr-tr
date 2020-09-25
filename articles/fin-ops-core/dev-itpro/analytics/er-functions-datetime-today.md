---
title: TODAY ER işlevi
description: Bu konu, TODAY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: e2ee153c1dde99810a78ed15c7505fa705088797
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745453"
---
# <a name="today-er-function"></a><span data-ttu-id="5d75d-103">TODAY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="5d75d-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d75d-104">`TODAY` işlev, geçerli uygulama sunucusu tarih temsil eden bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d75d-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d75d-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="5d75d-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="5d75d-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="5d75d-106">Return values</span></span>

<span data-ttu-id="5d75d-107">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="5d75d-107">*Date*</span></span>

<span data-ttu-id="5d75d-108">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="5d75d-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="5d75d-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="5d75d-109">Example</span></span>

<span data-ttu-id="5d75d-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d75d-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d75d-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5d75d-111">Additional resources</span></span>

[<span data-ttu-id="5d75d-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="5d75d-112">Date and time functions</span></span>](er-functions-category-datetime.md)
