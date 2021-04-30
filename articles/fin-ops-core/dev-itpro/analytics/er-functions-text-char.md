---
title: CHAR ER işlevi
description: Bu konu, CHAR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: f83dfe19e442b9e81d63a2b1dd3dd44aa2f594bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891195"
---
# <a name="char-er-function"></a><span data-ttu-id="3acd0-103">CHAR ER işlevi</span><span class="sxs-lookup"><span data-stu-id="3acd0-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3acd0-104">Bu `CHAR` işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="3acd0-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3acd0-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3acd0-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="3acd0-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="3acd0-106">Arguments</span></span>

<span data-ttu-id="3acd0-107">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="3acd0-107">`number`: *Integer*</span></span>

<span data-ttu-id="3acd0-108">Beklenen tek bir karaktere karşılık gelen sayı.</span><span class="sxs-lookup"><span data-stu-id="3acd0-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="3acd0-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="3acd0-109">Return values</span></span>

<span data-ttu-id="3acd0-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3acd0-110">*String*</span></span>

<span data-ttu-id="3acd0-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="3acd0-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3acd0-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="3acd0-112">Usage notes</span></span>

<span data-ttu-id="3acd0-113">Bu işlevin döndürdüğü dize **DOSYA** biçimi üst öğesinde seçtiğiniz kodlamaya bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3acd0-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="3acd0-114">Desteklenen kodlamalar listesi için bkz. [Kodlama sınıfı](/dotnet/api/system.text.encoding).</span><span class="sxs-lookup"><span data-stu-id="3acd0-114">For a list of the supported encodings, see [Encoding class](/dotnet/api/system.text.encoding).</span></span>

## <a name="example"></a><span data-ttu-id="3acd0-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="3acd0-115">Example</span></span>

<span data-ttu-id="3acd0-116">`CHAR (255)`, **"ÿ"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="3acd0-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3acd0-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3acd0-117">Additional resources</span></span>

[<span data-ttu-id="3acd0-118">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="3acd0-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]