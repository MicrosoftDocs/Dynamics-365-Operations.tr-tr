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
ms.openlocfilehash: 6f6f3326c9ca5cdcb3cef52f243d6d3da34251ce
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915936"
---
# <span data-ttu-id="0ff42-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="0ff42-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ff42-104">`ISVALIDCHARACTERISO7064` işlevi, belirtilen dize, geçerli bir uluslararası banka hesap numarasını (IBAN) temsil ediyorsa, **DOĞRU** *boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ff42-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="0ff42-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ff42-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff42-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0ff42-106">Syntax</span></span>

```
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="0ff42-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="0ff42-107">Arguments</span></span>

<span data-ttu-id="0ff42-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="0ff42-108">`text`: *String*</span></span>

<span data-ttu-id="0ff42-109">Bir IBAN'ı temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="0ff42-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ff42-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="0ff42-110">Return values</span></span>

<span data-ttu-id="0ff42-111">*Dize*</span><span class="sxs-lookup"><span data-stu-id="0ff42-111">*String*</span></span>

<span data-ttu-id="0ff42-112">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="0ff42-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0ff42-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="0ff42-113">Example</span></span>

<span data-ttu-id="0ff42-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ff42-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="0ff42-115">`ISVALIDCHARACTERISO7064 ("AT61")`, **YANLIŞ** döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ff42-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ff42-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0ff42-116">Additional resources</span></span>

[<span data-ttu-id="0ff42-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="0ff42-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
