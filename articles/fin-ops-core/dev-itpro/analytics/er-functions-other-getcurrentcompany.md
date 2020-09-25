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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744145"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="ceda1-103">GETCURRENTCOMPANY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="ceda1-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceda1-104">`GETCURRENTCOMPANY` işlevi, bir kullanıcının oturum açmış olduğu tüzel kişiliğin (şirket) kodunu temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ceda1-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceda1-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ceda1-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="ceda1-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ceda1-106">Return values</span></span>

<span data-ttu-id="ceda1-107">*Dize*</span><span class="sxs-lookup"><span data-stu-id="ceda1-107">*String*</span></span>

<span data-ttu-id="ceda1-108">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="ceda1-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ceda1-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="ceda1-109">Example</span></span>

<span data-ttu-id="ceda1-110">`GETCURRENTCOMPANY ()`, **Contoso Entertainment System USA** şirketinde oturum açmış bir kullanıcı için **USMF** döndürür.</span><span class="sxs-lookup"><span data-stu-id="ceda1-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ceda1-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ceda1-111">Additional resources</span></span>

[<span data-ttu-id="ceda1-112">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="ceda1-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
