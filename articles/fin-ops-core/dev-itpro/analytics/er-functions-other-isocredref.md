---
title: ISOCREDREF ER işlevi
description: Bu konu, ISOCREDREF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748329"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="fca65-103">ISOCREDREF ER işlevi</span><span class="sxs-lookup"><span data-stu-id="fca65-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fca65-104">`ISOCREDREF` işlevi, bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fca65-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca65-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="fca65-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="fca65-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="fca65-106">Arguments</span></span>

<span data-ttu-id="fca65-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="fca65-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="fca65-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fca65-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="fca65-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="fca65-109">Return values</span></span>

<span data-ttu-id="fca65-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="fca65-110">*String*</span></span>

<span data-ttu-id="fca65-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fca65-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fca65-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="fca65-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="fca65-113">ISO uyumlu olmayan alfabelerden sembolleri elemek için, `invoice number digits` bağımsız değişkeni işleve gönderilmeden önce çevrilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="fca65-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="fca65-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="fca65-114">Example</span></span>

<span data-ttu-id="fca65-115">`ISOCredRef ("VEND-200002")`, **"RF23VEND-200002"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="fca65-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fca65-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fca65-116">Additional resources</span></span>

[<span data-ttu-id="fca65-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="fca65-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]