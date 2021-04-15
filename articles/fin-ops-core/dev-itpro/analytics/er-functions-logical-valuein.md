---
title: VALUEIN ER işlevi
description: Bu konu, VALUEIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 08/18/2020
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
ms.openlocfilehash: 909aef5e52817a67e400f3132cb5d6ecc8a18906
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751763"
---
# <a name="valuein-er-function"></a><span data-ttu-id="20159-103">VALUEIN ER işlevi</span><span class="sxs-lookup"><span data-stu-id="20159-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20159-104">`VALUEIN` işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="20159-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="20159-105">Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="20159-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="20159-106">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="20159-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="20159-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="20159-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="20159-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="20159-108">Arguments</span></span>

<span data-ttu-id="20159-109">`input`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="20159-109">`input`: *Field*</span></span>

<span data-ttu-id="20159-110">*Kayıt listesi* türünde bir veri kaynağı öğesinin geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="20159-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="20159-111">Bu öğenin değeri eşleşir.</span><span class="sxs-lookup"><span data-stu-id="20159-111">The value of this item will be matched.</span></span>

<span data-ttu-id="20159-112">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="20159-112">`list`: *Record list*</span></span>

<span data-ttu-id="20159-113">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="20159-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="20159-114">`list item expression`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="20159-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="20159-115">Geçerli koşul işaret eden ya da belirtilen listenin eşleştirmek için kullanılacak tek bir alan içeren bir ifadeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="20159-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="20159-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="20159-116">Return values</span></span>

<span data-ttu-id="20159-117">*Boole*</span><span class="sxs-lookup"><span data-stu-id="20159-117">*Boolean*</span></span>

<span data-ttu-id="20159-118">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="20159-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="20159-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="20159-119">Usage notes</span></span>

<span data-ttu-id="20159-120">Genel olarak, `VALUEIN` işlevi bir dizi **OR** koşuluna çevrilir.</span><span class="sxs-lookup"><span data-stu-id="20159-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="20159-121">**OR** koşulları listesi büyükse ve SQL deyiminin maksimum toplam uzunluğu aşılacaksa [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20159-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="20159-122">Bazı durumlarda, bu `EXISTS JOIN` işleci kullanılarak veritabanı SQL deyimine çevrilebilir.</span><span class="sxs-lookup"><span data-stu-id="20159-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="20159-123">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="20159-123">Example 1</span></span>

<span data-ttu-id="20159-124">Model eşlemeniz içinde *Hesaplanan alan* türünün **Liste** veri kaynağını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="20159-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="20159-125">Bu veri kaynağı `SPLIT ("a,b,c", ",")` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="20159-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="20159-126">Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, List.Value)` ifade olarak yapılandırıldıysa, **DOĞRU** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="20159-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="20159-127">Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, `("B" = "b")` ifadesinin **DOĞRU** olduğu.</span><span class="sxs-lookup"><span data-stu-id="20159-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="20159-128">Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, LEFT(List.Value, 0))` ifade olarak yapılandırıldıysa, **YANLIŞ** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="20159-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="20159-129">Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `("B" = "")` ifadesinin **DOĞRU** olmadığı.</span><span class="sxs-lookup"><span data-stu-id="20159-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="20159-130">Böyle bir koşul metninde karakter sayısı üst sınırının 32.768 karakter olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="20159-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="20159-131">Bu nedenle, çalışma zamanında bu sınırı aşan veri kaynakları oluşturmamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="20159-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="20159-132">Sınır aşılırsa uygulama çalışmayı durdurur ve bir özel durum gönderilir.</span><span class="sxs-lookup"><span data-stu-id="20159-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="20159-133">Örneğin, veri kaynağı `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` olarak yapılandırılmışsa ve **List1** ve **List2** listeleri büyük miktarda kayıt içeriyorsa bu durum ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="20159-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="20159-134">Bazı durumlarda, `VALUEIN` işlevi `EXISTS JOIN` işleci kullanarak bir veritabanı ifadesi çevrilir.</span><span class="sxs-lookup"><span data-stu-id="20159-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="20159-135">Bu davranış, [`FILTER`](er-functions-list-filter.md) işlevi kullanıldığında ve aşağıdaki koşullar sağlandığında gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="20159-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="20159-136">**SORGU İSTE** seçeneği kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için kapatılır.</span><span class="sxs-lookup"><span data-stu-id="20159-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="20159-137">Hiçbir ek koşul, çalışma zamanında bu veri kaynağına uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="20159-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="20159-138">Kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için hiçbir iç içe ifade yapılandırılmaz.</span><span class="sxs-lookup"><span data-stu-id="20159-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="20159-139">`VALUEIN` işlevinin bir liste öğesi belirtilen veri kaynağının bir alanını belirtilir (bir ifade veya bir yöntem değil).</span><span class="sxs-lookup"><span data-stu-id="20159-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="20159-140">Bu örnekte daha önce açıklanan [`WHERE`](er-functions-list-where.md) işlevi yerine bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20159-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="20159-141">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="20159-141">Example 2</span></span>

<span data-ttu-id="20159-142">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="20159-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="20159-143">*Tablo kayıtları* türünün **İçinde** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="20159-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="20159-144">Bu veri kaynağı Intrastat tablosuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="20159-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="20159-145">*Tablo kayıtları* türünün **Port** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="20159-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="20159-146">Bu veri kaynağı IntrastatPort tablosuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="20159-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="20159-147">`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` olarak yapılandırılmış bir veri kaynağı çağrıldığında aşağıdaki SQL ifadesi Intrastat tablosunun filtre uygulanan kayıtlarını döndürmek için oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="20159-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="20159-148">**dataAreaId** alanları için nihai SQL deyimi `IN` işleci kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="20159-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="20159-149">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="20159-149">Example 3</span></span>

<span data-ttu-id="20159-150">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="20159-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="20159-151">**Le** veri kaynağına *hesaplanan alan* ekleyin.</span><span class="sxs-lookup"><span data-stu-id="20159-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="20159-152">Bu veri kaynağı `SPLIT ("DEMF,GBSI,USMF", ",")` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="20159-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="20159-153">*Tablo kayıtları* türünün **İçinde** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="20159-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="20159-154">Bu veri kaynağı Intrastat tablosuna başvuruyor ve bunun için **şirketler arası** seçeneği açık.</span><span class="sxs-lookup"><span data-stu-id="20159-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="20159-155">`FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` ifadesi olarak yapılandırılmış bir veri kaynağı çağrıldığında son SQL deyimi aşağıdaki koşulu içerir.</span><span class="sxs-lookup"><span data-stu-id="20159-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="20159-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="20159-156">Additional resources</span></span>

[<span data-ttu-id="20159-157">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="20159-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="20159-158">VALUEINLARGE işlevleri</span><span class="sxs-lookup"><span data-stu-id="20159-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]