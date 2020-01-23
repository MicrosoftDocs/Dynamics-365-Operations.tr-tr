---
title: LISTOFFIRSTITEM ER işlevi
description: Bu konu, LISTOFFIRSTITEM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917270"
---
# <span data-ttu-id="478c1-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="478c1-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="478c1-104">Bu `LISTOFFIRSTITEM` işlevi, belirtilen listenin yalnızca ilk kayıttan oluşan bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="478c1-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="478c1-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="478c1-105">Syntax</span></span>

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="478c1-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="478c1-106">Arguments</span></span>

<span data-ttu-id="478c1-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="478c1-107">`list`: *Record list*</span></span>

<span data-ttu-id="478c1-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="478c1-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="478c1-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="478c1-109">Return values</span></span>

<span data-ttu-id="478c1-110">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="478c1-110">*Record list*</span></span>

<span data-ttu-id="478c1-111">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="478c1-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="478c1-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="478c1-112">Example</span></span>

<span data-ttu-id="478c1-113">Bu ifade `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` **"A"** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="478c1-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="478c1-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="478c1-114">Additional resources</span></span>

[<span data-ttu-id="478c1-115">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="478c1-115">List functions</span></span>](er-functions-category-list.md)
