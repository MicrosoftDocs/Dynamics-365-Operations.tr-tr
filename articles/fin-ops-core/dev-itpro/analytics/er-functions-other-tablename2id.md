---
title: TABLENAME2ID ER işlevi
description: Bu konu, TABLENAME2ID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681170"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="cdc70-103">TABLENAME2ID ER işlevi</span><span class="sxs-lookup"><span data-stu-id="cdc70-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdc70-104">Bu `TABLENAME2ID` işlevi, belirtilen tablo için tablo kodunun sayısal gösterimini *tamsayı* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="cdc70-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc70-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="cdc70-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="cdc70-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="cdc70-106">Arguments</span></span>

<span data-ttu-id="cdc70-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="cdc70-107">`text`: *String*</span></span>

<span data-ttu-id="cdc70-108">Geçerli bir tablo adını gösteren bir metin değeri.</span><span class="sxs-lookup"><span data-stu-id="cdc70-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="cdc70-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="cdc70-109">Return values</span></span>

<span data-ttu-id="cdc70-110">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="cdc70-110">*Integer*</span></span>

<span data-ttu-id="cdc70-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="cdc70-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cdc70-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="cdc70-112">Usage notes</span></span>

<span data-ttu-id="cdc70-113">Bu işlevin yürütülmesi, aynı şirket adı kullanılsa bile farklı Microsoft Dynamics 365 Finance örneklerinde farklı sonuçlar elde edebilir.</span><span class="sxs-lookup"><span data-stu-id="cdc70-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="cdc70-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="cdc70-114">Example</span></span>

<span data-ttu-id="cdc70-115">`TABLENAME2ID ("Intrastat")`, **1510** döndürür.</span><span class="sxs-lookup"><span data-stu-id="cdc70-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdc70-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cdc70-116">Additional resources</span></span>

[<span data-ttu-id="cdc70-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="cdc70-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
