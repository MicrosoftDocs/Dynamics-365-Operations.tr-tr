---
title: FA_SUM ER işlevi
description: Bu konu, FA_SUM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744307"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="7a72d-103">FA_SUM ER işlevi</span><span class="sxs-lookup"><span data-stu-id="7a72d-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a72d-104">Bu `FA_SUM` işlev, belirtilen sabit kıymet maddesine, değer modeli koduna ve tarihlerin dönemine ait sabit kıymet tutarları için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a72d-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a72d-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7a72d-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="7a72d-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7a72d-106">Arguments</span></span>

<span data-ttu-id="7a72d-107">`fixed asset code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="7a72d-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="7a72d-108">Bakiyenin hesaplandığı bir sabit kıymet maddesinin kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="7a72d-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="7a72d-109">`value model code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="7a72d-109">`value model code`: *String*</span></span>

<span data-ttu-id="7a72d-110">Bakiyenin hesaplandığı bir değer modeli kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="7a72d-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="7a72d-111">`start date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="7a72d-111">`start date`: *Date*</span></span>

<span data-ttu-id="7a72d-112">Sabit kıymet tutarlarının hesaplandığı dönemin başlangıç tarihini temsil eden bir *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="7a72d-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="7a72d-113">`end date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="7a72d-113">`end date`: *Date*</span></span>

<span data-ttu-id="7a72d-114">Sabit kıymet tutarlarının hesaplandığı dönemin bitiş tarihini temsil eden bir *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="7a72d-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a72d-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7a72d-115">Return values</span></span>

<span data-ttu-id="7a72d-116">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="7a72d-116">*Container (record)*</span></span>

<span data-ttu-id="7a72d-117">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="7a72d-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="7a72d-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="7a72d-118">Example</span></span>

<span data-ttu-id="7a72d-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)`, **geçerli** değer modeli için hazırlanan sabit kıymet **comp-000001** için **Tarih1** ile **Tarih2** arasındaki bir dönem için veri kapsayıcısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7a72d-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a72d-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7a72d-120">Additional resources</span></span>

[<span data-ttu-id="7a72d-121">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="7a72d-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]