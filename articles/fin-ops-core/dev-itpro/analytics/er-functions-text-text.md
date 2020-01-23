---
title: TEXT ER işlevi
description: Bu konu, TEXT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915568"
---
# <span data-ttu-id="7894a-103"><a name="TEXT">TEXT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="7894a-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7894a-104">`TEXT` işlevi, belirtilen giriş geçerli uygulama örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra bleirtilen sayıyı *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="7894a-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="7894a-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7894a-105">Syntax</span></span>

```
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="7894a-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7894a-106">Arguments</span></span>

<span data-ttu-id="7894a-107">`number`: *Tamsayı* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="7894a-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="7894a-108">Bir metin dizesine dönüştürülmesi gereken sayı değeri.</span><span class="sxs-lookup"><span data-stu-id="7894a-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="7894a-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7894a-109">Return values</span></span>

<span data-ttu-id="7894a-110">*Dize*</span><span class="sxs-lookup"><span data-stu-id="7894a-110">*String*</span></span>

<span data-ttu-id="7894a-111">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="7894a-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7894a-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="7894a-112">Usage notes</span></span>

<span data-ttu-id="7894a-113">*Gerçek* türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="7894a-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="7894a-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="7894a-114">Example</span></span>

<span data-ttu-id="7894a-115">Microsoft Dynamics 365 Finance örneğinin sunucu yerel ayarı **EN-US** olarak tanımlanırsa, `TEXT (NOW ())` geçerli Finance oturum tarihi olan Aralık 17, 2015 değerini **"12/17/2015 07:59:23 AM"** metin dizesi olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="7894a-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="7894a-116">`TEXT (1/3)`, **"0.33"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="7894a-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7894a-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7894a-117">Additional resources</span></span>

[<span data-ttu-id="7894a-118">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="7894a-118">Text functions</span></span>](er-functions-category-text.md)
