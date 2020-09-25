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
ms.openlocfilehash: 8b4c65063cd22b5370ca6000a32c6fd1cc9ce6b6
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743843"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="94797-103">GUIDVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="94797-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94797-104">`GUIDVALUE` işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="94797-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="94797-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="94797-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="94797-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="94797-106">Arguments</span></span>

<span data-ttu-id="94797-107">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="94797-107">`input`: *String*</span></span>

<span data-ttu-id="94797-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="94797-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="94797-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="94797-109">Return values</span></span>

<span data-ttu-id="94797-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="94797-110">*GUID*</span></span>

<span data-ttu-id="94797-111">Sonuçta elde edilen genel benzersiz tanımlayıcı (GUID) değeri.</span><span class="sxs-lookup"><span data-stu-id="94797-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="94797-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="94797-112">Usage notes</span></span>

<span data-ttu-id="94797-113">Ters yönde dönüştürme yapmak için (diğer bir deyişle, *GUID* veri türünün belirtilen girişini *Dize* veri türünün veri öğesine dönüştürmek için), [TEXT()](er-functions-text-text.md) işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94797-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="94797-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="94797-114">Example</span></span>

<span data-ttu-id="94797-115">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="94797-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="94797-116">`GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` ifadeyi içeren *hesaplanmış alan* türünün **myID** bir veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="94797-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="94797-117">UserInfo tablosuna başvuran *Tablo kayıtları* türünün **Kullanıcılar** veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="94797-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="94797-118">Daha sonra, bir *GUID* veri türünün **ObjectID** alanı ile UserInfo tablosunu filtrelemek için `FILTER (Users, Users.objectId = myID)` gibi bir ifade kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94797-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94797-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="94797-119">Additional resources</span></span>

[<span data-ttu-id="94797-120">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="94797-120">Text functions</span></span>](er-functions-category-text.md)
