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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744107"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="bb7b9-103">ISOCREDREF ER işlevi</span><span class="sxs-lookup"><span data-stu-id="bb7b9-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb7b9-104">`ISOCREDREF` işlevi, bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7b9-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="bb7b9-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="bb7b9-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="bb7b9-106">Arguments</span></span>

<span data-ttu-id="bb7b9-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="bb7b9-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="bb7b9-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="bb7b9-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="bb7b9-109">Return values</span></span>

<span data-ttu-id="bb7b9-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="bb7b9-110">*String*</span></span>

<span data-ttu-id="bb7b9-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bb7b9-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="bb7b9-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="bb7b9-113">ISO uyumlu olmayan alfabelerden sembolleri elemek için, `invoice number digits` bağımsız değişkeni işleve gönderilmeden önce çevrilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="bb7b9-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="bb7b9-114">Example</span></span>

<span data-ttu-id="bb7b9-115">`ISOCredRef ("VEND-200002")`, **"RF23VEND-200002"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb7b9-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bb7b9-116">Additional resources</span></span>

[<span data-ttu-id="bb7b9-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="bb7b9-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
