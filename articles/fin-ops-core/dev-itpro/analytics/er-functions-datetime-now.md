---
title: NOW ER işlevi
description: Bu konu, NOW Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 8e549634b3856777aff610fa0e61c19bcad71dd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563522"
---
# <a name="now-er-function"></a><span data-ttu-id="52570-103">NOW ER işlevi</span><span class="sxs-lookup"><span data-stu-id="52570-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52570-104">`NOW` işlev, geçerli uygulama sunucusu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="52570-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="52570-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="52570-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="52570-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="52570-106">Return values</span></span>

<span data-ttu-id="52570-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="52570-107">*DateTime*</span></span>

<span data-ttu-id="52570-108">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="52570-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="52570-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="52570-109">Example</span></span>

<span data-ttu-id="52570-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarih/saat değerini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="52570-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52570-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="52570-111">Additional resources</span></span>

[<span data-ttu-id="52570-112">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="52570-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]