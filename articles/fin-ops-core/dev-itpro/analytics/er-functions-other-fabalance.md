---
title: FA_BALANCE ER işlevi
description: Bu konu, FA_BALANCE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ec78b9c5bf800503023315eb893076486b0a1fb0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744331"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="54fa1-103">FA_BALANCE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="54fa1-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54fa1-104">`FA_BALANCE` işlev, belirtilen sabit kıymet maddesine, değer modeli koduna, raporlama yılına ve raporlama tarihlerin dönemine ait sabit kıymet bakiyesi için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="54fa1-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fa1-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="54fa1-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="54fa1-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="54fa1-106">Arguments</span></span>

<span data-ttu-id="54fa1-107">`fixed asset code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="54fa1-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="54fa1-108">Bakiyenin hesaplandığı bir sabit kıymet maddesinin kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="54fa1-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="54fa1-109">`value model code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="54fa1-109">`value model code`: *String*</span></span>

<span data-ttu-id="54fa1-110">Bakiyenin hesaplandığı bir değer modeli kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="54fa1-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="54fa1-111">`reporting year`: *Numaralandırma değeri*</span><span class="sxs-lookup"><span data-stu-id="54fa1-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="54fa1-112">Bakiye hesaplaması için bir dönem tanımlayan **VarlıkYılı** uygulama numaralandırmasının sabit listesi değeri.</span><span class="sxs-lookup"><span data-stu-id="54fa1-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="54fa1-113">`reporting date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="54fa1-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="54fa1-114">Bakiye hesaplaması için bir tarih tanımlayan *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="54fa1-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="54fa1-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="54fa1-115">Return values</span></span>

<span data-ttu-id="54fa1-116">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="54fa1-116">*Container (record)*</span></span>

<span data-ttu-id="54fa1-117">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="54fa1-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="54fa1-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="54fa1-118">Example</span></span>

<span data-ttu-id="54fa1-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())`, geçerli uygulama oturum tarihinde **Geçerli** değer modeline sahip **COMP-000001** sabit kıymet bakiyeleri için hazırlanan veri kapsayıcısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="54fa1-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54fa1-120">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="54fa1-120">Additional resources</span></span>

[<span data-ttu-id="54fa1-121">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="54fa1-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]