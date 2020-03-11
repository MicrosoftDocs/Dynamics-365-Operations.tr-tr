---
title: SESSIONTODAY ER işlevi
description: Bu konu, SESSIONTODAY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042286"
---
# <span data-ttu-id="e142c-103"><a name="SESSIONTODAY">SESSIONTODAY ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="e142c-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e142c-104">`SESSIONTODAY` işlev, geçerli uygulama oturumu tarih temsil eden bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e142c-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e142c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e142c-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e142c-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e142c-106">Return values</span></span>

<span data-ttu-id="e142c-107">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="e142c-107">*Date*</span></span>

<span data-ttu-id="e142c-108">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="e142c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e142c-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="e142c-109">Example</span></span>

<span data-ttu-id="e142c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarihini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="e142c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e142c-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e142c-111">Additional resources</span></span>

[<span data-ttu-id="e142c-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="e142c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
