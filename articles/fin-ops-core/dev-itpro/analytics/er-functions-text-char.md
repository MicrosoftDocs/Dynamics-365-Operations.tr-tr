---
title: CHAR ER işlevi
description: Bu konu, CHAR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041251"
---
# <span data-ttu-id="2316c-103"><a name="CHAR">CHAR ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="2316c-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2316c-104">Bu `CHAR` işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2316c-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2316c-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2316c-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="2316c-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="2316c-106">Arguments</span></span>

<span data-ttu-id="2316c-107">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="2316c-107">`number`: *Integer*</span></span>

<span data-ttu-id="2316c-108">Beklenen tek bir karaktere karşılık gelen sayı.</span><span class="sxs-lookup"><span data-stu-id="2316c-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="2316c-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="2316c-109">Return values</span></span>

<span data-ttu-id="2316c-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2316c-110">*String*</span></span>

<span data-ttu-id="2316c-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="2316c-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2316c-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="2316c-112">Usage notes</span></span>

<span data-ttu-id="2316c-113">Bu işlevin döndürdüğü dize **DOSYA** biçimi üst öğesinde seçtiğiniz kodlamaya bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2316c-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="2316c-114">Desteklenen kodlamalar listesi için bkz. [Kodlama sınıfı](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="2316c-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="2316c-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="2316c-115">Example</span></span>

<span data-ttu-id="2316c-116">`CHAR (255)`, **"ÿ"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="2316c-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2316c-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2316c-117">Additional resources</span></span>

[<span data-ttu-id="2316c-118">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="2316c-118">Text functions</span></span>](er-functions-category-text.md)
