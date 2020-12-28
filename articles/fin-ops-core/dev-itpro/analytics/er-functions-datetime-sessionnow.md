---
title: SESSIONNOW ER işlevi
description: Bu konu, SESSIONNOW Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d70acb06194a28af0cc85eea440e9e4e937bc3bb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683855"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="ee74f-103">SESSIONNOW ER işlevi</span><span class="sxs-lookup"><span data-stu-id="ee74f-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee74f-104">`SESSIONNOW` işlevi, geçerli uygulama oturumu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee74f-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee74f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ee74f-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="ee74f-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ee74f-106">Return values</span></span>

<span data-ttu-id="ee74f-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="ee74f-107">*DateTime*</span></span>

<span data-ttu-id="ee74f-108">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="ee74f-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="ee74f-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="ee74f-109">Example</span></span>

<span data-ttu-id="ee74f-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarih/saat değerini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee74f-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee74f-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ee74f-111">Additional resources</span></span>

[<span data-ttu-id="ee74f-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="ee74f-112">Date and time functions</span></span>](er-functions-category-datetime.md)
