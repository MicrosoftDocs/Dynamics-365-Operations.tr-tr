---
title: GETCURRENTCOMPANY ER işlevi
description: Bu konu, GETCURRENTCOMPANY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: fcb5ef2f218a85bab25f830db583343504c46e98
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567556"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="bb7d7-103">GETCURRENTCOMPANY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="bb7d7-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb7d7-104">`GETCURRENTCOMPANY` işlevi, bir kullanıcının oturum açmış olduğu tüzel kişiliğin (şirket) kodunu temsil eden *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7d7-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="bb7d7-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="bb7d7-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="bb7d7-106">Return values</span></span>

<span data-ttu-id="bb7d7-107">*Dize*</span><span class="sxs-lookup"><span data-stu-id="bb7d7-107">*String*</span></span>

<span data-ttu-id="bb7d7-108">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bb7d7-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="bb7d7-109">Example</span></span>

<span data-ttu-id="bb7d7-110">`GETCURRENTCOMPANY ()`, **Contoso Entertainment System USA** şirketinde oturum açmış bir kullanıcı için **USMF** döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb7d7-111">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bb7d7-111">Additional resources</span></span>

[<span data-ttu-id="bb7d7-112">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="bb7d7-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]