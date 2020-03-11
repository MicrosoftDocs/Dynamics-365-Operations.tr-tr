---
title: EMPTYLIST ER işlevi
description: Bu konu, EMPTYLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042194"
---
# <span data-ttu-id="ac2d3-103"><a name="EMPTYLIST">EMPTYLIST ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="ac2d3-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac2d3-104">`EMPTYLIST` işlevi, belirtilmiş olan listeyi, liste yapısı için bir kaynak olarak kullanarak boş bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac2d3-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2d3-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ac2d3-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="ac2d3-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="ac2d3-106">Arguments</span></span>

<span data-ttu-id="ac2d3-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="ac2d3-107">`list`: *Record list*</span></span>

<span data-ttu-id="ac2d3-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="ac2d3-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ac2d3-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ac2d3-109">Return values</span></span>

<span data-ttu-id="ac2d3-110">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="ac2d3-110">*Record list*</span></span>

<span data-ttu-id="ac2d3-111">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="ac2d3-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="ac2d3-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="ac2d3-112">Example</span></span>

<span data-ttu-id="ac2d3-113">`EMPTYLIST (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac2d3-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac2d3-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ac2d3-114">Additional resources</span></span>

[<span data-ttu-id="ac2d3-115">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="ac2d3-115">List functions</span></span>](er-functions-category-list.md)
