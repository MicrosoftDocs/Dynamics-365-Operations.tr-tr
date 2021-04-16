---
title: VALUEINLARGE ER işlevi
description: Bu konuda, VALUEINLARGE Elektronik raporlama (ER) işlevinin kullanımı hakkında bilgi sunulmaktadır.
author: NickSelin
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 74d6856a0598293d87f79baabed4773d617164d0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743764"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="eb12b-103">VALUEINLARGE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="eb12b-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb12b-104">`VALUEINLARGE` işlevi, *Int64* veya *Tamsayı* türündeki belirtilen girişin, belirtilen listede belirli bir öğe değeriyle eşleşip eşleşmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="eb12b-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="eb12b-105">İşlev, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb12b-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="eb12b-106">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb12b-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="eb12b-107">`VALUEIN` işlevinin farkını anlamak için bu konudaki [Kullanım notu](#usage_note) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="eb12b-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb12b-108">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="eb12b-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="eb12b-109">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="eb12b-109">Arguments</span></span>

<span data-ttu-id="eb12b-110">`input`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="eb12b-110">`input`: *Field*</span></span>

<span data-ttu-id="eb12b-111">*Kayıt listesi* türünde bir veri kaynağı öğesinin geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="eb12b-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="eb12b-112">Bu öğenin değeri eşleşir.</span><span class="sxs-lookup"><span data-stu-id="eb12b-112">The value of this item will be matched.</span></span>

<span data-ttu-id="eb12b-113">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="eb12b-113">`list`: *Record list*</span></span>

<span data-ttu-id="eb12b-114">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="eb12b-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="eb12b-115">`list item expression`: *İfade*</span><span class="sxs-lookup"><span data-stu-id="eb12b-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="eb12b-116">Geçerli koşul işaret eden ya da belirtilen listenin eşleştirmek için kullanılacak tek bir alan içeren bir ifadeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="eb12b-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb12b-117">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="eb12b-117">Return values</span></span>

<span data-ttu-id="eb12b-118">*Boole*</span><span class="sxs-lookup"><span data-stu-id="eb12b-118">*Boolean*</span></span>

<span data-ttu-id="eb12b-119">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="eb12b-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="eb12b-120"><a name="usage_note">Kullanım notları</a></span><span class="sxs-lookup"><span data-stu-id="eb12b-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="eb12b-121">Belirtilen giriş, yapılan çağrıların doğrudan SQL deyimine çevrilebildiği *Int64* veya *Integer* türündeki bir veri kaynağı öğesini temsil ettiğinde, belirtilen liste geçici bir SQL tablosuna dönüştürülür ve eşleştirme tek bir `EXISTS JOIN` sorgusu yürütülerek veritabanında gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="eb12b-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="eb12b-122">Aksi takdirde, bu işlev [`VALUEIN`](er-functions-logical-valuein.md) işlevi olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="eb12b-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="eb12b-123">Belirtilen giriş, *Int64* ve *Tamsayı* türünden farklı bir öğe olarak tasarlanan veri kaynağı öğesini temsil ettiğinde tasarım sırasında, yapılandırılan ER ifadesi için `VALUEINLARGE` işlevinin uygulanabilir olmadığını bildiren bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="eb12b-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="eb12b-124">`VALUEINLARGE` işlev ifadesi yürütüldüğünde ve bu yürütme kapsamında birden fazla geçici tablo kullanıldığında, çalışma zamanı hatası oluşur.</span><span class="sxs-lookup"><span data-stu-id="eb12b-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="eb12b-125">Örnek</span><span class="sxs-lookup"><span data-stu-id="eb12b-125">Example</span></span>

<span data-ttu-id="eb12b-126">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="eb12b-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="eb12b-127">*Tablo kayıtları* türünün **İçinde** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="eb12b-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="eb12b-128">Bu veri kaynağı **Intrastat** tablosuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="eb12b-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="eb12b-129">**Şirketler arası** seçeneği **Hayır** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="eb12b-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="eb12b-130">*Hesaplanan alan* türünün **InMemory** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="eb12b-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="eb12b-131">Bu veri kaynağı `WHERE (In, In.Port <> "")` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="eb12b-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="eb12b-132">*Hesaplanan alan* türünün **InFiltered** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="eb12b-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="eb12b-133">Bu veri kaynağı `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="eb12b-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="eb12b-134">**InFiltered** veri kaynağı, **DEMF** şirket bağlamında çağrıldıysa uygulama veritabanında yeni bir geçici tablo oluşturulur, toplanan kayıt kimliği kodları bellek içi listesi bu tabloya eklenir ve **Intrastat** tablosunun filtrelenmiş kayıtlarını döndürmek için aşağıdaki SQL deyimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eb12b-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="eb12b-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="eb12b-135">Additional resources</span></span>

[<span data-ttu-id="eb12b-136">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="eb12b-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="eb12b-137">VALUEIN işlevleri</span><span class="sxs-lookup"><span data-stu-id="eb12b-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]