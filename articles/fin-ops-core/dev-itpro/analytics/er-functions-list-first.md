---
title: FIRST ER işlevi
description: Bu konu, FIRST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564747"
---
# <a name="first-er-function"></a><span data-ttu-id="62a2c-103">FIRST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="62a2c-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62a2c-104">Bu liste boş değilse, `FIRST` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="62a2c-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="62a2c-105">Liste boşsa, bu işlev bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62a2c-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a2c-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="62a2c-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="62a2c-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="62a2c-107">Arguments</span></span>

<span data-ttu-id="62a2c-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="62a2c-108">`list`: *Record list*</span></span>

<span data-ttu-id="62a2c-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="62a2c-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="62a2c-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="62a2c-110">Return values</span></span>

<span data-ttu-id="62a2c-111">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="62a2c-111">*Container (record)*</span></span>

<span data-ttu-id="62a2c-112">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="62a2c-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="62a2c-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62a2c-113">Example 1</span></span>

<span data-ttu-id="62a2c-114">Bu ifade `FIRST(SPLIT("ABC",1)).Value` **"A"** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="62a2c-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="62a2c-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="62a2c-115">Example 2</span></span>

<span data-ttu-id="62a2c-116">`FIRST(SPLIT("",1)).Value` ifadesi, çalışma zamanında bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62a2c-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62a2c-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="62a2c-117">Additional resources</span></span>

[<span data-ttu-id="62a2c-118">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="62a2c-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]