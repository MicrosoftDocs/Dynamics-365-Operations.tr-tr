---
title: SPLIT ER işlevi
description: Bu konu, SPLIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853455"
---
# <a name="split-er-function"></a><span data-ttu-id="5fb09-103">SPLIT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="5fb09-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fb09-104">`SPLIT` işlev, belirtilen girdi dizesini alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fb09-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="5fb09-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="5fb09-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="5fb09-106">Bu söz dizimi, belirtilen giriş dizesini her biri belirli uzunlukta alt dizelere bölün.</span><span class="sxs-lookup"><span data-stu-id="5fb09-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="5fb09-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="5fb09-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="5fb09-108">Bu söz dizimi belirtilen giriş dizesini belirli sınırlayıcıya dayanarak alt dizelere bölün.</span><span class="sxs-lookup"><span data-stu-id="5fb09-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="5fb09-109">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="5fb09-109">Arguments</span></span>

<span data-ttu-id="5fb09-110">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="5fb09-110">`input`: *String*</span></span>

<span data-ttu-id="5fb09-111">Bölünecek metin</span><span class="sxs-lookup"><span data-stu-id="5fb09-111">The text to split.</span></span>

<span data-ttu-id="5fb09-112">`length`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="5fb09-112">`length`: *Integer*</span></span>

<span data-ttu-id="5fb09-113">Tek bir alt dizenin maksimum uzunluğu.</span><span class="sxs-lookup"><span data-stu-id="5fb09-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="5fb09-114">`delimiter`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="5fb09-114">`delimiter`: *String*</span></span>

<span data-ttu-id="5fb09-115">Alt dizeleri ayırmak için kullanılan sınırlayıcı.</span><span class="sxs-lookup"><span data-stu-id="5fb09-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="5fb09-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="5fb09-116">Return values</span></span>

<span data-ttu-id="5fb09-117">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="5fb09-117">*Record list*</span></span>

<span data-ttu-id="5fb09-118">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="5fb09-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5fb09-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="5fb09-119">Usage notes</span></span>

<span data-ttu-id="5fb09-120">Döndürülen listenin kayıt yapısı, *dize* türünün **değer** alanından oluşur.</span><span class="sxs-lookup"><span data-stu-id="5fb09-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="5fb09-121">İade edilen her kayıt bu alanda oluşturulan alt dizeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5fb09-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="5fb09-122">`delimiter` bağımsız değişkeni boşsa, bir kayıt içeren yeni bir liste döner; kayıtta giriş metnini içeren *DİZE* **değer** alanı vardır.</span><span class="sxs-lookup"><span data-stu-id="5fb09-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="5fb09-123">Bu alan giriş metnini içerir.</span><span class="sxs-lookup"><span data-stu-id="5fb09-123">This field contains the input text.</span></span>

<span data-ttu-id="5fb09-124">`input` bağımsız değişkeni boşsa, yeni boş bir liste döner.</span><span class="sxs-lookup"><span data-stu-id="5fb09-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="5fb09-125">`input` veya `delimiter` bağımsız değişkeni (boş) belirtilmezse, bir uygulama özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5fb09-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="5fb09-126">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5fb09-126">Example 1</span></span>

<span data-ttu-id="5fb09-127">`SPLIT ("abcd", 3)`, *Dize* türünün **Değer** alanına sahip iki kaydı içeren yeni bir listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fb09-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="5fb09-128">İlk kayıttaki **Değer** alanı **"abc"** metnini içeriyor ve ikinci kayıttaki **Değer** alanı **"d"** metnini içeriyorsa.</span><span class="sxs-lookup"><span data-stu-id="5fb09-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5fb09-129">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5fb09-129">Example 2</span></span>

<span data-ttu-id="5fb09-130">`SPLIT ("XAb aBy", "aB")`, *Dize* türünün **Değer** alanına sahip üç kaydı içeren yeni bir listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fb09-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="5fb09-131">İlk kayıttaki **Değer** alanı, **"X"** metni, ikinci kayıttaki **Değer** alanı **"&nbsp;"** metni, üçüncü kayıttaki **Değer** alanı **"y"** metni içerir.</span><span class="sxs-lookup"><span data-stu-id="5fb09-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="5fb09-132">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5fb09-132">Example 3</span></span>

<span data-ttu-id="5fb09-133">Belirtilen giriş dizesinin bağımsız öğelerine erişmek için [INDEX](er-functions-list-index.md) fonksiyonunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fb09-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="5fb09-134">**Hesaplanmış alan** türüne ait **MyList** veri kaynağını girerseniz ve bunun için `SPLIT("abc", 1)` ifadesini yapılandırırsanız, `INDEX(MyList,2).Value` ifadesi **"b"** metnini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fb09-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="5fb09-135">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="5fb09-135">Example 4</span></span>

<span data-ttu-id="5fb09-136">Belirtilen giriş dizesinin bağımsız öğelerine erişmek için [ENUMERATE](er-functions-list-enumerate.md) fonksiyonunu da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fb09-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="5fb09-137">Önce **Hesaplanan alan** türünün **MyList** veri kaynağını girerseniz ve bunun için `SPLIT("abc", 1)` ifadesini yapılandırırsanız ve ardından **Hesaplanan alan** türünün **EnumeratedList** veri kaynağını girip bunu `ENUMERATE(MyList)` ifadesi için yapılandırırsanız `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` ifadesi **"b"** metnini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fb09-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fb09-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5fb09-138">Additional resources</span></span>

[<span data-ttu-id="5fb09-139">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="5fb09-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
