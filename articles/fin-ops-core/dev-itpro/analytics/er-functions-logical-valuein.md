---
title: VALUEIN ER işlevi
description: Bu konu, VALUEIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915982"
---
# <span data-ttu-id="99f3b-103"><a name="VALUEIN">VALUEIN ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="99f3b-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99f3b-104">`VALUEIN` işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="99f3b-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="99f3b-105">Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="99f3b-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="99f3b-106">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="99f3b-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f3b-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="99f3b-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="99f3b-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="99f3b-108">Arguments</span></span>

<span data-ttu-id="99f3b-109">`input`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="99f3b-109">`input`: *Field*</span></span>

<span data-ttu-id="99f3b-110">*Kayıt listesi* türünde bir veri kaynağı öğesinin geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="99f3b-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="99f3b-111">Bu öğenin değeri eşleşir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-111">The value of this item will be matched.</span></span>

<span data-ttu-id="99f3b-112">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="99f3b-112">`list`: *Record list*</span></span>

<span data-ttu-id="99f3b-113">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="99f3b-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="99f3b-114">`list item expression`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="99f3b-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="99f3b-115">Geçerli koşul işaret eden ya da belirtilen listenin eşleştirmek için kullanılacak tek bir alan içeren bir ifadeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="99f3b-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="99f3b-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="99f3b-116">Return values</span></span>

<span data-ttu-id="99f3b-117">*Boole*</span><span class="sxs-lookup"><span data-stu-id="99f3b-117">*Boolean*</span></span>

<span data-ttu-id="99f3b-118">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="99f3b-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="99f3b-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="99f3b-119">Usage notes</span></span>

<span data-ttu-id="99f3b-120">Genel olarak, `VALUEIN` işlevi bir dizi **OR** koşuluna çevrilir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="99f3b-121">Bazı durumlarda, bu `EXISTS JOIN` işleci kullanılarak veritabanı SQL deyimine çevrilebilir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="99f3b-122">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99f3b-122">Example 1</span></span>

<span data-ttu-id="99f3b-123">Model eşlemeniz içinde *Hesaplanan alan* türünün **Liste** veri kaynağını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="99f3b-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="99f3b-124">Bu veri kaynağı `SPLIT ("a,b,c", ",")` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="99f3b-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="99f3b-125">Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, List.Value)` ifade olarak yapılandırıldıysa, **DOĞRU** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="99f3b-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="99f3b-126">Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, `("B" = "b")` ifadesinin **DOĞRU** olduğu.</span><span class="sxs-lookup"><span data-stu-id="99f3b-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="99f3b-127">Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, LEFT(List.Value, 0))` ifade olarak yapılandırıldıysa, **YANLIŞ** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="99f3b-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="99f3b-128">Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `("B" = "")` ifadesinin **DOĞRU** olmadığı.</span><span class="sxs-lookup"><span data-stu-id="99f3b-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="99f3b-129">Böyle bir koşul metninde karakter sayısı üst sınırının 32.768 karakter olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="99f3b-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="99f3b-130">Bu nedenle, çalışma zamanında bu sınırı aşan veri kaynakları oluşturmamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="99f3b-131">Sınır aşılırsa uygulama çalışmayı durdurur ve bir özel durum gönderilir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="99f3b-132">Örneğin, veri kaynağı `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` olarak yapılandırılmışsa ve **List1** ve **List2** listeleri büyük miktarda kayıt içeriyorsa bu durum ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="99f3b-133">Bazı durumlarda, `VALUEIN` işlevi `EXISTS JOIN` işleci kullanarak bir veritabanı ifadesi çevrilir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="99f3b-134">Bu davranış, [FİLTRE](er-functions-list-filter.md) işlevi kullanıldığında ve aşağıdaki koşullar sağlandığında olur:</span><span class="sxs-lookup"><span data-stu-id="99f3b-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="99f3b-135">**SORGU İSTE** seçeneği kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için kapatılır.</span><span class="sxs-lookup"><span data-stu-id="99f3b-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="99f3b-136">Hiçbir ek koşul, çalışma zamanında bu veri kaynağına uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="99f3b-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="99f3b-137">Kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için hiçbir iç içe ifade yapılandırılmaz.</span><span class="sxs-lookup"><span data-stu-id="99f3b-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="99f3b-138">`VALUEIN` işlevinin bir liste öğesi belirtilen veri kaynağının bir alanını belirtilir (bir ifade veya bir yöntem değil).</span><span class="sxs-lookup"><span data-stu-id="99f3b-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="99f3b-139">Bu örnekte daha önce açıklandığı gibi [WHERE](er-functions-list-where.md) işlevi yerine bu seçeneği kullanmayı düşünün.</span><span class="sxs-lookup"><span data-stu-id="99f3b-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="99f3b-140">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="99f3b-140">Example 2</span></span>

<span data-ttu-id="99f3b-141">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="99f3b-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="99f3b-142">*Tablo kayıtları* türünün **İçinde** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="99f3b-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="99f3b-143">Bu veri kaynağı Intrastat tablosuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="99f3b-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="99f3b-144">*Tablo kayıtları* türünün **Port** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="99f3b-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="99f3b-145">Bu veri kaynağı IntrastatPort tablosuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="99f3b-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="99f3b-146">`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` olarak yapılandırılmış bir veri kaynağı çağrıldığında aşağıdaki SQL ifadesi Intrastat tablosunun filtre uygulanan kayıtlarını döndürmek için oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="99f3b-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="99f3b-147">**dataAreaId** alanları için nihai SQL deyimi `IN` işleci kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="99f3b-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="99f3b-148">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="99f3b-148">Example 3</span></span>

<span data-ttu-id="99f3b-149">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="99f3b-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="99f3b-150">**Le** veri kaynağına *hesaplanan alan* ekleyin.</span><span class="sxs-lookup"><span data-stu-id="99f3b-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="99f3b-151">Bu veri kaynağı `SPLIT ("DEMF,GBSI,USMF", ",")` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="99f3b-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="99f3b-152">*Tablo kayıtları* türünün **İçinde** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="99f3b-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="99f3b-153">Bu veri kaynağı Intrastat tablosuna başvuruyor ve bunun için **şirketler arası** seçeneği açık.</span><span class="sxs-lookup"><span data-stu-id="99f3b-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="99f3b-154">`FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` ifadesi olarak yapılandırılmış bir veri kaynağı çağrıldığında son SQL deyimi aşağıdaki koşulu içerir.</span><span class="sxs-lookup"><span data-stu-id="99f3b-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="99f3b-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="99f3b-155">Additional resources</span></span>

[<span data-ttu-id="99f3b-156">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="99f3b-156">Logical functions</span></span>](er-functions-category-logical.md)
