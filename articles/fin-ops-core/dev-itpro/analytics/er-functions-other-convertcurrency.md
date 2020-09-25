---
title: CONVERTCURRENCY ER işlevi
description: Bu konu, CONVERTCURRENCY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744323"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="eb239-103">CONVERTCURRENCY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="eb239-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb239-104">`CONVERTCURRENCY` işlev, belirtilen parasal tutarı kaynak para biriminden, belirtilen tarihte belirtilen şirketinin ayarlarını kullanarak belirtilen hedef para birimine dönüştürme sonucunu temsil eden *Gerçek* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb239-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb239-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="eb239-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="eb239-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="eb239-106">Arguments</span></span>

<span data-ttu-id="eb239-107">`amount`: *Tamsayı* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="eb239-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="eb239-108">Dönüştürülmesi gereken parasal tutarı gösteren sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="eb239-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="eb239-109">`source currency`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="eb239-109">`source currency`: *String*</span></span>

<span data-ttu-id="eb239-110">Kaynak para birimi kodu.</span><span class="sxs-lookup"><span data-stu-id="eb239-110">The code of the source currency.</span></span>

<span data-ttu-id="eb239-111">`target currency`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="eb239-111">`target currency`: *String*</span></span>

<span data-ttu-id="eb239-112">Hedef para birimi kodu.</span><span class="sxs-lookup"><span data-stu-id="eb239-112">The code of the target currency.</span></span>

<span data-ttu-id="eb239-113">`date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="eb239-113">`date`: *Date*</span></span>

<span data-ttu-id="eb239-114">Dönüştürme için Döviz kurunu belirlemek amacıyla kullanılan tarihi temsil eden bir *tarih* değeri.</span><span class="sxs-lookup"><span data-stu-id="eb239-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="eb239-115">`company`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="eb239-115">`company`: *String*</span></span>

<span data-ttu-id="eb239-116">Dönüştürme için kullanılan ayarları sağlayan şirketin kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="eb239-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb239-117">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="eb239-117">Return values</span></span>

<span data-ttu-id="eb239-118">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="eb239-118">*Real*</span></span>

<span data-ttu-id="eb239-119">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="eb239-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="eb239-120">Örnek</span><span class="sxs-lookup"><span data-stu-id="eb239-120">Example</span></span>

<span data-ttu-id="eb239-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")`, şimdiki oturum tarihinde, **DEMF** şirket ayarlarına dayalı olarak bir euro'nun ABD doları olarak karşılığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb239-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb239-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="eb239-122">Additional resources</span></span>

[<span data-ttu-id="eb239-123">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="eb239-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
