---
title: CONTAINS ER işlevi
description: Bu konu, CONTAINS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048882"
---
# <a name="contains-er-function"></a><span data-ttu-id="43d7f-103">CONTAINS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="43d7f-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43d7f-104">`CONTAINS` işlevi, belirtilen girişin belirtilen metni içerip içermediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="43d7f-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="43d7f-105">Belirtilen giriş belirtilen metni içeriyorsa **TRUE** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="43d7f-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="43d7f-106">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="43d7f-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d7f-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="43d7f-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="43d7f-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="43d7f-108">Arguments</span></span>

<span data-ttu-id="43d7f-109">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="43d7f-109">`input`: *String*</span></span>

<span data-ttu-id="43d7f-110">Değeri, ikinci bağımsız değişkeni içerebilecek *Dize* türünün veya dize sabitinin bir veri kaynağı öğesinin geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="43d7f-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="43d7f-111">`search text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="43d7f-111">`search text`: *String*</span></span>

<span data-ttu-id="43d7f-112">Değeri, ilk bağımsız değişkende bulunabilecek *Dize* veri türünün veya dize sabitinin bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="43d7f-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="43d7f-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="43d7f-113">Return values</span></span>

<span data-ttu-id="43d7f-114">*Boole*</span><span class="sxs-lookup"><span data-stu-id="43d7f-114">*Boolean*</span></span>

<span data-ttu-id="43d7f-115">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="43d7f-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="43d7f-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="43d7f-116">Usage notes</span></span>

<span data-ttu-id="43d7f-117">Bu işlev, yalnızca ilgili eşleme, [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)'de [Microsoft Dataverse](/power-platform/admin/data-integrator) öğesine erişmek için yapılandırıldığında [FILTER](er-functions-list-filter.md) işlevinin bir koşul ifadesini belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="43d7f-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="43d7f-118">Aksi durumda, tasarım zamanında özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="43d7f-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="43d7f-119">Aldığınız iletide, verimliliği artırmaya yardımcı olmak için `FILTER` işlevi yerine [WHERE](er-functions-list-where.md) işlevini kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="43d7f-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="43d7f-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="43d7f-120">Example 1</span></span>

<span data-ttu-id="43d7f-121">`CONTAINS ("abc", "d")` ifadesi **yanlış** değerini, `CONTAINS ("abc", "C")` ise **doğru** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="43d7f-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="43d7f-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="43d7f-122">Example 2</span></span>

<span data-ttu-id="43d7f-123">**Model** veri kaynağının **adres** alanı değeri **DEU** dizesini içeriyorsa `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` ifadesi **TRUE**'yu döndürür.</span><span class="sxs-lookup"><span data-stu-id="43d7f-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="43d7f-124">Aksi takdirde **YANLIŞ**'ı döndürür.</span><span class="sxs-lookup"><span data-stu-id="43d7f-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43d7f-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="43d7f-125">Additional resources</span></span>

[<span data-ttu-id="43d7f-126">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="43d7f-126">Logical functions</span></span>](er-functions-category-logical.md)
