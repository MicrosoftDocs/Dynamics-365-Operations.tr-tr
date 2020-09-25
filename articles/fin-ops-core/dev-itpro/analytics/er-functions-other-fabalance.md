---
title: FA_BALANCE ER işlevi
description: Bu konu, FA_BALANCE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a969e3a484208388fd82d7a714bee27b7fe64a9
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744179"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="60d7e-103">FA_BALANCE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="60d7e-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60d7e-104">`FA_BALANCE` işlev, belirtilen sabit kıymet maddesine, değer modeli koduna, raporlama yılına ve raporlama tarihlerin dönemine ait sabit kıymet bakiyesi için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="60d7e-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d7e-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="60d7e-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="60d7e-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="60d7e-106">Arguments</span></span>

<span data-ttu-id="60d7e-107">`fixed asset code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="60d7e-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="60d7e-108">Bakiyenin hesaplandığı bir sabit kıymet maddesinin kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="60d7e-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="60d7e-109">`value model code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="60d7e-109">`value model code`: *String*</span></span>

<span data-ttu-id="60d7e-110">Bakiyenin hesaplandığı bir değer modeli kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="60d7e-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="60d7e-111">`reporting year`: *Numaralandırma değeri*</span><span class="sxs-lookup"><span data-stu-id="60d7e-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="60d7e-112">Bakiye hesaplaması için bir dönem tanımlayan **VarlıkYılı** uygulama numaralandırmasının sabit listesi değeri.</span><span class="sxs-lookup"><span data-stu-id="60d7e-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="60d7e-113">`reporting date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="60d7e-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="60d7e-114">Bakiye hesaplaması için bir tarih tanımlayan *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="60d7e-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="60d7e-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="60d7e-115">Return values</span></span>

<span data-ttu-id="60d7e-116">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="60d7e-116">*Container (record)*</span></span>

<span data-ttu-id="60d7e-117">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="60d7e-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="60d7e-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="60d7e-118">Example</span></span>

<span data-ttu-id="60d7e-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())`, geçerli uygulama oturum tarihinde **Geçerli** değer modeline sahip **COMP-000001** sabit kıymet bakiyeleri için hazırlanan veri kapsayıcısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="60d7e-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60d7e-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="60d7e-120">Additional resources</span></span>

[<span data-ttu-id="60d7e-121">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="60d7e-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
