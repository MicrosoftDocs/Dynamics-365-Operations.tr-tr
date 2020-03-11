---
title: GETCURRENTCOMPANY ER işlevi
description: Bu konu, GETCURRENTCOMPANY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041435"
---
# <span data-ttu-id="d0d10-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="d0d10-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0d10-104">`GETCURRENTCOMPANY` işlevi, bir kullanıcının oturum açmış olduğu tüzel kişiliğin (şirket) kodunu temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0d10-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d10-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d0d10-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="d0d10-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d0d10-106">Return values</span></span>

<span data-ttu-id="d0d10-107">*Dize*</span><span class="sxs-lookup"><span data-stu-id="d0d10-107">*String*</span></span>

<span data-ttu-id="d0d10-108">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="d0d10-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d0d10-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="d0d10-109">Example</span></span>

<span data-ttu-id="d0d10-110">`GETCURRENTCOMPANY ()`, **Contoso Entertainment System USA** şirketinde oturum açmış bir kullanıcı için **USMF** döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0d10-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0d10-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d0d10-111">Additional resources</span></span>

[<span data-ttu-id="d0d10-112">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="d0d10-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
