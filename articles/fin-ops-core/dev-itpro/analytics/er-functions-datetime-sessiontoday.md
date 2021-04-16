---
title: SESSIONTODAY ER işlevi
description: Bu konu, SESSIONTODAY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746786"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="e3e2c-103">SESSIONTODAY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e3e2c-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3e2c-104">`SESSIONTODAY` işlev, geçerli uygulama oturumu tarih temsil eden bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3e2c-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e2c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e3e2c-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e3e2c-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e3e2c-106">Return values</span></span>

<span data-ttu-id="e3e2c-107">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="e3e2c-107">*Date*</span></span>

<span data-ttu-id="e3e2c-108">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="e3e2c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e3e2c-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="e3e2c-109">Example</span></span>

<span data-ttu-id="e3e2c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarihini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3e2c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3e2c-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e3e2c-111">Additional resources</span></span>

[<span data-ttu-id="e3e2c-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="e3e2c-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]