---
title: FA_SUM ER işlevi
description: Bu konu, FA_SUM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687708"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="13774-103">FA_SUM ER işlevi</span><span class="sxs-lookup"><span data-stu-id="13774-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13774-104">Bu `FA_SUM` işlev, belirtilen sabit kıymet maddesine, değer modeli koduna ve tarihlerin dönemine ait sabit kıymet tutarları için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="13774-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="13774-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="13774-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="13774-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="13774-106">Arguments</span></span>

<span data-ttu-id="13774-107">`fixed asset code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="13774-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="13774-108">Bakiyenin hesaplandığı bir sabit kıymet maddesinin kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="13774-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="13774-109">`value model code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="13774-109">`value model code`: *String*</span></span>

<span data-ttu-id="13774-110">Bakiyenin hesaplandığı bir değer modeli kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="13774-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="13774-111">`start date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="13774-111">`start date`: *Date*</span></span>

<span data-ttu-id="13774-112">Sabit kıymet tutarlarının hesaplandığı dönemin başlangıç tarihini temsil eden bir *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="13774-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="13774-113">`end date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="13774-113">`end date`: *Date*</span></span>

<span data-ttu-id="13774-114">Sabit kıymet tutarlarının hesaplandığı dönemin bitiş tarihini temsil eden bir *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="13774-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="13774-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="13774-115">Return values</span></span>

<span data-ttu-id="13774-116">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="13774-116">*Container (record)*</span></span>

<span data-ttu-id="13774-117">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="13774-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="13774-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="13774-118">Example</span></span>

<span data-ttu-id="13774-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)`, **geçerli** değer modeli için hazırlanan sabit kıymet **comp-000001** için **Tarih1** ile **Tarih2** arasındaki bir dönem için veri kapsayıcısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="13774-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13774-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="13774-120">Additional resources</span></span>

[<span data-ttu-id="13774-121">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="13774-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
