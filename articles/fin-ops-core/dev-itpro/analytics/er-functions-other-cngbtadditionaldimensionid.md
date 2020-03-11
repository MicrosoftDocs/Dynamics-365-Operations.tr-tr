---
title: CN_GBT_ADDITIONALDIMENSIONID ER işlevi
description: Bu konu, CN_GBT_ADDITIONALDIMENSIONID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 2395a1932e543e35ced28a2a6e56ab44835de19a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041550"
---
# <span data-ttu-id="c3364-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="c3364-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3364-104">Bu `CN_GBT_ADDITIONALDIMENSIONID` işlev, belirtilen dizeden alınan tek bir mali boyut kodunu temsil eden bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3364-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="c3364-105">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir dize.</span><span class="sxs-lookup"><span data-stu-id="c3364-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3364-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="c3364-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c3364-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="c3364-107">Arguments</span></span>

<span data-ttu-id="c3364-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="c3364-108">`text`: *String*</span></span>

<span data-ttu-id="c3364-109">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="c3364-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="c3364-110">`number`: Tamsayı</span><span class="sxs-lookup"><span data-stu-id="c3364-110">`number`: Integer</span></span>

<span data-ttu-id="c3364-111">Belirtilen dizedeki istenen boyutun sıra kodunu tanımlayan *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="c3364-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3364-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="c3364-112">Return values</span></span>

<span data-ttu-id="c3364-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="c3364-113">*String*</span></span>

<span data-ttu-id="c3364-114">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="c3364-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3364-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="c3364-115">Example</span></span>

<span data-ttu-id="c3364-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`, **"CC"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3364-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3364-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c3364-117">Additional resources</span></span>

[<span data-ttu-id="c3364-118">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="c3364-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
