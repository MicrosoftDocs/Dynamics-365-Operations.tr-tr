---
title: CN_GBT_ADDITIONALDIMENSIONID ER işlevi
description: Bu konu, CN_GBT_ADDITIONALDIMENSIONID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 5774bb6928ae321af923819d6b2cc609dbf35b99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564154"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="a471a-103">CN_GBT_ADDITIONALDIMENSIONID ER işlevi</span><span class="sxs-lookup"><span data-stu-id="a471a-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a471a-104">Bu `CN_GBT_ADDITIONALDIMENSIONID` işlev, belirtilen dizeden alınan tek bir mali boyut kodunu temsil eden bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a471a-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="a471a-105">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir dize.</span><span class="sxs-lookup"><span data-stu-id="a471a-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a471a-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a471a-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="a471a-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="a471a-107">Arguments</span></span>

<span data-ttu-id="a471a-108">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="a471a-108">`text`: *String*</span></span>

<span data-ttu-id="a471a-109">Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="a471a-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="a471a-110">`number`: Tamsayı</span><span class="sxs-lookup"><span data-stu-id="a471a-110">`number`: Integer</span></span>

<span data-ttu-id="a471a-111">Belirtilen dizedeki istenen boyutun sıra kodunu tanımlayan *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="a471a-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="a471a-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="a471a-112">Return values</span></span>

<span data-ttu-id="a471a-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="a471a-113">*String*</span></span>

<span data-ttu-id="a471a-114">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="a471a-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a471a-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="a471a-115">Example</span></span>

<span data-ttu-id="a471a-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`, **"CC"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="a471a-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a471a-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a471a-117">Additional resources</span></span>

[<span data-ttu-id="a471a-118">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="a471a-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]