---
title: DATETODATETIME ER işlevi
description: Bu konu, DATETODATETIME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 961ccd18e70d4f9851027492366a7d9408a668c5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042424"
---
# <span data-ttu-id="2e529-103"><a name="DATETODATETIME">DATETODATETIME ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="2e529-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e529-104">`DATETODATETIME` işlev, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir tarih değerinden bir tarih/saat değerine dönüştürülmüş bir *tarih saat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e529-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e529-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2e529-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="2e529-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="2e529-106">Arguments</span></span>

<span data-ttu-id="2e529-107">`date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="2e529-107">`date`: *Date*</span></span>

<span data-ttu-id="2e529-108">Değiştirilecek tarihi gösteren bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="2e529-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e529-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="2e529-109">Return values</span></span>

<span data-ttu-id="2e529-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="2e529-110">*DateTime*</span></span>

<span data-ttu-id="2e529-111">Sonuç tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="2e529-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2e529-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e529-112">Example 1</span></span>

<span data-ttu-id="2e529-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')`, 24 Aralık 2015 olan geçerli Microsoft Dynamics 365 Finance oturumunun tarihini **12/24/2015 12:00:00** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e529-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="2e529-114">Bu örnekte, **CompInfo** **Finance and Operations/Table** türünde bir elektronik raporlama (ER) veri kaynağıdır ve CompanyInfo tablosuna referans verir.</span><span class="sxs-lookup"><span data-stu-id="2e529-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="2e529-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2e529-115">Example 2</span></span>

<span data-ttu-id="2e529-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` **11/12/2019 12:00:00** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e529-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e529-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2e529-117">Additional resources</span></span>

[<span data-ttu-id="2e529-118">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="2e529-118">Date and time functions</span></span>](er-functions-category-datetime.md)
