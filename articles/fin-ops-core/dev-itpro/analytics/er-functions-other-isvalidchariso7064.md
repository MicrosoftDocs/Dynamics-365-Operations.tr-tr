---
title: ISVALIDCHARACTERISO7064 ER işlevi
description: Bu konu, ISVALIDCHARACTERISO7064 Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 1f102a6a3eafe3b066101370b94fa2f17ad3ad8b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748305"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="90fba-103">ISVALIDCHARACTERISO7064 ER işlevi</span><span class="sxs-lookup"><span data-stu-id="90fba-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90fba-104">`ISVALIDCHARACTERISO7064` işlevi, belirtilen dize, geçerli bir uluslararası banka hesap numarasını (IBAN) temsil ediyorsa, **DOĞRU** *boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="90fba-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="90fba-105">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="90fba-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="90fba-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="90fba-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="90fba-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="90fba-107">Arguments</span></span>

<span data-ttu-id="90fba-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="90fba-108">`text`: *String*</span></span>

<span data-ttu-id="90fba-109">Bir IBAN'ı temsil eden metin değeri.</span><span class="sxs-lookup"><span data-stu-id="90fba-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="90fba-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="90fba-110">Return values</span></span>

<span data-ttu-id="90fba-111">*Dize*</span><span class="sxs-lookup"><span data-stu-id="90fba-111">*String*</span></span>

<span data-ttu-id="90fba-112">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="90fba-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="90fba-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="90fba-113">Example</span></span>

<span data-ttu-id="90fba-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")`, **DOĞRU** döndürür.</span><span class="sxs-lookup"><span data-stu-id="90fba-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="90fba-115">`ISVALIDCHARACTERISO7064 ("AT61")`, **YANLIŞ** döndürür.</span><span class="sxs-lookup"><span data-stu-id="90fba-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90fba-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="90fba-116">Additional resources</span></span>

[<span data-ttu-id="90fba-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="90fba-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]