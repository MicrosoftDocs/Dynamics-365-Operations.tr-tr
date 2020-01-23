---
title: GUIDVALUE ER işlevi
description: Bu konu, GUIDVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915706"
---
# <span data-ttu-id="a94fa-103"><a name="GUIDVALUE">GUIDVALUE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="a94fa-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a94fa-104">`GUIDVALUE` işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="a94fa-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94fa-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a94fa-105">Syntax</span></span>

```
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="a94fa-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="a94fa-106">Arguments</span></span>

<span data-ttu-id="a94fa-107">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="a94fa-107">`input`: *String*</span></span>

<span data-ttu-id="a94fa-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="a94fa-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a94fa-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="a94fa-109">Return values</span></span>

<span data-ttu-id="a94fa-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a94fa-110">*GUID*</span></span>

<span data-ttu-id="a94fa-111">Sonuçta elde edilen genel benzersiz tanımlayıcı (GUID) değeri.</span><span class="sxs-lookup"><span data-stu-id="a94fa-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a94fa-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="a94fa-112">Usage notes</span></span>

<span data-ttu-id="a94fa-113">Ters yönde dönüştürme yapmak için (diğer bir deyişle, *GUID* veri türünün belirtilen girişini *Dize* veri türünün veri öğesine dönüştürmek için), [TEXT()](er-functions-text-text.md) işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a94fa-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="a94fa-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="a94fa-114">Example</span></span>

<span data-ttu-id="a94fa-115">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="a94fa-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="a94fa-116">`GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` ifadeyi içeren *hesaplanmış alan* türünün **myID** bir veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="a94fa-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="a94fa-117">UserInfo tablosuna başvuran *Tablo kayıtları* türünün **Kullanıcılar** veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="a94fa-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="a94fa-118">Daha sonra, bir *GUID* veri türünün **ObjectID** alanı ile UserInfo tablosunu filtrelemek için `FILTER (Users, Users.objectId = myID)` gibi bir ifade kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a94fa-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a94fa-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a94fa-119">Additional resources</span></span>

[<span data-ttu-id="a94fa-120">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="a94fa-120">Text functions</span></span>](er-functions-category-text.md)
