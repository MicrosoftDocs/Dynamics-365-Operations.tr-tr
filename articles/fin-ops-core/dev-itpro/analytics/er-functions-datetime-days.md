---
title: DAYS ER işlevi
description: Bu konu, DAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746903"
---
# <a name="days-er-function"></a><span data-ttu-id="893f1-103">DAYS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="893f1-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="893f1-104">`DAYS` işlev, belirli bir tarihte ve ikinci belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.</span><span class="sxs-lookup"><span data-stu-id="893f1-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="893f1-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="893f1-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="893f1-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="893f1-106">Arguments</span></span>

<span data-ttu-id="893f1-107">`date 1`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="893f1-107">`date 1`: *Date*</span></span>

<span data-ttu-id="893f1-108">Gün sayısı hesaplaması için başlangıç tarihi temsil eden bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="893f1-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="893f1-109">`date 2`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="893f1-109">`date 2`: *Date*</span></span>

<span data-ttu-id="893f1-110">Gün sayısı hesaplaması için bitiş tarihi temsil eden bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="893f1-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="893f1-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="893f1-111">Return values</span></span>

<span data-ttu-id="893f1-112">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="893f1-112">*Integer*</span></span>

<span data-ttu-id="893f1-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="893f1-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="893f1-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="893f1-114">Usage notes</span></span>

<span data-ttu-id="893f1-115">`DAYS` işlevi, ilk tarih ikinci tarihten sonra olduğunda pozitif bir değer döndürür; ilk tarih ikinci tarihle aynı olduğunda **0** (sıfır) değerini döndürür veya ilk tarih ikinci tarihten önceyse, negatif değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="893f1-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="893f1-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="893f1-116">Example</span></span>

<span data-ttu-id="893f1-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))`, **-1** döndürür.</span><span class="sxs-lookup"><span data-stu-id="893f1-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="893f1-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="893f1-118">Additional resources</span></span>

[<span data-ttu-id="893f1-119">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="893f1-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]