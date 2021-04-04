---
title: NULLCONTAINER ER işlevi
description: Bu konu, NULLCONTAINER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563234"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="be8d2-103">NULLCONTAINER ER işlevi</span><span class="sxs-lookup"><span data-stu-id="be8d2-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be8d2-104">`NULLCONTAINER` işlev, belirtilen kayıt listesi veya kayıtla aynı yapıya sahip bir boş *Konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="be8d2-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8d2-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="be8d2-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="be8d2-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="be8d2-106">Arguments</span></span>

<span data-ttu-id="be8d2-107">`list`: *Kayıt listesi* veya *konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="be8d2-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="be8d2-108">*Kayıt listesi* veya *konteyner (kayıt)* türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="be8d2-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="be8d2-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="be8d2-109">Return values</span></span>

<span data-ttu-id="be8d2-110">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="be8d2-110">*Container (record)*</span></span>

<span data-ttu-id="be8d2-111">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="be8d2-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="be8d2-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="be8d2-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="be8d2-113">Bu işlev artık kullanılmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="be8d2-113">This function is obsolete.</span></span> <span data-ttu-id="be8d2-114">Bunun yerine `EMPTYRECORD` işlevi kullanın.</span><span class="sxs-lookup"><span data-stu-id="be8d2-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="be8d2-115">Daha fazla bilgi için bkz. [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="be8d2-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="be8d2-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="be8d2-116">Example</span></span>

<span data-ttu-id="be8d2-117">`NULLCONTAINER (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür.</span><span class="sxs-lookup"><span data-stu-id="be8d2-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="be8d2-118">Daha fazla bilgi için bkz. [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="be8d2-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be8d2-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="be8d2-119">Additional resources</span></span>

[<span data-ttu-id="be8d2-120">Kayıt işlevleri</span><span class="sxs-lookup"><span data-stu-id="be8d2-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]