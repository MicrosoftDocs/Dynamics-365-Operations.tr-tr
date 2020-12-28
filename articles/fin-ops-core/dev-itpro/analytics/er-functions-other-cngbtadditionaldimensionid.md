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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686822"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="3f80e-103">CN_GBT_ADDITIONALDIMENSIONID ER işlevi</span><span class="sxs-lookup"><span data-stu-id="3f80e-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f80e-104">Bu `CN_GBT_ADDITIONALDIMENSIONID` işlev, belirtilen dizeden alınan tek bir mali boyut kodunu temsil eden bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f80e-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="3f80e-105">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir dize.</span><span class="sxs-lookup"><span data-stu-id="3f80e-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f80e-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3f80e-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="3f80e-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="3f80e-107">Arguments</span></span>

<span data-ttu-id="3f80e-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="3f80e-108">`text`: *String*</span></span>

<span data-ttu-id="3f80e-109">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="3f80e-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="3f80e-110">`number`: Tamsayı</span><span class="sxs-lookup"><span data-stu-id="3f80e-110">`number`: Integer</span></span>

<span data-ttu-id="3f80e-111">Belirtilen dizedeki istenen boyutun sıra kodunu tanımlayan *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="3f80e-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="3f80e-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="3f80e-112">Return values</span></span>

<span data-ttu-id="3f80e-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3f80e-113">*String*</span></span>

<span data-ttu-id="3f80e-114">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="3f80e-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3f80e-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="3f80e-115">Example</span></span>

<span data-ttu-id="3f80e-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`, **"CC"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f80e-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f80e-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3f80e-117">Additional resources</span></span>

[<span data-ttu-id="3f80e-118">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="3f80e-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
