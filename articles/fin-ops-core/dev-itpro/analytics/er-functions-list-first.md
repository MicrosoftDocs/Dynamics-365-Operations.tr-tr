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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917362"
---
# <span data-ttu-id="32071-103"><a name="FIRST">FIRST ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="32071-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32071-104">Bu liste boş değilse, `FIRST` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="32071-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="32071-105">Liste boşsa, bu işlev bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32071-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="32071-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="32071-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="32071-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="32071-107">Arguments</span></span>

<span data-ttu-id="32071-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="32071-108">`list`: *Record list*</span></span>

<span data-ttu-id="32071-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="32071-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="32071-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="32071-110">Return values</span></span>

<span data-ttu-id="32071-111">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="32071-111">*Container (record)*</span></span>

<span data-ttu-id="32071-112">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="32071-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="32071-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="32071-113">Example 1</span></span>

<span data-ttu-id="32071-114">Bu ifade `FIRST(SPLIT("ABC",1)).Value` **"A"** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="32071-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="32071-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="32071-115">Example 2</span></span>

<span data-ttu-id="32071-116">`FIRST(SPLIT("",1)).Value` ifadesi, çalışma zamanında bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32071-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32071-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="32071-117">Additional resources</span></span>

[<span data-ttu-id="32071-118">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="32071-118">List functions</span></span>](er-functions-category-list.md)
