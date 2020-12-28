---
title: SPLITLIST ER işlevi
description: Bu konu, SPLITLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: d0f527dcf313a6a5e3b6601cac9a0f6495f66833
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680357"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="d8c94-103">SPLITLIST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="d8c94-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8c94-104">`SPLITLIST` işlev, belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün.</span><span class="sxs-lookup"><span data-stu-id="d8c94-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="d8c94-105">Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8c94-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c94-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d8c94-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="d8c94-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d8c94-107">Arguments</span></span>

<span data-ttu-id="d8c94-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="d8c94-108">`list`: *Record list*</span></span>

<span data-ttu-id="d8c94-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="d8c94-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d8c94-110">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="d8c94-110">`number`: *Integer*</span></span>

<span data-ttu-id="d8c94-111">Toplu iş başına maksimum kayıt sayısı</span><span class="sxs-lookup"><span data-stu-id="d8c94-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="d8c94-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d8c94-112">Return values</span></span>

<span data-ttu-id="d8c94-113">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="d8c94-113">*Record list*</span></span>

<span data-ttu-id="d8c94-114">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="d8c94-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d8c94-115">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="d8c94-115">Usage notes</span></span>

<span data-ttu-id="d8c94-116">Aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:</span><span class="sxs-lookup"><span data-stu-id="d8c94-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="d8c94-117">**Değer:** *liste*</span><span class="sxs-lookup"><span data-stu-id="d8c94-117">**Value:** *List*</span></span>

    <span data-ttu-id="d8c94-118">Geçerli toplu işe ait kayıtların listesi.</span><span class="sxs-lookup"><span data-stu-id="d8c94-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="d8c94-119">**Batchnumber:** *tam sayı*</span><span class="sxs-lookup"><span data-stu-id="d8c94-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="d8c94-120">Döndürülen listedeki geçerli toplu iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="d8c94-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="d8c94-121">Örnek</span><span class="sxs-lookup"><span data-stu-id="d8c94-121">Example</span></span>

<span data-ttu-id="d8c94-122">Aşağıdaki örnekte, üç kaydın kayıt listesi olarak **Satırlar** veri kaynağı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d8c94-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="d8c94-123">Bu liste her biri en çok iki kayıt içeren toplu işlere ayrılır.</span><span class="sxs-lookup"><span data-stu-id="d8c94-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="d8c94-124">Aşağıdaki örnekte tasarlanmış biçim düzeni gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d8c94-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="d8c94-125">Bu biçim düzeninde, **Satırlar** veri kaynağına bağlamalar XML biçiminde çıktı üretmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d8c94-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="d8c94-126">Bu çıktı her toplu iş ve içindeki kayıtlar için ayrı ayrı düğümleri sunar.</span><span class="sxs-lookup"><span data-stu-id="d8c94-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="d8c94-127">Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d8c94-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="d8c94-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d8c94-128">Additional resources</span></span>

[<span data-ttu-id="d8c94-129">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="d8c94-129">List functions</span></span>](er-functions-category-list.md)
