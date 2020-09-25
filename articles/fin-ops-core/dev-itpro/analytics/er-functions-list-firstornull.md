---
title: FIRSTORNULL ER işlevi
description: Bu konu, FIRSTORNULL Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745212"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="0f32b-103">FIRSTORNULL ER işlevi</span><span class="sxs-lookup"><span data-stu-id="0f32b-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f32b-104">Bu kayıt boş değilse, `FIRSTORNULL` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f32b-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="0f32b-105">Kayıt boş ise, bu işlev boş bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f32b-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f32b-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0f32b-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="0f32b-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="0f32b-107">Arguments</span></span>

<span data-ttu-id="0f32b-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="0f32b-108">`list`: *Record list*</span></span>

<span data-ttu-id="0f32b-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="0f32b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f32b-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="0f32b-110">Return values</span></span>

<span data-ttu-id="0f32b-111">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="0f32b-111">*Container (record)*</span></span>

<span data-ttu-id="0f32b-112">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="0f32b-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="0f32b-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="0f32b-113">Example</span></span>

<span data-ttu-id="0f32b-114">İfade `FIRSTORNULL(SPLIT("",1)).Value` boş bir dize (**""**) döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="0f32b-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f32b-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0f32b-115">Additional resources</span></span>

[<span data-ttu-id="0f32b-116">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="0f32b-116">List functions</span></span>](er-functions-category-list.md)
