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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041289"
---
# <span data-ttu-id="1f9d6-103"><a name="TABLENAME2ID">TABLENAME2ID ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="1f9d6-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f9d6-104">Bu `TABLENAME2ID` işlevi, belirtilen tablo için tablo kodunun sayısal gösterimini *tamsayı* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9d6-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="1f9d6-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="1f9d6-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="1f9d6-106">Arguments</span></span>

<span data-ttu-id="1f9d6-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="1f9d6-107">`text`: *String*</span></span>

<span data-ttu-id="1f9d6-108">Geçerli bir tablo adını gösteren bir metin değeri.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f9d6-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="1f9d6-109">Return values</span></span>

<span data-ttu-id="1f9d6-110">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="1f9d6-110">*Integer*</span></span>

<span data-ttu-id="1f9d6-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1f9d6-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="1f9d6-112">Usage notes</span></span>

<span data-ttu-id="1f9d6-113">Bu işlevin yürütülmesi, aynı şirket adı kullanılsa bile farklı Microsoft Dynamics 365 Finance örneklerinde farklı sonuçlar elde edebilir.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="1f9d6-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="1f9d6-114">Example</span></span>

<span data-ttu-id="1f9d6-115">`TABLENAME2ID ("Intrastat")`, **1510** döndürür.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f9d6-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1f9d6-116">Additional resources</span></span>

[<span data-ttu-id="1f9d6-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="1f9d6-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
