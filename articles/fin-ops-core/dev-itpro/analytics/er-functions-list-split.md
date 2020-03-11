---
title: SPLIT ER işlevi
description: Bu konu, SPLIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 52a89f744cd37c543294522cc706ae7f47660e75
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070633"
---
# <span data-ttu-id="0c444-103"><a name="SPLIT">SPLIT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="0c444-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c444-104">`SPLIT` işlev, belirtilen girdi dizesini alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c444-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0c444-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="0c444-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="0c444-106">Bu söz dizimi, belirtilen giriş dizesini her biri belirli uzunlukta alt dizelere bölün.</span><span class="sxs-lookup"><span data-stu-id="0c444-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="0c444-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="0c444-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="0c444-108">Bu söz dizimi belirtilen giriş dizesini belirli sınırlayıcıya dayanarak alt dizelere bölün.</span><span class="sxs-lookup"><span data-stu-id="0c444-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="0c444-109">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="0c444-109">Arguments</span></span>

<span data-ttu-id="0c444-110">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="0c444-110">`input`: *String*</span></span>

<span data-ttu-id="0c444-111">Bölünecek metin</span><span class="sxs-lookup"><span data-stu-id="0c444-111">The text to split.</span></span>

<span data-ttu-id="0c444-112">`length`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="0c444-112">`length`: *Integer*</span></span>

<span data-ttu-id="0c444-113">Tek bir alt dizenin maksimum uzunluğu.</span><span class="sxs-lookup"><span data-stu-id="0c444-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="0c444-114">`delimiter`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="0c444-114">`delimiter`: *String*</span></span>

<span data-ttu-id="0c444-115">Alt dizeleri ayırmak için kullanılan sınırlayıcı.</span><span class="sxs-lookup"><span data-stu-id="0c444-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c444-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="0c444-116">Return values</span></span>

<span data-ttu-id="0c444-117">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="0c444-117">*Record list*</span></span>

<span data-ttu-id="0c444-118">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="0c444-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c444-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="0c444-119">Usage notes</span></span>

<span data-ttu-id="0c444-120">Döndürülen listenin kayıt yapısı, *dize* türünün **değer** alanından oluşur.</span><span class="sxs-lookup"><span data-stu-id="0c444-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c444-121">İade edilen her kayıt bu alanda oluşturulan alt dizeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="0c444-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="0c444-122">`delimiter` bağımsız değişkeni boşsa, bir kayıt içeren yeni bir liste döner; kayıtta giriş metnini içeren *DİZE* **değer** alanı vardır.</span><span class="sxs-lookup"><span data-stu-id="0c444-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c444-123">Bu alan giriş metnini içerir.</span><span class="sxs-lookup"><span data-stu-id="0c444-123">This field contains the input text.</span></span>

<span data-ttu-id="0c444-124">`input` bağımsız değişkeni boşsa, yeni boş bir liste döner.</span><span class="sxs-lookup"><span data-stu-id="0c444-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="0c444-125">`input` veya `delimiter` bağımsız değişkeni (boş) belirtilmezse, bir uygulama özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0c444-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c444-126">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c444-126">Example 1</span></span>

<span data-ttu-id="0c444-127">`SPLIT ("abcd", 3)`, *Dize* türünün **Değer** alanına sahip iki kaydı içeren yeni bir listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c444-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c444-128">İlk kayıttaki **Değer** alanı **"abc"** metnini içeriyor ve ikinci kayıttaki **Değer** alanı **"d"** metnini içeriyorsa.</span><span class="sxs-lookup"><span data-stu-id="0c444-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c444-129">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0c444-129">Example 2</span></span>

<span data-ttu-id="0c444-130">`SPLIT ("XAb aBy", "aB")`, *Dize* türünün **Değer** alanına sahip üç kaydı içeren yeni bir listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c444-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c444-131">İlk kayıttaki **Değer** alanı, **"X"** metni, ikinci kayıttaki **Değer** alanı **"&nbsp;"** metni, üçüncü kayıttaki **Değer** alanı **"y"** metni içerir.</span><span class="sxs-lookup"><span data-stu-id="0c444-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0c444-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0c444-132">Additional resources</span></span>

[<span data-ttu-id="0c444-133">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="0c444-133">List functions</span></span>](er-functions-category-list.md)
