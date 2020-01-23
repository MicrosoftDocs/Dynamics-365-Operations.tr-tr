---
title: ISOCREDREF ER işlevi
description: Bu konu, ISOCREDREF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916971"
---
# <span data-ttu-id="e24c5-103"><a name="ISOCREDREF">ISOCREDREF ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="e24c5-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e24c5-104">`ISOCREDREF` işlevi, bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e24c5-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24c5-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e24c5-105">Syntax</span></span>

```
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="e24c5-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e24c5-106">Arguments</span></span>

<span data-ttu-id="e24c5-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="e24c5-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="e24c5-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="e24c5-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="e24c5-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e24c5-109">Return values</span></span>

<span data-ttu-id="e24c5-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e24c5-110">*String*</span></span>

<span data-ttu-id="e24c5-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="e24c5-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e24c5-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="e24c5-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="e24c5-113">ISO uyumlu olmayan alfabelerden sembolleri elemek için, `invoice number digits` bağımsız değişkeni işleve gönderilmeden önce çevrilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e24c5-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="e24c5-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="e24c5-114">Example</span></span>

<span data-ttu-id="e24c5-115">`ISOCredRef ("VEND-200002")`, **"RF23VEND-200002"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="e24c5-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e24c5-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e24c5-116">Additional resources</span></span>

[<span data-ttu-id="e24c5-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="e24c5-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
