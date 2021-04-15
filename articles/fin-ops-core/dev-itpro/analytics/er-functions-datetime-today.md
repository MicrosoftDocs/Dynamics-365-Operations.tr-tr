---
title: TODAY ER işlevi
description: Bu konu, TODAY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746759"
---
# <a name="today-er-function"></a><span data-ttu-id="c778f-103">TODAY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="c778f-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c778f-104">`TODAY` işlev, geçerli uygulama sunucusu tarih temsil eden bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="c778f-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="c778f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="c778f-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="c778f-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="c778f-106">Return values</span></span>

<span data-ttu-id="c778f-107">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="c778f-107">*Date*</span></span>

<span data-ttu-id="c778f-108">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="c778f-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="c778f-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="c778f-109">Example</span></span>

<span data-ttu-id="c778f-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="c778f-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c778f-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c778f-111">Additional resources</span></span>

[<span data-ttu-id="c778f-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="c778f-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]