---
title: TABLENAME2ID ER işlevi
description: Bu konu, TABLENAME2ID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746567"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="e6a66-103">TABLENAME2ID ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e6a66-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6a66-104">Bu `TABLENAME2ID` işlevi, belirtilen tablo için tablo kodunun sayısal gösterimini *tamsayı* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6a66-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a66-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e6a66-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="e6a66-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e6a66-106">Arguments</span></span>

<span data-ttu-id="e6a66-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="e6a66-107">`text`: *String*</span></span>

<span data-ttu-id="e6a66-108">Geçerli bir tablo adını gösteren bir metin değeri.</span><span class="sxs-lookup"><span data-stu-id="e6a66-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="e6a66-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e6a66-109">Return values</span></span>

<span data-ttu-id="e6a66-110">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="e6a66-110">*Integer*</span></span>

<span data-ttu-id="e6a66-111">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="e6a66-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e6a66-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="e6a66-112">Usage notes</span></span>

<span data-ttu-id="e6a66-113">Bu işlevin yürütülmesi, aynı şirket adı kullanılsa bile farklı Microsoft Dynamics 365 Finance örneklerinde farklı sonuçlar elde edebilir.</span><span class="sxs-lookup"><span data-stu-id="e6a66-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="e6a66-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="e6a66-114">Example</span></span>

<span data-ttu-id="e6a66-115">`TABLENAME2ID ("Intrastat")`, **1510** döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6a66-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6a66-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e6a66-116">Additional resources</span></span>

[<span data-ttu-id="e6a66-117">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="e6a66-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]