---
title: ORDERBY ER işlevi
description: Bu konu, ORDERBY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: c39700fab90265ed1915b4815a6bb27af58d9516
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686476"
---
# <a name="orderby-er-function"></a><span data-ttu-id="07e28-103">ORDERBY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="07e28-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07e28-104">`ORDERBY` işlev belirtilen bağımsız değişkenlere göre sıralandıktan sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="07e28-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="07e28-105">Bu bağımsız değişkenler ifadeler olarak tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="07e28-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e28-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="07e28-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="07e28-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="07e28-107">Arguments</span></span>

<span data-ttu-id="07e28-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="07e28-108">`list`: *Record list*</span></span>

<span data-ttu-id="07e28-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="07e28-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="07e28-110">`expression 1`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="07e28-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="07e28-111">Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="07e28-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="07e28-112">Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="07e28-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="07e28-113">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="07e28-113">This argument is required.</span></span>

<span data-ttu-id="07e28-114">`expression N`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="07e28-114">`expression N`: *Field*</span></span>

<span data-ttu-id="07e28-115">Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="07e28-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="07e28-116">Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="07e28-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="07e28-117">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="07e28-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="07e28-118">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="07e28-118">Return values</span></span>

<span data-ttu-id="07e28-119">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="07e28-119">*Record list*</span></span>

<span data-ttu-id="07e28-120">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="07e28-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="07e28-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07e28-121">Example 1</span></span>

<span data-ttu-id="07e28-122">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("C|B|A", "|")` deyim içeriyorsa, `FIRST( ORDERBY( DS, DS. Value)).Value` ifadesi **A** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="07e28-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="07e28-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="07e28-123">Example 2</span></span>

<span data-ttu-id="07e28-124">**Satıcı**, VendTable tablosuna başvuran elektronik raporlama (ER) kaynağı olarak yapılandırılırsa, `ORDERBY (Vendors, Vendors.'name()')` ifadesi, satıcıların isme göre sıralanan listesini artan sıraya göre dizilmiş şekilde döndürür.</span><span class="sxs-lookup"><span data-stu-id="07e28-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07e28-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="07e28-125">Additional resources</span></span>

[<span data-ttu-id="07e28-126">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="07e28-126">List functions</span></span>](er-functions-category-list.md)
