---
title: FILTER ER işlevi
description: Bu konu, FILTER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746615"
---
# <a name="filter-er-function"></a><span data-ttu-id="13713-103">FILTER ER işlevi</span><span class="sxs-lookup"><span data-stu-id="13713-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13713-104">`FILTER` işlev, belirtilen koşula filtre uygulayan bir sorgu değiştirildikten sonra bir *kayıt listesi* değeri olarak belirtilmiş listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="13713-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="13713-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="13713-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="13713-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="13713-106">Arguments</span></span>

<span data-ttu-id="13713-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="13713-107">`list`: *Record list*</span></span>

<span data-ttu-id="13713-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="13713-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="13713-109">`condition`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="13713-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="13713-110">Belirtilen listenin kayıtlarını filtrelemek için kullanılan geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="13713-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="13713-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="13713-111">Return values</span></span>

<span data-ttu-id="13713-112">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="13713-112">*Record list*</span></span>

<span data-ttu-id="13713-113">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="13713-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="13713-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="13713-114">Usage notes</span></span>

<span data-ttu-id="13713-115">[WHERE](er-functions-list-where.md) işlevinden farklı olarak bu işlev, belirtilen koşul *Tablo kayıtları* türünün herhangi bir Elektronik raporlama (ER) veri kaynağına veritabanı düzeyinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="13713-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="13713-116">Liste ve koşul tablolar ve ilişkiler kullanılarak tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="13713-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="13713-117">Bu işlev için yapılandırılmış olan bir veya her iki bağımsız değişken (`list` ve `condition`) bu isteğin doğrudan SQL aramasına çevrilmesine izin vermiyorsa, tasarım zamanında bir özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="13713-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="13713-118">Bu özel durum kullanıcıya, veritabanını sorgulamak için `list`veya `condition` kullanılıp kullanlamadığını bildirir.</span><span class="sxs-lookup"><span data-stu-id="13713-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="13713-119">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13713-119">Example 1</span></span>

<span data-ttu-id="13713-120">**Satıcı**, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, `FILTER (Vendors, Vendors.VendGroup = "40")` ifadesi, yalnızca grup 40'a dahil olan satıcıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="13713-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="13713-121">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="13713-121">Example 2</span></span>

<span data-ttu-id="13713-122">**Satıcı**, VendTable tablosuna başvuran bir ER veri kaynağı olarak yapılandırılırsa ve **parmVendorBankGroup**, *Dize* veri türünde bir değer döndüren ER veri kaynağı olarak yapılandırılırsa, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` ifadesi yalnızca belirli bir banka grubuna ait satıcı hesaplarının bulunduğu bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="13713-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="13713-123">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="13713-123">Example 3</span></span>

<span data-ttu-id="13713-124">*Hesaplanmış alan* türünün **DS** bir veri kaynağını girersiniz ve `SPLIT ("A,B,C", ",")` ifadesini içerir.</span><span class="sxs-lookup"><span data-stu-id="13713-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="13713-125">Daha sonra başka bir ifade girersiniz; `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="13713-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="13713-126">Bu ifadeyi ER formül tasarımcısında kaydetmeye çalıştığınızda, aşağıdaki özel durum oluşturulur: "doğrulama hatası: FILTER işlevinin liste ifadesi sorgulanabilir değil."</span><span class="sxs-lookup"><span data-stu-id="13713-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13713-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="13713-127">Additional resources</span></span>

[<span data-ttu-id="13713-128">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="13713-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]