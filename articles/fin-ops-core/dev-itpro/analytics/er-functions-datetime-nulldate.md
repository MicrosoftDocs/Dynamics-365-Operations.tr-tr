---
title: NULLDATE ER işlevi
description: Bu konu, NULLDATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563474"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="04f8f-103">NULLDATE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="04f8f-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04f8f-104">`NULLDATE` işlev, **boş** tarihi temsil eden bir *tarih* değeri döndürür (1 Ocak, 1900).</span><span class="sxs-lookup"><span data-stu-id="04f8f-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="04f8f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="04f8f-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="04f8f-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="04f8f-106">Return values</span></span>

<span data-ttu-id="04f8f-107">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="04f8f-107">*Date*</span></span>

<span data-ttu-id="04f8f-108">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="04f8f-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="04f8f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04f8f-109">Example 1</span></span>

<span data-ttu-id="04f8f-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` belirtilen özel biçime dayalı olarak, 1 Ocak 1900 arasındaki **boş** tarihi **"1900-01-01"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="04f8f-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="04f8f-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="04f8f-111">Example 2</span></span>

<span data-ttu-id="04f8f-112">`IF( Invoice.DocumentDate = NULLDATE(), true, false)`, **Documentdate** alanının değeri **boş** tarihine eşit olduğunda ifade **doğru** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="04f8f-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="04f8f-113">Bu örnekte, **Fatura** **Finance/Operations kyıtları** türünde bir elektronik raporlama (ER) veri kaynağıdır ve CustInvoiceJour tablosuna referans verir.</span><span class="sxs-lookup"><span data-stu-id="04f8f-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04f8f-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="04f8f-114">Additional resources</span></span>

[<span data-ttu-id="04f8f-115">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="04f8f-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]