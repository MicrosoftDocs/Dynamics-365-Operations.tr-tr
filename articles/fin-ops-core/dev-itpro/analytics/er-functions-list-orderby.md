---
title: ORDERBY ER işlevi
description: Bu konu, ORDERBY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5a995713a795b3f24a4fcfadcc4be596e932a22c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564178"
---
# <a name="orderby-er-function"></a><span data-ttu-id="7bf0b-103">ORDERBY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="7bf0b-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bf0b-104">`ORDERBY` işlev belirtilen bağımsız değişkenlere göre sıralandıktan sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="7bf0b-105">Bu bağımsız değişkenler ifadeler olarak tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf0b-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7bf0b-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="7bf0b-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7bf0b-107">Arguments</span></span>

<span data-ttu-id="7bf0b-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7bf0b-108">`list`: *Record list*</span></span>

<span data-ttu-id="7bf0b-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7bf0b-110">`expression 1`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="7bf0b-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="7bf0b-111">Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="7bf0b-112">Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="7bf0b-113">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-113">This argument is required.</span></span>

<span data-ttu-id="7bf0b-114">`expression N`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="7bf0b-114">`expression N`: *Field*</span></span>

<span data-ttu-id="7bf0b-115">Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="7bf0b-116">Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="7bf0b-117">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="7bf0b-118">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7bf0b-118">Return values</span></span>

<span data-ttu-id="7bf0b-119">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7bf0b-119">*Record list*</span></span>

<span data-ttu-id="7bf0b-120">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="7bf0b-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7bf0b-121">Example 1</span></span>

<span data-ttu-id="7bf0b-122">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("C|B|A", "|")` deyim içeriyorsa, `FIRST( ORDERBY( DS, DS. Value)).Value` ifadesi **A** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7bf0b-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7bf0b-123">Example 2</span></span>

<span data-ttu-id="7bf0b-124">**Satıcı**, VendTable tablosuna başvuran elektronik raporlama (ER) kaynağı olarak yapılandırılırsa, `ORDERBY (Vendors, Vendors.'name()')` ifadesi, satıcıların isme göre sıralanan listesini artan sıraya göre dizilmiş şekilde döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bf0b-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7bf0b-125">Additional resources</span></span>

[<span data-ttu-id="7bf0b-126">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="7bf0b-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]