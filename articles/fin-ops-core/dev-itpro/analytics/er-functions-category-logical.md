---
title: Mantıksal kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen mantıksal işlevleri hakkında bilgi sağlar.
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916649"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="a0a27-103">Mantıksal kategorisindeki ER işlevlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="a0a27-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0a27-104">Elektronik raporlama (ER) mantıksal işlevleri tek bir ifadede birden fazla karşılaştırma gerçekleştirmek veya çoklu koşulları sınamak amacıyla mantıksal değerlerle çalışmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a0a27-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="a0a27-105">Bu konu, bu işlevlerin özetini sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a0a27-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="a0a27-106">Desteklenen işlevler listesi</span><span class="sxs-lookup"><span data-stu-id="a0a27-106">List of supported functions</span></span>

| <span data-ttu-id="a0a27-107">İşlev</span><span class="sxs-lookup"><span data-stu-id="a0a27-107">Function</span></span> | <span data-ttu-id="a0a27-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0a27-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="a0a27-109">Ve</span><span class="sxs-lookup"><span data-stu-id="a0a27-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="a0a27-110">Belirtilen koşulların tümü **doğru** ise, bu işlev *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="a0a27-111">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="a0a27-112">Sandık</span><span class="sxs-lookup"><span data-stu-id="a0a27-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="a0a27-113">Bu işlev, belirtilen ifadenin değerini belirtilen alternatif seçeneklerle değerlendirir ve belirtilen ifadenin değerine eşit ilk seçeneğin sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="a0a27-114">Tersi durumda, varsayılan bir sonuç çağrılan işlevin son bağımsız değişkeni olarak bir seçenek tarafından belirtilmedikçe, isteğe bağlı bir varsayılan sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="a0a27-115">Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="a0a27-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="a0a27-116">Eğer</span><span class="sxs-lookup"><span data-stu-id="a0a27-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="a0a27-117">Bu işlev, belirtilen koşul karşılandığında ilk belirtilen değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="a0a27-118">Aksi takdirde, ikinci belirtilen değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="a0a27-119">Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="a0a27-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="a0a27-120">Not</span><span class="sxs-lookup"><span data-stu-id="a0a27-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="a0a27-121">Bu işlev, belirtilen koşulun ters çevrilmiş mantıksal değerini bir *Boole* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="a0a27-122">Veya</span><span class="sxs-lookup"><span data-stu-id="a0a27-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="a0a27-123">Belirtilen koşulların tümü yanlış ise, bu işlev **yanlış** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="a0a27-124">Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="a0a27-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="a0a27-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="a0a27-126">Bu işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a0a27-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="a0a27-127">Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="a0a27-128">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0a27-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a0a27-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a0a27-129">Additional resources</span></span>

[<span data-ttu-id="a0a27-130">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="a0a27-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a0a27-131">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="a0a27-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a0a27-132">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="a0a27-132">Electronic reporting formula language</span></span>](er-formula-language.md)
