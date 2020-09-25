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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744443"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="4cd7c-103">CN_GBT_ADDITIONALDIMENSIONID ER işlevi</span><span class="sxs-lookup"><span data-stu-id="4cd7c-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cd7c-104">Bu `CN_GBT_ADDITIONALDIMENSIONID` işlev, belirtilen dizeden alınan tek bir mali boyut kodunu temsil eden bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4cd7c-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="4cd7c-105">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir dize.</span><span class="sxs-lookup"><span data-stu-id="4cd7c-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd7c-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="4cd7c-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="4cd7c-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="4cd7c-107">Arguments</span></span>

<span data-ttu-id="4cd7c-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="4cd7c-108">`text`: *String*</span></span>

<span data-ttu-id="4cd7c-109">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="4cd7c-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="4cd7c-110">`number`: Tamsayı</span><span class="sxs-lookup"><span data-stu-id="4cd7c-110">`number`: Integer</span></span>

<span data-ttu-id="4cd7c-111">Belirtilen dizedeki istenen boyutun sıra kodunu tanımlayan *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="4cd7c-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="4cd7c-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="4cd7c-112">Return values</span></span>

<span data-ttu-id="4cd7c-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="4cd7c-113">*String*</span></span>

<span data-ttu-id="4cd7c-114">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="4cd7c-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4cd7c-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="4cd7c-115">Example</span></span>

<span data-ttu-id="4cd7c-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`, **"CC"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="4cd7c-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cd7c-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4cd7c-117">Additional resources</span></span>

[<span data-ttu-id="4cd7c-118">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="4cd7c-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
