---
title: ISVALIDCHARACTERISO7064 ER işlevi
description: Bu konu, ISVALIDCHARACTERISO7064 Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041412"
---
# <span data-ttu-id="d9af3-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="d9af3-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9af3-104">`ISVALIDCHARACTERISO7064` işlevi, belirtilen dize, geçerli bir uluslararası banka hesap numarasını (IBAN) temsil ediyorsa, **DOĞRU** *boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9af3-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="d9af3-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9af3-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9af3-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d9af3-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="d9af3-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d9af3-107">Arguments</span></span>

<span data-ttu-id="d9af3-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="d9af3-108">`text`: *String*</span></span>

<span data-ttu-id="d9af3-109">Bir IBAN'ı temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="d9af3-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="d9af3-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d9af3-110">Return values</span></span>

<span data-ttu-id="d9af3-111">*Dize*</span><span class="sxs-lookup"><span data-stu-id="d9af3-111">*String*</span></span>

<span data-ttu-id="d9af3-112">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="d9af3-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d9af3-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="d9af3-113">Example</span></span>

<span data-ttu-id="d9af3-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9af3-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="d9af3-115">`ISVALIDCHARACTERISO7064 ("AT61")`, **YANLIŞ** döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9af3-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9af3-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d9af3-116">Additional resources</span></span>

[<span data-ttu-id="d9af3-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="d9af3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
