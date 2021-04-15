---
title: EMPTYLIST ER işlevi
description: Bu konu, EMPTYLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746687"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="353ef-103">EMPTYLIST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="353ef-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="353ef-104">`EMPTYLIST` işlevi, belirtilmiş olan listeyi, liste yapısı için bir kaynak olarak kullanarak boş bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="353ef-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="353ef-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="353ef-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="353ef-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="353ef-106">Arguments</span></span>

<span data-ttu-id="353ef-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="353ef-107">`list`: *Record list*</span></span>

<span data-ttu-id="353ef-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="353ef-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="353ef-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="353ef-109">Return values</span></span>

<span data-ttu-id="353ef-110">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="353ef-110">*Record list*</span></span>

<span data-ttu-id="353ef-111">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="353ef-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="353ef-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="353ef-112">Example</span></span>

<span data-ttu-id="353ef-113">`EMPTYLIST (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="353ef-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="353ef-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="353ef-114">Additional resources</span></span>

[<span data-ttu-id="353ef-115">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="353ef-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]