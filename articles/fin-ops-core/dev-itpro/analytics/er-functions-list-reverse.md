---
title: REVERSE ER işlevi
description: Bu konu, REVERSE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755216"
---
# <a name="reverse-er-function"></a><span data-ttu-id="86cab-103">REVERSE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="86cab-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86cab-104">Bu `REVERSE` işlev, ters sırada sıralama düzeninde *kayıt listesi* değeri olarak belirtilen listeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="86cab-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cab-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="86cab-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="86cab-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="86cab-106">Arguments</span></span>

<span data-ttu-id="86cab-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="86cab-107">`list`: *Record list*</span></span>

<span data-ttu-id="86cab-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="86cab-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="86cab-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="86cab-109">Return values</span></span>

<span data-ttu-id="86cab-110">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="86cab-110">*Record list*</span></span>

<span data-ttu-id="86cab-111">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="86cab-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="86cab-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="86cab-112">Example 1</span></span>

<span data-ttu-id="86cab-113">*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("C|B|A", "|")` deyim içeriyorsa, `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` ifadesi **C** metin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="86cab-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="86cab-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="86cab-114">Example 2</span></span>

<span data-ttu-id="86cab-115">**Satıcı**, VendTable tablosuna başvuran elektronik raporlama (ER) kaynağı olarak yapılandırılırsa, `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` ifadesi, satıcıların isme göre sıralanan listesini azalan sıraya göre dizilmiş şekilde döndürür.</span><span class="sxs-lookup"><span data-stu-id="86cab-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86cab-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="86cab-116">Additional resources</span></span>

[<span data-ttu-id="86cab-117">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="86cab-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]