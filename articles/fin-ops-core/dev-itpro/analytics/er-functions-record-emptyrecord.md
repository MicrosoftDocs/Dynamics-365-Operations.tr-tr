---
title: EMPTYRECORD ER işlevi
description: Bu konu, EMPTYRECORD Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746543"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="d97f9-103">EMPTYRECORD ER işlevi</span><span class="sxs-lookup"><span data-stu-id="d97f9-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d97f9-104">`EMPTYRECORD` işlev, belirtilen kayıt listesi veya kayıtla aynı yapıya sahip bir boş *Konteyner (kayıt)* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d97f9-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97f9-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d97f9-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="d97f9-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d97f9-106">Arguments</span></span>

<span data-ttu-id="d97f9-107">`list`: *Kayıt listesi* veya *konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="d97f9-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="d97f9-108">*Kayıt listesi* veya *konteyner (kayıt)* türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="d97f9-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d97f9-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d97f9-109">Return values</span></span>

<span data-ttu-id="d97f9-110">*Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="d97f9-110">*Container (record)*</span></span>

<span data-ttu-id="d97f9-111">Sonuç kayıt değeri.</span><span class="sxs-lookup"><span data-stu-id="d97f9-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d97f9-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="d97f9-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="d97f9-113">Boş kayıt, tüm alanlarda boş değeri bulunan kayıttır.</span><span class="sxs-lookup"><span data-stu-id="d97f9-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="d97f9-114">Boş değer sayılar için **0** (sıfır), dizeler için boş bir dize vb.'dir.</span><span class="sxs-lookup"><span data-stu-id="d97f9-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="d97f9-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="d97f9-115">Example</span></span>

<span data-ttu-id="d97f9-116">`EMPTYRECORD (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür.</span><span class="sxs-lookup"><span data-stu-id="d97f9-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="d97f9-117">Daha fazla bilgi için bkz. [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="d97f9-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d97f9-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d97f9-118">Additional resources</span></span>

[<span data-ttu-id="d97f9-119">Kayıt işlevleri</span><span class="sxs-lookup"><span data-stu-id="d97f9-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]