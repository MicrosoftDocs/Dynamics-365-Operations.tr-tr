---
title: FIRST ER işlevi
description: Bu konu, FIRST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745237"
---
# <a name="first-er-function"></a><span data-ttu-id="e5675-103">FIRST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e5675-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5675-104">Bu liste boş değilse, `FIRST` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5675-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="e5675-105">Liste boşsa, bu işlev bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5675-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5675-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e5675-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="e5675-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e5675-107">Arguments</span></span>

<span data-ttu-id="e5675-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="e5675-108">`list`: *Record list*</span></span>

<span data-ttu-id="e5675-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="e5675-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e5675-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e5675-110">Return values</span></span>

<span data-ttu-id="e5675-111">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="e5675-111">*Container (record)*</span></span>

<span data-ttu-id="e5675-112">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="e5675-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e5675-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5675-113">Example 1</span></span>

<span data-ttu-id="e5675-114">Bu ifade `FIRST(SPLIT("ABC",1)).Value` **"A"** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5675-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e5675-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e5675-115">Example 2</span></span>

<span data-ttu-id="e5675-116">`FIRST(SPLIT("",1)).Value` ifadesi, çalışma zamanında bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5675-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5675-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e5675-117">Additional resources</span></span>

[<span data-ttu-id="e5675-118">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="e5675-118">List functions</span></span>](er-functions-category-list.md)
