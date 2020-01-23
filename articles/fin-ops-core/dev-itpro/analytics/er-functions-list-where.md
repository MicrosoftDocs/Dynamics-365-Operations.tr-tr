---
title: WHERE ER işlevi
description: Bu konu, WHERE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916097"
---
# <span data-ttu-id="7b6ea-103"><a name="WHERE">WHERE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="7b6ea-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b6ea-104">`WHERE` işlev belirtilen koşula göre filtrelendikten sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6ea-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7b6ea-105">Syntax</span></span>

```
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="7b6ea-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7b6ea-106">Arguments</span></span>

<span data-ttu-id="7b6ea-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7b6ea-107">`list`: *Record list*</span></span>

<span data-ttu-id="7b6ea-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7b6ea-109">`condition`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="7b6ea-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="7b6ea-110">Belirtilen listenin kayıtlarını filtrelemek için kullanılan geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="7b6ea-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7b6ea-111">Return values</span></span>

<span data-ttu-id="7b6ea-112">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7b6ea-112">*Record list*</span></span>

<span data-ttu-id="7b6ea-113">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7b6ea-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="7b6ea-114">Usage notes</span></span>

<span data-ttu-id="7b6ea-115">[FILTER](er-functions-list-filter.md) işlevinden farklı olarak bu işlev, belirtilen koşul bellekteki *Kayıt listesi* türünün herhangi bir Elektronik raporlama (ER) veri kaynağına uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="7b6ea-116">Bu işlev için yapılandırılmış olan bağımsız değişkenler (`list` ve `condition`) bu isteğin doğrudan SQL aramasına çevrilmesine izin veriyorsa, tasarım zamanında bir uyarı mesajı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="7b6ea-117">Bu ileti kullanıcıya `WHERE` yerine [FILTER](er-functions-list-filter.md) işlevi kullanılıyorsa performansın iyileşme olasılığı olduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="7b6ea-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b6ea-118">Example 1</span></span>

<span data-ttu-id="7b6ea-119">**Satıcı**, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, `WHERE (Vendors, Vendors.VendGroup = "40")` ifadesi, yalnızca grup 40'a dahil olan satıcıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="7b6ea-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7b6ea-120">Example 2</span></span>

<span data-ttu-id="7b6ea-121">*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `WHERE( DS, DS.Value = "B")` ifadesi, **Değer** alanında **"B"** metni içeren tek bir kayıt listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7b6ea-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b6ea-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7b6ea-122">Additional resources</span></span>

[<span data-ttu-id="7b6ea-123">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="7b6ea-123">List functions</span></span>](er-functions-category-list.md)
