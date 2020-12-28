---
title: Tür dönüştürme kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen dönüştürme işlevleri hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686087"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="5361f-103">Tür dönüştürme kategorisindeki ER işlevlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="5361f-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5361f-104">Elektronik raporlama (ER) tür dönüştürme işlevleri, değerleri türler arasında dönüştürmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5361f-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="5361f-105">Bu konu, bu işlevlerin özetini sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5361f-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="5361f-106">Tür dönüştürme işlevleri</span><span class="sxs-lookup"><span data-stu-id="5361f-106">Type conversion functions</span></span>

| <span data-ttu-id="5361f-107">İşlev</span><span class="sxs-lookup"><span data-stu-id="5361f-107">Function</span></span> | <span data-ttu-id="5361f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5361f-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="5361f-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="5361f-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="5361f-110">Bu işlevi, belirtilen dizeyi temsil eden bir *Int64* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="5361f-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="5361f-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="5361f-112">Bu işlevi, belirtilen dizeyi temsil eden bir *Int* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="5361f-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="5361f-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="5361f-114">Bu işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="5361f-115">Dönüştürme sırasında, belirtilen ondalık ve basamak gruplandırma ayırıcıları dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="5361f-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="5361f-116">Değer</span><span class="sxs-lookup"><span data-stu-id="5361f-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="5361f-117">Bu işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="5361f-118">Tarih ve zaman kategorisindeki tür dönüştürme işlevleri</span><span class="sxs-lookup"><span data-stu-id="5361f-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="5361f-119">Aşağıdaki tabloda [tarih ve saat kategorisinde](er-functions-category-datetime.md) tür dönüştürme işlevleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5361f-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="5361f-120">İşlev</span><span class="sxs-lookup"><span data-stu-id="5361f-120">Function</span></span> | <span data-ttu-id="5361f-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="5361f-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="5361f-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="5361f-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="5361f-123">Bu işlev, belirli bir *Dize* değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih/saat değeri olarak gösteren bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="5361f-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="5361f-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="5361f-125">Bu işlev, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir *Tarih* değerinden bir tarih/saat değerine dönüştürülmüş bir *tarih saat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="5361f-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="5361f-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="5361f-127">Bu işlev, belirli bir *Dize* değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih değeri olarak gösteren bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="5361f-128">Liste kategorisindeki tür dönüştürme işlevleri</span><span class="sxs-lookup"><span data-stu-id="5361f-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="5361f-129">Aşağıdaki tabloda [liste kategorisinde](er-functions-category-list.md) tür dönüştürme işlevleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5361f-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="5361f-130">İşlev</span><span class="sxs-lookup"><span data-stu-id="5361f-130">Function</span></span> | <span data-ttu-id="5361f-131">Tanım</span><span class="sxs-lookup"><span data-stu-id="5361f-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="5361f-132">Liste</span><span class="sxs-lookup"><span data-stu-id="5361f-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="5361f-133">Bu işlevi, *konteyner (kayıt)* türünün belirtilen bağımsız değişkenlerden oluşturulmuş yeni listeden oluşan yeni bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="5361f-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="5361f-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="5361f-135">Bu işlev, *numaralandırmanın* veya *konteyner (kayıt)* türünün belirli bağımsız değişkeninin yapısına göre oluşturulan bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="5361f-136">Böl</span><span class="sxs-lookup"><span data-stu-id="5361f-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="5361f-137">Bu işlev, belirtilen *Dize* değeri alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="5361f-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="5361f-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="5361f-139">Bu işlevi, belirtilen *Kayıt listesi* değerindeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="5361f-140">Değerler belirtilen sınırlayıcı ile ayrılır.</span><span class="sxs-lookup"><span data-stu-id="5361f-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="5361f-141">Metin kategorisindeki tür dönüştürme işlevleri</span><span class="sxs-lookup"><span data-stu-id="5361f-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="5361f-142">Aşağıdaki tabloda [metin kategorisinde](er-functions-category-text.md) tür dönüştürme işlevleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5361f-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="5361f-143">İşlev</span><span class="sxs-lookup"><span data-stu-id="5361f-143">Function</span></span> | <span data-ttu-id="5361f-144">Tanım</span><span class="sxs-lookup"><span data-stu-id="5361f-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="5361f-145">Char</span><span class="sxs-lookup"><span data-stu-id="5361f-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="5361f-146">Bu işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="5361f-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="5361f-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="5361f-148">Bu işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="5361f-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="5361f-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="5361f-150">Bu işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde belirtilen sayıyı gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="5361f-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="5361f-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="5361f-152">Bu işlev, belirtilen dizgi için hızlı yanıt kodu (QR kodu) görüntüsünü ikili biçimde gösteren bir *konteyner* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="5361f-153">Metin</span><span class="sxs-lookup"><span data-stu-id="5361f-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="5361f-154">Bu işlevi, belirtilen giriş geçerli uygulama örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra bleirtilen sayıyı *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="5361f-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5361f-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5361f-155">Additional resources</span></span>

[<span data-ttu-id="5361f-156">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="5361f-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5361f-157">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="5361f-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="5361f-158">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="5361f-158">Electronic reporting formula language</span></span>](er-formula-language.md)
