---
title: ENDSWITH ER işlevi
description: Bu konu, ENDSWITH Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: bdd2f364e2d0b80d3df20592ec827dcabf99a06c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745413"
---
# <a name="endswith-er-function"></a><span data-ttu-id="98ea4-103">ENDSWITH ER işlevi</span><span class="sxs-lookup"><span data-stu-id="98ea4-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98ea4-104">`ENDSWITH` işlevi, belirtilen girişin belirtilen metin ile bitip bitmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="98ea4-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="98ea4-105">Belirtilen giriş belirtilen metinle sonlanıyorsa **TRUE** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="98ea4-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="98ea4-106">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="98ea4-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ea4-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="98ea4-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="98ea4-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="98ea4-108">Arguments</span></span>

<span data-ttu-id="98ea4-109">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="98ea4-109">`input`: *String*</span></span>

<span data-ttu-id="98ea4-110">Değeri, ikinci bağımsız değişkenle bitebilecek *Dize* türünün veya dize sabitinin bir veri kaynağı öğesinin geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="98ea4-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="98ea4-111">`start text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="98ea4-111">`start text`: *String*</span></span>

<span data-ttu-id="98ea4-112">Değeri, ilk bağımsız değişkenin sonunda olabilecek *Dize* veri türünün veya dize sabitinin bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="98ea4-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="98ea4-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="98ea4-113">Return values</span></span>

<span data-ttu-id="98ea4-114">*Boole*</span><span class="sxs-lookup"><span data-stu-id="98ea4-114">*Boolean*</span></span>

<span data-ttu-id="98ea4-115">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="98ea4-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98ea4-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="98ea4-116">Usage notes</span></span>

<span data-ttu-id="98ea4-117">Bu işlev, yalnızca ilgili eşleme, [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)'de [Microsoft Dataverse](../data-entities/data-integration-cds.md) öğesine erişmek için yapılandırıldığında [FILTER](er-functions-list-filter.md) işlevinin bir koşul ifadesini belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="98ea4-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="98ea4-118">Aksi durumda, tasarım zamanında özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="98ea4-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="98ea4-119">Aldığınız iletide, verimliliği artırmaya yardımcı olmak için `FILTER` işlevi yerine [WHERE](er-functions-list-where.md) işlevini kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="98ea4-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="98ea4-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98ea4-120">Example 1</span></span>

<span data-ttu-id="98ea4-121">`ENDSWITH ("abc", "d")` ifadesi **yanlış** değerini, `ENDSWITH ("abc", "C")` ise **doğru** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="98ea4-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="98ea4-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="98ea4-122">Example 2</span></span>

<span data-ttu-id="98ea4-123">**Model** veri kaynağının **adres** alanı değeri **USA** dizesiyle sona eriyorsa `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` ifadesi **doğru**'yu döndürür.</span><span class="sxs-lookup"><span data-stu-id="98ea4-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="98ea4-124">Aksi takdirde **YANLIŞ**'ı döndürür.</span><span class="sxs-lookup"><span data-stu-id="98ea4-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98ea4-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="98ea4-125">Additional resources</span></span>

[<span data-ttu-id="98ea4-126">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="98ea4-126">Logical functions</span></span>](er-functions-category-logical.md)
