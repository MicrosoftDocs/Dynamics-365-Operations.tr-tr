---
title: FIRSTORNULL ER işlevi
description: Bu konu, FIRSTORNULL Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753228"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="7f17f-103">FIRSTORNULL ER işlevi</span><span class="sxs-lookup"><span data-stu-id="7f17f-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f17f-104">Bu kayıt boş değilse, `FIRSTORNULL` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f17f-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="7f17f-105">Kayıt boş ise, bu işlev boş bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f17f-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f17f-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7f17f-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="7f17f-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7f17f-107">Arguments</span></span>

<span data-ttu-id="7f17f-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7f17f-108">`list`: *Record list*</span></span>

<span data-ttu-id="7f17f-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7f17f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f17f-110">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7f17f-110">Return values</span></span>

<span data-ttu-id="7f17f-111">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="7f17f-111">*Container (record)*</span></span>

<span data-ttu-id="7f17f-112">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="7f17f-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="7f17f-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="7f17f-113">Example</span></span>

<span data-ttu-id="7f17f-114">İfade `FIRSTORNULL(SPLIT("",1)).Value` boş bir dize (**""**) döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="7f17f-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f17f-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7f17f-115">Additional resources</span></span>

[<span data-ttu-id="7f17f-116">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="7f17f-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]