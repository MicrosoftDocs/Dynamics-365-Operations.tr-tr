---
title: LEFT ER işlevi
description: Bu konu, LEFT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570004"
---
# <a name="left-er-function"></a><span data-ttu-id="d2cff-103">LEFT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="d2cff-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2cff-104">Bu `LEFT` işlev belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d2cff-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cff-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d2cff-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="d2cff-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d2cff-106">Arguments</span></span>

<span data-ttu-id="d2cff-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="d2cff-107">`text`: *String*</span></span>

<span data-ttu-id="d2cff-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="d2cff-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="d2cff-109">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="d2cff-109">`number`: *Integer*</span></span>

<span data-ttu-id="d2cff-110">Orijinal metnin başından itibaren döndürülmesi gereken karakter sayısı.</span><span class="sxs-lookup"><span data-stu-id="d2cff-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d2cff-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d2cff-111">Return values</span></span>

<span data-ttu-id="d2cff-112">*Dize*</span><span class="sxs-lookup"><span data-stu-id="d2cff-112">*String*</span></span>

<span data-ttu-id="d2cff-113">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="d2cff-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d2cff-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="d2cff-114">Example</span></span>

<span data-ttu-id="d2cff-115">`LEFT ("Sample", 3)`, **"Sam"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="d2cff-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2cff-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d2cff-116">Additional resources</span></span>

[<span data-ttu-id="d2cff-117">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="d2cff-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]