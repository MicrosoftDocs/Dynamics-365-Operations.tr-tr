---
title: STARTSWITH ER işlevi
description: Bu konu, STARTSWITH Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ef7e9c88abff2b4b58ecb8abf1e69f7853f9b3fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751692"
---
# <a name="startswith-er-function"></a><span data-ttu-id="eaaa9-103">STARTSWITH ER işlevi</span><span class="sxs-lookup"><span data-stu-id="eaaa9-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaaa9-104">`STARTSWITH` işlevi, belirtilen girişin belirtilen metin ile başlayıp başlamadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="eaaa9-105">Belirtilen giriş belirtilen metinle başlıyorsa **TRUE** *Boole* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="eaaa9-106">Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaaa9-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="eaaa9-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="eaaa9-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="eaaa9-108">Arguments</span></span>

<span data-ttu-id="eaaa9-109">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="eaaa9-109">`input`: *String*</span></span>

<span data-ttu-id="eaaa9-110">Değeri, ikinci bağımsız değişkenle başlayabilecek *Dize* türünün veya dize sabitinin bir veri kaynağı öğesinin geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="eaaa9-111">`start text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="eaaa9-111">`start text`: *String*</span></span>

<span data-ttu-id="eaaa9-112">Değeri, ilk bağımsız değişkenin başında olabilecek *Dize* veri türünün veya dize sabitinin bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="eaaa9-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="eaaa9-113">Return values</span></span>

<span data-ttu-id="eaaa9-114">*Boole*</span><span class="sxs-lookup"><span data-stu-id="eaaa9-114">*Boolean*</span></span>

<span data-ttu-id="eaaa9-115">Sonuç *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eaaa9-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="eaaa9-116">Usage notes</span></span>

<span data-ttu-id="eaaa9-117">Bu işlev, yalnızca ilgili eşleme, [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)'de [Microsoft Dataverse](../data-entities/data-integration-cds.md) öğesine erişmek için yapılandırıldığında [FILTER](er-functions-list-filter.md) işlevinin bir koşul ifadesini belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="eaaa9-118">Aksi durumda, tasarım zamanında özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="eaaa9-119">Aldığınız iletide, verimliliği artırmaya yardımcı olmak için `FILTER` işlevi yerine [WHERE](er-functions-list-where.md) işlevini kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="eaaa9-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eaaa9-120">Example 1</span></span>

<span data-ttu-id="eaaa9-121">`STARTSWITH ("abc", "d")` ifadesi **yanlış** değerini, `STARTSWITH ("abc", "A")` ise **doğru** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="eaaa9-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="eaaa9-122">Example 2</span></span>

<span data-ttu-id="eaaa9-123">**Model** veri kaynağının **adres** alanı değeri **123 Coffee Street** dizesiyle başlıyorsa `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` ifadesi **doğru**'yu döndürür.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="eaaa9-124">Aksi takdirde **YANLIŞ**'ı döndürür.</span><span class="sxs-lookup"><span data-stu-id="eaaa9-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eaaa9-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="eaaa9-125">Additional resources</span></span>

[<span data-ttu-id="eaaa9-126">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="eaaa9-126">Logical functions</span></span>](er-functions-category-logical.md)
