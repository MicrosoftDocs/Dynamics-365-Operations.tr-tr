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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041389"
---
# <span data-ttu-id="18d0c-103"><a name="ISOCREDREF">ISOCREDREF ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="18d0c-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18d0c-104">`ISOCREDREF` işlevi, bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="18d0c-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d0c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="18d0c-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="18d0c-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="18d0c-106">Arguments</span></span>

<span data-ttu-id="18d0c-107">`invoice number digits`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="18d0c-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="18d0c-108">Fatura numarasının rakamlarını temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="18d0c-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="18d0c-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="18d0c-109">Return values</span></span>

<span data-ttu-id="18d0c-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="18d0c-110">*String*</span></span>

<span data-ttu-id="18d0c-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="18d0c-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="18d0c-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="18d0c-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="18d0c-113">ISO uyumlu olmayan alfabelerden sembolleri elemek için, `invoice number digits` bağımsız değişkeni işleve gönderilmeden önce çevrilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="18d0c-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="18d0c-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="18d0c-114">Example</span></span>

<span data-ttu-id="18d0c-115">`ISOCredRef ("VEND-200002")`, **"RF23VEND-200002"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="18d0c-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18d0c-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="18d0c-116">Additional resources</span></span>

[<span data-ttu-id="18d0c-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="18d0c-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
