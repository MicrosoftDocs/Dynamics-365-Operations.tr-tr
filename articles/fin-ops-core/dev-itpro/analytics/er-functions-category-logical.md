---
title: Mantıksal kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen mantıksal işlevleri hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705107"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="ec658-103">Mantıksal kategorisindeki ER işlevlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="ec658-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec658-104">Elektronik raporlama (ER) mantıksal işlevleri tek bir ifadede birden fazla karşılaştırma gerçekleştirmek veya çoklu koşulları sınamak amacıyla mantıksal değerlerle çalışmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec658-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="ec658-105">Bu konu, bu işlevlerin özetini sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ec658-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="ec658-106">Desteklenen işlevler listesi</span><span class="sxs-lookup"><span data-stu-id="ec658-106">List of supported functions</span></span>

| <span data-ttu-id="ec658-107">İşlev</span><span class="sxs-lookup"><span data-stu-id="ec658-107">Function</span></span> | <span data-ttu-id="ec658-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec658-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ec658-109">Ve</span><span class="sxs-lookup"><span data-stu-id="ec658-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="ec658-110">Belirtilen koşulların tümü **doğru** ise, bu işlev *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="ec658-111">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="ec658-112">Sandık</span><span class="sxs-lookup"><span data-stu-id="ec658-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="ec658-113">Bu işlev, belirtilen ifadenin değerini belirtilen alternatif seçeneklerle değerlendirir ve belirtilen ifadenin değerine eşit ilk seçeneğin sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="ec658-114">Tersi durumda, varsayılan bir sonuç çağrılan işlevin son bağımsız değişkeni olarak bir seçenek tarafından belirtilmedikçe, isteğe bağlı bir varsayılan sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="ec658-115">Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="ec658-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="ec658-116">Eğer</span><span class="sxs-lookup"><span data-stu-id="ec658-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="ec658-117">Bu işlev, belirtilen koşul karşılandığında ilk belirtilen değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="ec658-118">Aksi takdirde, ikinci belirtilen değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="ec658-119">Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="ec658-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="ec658-120">Not</span><span class="sxs-lookup"><span data-stu-id="ec658-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="ec658-121">Bu işlev, belirtilen koşulun ters çevrilmiş mantıksal değerini bir *Boole* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="ec658-122">Veya</span><span class="sxs-lookup"><span data-stu-id="ec658-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="ec658-123">Belirtilen koşulların tümü yanlış ise, bu işlev **yanlış** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="ec658-124">Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="ec658-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="ec658-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="ec658-126">Bu işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="ec658-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="ec658-127">Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="ec658-128">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="ec658-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="ec658-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="ec658-130">Bu işlev, *Int64* veya *Tamsayı* türündeki belirtilen girişin, belirtilen listede belirli bir öğe değeriyle eşleşip eşleşmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="ec658-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="ec658-131">Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="ec658-132">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec658-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="ec658-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ec658-133">Additional resources</span></span>

[<span data-ttu-id="ec658-134">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="ec658-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ec658-135">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="ec658-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ec658-136">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="ec658-136">Electronic reporting formula language</span></span>](er-formula-language.md)
