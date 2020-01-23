---
title: CASE ER işlevi
description: Bu konu, CASE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916074"
---
# <span data-ttu-id="15164-103"><a name="CASE">CASE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="15164-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15164-104">`CASE` işlev, belirtilen ifadenin değerini belirtilen alternatif seçeneklerle değerlendirir ve belirtilen ifadenin değerine eşit ilk seçeneğin sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="15164-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="15164-105">Tersi durumda, varsayılan bir sonuç çağrılan işlevin son bağımsız değişkeni olarak bir seçenek tarafından belirtilmedikçe, isteğe bağlı bir varsayılan sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="15164-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="15164-106">Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="15164-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="15164-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="15164-107">Syntax</span></span>

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="15164-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="15164-108">Arguments</span></span>

<span data-ttu-id="15164-109">`expression`: *Temel veri türü* (Boole, sayısal veya metin)</span><span class="sxs-lookup"><span data-stu-id="15164-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="15164-110">Temel veri türü değerini döndüren geçerli bir ifade.</span><span class="sxs-lookup"><span data-stu-id="15164-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="15164-111">`option 1`: *Temel veri türü* (Boole, sayısal veya metin)</span><span class="sxs-lookup"><span data-stu-id="15164-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="15164-112">Çağrılan işlevin `expression` bağımsız değişkeniyle aynı temel veri türü değerini döndüren geçerli bir ifade.</span><span class="sxs-lookup"><span data-stu-id="15164-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="15164-113">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="15164-113">This argument is required.</span></span>

<span data-ttu-id="15164-114">`result 1`: *Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="15164-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="15164-115">Önceki seçeneğe karşılık gelen iade sonucu.</span><span class="sxs-lookup"><span data-stu-id="15164-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="15164-116">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="15164-116">This argument is required.</span></span>

<span data-ttu-id="15164-117">`option N`: *Temel veri türü* (Boole, sayısal veya metin)</span><span class="sxs-lookup"><span data-stu-id="15164-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="15164-118">Çağrılan işlevin `expression` bağımsız değişkeniyle aynı temel veri türü değerini döndüren geçerli bir ifade.</span><span class="sxs-lookup"><span data-stu-id="15164-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="15164-119">Bu bağımsız değişken isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="15164-119">This argument is optional.</span></span>

<span data-ttu-id="15164-120">`result N`: *Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="15164-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="15164-121">Önceki seçeneğe karşılık gelen iade sonucu.</span><span class="sxs-lookup"><span data-stu-id="15164-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="15164-122">Bu bağımsız değişken isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="15164-122">This argument is optional.</span></span>

<span data-ttu-id="15164-123">`default result`: *Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="15164-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="15164-124">Eşleşme yoksa, döndürülmesi gereken sonuç.</span><span class="sxs-lookup"><span data-stu-id="15164-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="15164-125">Bu bağımsız değişken isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="15164-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="15164-126">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="15164-126">Return values</span></span>

<span data-ttu-id="15164-127">*Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="15164-127">*Any of the supported data types*</span></span>

<span data-ttu-id="15164-128">Desteklenen veri türlerinin herhangi birinin sonuç değeri.</span><span class="sxs-lookup"><span data-stu-id="15164-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="15164-129">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="15164-129">Usage notes</span></span>

<span data-ttu-id="15164-130">Çalışma zamanında bir eşleşme yoksa ve isteğe bağlı olarak bir varsayılan sonuç tanımlanmamışsa, bir özel durum atılır.</span><span class="sxs-lookup"><span data-stu-id="15164-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="15164-131">Tüm sonuçların aynı veri türü kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="15164-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="15164-132">Yapılandırılan sonuçların veri türleri eşleşmezse, tasarım zamanında özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="15164-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="15164-133">İlk sonuç değeri ve *N*'ci sonuç değer *konteyner (kayıt)* veya *kayıt listesi* veri türünün değerleri ise, sonuç yalnızca her iki değerde bulunan alanlara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="15164-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="15164-134">Örnek</span><span class="sxs-lookup"><span data-stu-id="15164-134">Example</span></span>

<span data-ttu-id="15164-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")`, geçerli uygulama oturum tarihi, Ekim ve Aralık arasında ise, **"kış"** dizesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="15164-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="15164-136">Aksi halde, boş bir dize döndürür.</span><span class="sxs-lookup"><span data-stu-id="15164-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15164-137">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="15164-137">Additional resources</span></span>

[<span data-ttu-id="15164-138">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="15164-138">Logical functions</span></span>](er-functions-category-logical.md)
