---
title: IF ER işlevi
description: Bu konu, IF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 87e252a2751beeecb51e512cae38b271c1456fae
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744707"
---
# <a name="if-er-function"></a><span data-ttu-id="729b8-103">IF ER işlevi</span><span class="sxs-lookup"><span data-stu-id="729b8-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="729b8-104">`IF` işlevi, belirtilen koşul karşılandığında ilk belirtilen değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="729b8-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="729b8-105">Aksi takdirde, ikinci belirtilen değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="729b8-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="729b8-106">Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="729b8-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="729b8-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="729b8-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="729b8-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="729b8-108">Arguments</span></span>

<span data-ttu-id="729b8-109">`condition`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="729b8-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="729b8-110">Test işlem uygulanacak geçerli bir koşullu ifade.</span><span class="sxs-lookup"><span data-stu-id="729b8-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="729b8-111">`first value`: *Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="729b8-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="729b8-112">Koşul karşılanırsa döndürülen sonuç.</span><span class="sxs-lookup"><span data-stu-id="729b8-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="729b8-113">`second value`: *Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="729b8-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="729b8-114">Koşul karşılanmazsa döndürülen sonuç.</span><span class="sxs-lookup"><span data-stu-id="729b8-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="729b8-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="729b8-115">Return values</span></span>

<span data-ttu-id="729b8-116">*Desteklenen veri türlerinden herhangi biri*</span><span class="sxs-lookup"><span data-stu-id="729b8-116">*Any of the supported data types*</span></span>

<span data-ttu-id="729b8-117">Desteklenen veri türlerinin herhangi birinin sonuç değeri.</span><span class="sxs-lookup"><span data-stu-id="729b8-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="729b8-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="729b8-118">Usage notes</span></span>

<span data-ttu-id="729b8-119">`first value` ve `second value` bağımsız değişkenlerin aynı veri türü kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="729b8-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="729b8-120">Yapılandırılan değerlerin veri türleri eşleşmezse, tasarım zamanında özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="729b8-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="729b8-121">İlk değer ve ikinci değer *konteyner (kayıt)* veya *kayıt listesi* veri türünün değerleri ise, sonuç yalnızca her iki değerde bulunan alanlara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="729b8-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="729b8-122">Örnek</span><span class="sxs-lookup"><span data-stu-id="729b8-122">Example</span></span>

<span data-ttu-id="729b8-123">`IF (1=2, "condition is met", "condition is not met")`, **Koşul karşılanmadığında** dizesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="729b8-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="729b8-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="729b8-124">Additional resources</span></span>

[<span data-ttu-id="729b8-125">Mantıksal işlevler</span><span class="sxs-lookup"><span data-stu-id="729b8-125">Logical functions</span></span>](er-functions-category-logical.md)
