---
title: MID ER işlevi
description: Bu konu, MID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915614"
---
# <span data-ttu-id="12acb-103"><a name="MID">MID ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="12acb-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12acb-104">Bu `MID` işlev belirtilen pozisyondan başlayarak belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="12acb-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="12acb-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="12acb-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="12acb-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="12acb-106">Arguments</span></span>

<span data-ttu-id="12acb-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="12acb-107">`text`: *String*</span></span>

<span data-ttu-id="12acb-108">Karakterlerin alınacağı metni belirten bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="12acb-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="12acb-109">`starting position`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="12acb-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="12acb-110">Belirtilen metinden ilk karakterin döndürülmesi gereken konumu belirten bir *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="12acb-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="12acb-111">`number of characters`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="12acb-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="12acb-112">Belirtilen pozisyondan başlayarak döndürülmesi gereken karakter sayısını belirten bir *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="12acb-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="12acb-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="12acb-113">Return values</span></span>

<span data-ttu-id="12acb-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="12acb-114">*String*</span></span>

<span data-ttu-id="12acb-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="12acb-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="12acb-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="12acb-116">Usage notes</span></span>

<span data-ttu-id="12acb-117">`starting position` bağımsız değişkenin değeri 0 (sıfır) değerinden küçükse, döndürülen karakterler belirtilen dizedeki ilk konumdan sayılır.</span><span class="sxs-lookup"><span data-stu-id="12acb-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="12acb-118">`starting position` bağımsız değişkenin değeri belirtilen dizenin uzunluğunu aşarsa, boş bir dize döndürülür.</span><span class="sxs-lookup"><span data-stu-id="12acb-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="12acb-119">Örnek</span><span class="sxs-lookup"><span data-stu-id="12acb-119">Example</span></span>

<span data-ttu-id="12acb-120">`MID ("Sample", 2, 3)`, **"amp"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="12acb-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12acb-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="12acb-121">Additional resources</span></span>

[<span data-ttu-id="12acb-122">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="12acb-122">Text functions</span></span>](er-functions-category-text.md)
