---
title: PADLEFT ER işlevi
description: Bu konu, PADLEFT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040975"
---
# <span data-ttu-id="2ab7c-103"><a name="PADLEFT">PADLEFT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="2ab7c-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ab7c-104">`PADLEFT` işlevi, belirtilen dizenin başlangıcının belirtilen karakterlerle doldurulduğu belirtilen uzunlukta bir *dize* döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ab7c-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab7c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2ab7c-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="2ab7c-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="2ab7c-106">Arguments</span></span>

<span data-ttu-id="2ab7c-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2ab7c-107">`text`: *String*</span></span>

<span data-ttu-id="2ab7c-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="2ab7c-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="2ab7c-109">`length`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="2ab7c-109">`length`: *Integer*</span></span>

<span data-ttu-id="2ab7c-110">Doldurulmuş dizedeki son karakter sayısını temsil eden bir *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="2ab7c-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="2ab7c-111">`padding chars`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2ab7c-111">`padding chars`: *String*</span></span>

<span data-ttu-id="2ab7c-112">Doldurma için kullanılacak karakterler.</span><span class="sxs-lookup"><span data-stu-id="2ab7c-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ab7c-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="2ab7c-113">Return values</span></span>

<span data-ttu-id="2ab7c-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2ab7c-114">*String*</span></span>

<span data-ttu-id="2ab7c-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="2ab7c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2ab7c-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="2ab7c-116">Example</span></span>

<span data-ttu-id="2ab7c-117">`PADLEFT ("1234", 10, "`&nbsp;`")`, **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** metin dizesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ab7c-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ab7c-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2ab7c-118">Additional resources</span></span>

[<span data-ttu-id="2ab7c-119">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="2ab7c-119">Text functions</span></span>](er-functions-category-text.md)
