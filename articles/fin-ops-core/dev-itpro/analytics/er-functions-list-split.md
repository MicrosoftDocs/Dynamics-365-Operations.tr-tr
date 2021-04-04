---
title: SPLIT ER işlevi
description: Bu konu, SPLIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 806a0995f0c138f4e80396bb993bc6f41bc7c827
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567354"
---
# <a name="split-er-function"></a><span data-ttu-id="b81f7-103">SPLIT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="b81f7-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b81f7-104">`SPLIT` işlev, belirtilen girdi dizesini alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="b81f7-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b81f7-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="b81f7-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="b81f7-106">Bu söz dizimi, belirtilen giriş dizesini her biri belirli uzunlukta alt dizelere bölün.</span><span class="sxs-lookup"><span data-stu-id="b81f7-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="b81f7-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="b81f7-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="b81f7-108">Bu söz dizimi belirtilen giriş dizesini belirli sınırlayıcıya dayanarak alt dizelere bölün.</span><span class="sxs-lookup"><span data-stu-id="b81f7-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="b81f7-109">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b81f7-109">Arguments</span></span>

<span data-ttu-id="b81f7-110">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b81f7-110">`input`: *String*</span></span>

<span data-ttu-id="b81f7-111">Bölünecek metin</span><span class="sxs-lookup"><span data-stu-id="b81f7-111">The text to split.</span></span>

<span data-ttu-id="b81f7-112">`length`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="b81f7-112">`length`: *Integer*</span></span>

<span data-ttu-id="b81f7-113">Tek bir alt dizenin maksimum uzunluğu.</span><span class="sxs-lookup"><span data-stu-id="b81f7-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="b81f7-114">`delimiter`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b81f7-114">`delimiter`: *String*</span></span>

<span data-ttu-id="b81f7-115">Alt dizeleri ayırmak için kullanılan sınırlayıcı.</span><span class="sxs-lookup"><span data-stu-id="b81f7-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="b81f7-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b81f7-116">Return values</span></span>

<span data-ttu-id="b81f7-117">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="b81f7-117">*Record list*</span></span>

<span data-ttu-id="b81f7-118">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="b81f7-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b81f7-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="b81f7-119">Usage notes</span></span>

<span data-ttu-id="b81f7-120">Döndürülen listenin kayıt yapısı, *dize* türünün **değer** alanından oluşur.</span><span class="sxs-lookup"><span data-stu-id="b81f7-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="b81f7-121">İade edilen her kayıt bu alanda oluşturulan alt dizeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="b81f7-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="b81f7-122">`delimiter` bağımsız değişkeni boşsa, bir kayıt içeren yeni bir liste döner; kayıtta giriş metnini içeren *DİZE* **değer** alanı vardır.</span><span class="sxs-lookup"><span data-stu-id="b81f7-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="b81f7-123">Bu alan giriş metnini içerir.</span><span class="sxs-lookup"><span data-stu-id="b81f7-123">This field contains the input text.</span></span>

<span data-ttu-id="b81f7-124">`input` bağımsız değişkeni boşsa, yeni boş bir liste döner.</span><span class="sxs-lookup"><span data-stu-id="b81f7-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="b81f7-125">`input` veya `delimiter` bağımsız değişkeni (boş) belirtilmezse, bir uygulama özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b81f7-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="b81f7-126">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b81f7-126">Example 1</span></span>

<span data-ttu-id="b81f7-127">`SPLIT ("abcd", 3)`, *Dize* türünün **Değer** alanına sahip iki kaydı içeren yeni bir listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b81f7-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="b81f7-128">İlk kayıttaki **Değer** alanı **"abc"** metnini içeriyor ve ikinci kayıttaki **Değer** alanı **"d"** metnini içeriyorsa.</span><span class="sxs-lookup"><span data-stu-id="b81f7-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b81f7-129">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b81f7-129">Example 2</span></span>

<span data-ttu-id="b81f7-130">`SPLIT ("XAb aBy", "aB")`, *Dize* türünün **Değer** alanına sahip üç kaydı içeren yeni bir listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b81f7-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="b81f7-131">İlk kayıttaki **Değer** alanı, **"X"** metni, ikinci kayıttaki **Değer** alanı **"&nbsp;"** metni, üçüncü kayıttaki **Değer** alanı **"y"** metni içerir.</span><span class="sxs-lookup"><span data-stu-id="b81f7-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b81f7-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b81f7-132">Additional resources</span></span>

[<span data-ttu-id="b81f7-133">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="b81f7-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]