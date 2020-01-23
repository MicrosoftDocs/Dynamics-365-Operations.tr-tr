---
title: NOT ER işlevi
description: Bu konu, NOT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916051"
---
# <span data-ttu-id="e5f9b-103"><a name="NOT">NOT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="e5f9b-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5f9b-104">`NOT` işlev, belirtilen koşulun ters çevrilmiş mantıksal değerini bir *Boole* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f9b-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e5f9b-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="e5f9b-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e5f9b-106">Arguments</span></span>

<span data-ttu-id="e5f9b-107">`condition`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="e5f9b-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="e5f9b-108">Ters işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="e5f9b-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e5f9b-109">Return values</span></span>

<span data-ttu-id="e5f9b-110">*Boole*</span><span class="sxs-lookup"><span data-stu-id="e5f9b-110">*Boolean*</span></span>

<span data-ttu-id="e5f9b-111">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="e5f9b-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="e5f9b-112">Example</span></span>

<span data-ttu-id="e5f9b-113">`NOT (TRUE)`, **YANLIŞ** döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5f9b-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e5f9b-114">Additional resources</span></span>

[<span data-ttu-id="e5f9b-115">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="e5f9b-115">Logical functions</span></span>](er-functions-category-logical.md)
