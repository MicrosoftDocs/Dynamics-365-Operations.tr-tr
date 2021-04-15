---
title: SPLITLIST ER işlevi
description: Bu konu, SPLITLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745581"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="b236b-103">SPLITLIST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="b236b-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b236b-104">`SPLITLIST` işlev, belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün.</span><span class="sxs-lookup"><span data-stu-id="b236b-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="b236b-105">Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="b236b-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b236b-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="b236b-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="b236b-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="b236b-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="b236b-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b236b-108">Arguments</span></span>

<span data-ttu-id="b236b-109">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="b236b-109">`list`: *Record list*</span></span>

<span data-ttu-id="b236b-110">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="b236b-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b236b-111">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="b236b-111">`number`: *Integer*</span></span>

<span data-ttu-id="b236b-112">Toplu iş başına maksimum kayıt sayısı</span><span class="sxs-lookup"><span data-stu-id="b236b-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="b236b-113">`on-demand reading flag`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="b236b-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="b236b-114">İsteğe bağlı olarak alt liste öğelerinin oluşturulup oluşturulmayacağını belirten bir *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="b236b-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="b236b-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b236b-115">Return values</span></span>

<span data-ttu-id="b236b-116">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="b236b-116">*Record list*</span></span>

<span data-ttu-id="b236b-117">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="b236b-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b236b-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="b236b-118">Usage notes</span></span>

<span data-ttu-id="b236b-119">Aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:</span><span class="sxs-lookup"><span data-stu-id="b236b-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="b236b-120">**Değer:** *liste*</span><span class="sxs-lookup"><span data-stu-id="b236b-120">**Value:** *List*</span></span>

    <span data-ttu-id="b236b-121">Geçerli toplu işe ait kayıtların listesi.</span><span class="sxs-lookup"><span data-stu-id="b236b-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="b236b-122">**Batchnumber:** *tam sayı*</span><span class="sxs-lookup"><span data-stu-id="b236b-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="b236b-123">Döndürülen listedeki geçerli toplu iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="b236b-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="b236b-124">İsteğe bağlı okuma bayrağı **True** olarak ayarlandığında bellek tüketiminde azalma sağlayan, ancak öğeler sıralı olarak kullanılmıyorsa performans düşüşüne neden olabilecek alt listeler istek üzerine oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b236b-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="b236b-125">Örnek</span><span class="sxs-lookup"><span data-stu-id="b236b-125">Example</span></span>

<span data-ttu-id="b236b-126">Aşağıdaki örnekte, üç kaydın kayıt listesi olarak **Satırlar** veri kaynağı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b236b-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="b236b-127">Bu liste her biri en çok iki kayıt içeren toplu işlere ayrılır.</span><span class="sxs-lookup"><span data-stu-id="b236b-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="b236b-128">Aşağıdaki örnekte tasarlanmış biçim düzeni gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b236b-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="b236b-129">Bu biçim düzeninde, **Satırlar** veri kaynağına bağlamalar XML biçiminde çıktı üretmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b236b-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="b236b-130">Bu çıktı her toplu iş ve içindeki kayıtlar için ayrı ayrı düğümleri sunar.</span><span class="sxs-lookup"><span data-stu-id="b236b-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="b236b-131">Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b236b-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="b236b-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b236b-132">Additional resources</span></span>

[<span data-ttu-id="b236b-133">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="b236b-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
