---
title: DAYS ER işlevi
description: Bu konu, DAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916304"
---
# <span data-ttu-id="6be0f-103"><a name="DAYS">DAYS ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="6be0f-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6be0f-104">`DAYS` işlev, belirli bir tarihte ve ikinci belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6be0f-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be0f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="6be0f-105">Syntax</span></span>

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="6be0f-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="6be0f-106">Arguments</span></span>

<span data-ttu-id="6be0f-107">`date 1`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="6be0f-107">`date 1`: *Date*</span></span>

<span data-ttu-id="6be0f-108">Gün sayısı hesaplaması için başlangıç tarihi temsil eden bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="6be0f-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="6be0f-109">`date 2`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="6be0f-109">`date 2`: *Date*</span></span>

<span data-ttu-id="6be0f-110">Gün sayısı hesaplaması için bitiş tarihi temsil eden bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="6be0f-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="6be0f-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="6be0f-111">Return values</span></span>

<span data-ttu-id="6be0f-112">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="6be0f-112">*Integer*</span></span>

<span data-ttu-id="6be0f-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="6be0f-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6be0f-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="6be0f-114">Usage notes</span></span>

<span data-ttu-id="6be0f-115">`DAYS` işlevi, ilk tarih ikinci tarihten sonra olduğunda pozitif bir değer döndürür; ilk tarih ikinci tarihle aynı olduğunda **0** (sıfır) değerini döndürür veya ilk tarih ikinci tarihten önceyse, negatif değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="6be0f-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="6be0f-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="6be0f-116">Example</span></span>

<span data-ttu-id="6be0f-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))`, **-1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="6be0f-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6be0f-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6be0f-118">Additional resources</span></span>

[<span data-ttu-id="6be0f-119">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="6be0f-119">Date and time functions</span></span>](er-functions-category-datetime.md)
